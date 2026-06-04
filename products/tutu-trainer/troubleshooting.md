# TutuTrainer Troubleshooting

## Official Download

Open https://zhaotutu.xyz and choose the fully automated LoRA model trainer from the download area.

## 1. Log shows out of memory

The selected model or training configuration exceeds available VRAM.

Recommended actions:

1. Use a cloud GPU workflow if local VRAM is not enough.
2. Choose a smaller model architecture.
3. Reduce dataset size, especially for editing models.
4. Close other GPU-heavy applications before training.

Cloud GPU entry referenced in the source document:

https://lincore.wuying.aliyun.com/?spm=5176.43105039.J_vUIfvN494LRvoTKxXOP77.2.31063b3fwIRAvU#/

## 2. FLUX2 K series reports separated files

FLUX2 K series training requires a merged model format, commonly the ComfyUI-style merged format.

Older versions used separated files. Because the model files were too large and inconvenient for users, the current workflow changed to merged format. If you used an older version, delete the old FLUX2 K model folder and download the current model again.

## 3. Dataset is in the folder but does not appear in the app

After opening the app, first check whether the configured path is correct. The path may not be pointing to the folder you think it is pointing to. Set the correct dataset path in the app and refresh the list.

## 4. Format conversion always fails

Format conversion requires the correct VAE and related files. Current conversion support is mainly for SDXL and SD1.5, and conversion may require network access.

Many SDXL base models already include VAE-related content, so confirm the model type before conversion.

## 5. Training has no error but stays at 0, or training time is extremely long

This is usually caused by insufficient resources. Try a different model for training, or reduce dataset size for editing models.

It may also be caused by dataset naming. Do not name dataset folders directly as `1`, `2`, `3`. Names like `01`, `02`, `03` are better. The safest option is simple English letters plus numbers, such as `work01` or `work02`.

## 6. Why are there so many steps? Why is training longer than other trainers?

The step count is calculated according to an upper-bound estimate. It does not mean the task must always finish every step. If the result has already fitted well enough, you can stop early and test the output.
