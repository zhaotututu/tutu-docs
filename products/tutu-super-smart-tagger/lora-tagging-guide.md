# After 10,000 LoRAs, This Is How I Tag Images for Training

## 0. The Common Pain Point

You spend hours collecting images, follow a popular LoRA tutorial step by step, hit Train, and the result is disappointing.

For example, you are training a LoRA for an anime-style character. You:

- Collect a few dozen images, with varied styles but consistent outfit and appearance.
- Run an auto-tagging tool.
- Add the trigger word to every caption.
- Start training.

What you get back is often:

- A stitched-together result with warped anatomy.
- A character that kind of looks right, but the face is not stable.
- Clothing that is never exactly right.
- Background, pose, and style that do not follow your prompts reliably.

You double-check the workflow and parameters and think: I did everything the tutorials said. Why is this still bad?

This frustration is extremely common in LoRA training. So where is the real problem?

---

## 1. Why the Usual Fixes Often Do Not Fix Anything

Most advice falls into three big camps.

### 1. More or Better Data

You are told your dataset is:

- Not high-res enough.
- Not large enough.
- Not diverse enough.

So the advice becomes: get more images, get better images.

That is fair. Data quality and diversity absolutely matter. But in practice, even with dozens or hundreds of clean, on-model images, good pose and composition variety, and a dataset that follows common best-practice checklists, your LoRA can still:

- Miss important details.
- Require many rerolls to get a usable result.
- Fail to consistently reproduce the trained character.

So dataset quality alone is not the whole story.

### 2. Hyperparameter Tuning Will Save You

This camp focuses on:

- Learning rate.
- Optimizer.
- Network rank, dim, and alpha.
- Steps, scheduler, warmup, and related training settings.

These settings matter, but mainly for convergence, stability versus exploding or underfitting, and general sharpness or base quality.

If your LoRA already trains successfully and can generate images without collapsing, but the content is wrong or hard to control, simply changing hyperparameters usually will not magically fix it.

At that point, the core issue is rarely whether you used cosine learning rate instead of constant learning rate.

### 3. Coarse Tagging Only

This camp says your captions are too detailed and that you are overfitting. You are told to:

- Simplify descriptions.
- Avoid too many details.
- Describe only the main subject plus simple context.

But this advice often stays vague:

- Why exactly is too much detail bad?
- What counts as useful detail versus harmful detail?
- How do you stay coarse without losing important information?

If you test it systematically, the result is often not so simple.

Set A uses detailed captions, perhaps auto-tagged with most attributes kept. Set B uses deliberately simplified captions that focus on subject and composition while ignoring details.

You may see that Set A rarely recreates the training subject perfectly and always misses something. Set B may look fine with simple prompts, but becomes unstable or less controllable when you add complex scenes, ask for specific poses, or mix in extra style conditions.

The conclusion is that coarse captions are not magic. Simplifying can help sometimes, but it can also destroy useful information.

So the real question becomes: what should a good LoRA caption look like? What exactly are we optimizing for?

---

## 2. The Missing Piece: What CLIP Is Actually Doing for Your LoRA

To answer that, look at what is underneath: CLIP, T5, or whichever text encoder your model uses.

In both text-to-image and image-to-image, the text encoder is the bridge between text and visual features.

At generation time:

- Your text is encoded into semantic vectors.
- Those vectors guide denoising.
- The denoising process produces the final image.

At LoRA training time:

- Each training pair is an image and text.
- The model learns that when it sees this text embedding, it should produce these visual features.

For convenience, this guide says CLIP, but the same idea applies to whatever text encoder and cross-attention stack your model uses.

In LoRA training, captions are not just descriptions. They are the only symbolic channel through which you tell the model: this specific visual concept equals this trigger word or this piece of text.

The real goal of captions is to help the model unambiguously learn what the new concept is, and what around it is variable and controllable.

Once you see that, caption quality is no longer about detailed versus coarse. It becomes: does this image-text pair clearly teach the right concepts?

---

