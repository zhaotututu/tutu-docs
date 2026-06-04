# Tutu Video Prompt Tool Overview

Tutu Video Prompt Tool V2.0 is a Windows desktop tool for expanding short ideas into richer prompts for AI video generation. It supports both text-to-video and image-to-video workflows.

The tool is designed for creators who want faster prompt drafting, reusable prompt history, and more consistent camera, lighting, style, motion, and scene descriptions.

Official website: https://zhaotutu.xyz

## What It Does

Tutu Video Prompt Tool takes a short prompt and expands it into a more structured video prompt.

It can add details such as:

- Subject appearance.
- Action and motion.
- Scene and background.
- Camera movement.
- Lighting.
- Style.
- Composition.
- Image-to-video motion direction.
- Negative prompt guidance.

## Core Features

| Feature area | V2.0 upgrade | User benefit |
| --- | --- | --- |
| Interface | Dark and light themes | More comfortable for long sessions. |
| Efficiency | AI naming and one-click apply | Reduces repetitive prompt management work. |
| Personalization | Custom templates and default negative prompts | Fits personal creation style. |
| Stability | Qwen-based text and vision model workflow | Improves prompt expansion success rate. |

## Text-to-Video Mode

Text-to-video mode expands a short written idea.

Example input:

```text
a girl dancing
```

Example expanded direction:

```text
documentary photography style, a young East Asian girl wearing a flowing white dress dances in an open square at dusk, medium shot with smooth tracking camera movement, soft natural light, orange sunset background, hair and skirt moving with the wind, dynamic yet graceful motion
```

Available style templates may include:

- Standard.
- Anime.
- Cinematic.
- Realistic.

The exact template list can vary by version.

## Image-to-Video Mode

Image-to-video mode uses an uploaded image plus optional keywords to generate a prompt that fits the image.

The tool can help describe:

- Main subject.
- Color palette.
- Composition.
- Visual style.
- Motion direction.
- Lighting.
- Elements that should remain consistent with the source image.

For example, after uploading an anime character image, the tool may add terms related to cel shading, anime rendering, light effects, and character motion.

## Prompt Library

The prompt library helps you save, find, and reuse generated prompts.

Supported library behavior includes:

- Automatic saving of generated prompts.
- Date filters such as today, this week, and this month.
- Type labels for different prompt categories.
- Search.
- Copy, edit, and delete actions.
- One-click apply where supported by the installed version.

## Custom Settings

The settings page can include:

- API key management.
- Theme switching.
- Language switching between Chinese and English.
- Custom system prompt templates.
- Default negative prompt settings.

## Quick Start

1. Download and install the latest version from the official channel.
2. Register or sign in to the required model service if your workflow uses an external API key.
3. Add your API key in settings.
4. Choose text-to-video or image-to-video mode.
5. Enter a short prompt, and upload an image if needed.
6. Choose a style template.
7. Generate the expanded prompt.
8. Copy or apply the result to your video generation workflow.

## System Requirements

- Windows 10 or Windows 11.
- About 2 GB of free storage.
- Network access for API calls.
- No Python environment required for normal installer usage.
- No coding knowledge required for normal use.

## Notes

- Generated prompts are suggestions and should be reviewed before use.
- Different video models may respond differently to the same expanded prompt.
- Some models work better with shorter prompts; others benefit from detailed prompts.
- Keep useful prompts in the library so you can compare what actually works.

## FAQ

### Do I need a paid API?

The tool uses an external model service API key for supported workflows. Some providers offer free quotas, but quota, pricing, and availability are controlled by the provider and may change. Check the provider account page before heavy usage.

### What if the result is unstable?

Try adjusting creativity or diversity parameters, switching templates, simplifying the prompt, or changing the model setting if the installed version supports it.

### Is this a developer tool?

No. The installer workflow is intended for non-technical users. You do not need to configure Python or run code for normal use.
