# Troubleshooting

This section collects common questions about installation, updates, login, credits, models, video workflows, element editing, and feedback. When you encounter a problem, first locate the subsection related to the page or operation you are using.

Download the app from https://zhaotutu.xyz. At the bottom of the page, choose the download entry for Tutu Super Smart Tagger. The official site entry and cloud-drive entry are updated together.

Support site: https://zhaotutu.xyz

## Installation, Updates, and Login

### What is the latest version? Where should I download it?

The latest version is based on the current public release shown by the app and official website. Download from the official site at https://zhaotutu.xyz. Do not continue relying on historical cloud-drive direct links or old update packages.

### What should I do if update says "Please insert disk 3"?

This is a common issue caused by old update packages or installer cache. Close the app, download the latest installer or update package from the official site, and install again. If Ollama or runtime dependencies are already installed, you do not need to reinstall those bundled components.

### Why do I now need to log in or register?

The current version includes an account center. After logging in or registering with email verification, the app can synchronize credits, device authorization, subscriptions, invitation code, and online transaction history. New users need to confirm the user agreement before registration.

### I already bought an activation code as an old user. Do I need to buy again?

No. After logging in or registering, the system tries to recognize older authorization according to the current device information. Open Account and Credits to view device authorization, activation status, and subscription information.

## Account, Credits, and Charging

### How do I view credits and transaction history?

Open Account and Credits, then click refresh to synchronize server-side credits and transaction history. The transaction range can be the last 3 months, last 6 months, last 1 year, or all records, which is useful for cross-device reconciliation.

### Will default AI charge repeatedly?

The default AI charging flow has been tightened. Image, paired-image, and video requests write transaction history after success. When the same video generates scene description, summary, and spoken script at the same time, the app merges them into one video-understanding request and charges credits once according to the real amount returned by the server.

### What if credit charging fails or transaction history does not appear?

First refresh credits and transaction history on the account page, and confirm the selected transaction range. The app writes successful default AI charges only after success. Failed tasks, insufficient credits, or missing results should not appear as successful charges.

### Are credits still available after changing computers?

Credits follow the account. Log in with the same account to view balance and transaction history. Device authorization follows hardware and does not automatically migrate to another computer just because the same account logs in.

## Image Reverse Prompts, Prompts, and Image Generation

### What should I do if image prompts or image generation fail?

Read the specific reason shown in the dialog. Possible causes include insufficient credits, unavailable model, too frequent requests, oversized images, temporary API issues, or API key configuration errors. Default AI can be used directly. External models require checking keys and model availability in Model Settings.

### How do I choose Prompt Phrase Mode, Natural Language Mode, or Reference Reverse Captioning?

Use Prompt Phrase Mode when you need keywords and tags. Use Natural Language Mode when you need complete descriptive sentences. Use Reference Reverse Captioning when you need to describe the change from a source image to a result image.

### Must I configure a model before first use?

No. In Default Mode, logging in and buying credits is enough to use default AI. Advanced configuration is needed only when using your own API key, local model, or custom provider.

## Video Reverse Prompts and Online Videos

### Where is video batch reverse captioning?

Open Video Prompt Reverse Captioning, select a project, and import videos. Then use the batch reverse entry in the video list or detail page to generate scene descriptions, summaries, or spoken scripts. After completion, the page automatically switches to generated results.

### How do I import online videos?

Click Link Online Video on the video page, paste a video link or shared text, and the system automatically recognizes the link inside it. If the platform restricts access, the link is invalid, or the network environment does not support it, the interface shows the failure reason. In that case, download the video locally and import it as a local video.

### Should I still look for the old YouTube analysis button?

No. Do not follow older documents that point to a separate YouTube analysis button. The current unified path is Link Online Video on the video page. Paste a link or shared text there.

### Does generating scene description, summary, and spoken script for the same video charge multiple times?

In default AI gateway mode, the app tries to merge them into one video-understanding request and charge credits once according to the real amount returned by the server, avoiding repeated analysis.

### Where is AI video enhancement?

The AI video enhancement button is still hidden from the main interface and is not part of the regular workflow. Video element editing and package export remain available.

## Element Editor, Local Models, and Performance

### Why does Element Editor say models are missing or processing cannot run?

Element removal and video repair depend on local models and GPU. Start task-style download from the video model or Element Editor entry first, then wait until speed, downloaded size, remaining time, and related states complete. Without an available GPU, these processing workflows are blocked.

### How do I choose manual box selection or automatic recognition?

Automatic recognition is suitable when the model should locate the target by itself. Manual box selection is suitable for watermarks, subtitles, fixed corner labels, regular rectangular areas, and other clearly positioned targets. The current version supports switching to manual box selection in Element Editor.

### Where did the old video model configuration page go?

It is now managed under System Configuration -> Model Settings. Video reverse-captioning capability is controlled through model configuration, external providers, and the video reverse-prompt marker.

### What should I do if the app is slow or tasks are slow?

Reduce the number of tasks running at the same time. Check VRAM, memory, and disk space in the bottom status bar. For local-model tasks, also confirm that the model is fully downloaded and loaded correctly. After tasks finish, use Clear VRAM in the bottom bar to release leftover VRAM.

## Projects, Batch Processing, and Interface Settings

### For first use, should I create a new project or import a project?

In most cases, create a new project first. Import Labeled Dataset is only for continuing to edit old prompt or natural-language caption datasets.

### Why does the image or video entry say I need to select a project first?

Images, videos, and generated results all belong to a project. Return to Project Management and click a project row to set the current project.

### What is batch processing mainly used for now?

It is mainly used for resizing or formatting images, renaming materials, and detecting similar images. Export images from the corresponding image mode. Run video batch reverse captioning and export from the video page.

### Can Detect Similar Images delete images directly?

The page provides deletion operations, but deletion is high risk. Preview first, confirm the range, and back up if necessary.

### Where do I change language and dark mode?

Open System Configuration -> Other Settings to change language. Theme is switched from the top-bar theme button among Follow System, Light, and Dark.

## If the Problem Still Cannot Be Solved

### What should I do if the problem still exists?

Record the app version, operation page, error text, whether you used default AI, external model, or local model, and the approximate format of the video or image. Then contact Tutu support. For credit-related issues, also provide an account-page transaction-history screenshot or the time of the charge.

### How do I contact technical support?

QQ: `331506796`

WeChat: `tujiang0411`

When giving feedback, include account email, problem screenshots, task type, and necessary logs.
