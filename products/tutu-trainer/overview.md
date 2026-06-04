# Overview

> Bring AI model training back to what matters: simple, efficient, and professional.

Official download site: https://zhaotutu.xyz

Open the official site and choose the fully automated LoRA model trainer from the download area.

## Product Overview

TutuTrainer is AI model training software built for deep-learning enthusiasts, researchers, and AI practitioners. Its mission is to make complex AI training as simple as installing a game while preserving professional training capabilities.

## Core Value

Zero-barrier start. Broad model support. Intelligent training. Ready to use after installation.

Traditional AI training tools often require users to:

* Manually install Python, CUDA, and PyTorch.
* Configure complex environment variables.
* Debug dependency conflicts.
* Learn command-line parameters.
* Repeatedly test parameters to find a workable setup.

TutuTrainer is designed to remove that friction.

***

## Core Features

## 1. True Zero-Environment Setup

### One-click installation with no prerequisite environment

A typical training-tool setup may require:

```
1. Install Python and configure environment variables.
2. Install CUDA and verify driver compatibility.
3. Install PyTorch and choose the correct CUDA version.
4. Install many Python dependencies and resolve conflicts.
5. Configure a virtual environment to avoid polluting the system.
6. Hope everything runs correctly.
```

TutuTrainer setup is simpler:

```
1. Download TutuTrainer Setup.
2. Double-click the executable and open the app.
3. Start training.
Estimated time: 5-10 minutes.
```

| Feature               | TutuTrainer                 | Traditional Training Tools   |
| --------------------- | --------------------------- | ---------------------------- |
| Installation time     | 5-10 minutes                | 2-4 hours                    |
| Environment setup     | No manual configuration     | Requires technical knowledge |
| Dependency conflicts  | Avoided by packaged runtime | Common issue                 |
| System pollution      | Clean installation          | Multiple Python environments |
| Uninstall cleanliness | Clean uninstall             | Often leaves files           |
| Offline operation     | Fully supported             | Often needs network access   |

***

## 2. Broad Model Architecture Support

TutuTrainer is not a single-model trainer. It is a general AI training platform for image generation, video generation, and image editing models.

### Image Generation Models

| Model Family            | Supported Versions | VRAM Guidance | Notes                                 |
| ----------------------- | ------------------ | ------------- | ------------------------------------- |
| Anima                   | Base               | 8 GB          | Lightweight image generation workflow |
| ERNIE-Image             | Base               | 24 GB         | ERNIE image generation                |
| FLUX.1                  | Dev                | 24 GB         | High-end image generation             |
| FLUX.2 \[Klein] 4B Base | 4B Base            | 16 GB         | FLUX.2 Klein image generation         |
| FLUX.2 \[Klein] 9B Base | 9B Base            | 24 GB         | Larger FLUX.2 Klein image generation  |
| Qwen-Image              | Base               | 24 GB         | Qwen image generation                 |
| Qwen-Image-2512         | 2512               | 32 GB         | Newer Qwen image generation workflow  |
| SD 1.5                  | Full series        | 8 GB          | Classic lightweight Stable Diffusion  |
| SDXL                    | Base 1.0           | 16 GB         | High-quality Stable Diffusion XL      |
| Z-Image                 | Base               | 24 GB         | Z-Image base model workflow           |
| Z-Image De-Turbo        | De-Turbo           | 24 GB         | De-Turbo Z-Image workflow             |

### Video Generation Models

| Model Family          | Supported Versions | VRAM Guidance | Notes                                   |
| --------------------- | ------------------ | ------------- | --------------------------------------- |
| LTX-2 (Video+Audio)   | LTX-2              | 32 GB         | Video and audio training workflow       |
| LTX-2.3 (Video+Audio) | LTX-2.3            | 32 GB         | Newer video and audio training workflow |
| Wan 2.2 I2V (14B)     | 14B                | 24 GB         | Image-to-video training workflow        |
| Wan 2.2 T2V (14B)     | 14B                | 24 GB         | Text-to-video training workflow         |
| Wan 2.2 TI2V (5B)     | 5B                 | 16 GB         | Lighter text/image-to-video workflow    |

### Instruction and Editing Models

| Model Family         | Supported Versions | VRAM Guidance | Notes                               |
| -------------------- | ------------------ | ------------- | ----------------------------------- |
| FLUX.1-Kontext-dev   | Dev                | 24 GB         | Context-aware editing based on FLUX |
| Qwen-Image-Edit      | Original           | 32 GB         | Instruction-based image editing     |
| Qwen-Image-Edit-2509 | 2509               | 32 GB         | Qwen image-editing workflow         |
| Qwen-Image-Edit-2511 | 2511               | 32 GB         | Newer Qwen image-editing workflow   |

