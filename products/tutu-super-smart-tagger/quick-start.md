# Tutu Super Smart Tagger Quick Start

Welcome to Tutu Super Smart Tagger. This quick start walks through the core workflow from installation to the first image and video captioning runs. If this is your first time using the app, read the sections in order. If you already know the basics, jump directly to the workflow you need.

Official download site: https://zhaotutu.xyz

## Optional Auxiliary Model Download

The package `llama-joycaption-beta-one` is an optional captioning model. Some users have unstable connections to the original hosting site, so mirror links are provided for convenience. Downloading this model is optional and does not affect the default cloud AI workflow.

MEGA:

`llama-joycaption-beta-one.rar`

https://mega.nz/file/sdoThDyZ#H9RpbTNKHbkqydRcQLpkSjclrF87rnRHHVR3DXue_Bw

Baidu Netdisk:

`llama-joycaption-beta-one.rar`

https://pan.baidu.com/s/1A3UGD-o4_L4NEmoaWv_mJg?pwd=qvkn

Extraction code: `qvkn`

Quark:

`llama-joycaption-beta-one.rar`

https://pan.quark.cn/s/a19f8a5e63d2

## Prepare the Runtime Environment

The installer package includes the main application and `vc_redist.x64.exe`. Install `vc_redist.x64.exe` first, then install Tutu Super Smart Tagger. If this runtime is already installed on your computer, you can skip it.

Ollama download site: https://www.ollama.com

Ollama is only required when you use local-model captioning. If you use the default AI workflow, you do not need to install or configure Ollama. When local mode is enabled, Ollama must stay running in the background, otherwise local captioning cannot work. The Ollama installer is simple: keep the default options and continue through the setup wizard. After installation, you can close the popup dialog as long as the Ollama tray icon remains visible in the lower-right system tray.

## Installation Notes

Install according to the prompts, but keep the installation path in English letters only. Do not use Chinese characters, special symbols, or unusual punctuation in the installation path. Otherwise, translation-related functions may not work correctly.

Do not close the installer without reason, and do not repeatedly switch backward and forward during installation. Before installing, it is recommended to close antivirus tools that may interfere with installation. Avoid installing the app into restricted system directories such as `C:\Program Files (x86)`.

It is recommended to install and open the app as administrator. The software contains many features, so the first launch may take a long time. Wait patiently until the interface finishes loading.

The original Chinese video guide is available here:

https://www.bilibili.com/video/BV1XjEez5EAN/?spm_id_from=333.1387.homepage.video_card.click

Each version update may add many new features. The full Chinese video collection contains more than ten videos. This English guide covers the same core usage path in text form, but watching the videos can still help if you are comfortable with Chinese-language tutorials.

For support, contact:

- QQ: `331506796`
- WeChat: `tujiang0411`

You can also apply to join one of the QQ groups for update support and community help:

- Tutu Pink Room: `628266084`
- Tutu Black Room: `950351015`
- Tutu Green Room: `903753035`

Choose any group you like. They provide the same kind of support.

---

## 0.1 First Use

### Step 1: Open the App After Installation

1. After installation, find the Tutu Super Smart Tagger shortcut on the desktop or in the Start menu. The default shortcut name may be `tutu-super-smart-marker`.

![Tutu Super Smart Tagger desktop shortcut](../../assets/tutu-super-smart-tagger/quick-start/quick-start-01-shortcut.png)

2. Double-click the shortcut to launch the app.

![Opening the app from the shortcut](../../assets/tutu-super-smart-tagger/quick-start/quick-start-02-open-app.png)

3. After the app opens, it enters the login page.

The login page is the unified account login page used by Tutu products.

![Unified account login page](../../assets/tutu-super-smart-tagger/quick-start/quick-start-03-login-page.png)

### Step 2: Log In or Register a Tutu Account

1. If you already have an account, enter your account information and log in directly.

2. Tutu products share the same account system. For example, if you registered an account in Tutu Video Publisher, you can use the same account to log in to Tutu Super Smart Tagger.

3. If you do not have an account, switch to the registration page from the login page. Follow the prompts to enter your email verification code and required information, then return to the login page.

The registration page is where you enter your email verification code, password, and invitation code.

![Account registration page](../../assets/tutu-super-smart-tagger/quick-start/quick-start-04-register-page.png)

4. After login succeeds, the app synchronizes your account, credits, subscription status, and device authorization status.

![Account status after login](../../assets/tutu-super-smart-tagger/quick-start/quick-start-05-account-status.png)

### Step 3: Start with the Lowest-Priced Credit Package

1. After login, open the account or credits page and choose the credit purchase entry.

2. For a first test, buy the lowest-priced credit package available in your region. In the original Chinese flow, this is the 12 RMB package. This lets you confirm that the default AI workflow works correctly before you spend more.

![Credit purchase entry](../../assets/tutu-super-smart-tagger/quick-start/quick-start-06-buy-credits.png)

3. After payment, return to the app. Refresh or re-enter the account page and confirm that the credits have arrived.

4. Credits are used by default AI features such as image prompt reverse captioning, natural-language descriptions, paired descriptions, and video understanding.

### Step 4: Go to Captioning and Start Directly

1. Return to the main interface. Open Project Management and create or select a project.

![Project management page](../../assets/tutu-super-smart-tagger/quick-start/quick-start-07-project-management.png)