## 3. Core Strategy: Define the Concept Clearly and Describe Variables Precisely

A practical strategy follows from this:

1. Precisely define the core concept.
2. Accurately describe the things you want to control as variables.

These two decisions determine whether your LoRA becomes stable, controllable, and reusable across prompts.

### 3.1 Step One: Precisely Define the Core Concept

This is the foundation.

Your caption must clearly tell the model: this specific thing is what the trigger word means.

Imagine an image with:

- A sci-fi battlefield.
- A soldier in futuristic armor.
- A small yellow cartoon-like head.
- City ruins, smoke, fire, explosions, and dramatic lighting.

A typical auto-caption might say that the image depicts a sci-fi war scene with a warrior in futuristic armor, a small yellow cartoon-like head, deep blue and silver armor, a ruined city, smoke, flames, debris, low-angle composition, dark atmosphere, strong lighting contrast, cinematic style, and so on.

That caption sounds detailed and correct, but it never defines a new concept. It never says that this character is your trigger word.

From the model's perspective, it is unclear what the new concept is:

- Is it the armor?
- The yellow head?
- The entire scene style?
- The low-angle cinematic look?

If your trigger word is `my_character_trigger` and you want it to represent this specific character design, the caption should make that explicit:

`The image shows my_character_trigger standing in a sci-fi war scene, holding a futuristic gun...`

Then remove armor micro-detail descriptions unless they are meant to be controlled later as variables.

If someday you want prompts such as:

- `my_character_trigger eating at home`
- `my_character_trigger shopping in a mall`

Then the definition of `my_character_trigger` should be tight and stable, while scene, pose, and activity should be treated as variables rather than baked into the core concept.

A better caption pattern is:

- A short, explicit definition of the subject tied to the trigger.
- Extra details only when they are generic, useful in other contexts, or explicit variables you intend to control.

The caption can be rewritten like this:

`The image depicts a sci-fi war scene, with the main subject being my_character_trigger. The character is raising a futuristic gun and aiming forward, as if in the middle of an intense battle. The background is a ruined city filled with smoke and flames, with debris and rubble from destroyed buildings scattered around. The overall atmosphere is dark and oppressive, broken by firelight and explosions, creating a tense battlefield. The character is centered in the frame and shown from a low angle. The lighting is dark but illuminated by fire and explosions, creating strong contrast. The overall look is cinematic, with strong visual impact and a clear sense of narrative.`

### 3.2 Step Two: Describe the Variables You Want to Control

Defining the core concept is not enough if you want high controllability.

You also need to teach the model that certain properties are not part of the core concept. They are independent things you can change with prompts.

Typical variables include:

- Appearance details such as hairstyle, hair color, accessories, props, and outfit pieces.
- State and action such as smiling, angry, crying, standing, running, jumping, aiming, blocking, and talking.
- Environment and scene such as city, desert, forest, spaceship interior, day, night, sunset, soft light, backlight, and dramatic contrast.
- Style and material such as anime, semi-realistic, painterly, metal, cloth, fur, or skin rendering.

Why explicitly describe these variables?

If the dataset always shows the character in silver armor and your captions never mention armor color, the model will likely treat silver armor as part of the core concept.

Later, when you prompt `trigger word, wearing a sweater`, you may get a sweater mixed with random armor, the character may stubbornly stay in armor, or the output may break.

A better approach is to collect images where armor color, background, expression, pose, and related variables actually vary. Then caption them clearly:

- `my_character_trigger wearing silver armor`
- `my_character_trigger wearing red armor`
- `my_character_trigger with a smiling expression`
- `my_character_trigger in a desert wasteland background`

Then the model learns:

- `my_character_trigger` means the character.
- Armor color, expression, and background are separate controls.

That is how you get prompts such as:

`my_character_trigger, wearing red armor, smiling, in a desert wasteland background`

and the LoRA actually understands and respects each part.

This is also why a basic usable LoRA may only need a few dozen images, while a highly controllable professional LoRA needs many more carefully varied examples with accurate, consistent captions for those variables.

