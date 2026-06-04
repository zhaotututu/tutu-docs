# Tutu Super Smart Tagger Troubleshooting

This top-level FAQ collects the most common issues. For the complete troubleshooting chapter, see [User Guide: Troubleshooting](user-guide/troubleshooting.md).

Official download site: https://zhaotutu.xyz

Open the official site and choose Super Smart Tagger from the download area. The official website and cloud-drive download entry are updated together.

## 1. What is the latest version? Where should I download it?

The current latest public version is 1.1.7. Download it from the bottom download area of https://zhaotutu.xyz. Do not rely on historical cloud-drive direct links or old update packages.

## 2. What should I do if update says "Please insert disk 3"?

This is usually caused by an old update package or installer cache. Close the app, download the latest 1.1.7 installer or update package from the official site, and install again. If Ollama or runtime dependencies are already installed, you do not need to reinstall those bundled components.

## 3. Why do I now need to log in or register?

Version 1.1.7 includes the account center. After logging in or registering with email verification, the app can synchronize credits, device authorization, subscriptions, invitation code, and online transaction history. New users need to confirm the user agreement before registration.

## 4. I already bought an activation code. Do I need to buy again?

No. After logging in or registering, the system tries to recognize older authorization based on the current device information. Open Account and Credits to view device authorization, activation status, and subscription information.

## 5. How do I view credits and transaction history?

Open Account and Credits, then click refresh to synchronize server-side credits and transaction history. Available ranges include the last 3 months, last 6 months, last 1 year, and all records. This is useful for cross-device reconciliation.

## 6. Will default AI charge repeatedly?

The default AI charging flow has been tightened in 1.1.7. Image, paired-image, and video requests write transaction history after success. When the same video generates scene description, summary, and spoken script at the same time, they are merged into one video-understanding request and charged once according to the real amount returned by the server.

## 7. What should I do if image prompts or image generation fail?

Read the specific reason shown in the dialog. Possible causes include insufficient credits, unavailable model, too frequent requests, oversized images, temporary API issues, or API key configuration errors. Default AI can be used directly. External models require checking keys and model availability in Model Settings.

## 8. Where is video batch reverse captioning?

Open Video Prompt Reverse Captioning, select a project, and import videos. Then use the batch reverse entry in the video list or detail page to generate scene descriptions, summaries, or spoken scripts. After completion, the page automatically switches to the generated result.

## 9. How do I import online videos?

Click Link Online Video on the video page, paste a video link or shared text, and the system automatically recognizes the link inside it. If the platform restricts access, the link is invalid, or the network environment does not support it, the interface shows the failure reason. In that case, download the video locally and import it as a local video.

## 10. Why does Element Editor say models are missing or processing cannot run?

Element removal and video repair depend on local models and GPU. Start task-style download from the video model or Element Editor entry first, then wait until speed, downloaded size, remaining time, and related states complete. Without an available GPU, this kind of processing is blocked.

## 11. How do I choose manual box selection or automatic recognition?

Automatic recognition is suitable when the model should locate the target by itself. Manual box selection is suitable for watermarks, subtitles, fixed corner labels, regular rectangular areas, and other clearly positioned targets. Version 1.1.7 supports switching to manual box selection in Element Editor.

## 12. Where do I change language and dark mode?

Open Other Settings. Language can be Follow System, Chinese, or English. Theme can be Follow System, Light, or Dark. The top theme button can also switch quickly.

## 13. What should I do if the problem still exists?

Record the app version, operation page, error text, whether you used default AI, external model, or local model, and the approximate format of the video or image. Then contact Tutu support. For credit-related issues, also provide an account-page transaction-history screenshot or the time of the charge.

Support:

- QQ: `331506796`
- WeChat: `tujiang0411`