2. Open the Image Prompt Reverse Captioning page from the top navigation. Choose Prompt Phrase Mode, Natural Language Description, or Reference Reverse Captioning based on your task.

3. After importing images, you can generate captions for one image or run batch generation. The default AI uses your credits to complete the processing.

4. After reviewing the generated results, use the page controls to save, export, or perform batch operations.

![Image captioning workspace](../../assets/tutu-super-smart-tagger/quick-start/quick-start-08-image-captioning.png)

### Step 5: When You Need Model Configuration

1. Regular new users do not need to configure a model and do not need to prepare an API key.

2. If you want to use your own API key, a custom provider, a local model, or local GPU processing, open System Configuration and complete the advanced setup there.

## 0.2 Image Captioning Quick Start

Image captioning is the core feature of the app. It adds tags or descriptions to images and helps you build training datasets. This section walks through one complete captioning run.

Prompt Phrase Mode can be completed in four steps.

### Step 1: Create and Select a Project

Open Project Management, click the New Project button, fill in the required information, and create the project.

![Create a new project](../../assets/tutu-super-smart-tagger/quick-start/quick-start-09-new-project.png)

After the project is created, select it.

![Select the newly created project](../../assets/tutu-super-smart-tagger/quick-start/quick-start-10-select-project.png)

### Step 2: Import and Select Images

1. Click Image Prompt Reverse Captioning in the navigation bar, then choose Prompt Phrase Mode.

![Open Prompt Phrase Mode](../../assets/tutu-super-smart-tagger/quick-start/quick-start-11-phrase-mode.png)

2. Click the Import Images button in the toolbar.

![Import images button](../../assets/tutu-super-smart-tagger/quick-start/quick-start-12-import-images.png)

3. Choose one or more images. Multi-select is supported. You can also use batch selection. If no image is selected, the captioning function processes all images on the current page by default.

![Select images for captioning](../../assets/tutu-super-smart-tagger/quick-start/quick-start-13-select-images.png)

### Step 3: Generate Reverse Prompts

1. Click the Smart Generate button in the toolbar. It is the round button with the magic-wand icon.

![Smart Generate button](../../assets/tutu-super-smart-tagger/quick-start/quick-start-14-smart-generate.png)

2. Choose a generation mode based on your task. If the result is for art-creation reference, choose a general description. If the result is for LoRA model training or similar training tasks, choose a more precise mode.

![Choose generation mode](../../assets/tutu-super-smart-tagger/quick-start/quick-start-15-generation-mode.png)

3. Click Start Execution.

![Start execution button](../../assets/tutu-super-smart-tagger/quick-start/quick-start-16-start-task.png)

4. Wait for generation to finish. Tags are added to the images automatically.

![Generated tags added to images](../../assets/tutu-super-smart-tagger/quick-start/quick-start-17-generated-tags.png)

### Step 4: Export the Dataset

1. Click the Export Dataset button in the toolbar. It is the round button with the download icon.

![Export dataset button](../../assets/tutu-super-smart-tagger/quick-start/quick-start-18-export-dataset.png)

2. Choose the output directory.

3. Click Start Export.

4. After export completes, the dataset files are saved in the selected folder.

You have now completed your first image captioning workflow.

Advanced tips:

- You can manually add, edit, and delete tags.
- Batch operations let you process many images at once.
- Element filtering and other advanced processing tools are available for more complex workflows.
- For the full Prompt Phrase Mode behavior, read the detailed Image Prompt Reverse Captioning chapter.

Natural Language Mode follows a similar workflow and is used to generate more detailed natural-language descriptions.

Reference Reverse Captioning is used to build image-relationship datasets. Read the Reference Reverse Captioning section for the full workflow.

---

## 0.3 Video Reverse Prompt Quick Start

Video captioning provides AI-assisted video processing, including scene detection, content analysis, and clipping-related workflows.

### Step 1: Import a Video

1. Click Video Prompt Reverse Captioning in the navigation bar.

2. Click Import Local Video or Link Online Video in the toolbar, then add the video.

![Import local video or link online video](../../assets/tutu-super-smart-tagger/quick-start/quick-start-19-import-video.png)

3. Wait for processing to finish. A progress dialog is displayed during processing.

### Step 2: Generate AI Content

1. Select one or more video files.

2. Click Batch Reverse Prompts.

![Batch reverse prompts button](../../assets/tutu-super-smart-tagger/quick-start/quick-start-20-batch-video-caption.png)

3. Choose the processing type you need, then start batch prompt reverse captioning.

![Choose video processing type](../../assets/tutu-super-smart-tagger/quick-start/quick-start-21-video-processing-type.png)

### Step 3: Export

![Video export page](../../assets/tutu-super-smart-tagger/quick-start/quick-start-22-video-export.png)

1. Click Batch Export.

![Start batch export](../../assets/tutu-super-smart-tagger/quick-start/quick-start-23-start-video-export.png)

2. Choose a suitable location.

3. Click Start Batch Export.

---

## Next Steps

After finishing the quick start, continue with the following:

1. Learn the detailed chapters. Watch the video collection and read the full guide to understand every feature: https://space.bilibili.com/431046154/lists/6441798?type=season

2. Practice with your own data. Try each function with real image and video material.

3. If you run into problems, read the troubleshooting chapter.

This quick start only covers the most basic operating path. It helps you become familiar with the main functions, but the app contains many more features. Read the detailed chapters according to your actual workflow.
