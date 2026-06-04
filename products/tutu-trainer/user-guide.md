# TutuTrainer User Guide

This guide explains the normal desktop workflow for training your first LoRA with TutuTrainer.

Official website: https://zhaotutu.xyz

## System Requirements

TutuTrainer is a Windows desktop application. A supported NVIDIA GPU is strongly recommended for local training. Larger model families require more VRAM.

General guidance:

- SD1.5 workflows can run on lower VRAM than SDXL or FLUX-style workflows.
- SDXL workflows usually need more memory and longer training time.
- FLUX, Qwen-Image, Z-Image, FLUX2, ERNIE-Image, and video-related workflows may require high VRAM or cloud GPU resources.
- Keep enough disk space for models, datasets, logs, samples, and outputs.

If your local GPU is not enough, consider a cloud GPU environment.

## Install and Start

1. Download the installer from https://zhaotutu.xyz.
2. Run the installer.
3. Launch TutuTrainer from the desktop or Start menu.
4. On first launch, wait for the interface to load. The first run may take longer than later runs.
5. If Windows prompts for a WebView2 Runtime dependency, install it before continuing.

## Configure Paths

Open the dashboard and use path settings to configure the folders used by the application.

Recommended paths:

- Training output folder: where completed LoRA files and job outputs are saved.
- Dataset folder: where training datasets are stored.
- Model folder: where base models are stored.

After changing paths, save the settings and confirm the UI can see your datasets and models.

## Prepare a Dataset

1. Open the dataset page.
2. Create a dataset with a clear English folder name, such as `my_character` or `product_style_v1`.
3. Import images into the dataset.
4. Use supported image formats such as JPG, JPEG, and PNG.
5. Add captions for each image.

Captions should describe the content of the image. Depending on the model and training goal, captions may be written as natural-language descriptions or prompt-style tag phrases.

Example:

```text
a beautiful woman with red hair, wearing a blue dress, standing in a garden, natural lighting
```

For large datasets, use a captioning tool such as Tutu Super Smart Tagger to generate and review captions in batches.

## Choose Training Inputs

Open the training dashboard and choose:

- Model architecture.
- Model source.
- Target dataset.
- Sample prompts, if you want periodic preview images.
- Output path.

Model source options may include:

- Automatic download: use this when you want TutuTrainer to fetch required files when available.
- Local model: use this when you already have the model files on disk.
- Custom model: use this for models you configured in the model manager.

## Start Training

1. Check that the dataset and model choices are correct.
2. Click the start training button.
3. TutuTrainer calculates recommended training parameters based on the selected model, dataset, and device situation.
4. Monitor the training job from the dashboard.

During training, you can watch:

- Current job progress.
- GPU status.
- Logs.
- Sampling output.
- Output folder updates.

## Review Results

After training finishes:

1. Open the job output folder.
2. Review the generated LoRA files.
3. Check samples and logs.
4. Test the trained LoRA in your target generation workflow.

If the result is undertrained, overtrained, unstable, or does not follow prompts well, review the dataset quality, caption strategy, trigger word, model choice, and training duration.

## Dataset Management Tips

- Keep one concept per dataset when possible.
- Use consistent captions.
- Avoid mixing too many unrelated styles, outfits, backgrounds, or subject identities unless that is your goal.
- Remove low-quality, blurry, duplicated, or misleading images.
- Use clear folder names and keep backups of important datasets.

## Base Model Management

Use the model manager to organize base models and custom models. When using local models, verify that all required files are present. Some model families require additional components such as VAE files or specific merged formats.

## Best Practices

- Start with a small clean dataset before scaling up.
- Keep captions honest: describe what is visible and avoid forcing unrelated tags into every image.
- Use sample prompts to check progress during training.
- Stop early if the model has already reached the quality you need.
- Keep old outputs until you have tested the new one.
- Use official downloads and avoid modified model packages from unknown sources.
