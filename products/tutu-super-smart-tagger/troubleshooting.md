# Tutu Super Smart Tagger Troubleshooting

## Where Do I Download the Latest Version?

Use https://zhaotutu.xyz and choose the Super Smart Tagger package from the download area. Treat older cloud-drive links as historical references.

## Windows Asks for Another Disk During Update

This can happen with old update packages or cached installer state.

Try:

1. Close the application.
2. Download the latest installer or update package from the official website.
3. Run the latest package.
4. If you already installed optional runtime components, you usually do not need to install them again.

## Why Do I Need to Log In?

The account center is used to synchronize credits, device authorization, subscription state, invitation information, activation status, and online transaction records.

## I Bought an Older Activation Code. Do I Need to Buy Again?

The source documentation says old users should not need to repurchase only because the account center changed. Log in or register, then check the account page for device authorization, activation state, and subscription information.

If the account page does not show the expected state, contact official support through the channels shown in the application or website.

## How Do I Check Credits and Transactions?

Open the account page and refresh the server-side credit and transaction information. The app may provide time ranges such as recent months, recent year, or all records depending on version.

## Will Default AI Charge Twice?

Use the in-app billing and transaction records as the source of truth. In general, a successful request should create a successful record, while failed requests, insufficient-credit cases, or missing-result cases should not be treated as successful output.

## Image Captioning Fails

Check:

- The images are supported and readable.
- The selected model or default AI is available.
- The account has enough credits when using default AI.
- Your API key is valid if using a custom provider.
- Network access is available for online models.
- Local model services are running if using local models.

## Video Batch Reverse Captioning

Open the video reverse-captioning area, select a project, import videos, and use the batch entry from the list or detail page. After processing, review generated results before export.

## Online Video Import

Paste a supported video link or sharing text. The application attempts to detect the video URL automatically. If detection fails, paste the direct link when possible.

## API Key Safety

Never share API keys, cookies, or access tokens in public screenshots, support posts, or documents. If a key is exposed, rotate it with the provider.