VRAM guidance is practical guidance for normal use, not a hard guarantee. Actual requirements can change with dataset size, resolution, selected precision, quantization, cache settings, and other running applications.

### Dataset Format Support

* Image datasets such as PNG, JPG, and WEBP.
* Video datasets such as MP4, AVI, and MOV with automatic frame extraction.
* Control datasets such as ControlNet and multi-control workflows.
* Image-to-video datasets with first-frame extraction.
* Automatic resolution handling with intelligent cropping and scaling.
* Multi-resolution buckets for efficient training at different sizes.

***

## 3. Intelligent Training

### Automatic parameter optimization

Traditional training often forces users to decide:

```
learning_rate: 1e-4 or 1e-5?
batch_size: 1 or 4?
gradient_accumulation: how many steps?
optimizer: AdamW, Prodigy, or Adafactor?
lr_scheduler: constant, cosine, or polynomial?
timestep_sampling: uniform or shifted?
noise_offset: use it or not?
min_snr_gamma: 5 or disabled?
```

TutuTrainer's design is to let regular users choose the core training intent while the app handles the rest automatically. The user focuses on model architecture, model source, dataset, sample prompts, and paths. Training parameters are recommended by the app according to the selected model and task.

***

## 4. Modern Graphical Interface

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Training Dashboard

* Real-time training progress visualization.
* GPU usage, VRAM usage, and temperature monitoring.
* Automatic sample preview updates.
* Real-time training speed display.

### Task Management Center

* Visual configuration editor.
* Training task queue management.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### Smart File Management

* Automatic dataset scanning.
* Image preview grid.
* Caption file editing.
* Batch renaming tools.
* Dataset quality checks.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

### Training History

* Training record archive.
* Hyperparameter comparison.
* Model version management.
* Training log replay.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

### User Experience Details

* Responsive layout from 1080p to 4K.
* Dark theme for long working sessions.
* Smart desktop notifications after training completes.
* Automatic configuration saving.
* Global search for models and datasets.
* Keyboard shortcuts for advanced users.

***

## 5. Resource Ecosystem

### Built-in Resource Library

TutuTrainer provides model resources and supports one-click cloud-drive downloads.

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

### Automatic Model Download

Supported model sources include:

* Hugging Face Hub.
* ModelScope.
* Local paths for offline use.

Example automatic download flow:

```
Click New Training.
Choose FLUX.1-dev.
Check whether the model exists locally.
If not, download from the fastest source.
Show progress and estimated time.
Verify integrity after download.
```

### Built-in Help

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

* Hover tips for parameters.
* Visual examples.
* Best practices.
* Common issue guidance.

***

## 6. Reliable Training Protection

### Interrupted Training Recovery

* Automatic checkpoints.
* Resume after interruption.
* Multiple training versions retained.

### Logging

```
logs/
├── training_20241218_143052.log
├── system_20241218.log
├── error_20241218.log
```

***

## Target Users

### AI Art Creators

* Train personal art-style LoRAs.
* Create virtual characters and IP assets.
* Fine-tune commercial generation models.

### Video Creators

* Train video-style models.
* Customize image-to-video models.
* Learn motion effects.

### Researchers

* Quickly validate ideas.
* Manage comparison experiments.
* Reproduce paper results.

### Business Users

* Train on private data.
* Manage model assets.
* Schedule batch tasks.

***

## System Requirements

Recommended configuration:

* OS: Windows 10 64-bit, Build 17763 or later.
* GPU: NVIDIA RTX 4090 or better, 24 GB VRAM.
* Memory: 64 GB RAM.
* Storage: 50 GB free space, SSD recommended.

***

## Typical Scenario: Character LoRA

Goal: train a virtual IP character for a client.

Steps:

1. Prepare 30-50 character photos with different angles, expressions, and outfits.
2. Put them into a new dataset folder.
3. Open TutuTrainer and choose a suitable model architecture.
4. Select the dataset path.
5. Start training in automatic mode.
6. Wait for training to finish.
7. Find the trained LoRA in the output folder.

Expected result:

* The model can reproduce the character appearance.
* Character consistency is maintained.
* Pose, outfit, and background can still be controlled by prompts.

## License

* Personal use: free.
* Commercial use: allowed. Keep the copyright notice.

## Start Now

Do not let complex environment configuration block your creativity.
