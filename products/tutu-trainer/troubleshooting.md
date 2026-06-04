# TutuTrainer Troubleshooting

This page collects common TutuTrainer issues and practical fixes.

## Out of Memory

If logs mention out-of-memory, the selected workflow needs more VRAM than the current device can provide.

Try:

- Use a GPU with more VRAM.
- Move the job to a cloud GPU.
- Use a lighter model family.
- Reduce dataset size or image requirements if the workflow allows it.
- Close other GPU-heavy applications before training.

Large models such as FLUX, SDXL, Qwen-Image, Z-Image, FLUX2, ERNIE-Image, and video-related models can require much more memory than SD1.5-style workflows.

## FLUX2 K Models Report Split Files

Some FLUX2 K workflows require merged ComfyUI-style model files instead of older split-file layouts.

If you used an older release that downloaded split files, remove the old FLUX2 K model folder and download the model again from the current workflow.

## Dataset Folder Exists but Does Not Appear

The most common cause is a path mismatch.

Check:

- The dataset root configured in path settings.
- Whether your dataset is inside the selected dataset root.
- Whether the dataset folder contains supported image files.
- Whether the application needs to be refreshed or restarted after path changes.

## Model Format Conversion Fails

Format conversion requires the correct model files and sometimes additional components such as VAE files. Some SDXL models include VAE data inside the base model, while others expect external files.

General checks:

- Confirm the source model type.
- Confirm the target conversion type is supported by your installed version.
- Confirm required VAE or companion files are configured.
- Keep network access available if the conversion needs to download configuration files.

At the time of the source documentation, conversion was mainly described for SDXL and SD1.5-style workflows.

## Training Stays at 0 Percent or Takes Too Long

Some jobs take time before visible progress appears. Larger models and larger datasets can be slow.

Check:

- GPU usage.
- Job logs.
- Dataset size.
- Selected model family.
- Output and cache paths.

If the model already appears fitted before the planned maximum steps, you can stop early and test the output, depending on the workflow and your goal.

## Too Many Steps

The recommended step count is calculated conservatively. You do not always need to complete every planned step. If samples already look good and no longer improve, stop and test the current output.

## Installer or Runtime Prompts

If Windows asks for WebView2 Runtime, install it and restart the application. Use official Microsoft or bundled runtime sources only.
