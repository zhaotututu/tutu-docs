# After 10,000 LoRAs: How to Tag Images for Training

This public article explains a practical way to think about captions and tags for LoRA training.

## The Common Pain Point

Many users collect images, run an automatic tagging tool, add a trigger word to every caption, train a LoRA, and still get unstable results.

Typical symptoms:

- The subject is not stable.
- Clothing details drift.
- The face changes from image to image.
- Background, pose, and style do not follow prompts reliably.
- The output looks like a mixture of incompatible examples.

The problem is often not just the training script. It is the dataset and caption strategy.

## Captions Tell the Model What to Learn

A caption is not just a description. In training, it also tells the model which visual features should be associated with which words.

If a detail appears in every image but is never captioned, the model may treat it as part of the trigger concept. If a detail varies but is captioned inconsistently, the model may learn unstable associations.

## Separate Stable Identity From Variable Details

When training a character or product LoRA, separate:

- Stable identity: the thing you want the LoRA to learn.
- Variable details: pose, background, lighting, camera angle, expression, outfit changes, and style.
- Optional attributes: details you want the prompt to control later.

The trigger word should represent the stable concept. Variable details should be captioned when you want the model to keep them controllable.

## Do Not Put Everything Into the Trigger Word

If every caption is only:

```text
my_character
```

the model may bind face, clothing, background, pose, lighting, and style all into one concept. This makes the LoRA hard to control.

Better captions describe meaningful visible details:

```text
my_character, red hair, blue dress, standing outdoors, garden background, soft daylight
```

Use a style that matches the model family and your training goal.

## When to Keep a Tag

Keep a tag when:

- The detail is visible.
- The detail varies across images.
- You want to control that detail at generation time.
- The model benefits from explicit tags for that concept.

Examples:

- outfit type.
- hair color.
- camera angle.
- background type.
- pose.
- expression.
- lighting.

## When to Remove a Tag

Remove or avoid a tag when:

- The detail is not visible.
- The tag is wrong.
- The tag is duplicated.
- The tag describes a detail you intentionally want absorbed into the trigger concept.
- The tag comes from an auto-tagger hallucination.

Bad tags can teach bad associations.

## Natural Captions vs Tag Phrases

Some workflows prefer comma-separated tags. Others work better with natural-language captions.

Tag phrase example:

```text
my_character, long hair, school uniform, sitting, classroom, soft light
```

Natural caption example:

```text
my_character is sitting in a classroom, wearing a school uniform, with long hair and soft indoor lighting.
```

Choose the caption style that matches the base model, trainer, and dataset type.

## Dataset Consistency

Before training, check:

- Are images sharp enough?
- Are there duplicates?
- Are there conflicting styles?
- Are important details captioned consistently?
- Is the trigger word spelled exactly the same each time?
- Are captions aligned with the correct image files?

Clean datasets usually beat messy large datasets.

## Practical Workflow

1. Collect images.
2. Remove low-quality and duplicate images.
3. Generate initial captions with Tutu Super Smart Tagger or another captioning tool.
4. Review captions manually.
5. Decide which details belong to the trigger concept and which should remain prompt-controllable.
6. Train a test LoRA.
7. Evaluate outputs with prompts that test identity, outfit, background, pose, and style separately.
8. Adjust captions and dataset composition if needed.

## Final Rule

Captioning is part of model design. Do not treat it as a mechanical last step. A good caption strategy makes the trained LoRA easier to control, easier to test, and easier to improve.