Better controllability is not magic. It largely comes from more distinct variables, clearer demonstrations of how they change, and more accurate structured captions encoding them.

---

## 4. Why Simplified Tags Sometimes Work and Where They Fail

Now revisit the advice to simplify tags.

Once you understand core concept definition and variable description, it becomes clearer why simplification can sometimes help.

If captions over-describe every small fixed detail of the subject and background, list every cloud, every brick, and every tiny decoration, much of that text is noise for LoRA training.

It does not help define the core concept. It does not help define variables. It clutters the text embedding and can pollute prompt space.

On modern models, this can appear as:

- Less reliable response to important prompt tokens.
- Environment or action prompts being ignored more often.
- Strange failures when combining multiple conditions.

If you take a well-designed LoRA and add lots of irrelevant detail to the captions, then retrain with the same images and parameters, you may see worse environment control, worse action and pose response, and more random side effects from polluted text embeddings.

So yes, simplifying captions to remove irrelevant detail can reduce noise, reduce prompt pollution, and make LoRA behavior cleaner.

But that does not mean simpler is always better.

### What Must Not Be Simplified Away

Do not remove:

- The clear definition of your core concept.
- The variables you want to control, such as pose, background, clothing, and expression.

If you simplify everything down to `trigger word` plus `girl`, you may get a barely defined blob of style, weak fine-grained control, and poor alignment with the intended character.

### What Should Be Simplified

Simplify:

- Fixed details you do not intend to control as variables.
- Overly specific one-off elements that will not generalize.
- Details that do not belong to the core concept and only clutter the caption.

### What to Aim For

Aim for captions with enough detail to define the concept and encode the variables, but not so much detail that the caption becomes a wall of noise and important tokens lose weight.

The wording should be structured and logical, similar to a well-written prompt you would actually use at inference time.

---

## 5. Auto-Tagging: Where Tools Help and Where They Hurt

Even if you understand the ideal caption strategy, real life becomes hard when you have 100, 500, or 1,000 images.

Hand-writing captions for everything is not fun.

So we naturally use auto-taggers and auto-caption tools. They help, but they have inherent limitations for LoRA training.

First, they do not know your core concept. They can see and describe the image, but they do not know which part should be tied to the trigger word or what you consider important.

Second, they often over-describe the subject. They can produce many tiny details about clothing, lighting, and background, with little understanding of what is core, what is variable, and what is noise.

Third, they are not optimized for LoRA's needs. They are designed for generic image description or tagging, not for concept definition, variable separation, or avoiding prompt pollution.

The result is that auto-captions are a great starting point, but serious LoRA work usually needs:

- Heavy editing.
- Consistency checks.
- Manual decisions about what to keep, drop, or rephrase.

That is exactly where productivity drops.

---

## 6. Practical Takeaways

After training and testing many LoRAs, my experience is:

1. Every step matters.

Data collection, captioning, network settings, and training setup all affect the final behavior. Any shortcut tends to reappear later as strange behavior.

2. Captioning is not just describing the picture.

Captioning is how you define the core concept, declare what is variable and controllable, and avoid polluting prompt space.

3. Good LoRA captions usually follow a pattern.

They explicitly bind the trigger word to the subject, explicitly describe variables you care about, avoid over-describing fixed non-variable details, and stay structured, readable, and not bloated.

4. Simplify tags only by simplifying the right things.

Remove noise and irrelevant details, but keep the concept and variables clear.

5. Auto-taggers are tools, not oracles.

Use them as a baseline, then reshape captions around concept definition, variable coverage, and pollution control.

If you are deep into AIGC work such as LoRA training, text-to-image, text-to-video, or image-to-video, compare your tagging process against these questions:

- Does the caption clearly bind the trigger word to the intended concept?
- Does it distinguish the core concept from controllable variables?
- Does it remove irrelevant one-off details?
- Does it preserve variables you actually want to control later?
- Would the caption still make sense as a prompt at inference time?

That is the standard I use when building captions for training.
