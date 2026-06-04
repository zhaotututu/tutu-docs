# TutuTrainer Cloud Image Guide

This page explains how to think about cloud or mirrored environments for TutuTrainer.

Some users prefer a cloud GPU environment when local hardware is not strong enough for large model families. The original Chinese documentation included a cloud image guide for a preconfigured trainer environment. The English version keeps the operational guidance but avoids tying users to a single local-only assumption.

## When to Use a Cloud GPU

Consider cloud GPU training when:

- Your local GPU runs out of memory.
- You want to train FLUX, SDXL, Qwen-Image, Z-Image, FLUX2, ERNIE-Image, or other high-memory models.
- Local training is too slow.
- You want a clean, repeatable environment.

## Basic Workflow

1. Start the cloud machine or image.
2. Launch TutuTrainer from the desktop shortcut or installed application entry.
3. Wait for the interface to load.
4. Open path settings.
5. Configure dataset, model, and output folders.
6. Upload or mount your dataset.
7. Choose the model architecture and model source.
8. Start training and monitor GPU usage.
9. Download the final output files when training is complete.

## Path Setup

Cloud environments often use different disk paths from your local PC. Always check the configured paths before starting a job:

- Dataset path.
- Model path.
- Output path.
- Temporary or cache path, if exposed by the installed version.

If your dataset folder exists but does not appear in the UI, the most common cause is that TutuTrainer is looking at a different dataset root.

## Data Transfer Tips

- Compress large datasets before upload when possible.
- Avoid uploading duplicate files.
- Keep a local backup of important datasets.
- Download final LoRA files, sample images, and logs before shutting down a temporary cloud instance.

## Cost and Safety Notes

- Cloud GPU time, storage, and network traffic may create third-party costs.
- Do not leave paid cloud machines running when they are not needed.
- Do not store private API keys, account cookies, or personal files on shared or untrusted machines.
- If a cloud image is provided by an unofficial source, treat it as untrusted.

## Troubleshooting

If the cloud image cannot see your data:

- Recheck the mounted folder path.
- Reopen path settings inside TutuTrainer.
- Confirm the dataset folder contains image files and captions.
- Restart the application after changing paths.

If training fails with out-of-memory errors:

- Use a GPU with more VRAM.
- Reduce dataset or resolution requirements where the UI allows it.
- Choose a lighter model family if appropriate.
- Use the official recommended workflow for the selected model architecture.
