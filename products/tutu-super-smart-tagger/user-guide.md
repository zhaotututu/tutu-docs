# Tutu Super Smart Tagger User Guide

This guide covers the main user-facing workflows in Tutu Super Smart Tagger.

## First Run and Account

After installation, open the application from the desktop or Start menu.

The current workflow starts with login or registration:

- Existing users can log in directly.
- New users can register with email verification.
- After login, the account page shows credits, subscription information, device authorization, activation state, invitation information, and transaction records.

Older activation-code flows may still appear in historical documents, but the current public guidance is to use the account page inside the official application.

## Default AI

The default AI is intended for users who want to start immediately without configuring their own model provider.

It can be used for:

- Image prompt reverse captioning.
- Natural-language descriptions.
- Paired image descriptions.
- Video understanding.

Successful default-AI requests may consume credits depending on the product rules shown in the app. Failed requests or missing results should not be treated as successful output.

## Model Configuration

Advanced users can configure:

- External model APIs.
- Local models.
- Custom compatible endpoints.
- API keys from supported providers.

Keep API keys private. Do not publish them in screenshots, logs, shared documents, or support messages.

## Image Prompt Workflow

Use this workflow when you want prompt-style tags for training or generation.

1. Create or open an image project.
2. Import images.
3. Choose prompt-phrase generation.
4. Run batch generation.
5. Review tags.
6. Remove wrong, duplicated, or misleading tags.
7. Export the final captions.

## Natural-Language Caption Workflow

Use this workflow when the training model benefits from full-sentence captions.

1. Import images.
2. Choose natural-language description.
3. Generate descriptions.
4. Review descriptions for visual accuracy.
5. Edit any hallucinated or missing details.
6. Export captions.

Good captions describe what is visible. Avoid adding details that are not in the image unless you intentionally need a training trigger.

## Paired Image Description Workflow

Use paired descriptions for image editing datasets where each item has a source image and a result image.

1. Prepare source/result image pairs.
2. Import or organize the pairs in the project.
3. Use paired reverse captioning.
4. Review the generated transformation description.
5. Export the paired dataset.

This is useful for workflows that need descriptions of how one image changes into another.

## Batch Processing

Batch processing helps process many images or videos at once.

Before running a large batch:

- Test on a small subset.
- Confirm the model and mode are correct.
- Confirm enough credits or local resources are available.
- Keep the application open until the batch completes.

## Video Workflows

The video area can process local videos and supported online video links.

Possible outputs include:

- Scene descriptions.
- Video summaries.
- Spoken-script notes.
- Batch reverse captioning results.

After generation, review the output because video understanding can miss fast cuts, small text, or ambiguous scenes.

## Element Editor

The element editor supports automatic recognition and manual selection. It is useful when you need to identify or work around repeated elements such as:

- Watermarks.
- Subtitles.
- Logos.
- Fixed screen regions.

Use manual selection when automatic detection is not precise enough.

## Export

Export generated data after review. Choose the format that matches your downstream workflow. For LoRA training, keep captions aligned with image file names and dataset folders.

## Update and Language

The application may support system-language following and manual language selection. It also includes clearer update feedback and task-style model downloads in current versions.

Use the official website for installers and update packages.
