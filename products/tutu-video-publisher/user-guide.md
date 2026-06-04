# Tutu Video Publisher User Guide

Tutu Video Publisher is a Windows application for scheduling and publishing videos across multiple platforms. You upload a video, configure target platforms, and optionally let AI generate platform-specific titles, descriptions, tags, and cover images.

Source document version: v1.1.8, updated April 13, 2026.

Official website: https://zhaotutu.xyz

## Contents

- [Product Overview](#product-overview)
- [Quick Start](#quick-start)
- [Account and Credits](#account-and-credits)
- [Platform Account Management](#platform-account-management)
- [Publishing Plans](#publishing-plans)
- [Dashboard](#dashboard)
- [AI Analysis](#ai-analysis)
- [System Settings](#system-settings)
- [FAQ](#faq)
- [Credit Rules](#credit-rules)
- [API and Agent Integration](#api-and-agent-integration)
- [Contact and Feedback](#contact-and-feedback)

## Product Overview

Tutu Video Publisher helps creators and operators publish one video to multiple platforms through a scheduled workflow. It is designed for users who need repeatable publishing, multi-account operation, AI-assisted copywriting, and simple status monitoring.

### Supported Platforms

| Platform | Login method | Typical session validity |
| --- | --- | --- |
| Douyin | Browser QR-code login | About 5 days |
| Kuaishou | Browser QR-code login | About 5 days |
| Bilibili | TV-side QR-code login | Longer |
| WeChat Channels | WeChat QR-code login | About 24 hours |
| TikTok | Browser login | About 5 days |
| YouTube | Google OAuth authorization | Long-term |
| Weibo | Browser login | About 5 days |

Important: WeChat Channels sessions are usually valid for about 24 hours. Verify or log in again before publishing to WeChat Channels each day.

## Quick Start

Complete these five steps to schedule your first automatic publish.

### Step 1: Register and Sign In

1. Open the app.
2. Click Account & Credits in the left navigation.
3. Switch to registration mode.
4. Enter your email address, verification code, and password.
5. Add credits if you plan to use AI auto-completion.

AI auto-completion is optional, but strongly recommended because it can save a lot of manual title, description, tag, and cover work.

### Step 2: Configure Platform Accounts

1. Click Settings in the left navigation.
2. Find Platform Configuration.
3. Find the platform you want to use, such as Douyin.
4. Turn on the platform switch.
5. Click Add Account.
6. Follow the login instructions in the popup.

Configure at least one platform account before continuing.

### Step 3: Set Daily Publishing Times

1. Open Settings.
2. Find Daily Publishing Times.
3. Click Add Time.
4. Enter times such as `11:00` and `17:00`.
5. Click Save.

### Step 4: Upload and Schedule a Video

1. Click Publishing Plans in the left navigation.
2. Click the plus button beside any time slot, or click New.
3. Upload a video file. Supported formats include MP4, MOV, AVI, and MKV.
4. Select target platforms.
5. Fill in platform content manually, or use AI auto-completion.
6. Click Confirm or Save.

The video is added to the selected publishing time slot.

### Step 5: Start the Scheduler

1. Click Dashboard in the left navigation.
2. Click Start Scheduler at the top.
3. When the scheduled time arrives, the app starts the publishing workflow automatically.

Your first video is now in the automatic publishing flow.

## Account and Credits

### Register an Account

1. Open Account & Credits.
2. Switch to Register mode.
3. Fill in the required information:
   - Email: used for login and notifications.
   - Verification code: request a code and enter it before it expires.
   - Password: at least 6 characters.
   - Invitation code: optional. If valid, both sides can receive a reward after the conditions are met.
4. Read and accept the user agreement after the reading timer is complete.
5. Click Register.

### Sign In

1. Enter your email and password.
2. Click Sign In.
3. After login, the page shows account information and credit balance.

### Account Information

After signing in, you can view:

- Email address of the current account.
- Registration date.
- Your invitation code.
- Credit balance.
- Refresh action for syncing the latest balance.

### Invitation Reward Rules

1. Share your invitation code with another user.
2. The invited user enters your code during registration.
3. The invited user completes a first recharge and consumes at least 10 credits.
4. Both accounts receive 10 credits.

Note: invitation rewards are not issued immediately during the first 72 hours after the first recharge.

## Platform Account Management

### Add a Platform Account

1. Open Settings -> Platform Configuration.
2. Find the target platform.
3. Make sure the platform switch is enabled.
4. Click Add Account or Re-login.
5. Follow the popup instructions.

Platform login methods differ.

#### Douyin and Kuaishou

The app opens a browser login page. Scan the QR code in the browser, complete login, then return to the app and confirm.

#### Bilibili

Open the Bilibili app, use the scan function, scan the QR code in the popup, and confirm.

#### WeChat Channels

Open WeChat, use Scan, scan the QR code in the popup, and confirm.

WeChat Channels sessions usually last about 24 hours, so daily re-login may be required.

#### TikTok

TikTok requires a network environment that can access TikTok. The app opens a browser. Sign in manually, then return to the app and confirm.

#### YouTube

First-time configuration requires Google OAuth credentials. Follow the configuration guide shown inside the app. After configuration, click Authorize and approve access in the browser.

YouTube OAuth authorization is usually long-term and does not require frequent re-login.

#### Weibo

The app opens a browser. Sign in to Weibo manually, then return to the app and confirm.

### Manage Multiple Accounts

Each platform can store multiple accounts, which is useful for matrix operation or separate content lines.

Open the platform card and click Manage. In the management dialog, you can:

- Add or edit an account note, such as `test account` or `backup account`.
- Set an account as active.
- Delete non-active accounts.
- Re-authenticate an existing account with a new cookie or session.
- Open the platform homepage with the saved login state.

Only one account per platform is active for publishing at a time.

### Verify Account Status

Platform sessions expire. Check account status before publishing.

| Status | Color | Meaning |
| --- | --- | --- |
| Normal | Green | Recently verified and available for publishing. |
| Invalid | Red | Cookie or session expired. Log in again. |
| Not checked | Gray | Not verified yet. Manual verification is recommended. |

Actions:

- Single verification: click Verify on a platform card.
- Batch verification: click Verify All to check all enabled platforms.

Recommended practice: verify all enabled platform accounts before a publishing session to avoid failed tasks caused by expired login state.

### Account Groups and One-Click Switching

Account groups are useful for multi-account matrix operation, vertical content lines, and A/B testing.

An account group binds accounts from multiple platforms into one group. When you activate the group, the app switches all included platforms to the corresponding accounts.

1. Open Settings -> Account Groups.
2. Click New Group.
3. Enter a group name and description.
4. Assign accounts for each platform in the group.
5. Click One-Click Switch to activate the group.

## Publishing Plans

Publishing Plans is the core scheduling page.

### Page Structure

The page uses a timeline layout and usually shows today plus upcoming days.

Each time slot can include:

- Publishing time, such as `11:00`.
- Video filename.
- Tags, with a limited number shown in the slot.
- Platform icons.
- Status: Pending, Completed, Failed, or Skipped.
- AI status: Not started, Queued, Analyzing, Completed, or Failed.
- Actions: AI Auto-Complete, Replace, Edit, Delete.

### Add a New Plan

Adding a plan uses a two-step wizard.

#### Step 1: Choose a Video

Options:

- Upload a new video by clicking the upload area or dragging a file into it.
- Select a video already in the queue.
- Search by filename when selecting from the queue.

After selection, the right side shows a video preview player. Confirm that it is the correct video before continuing.

#### Step 2: Publishing Settings

Configure:

- Publishing platforms. Multiple platforms can be selected.
- AI analysis options.
- Overseas platform text language.
- Title style.
- Custom title, description, and tags.
- Custom cover image.

You can fill the fields manually or let AI generate them first and then edit the result.

Click Save to place the plan into the selected time slot.

### Quick Video Assignment

If the queue already contains multiple videos, use quick assignment to fill empty slots.

| Button | Function |
| --- | --- |
| Assign Today | Assign queued videos to empty slots today. |
| Assign Three Days | Assign queued videos to empty slots over the next three days. |
| Assign Seven Days | Assign queued videos to empty slots over the next seven days. |

Automatic assignment follows the order of videos in the queue. Existing scheduled slots are not overwritten.

### Drag to Swap Videos

1. Hold the content area of a slot.
2. Drag it to another slot.
3. The two videos swap positions while the time slots stay unchanged.

Only Pending slots can be dragged and swapped.

### Edit an Existing Plan

Click Edit beside a slot to change:

- Publishing platforms.
- AI analysis language and title style.
- Title, description, and tags.
- Manual overrides for AI-generated content.
- Cover image.

### Open the Queue Folder

Click Queue Folder in the toolbar to open the local `queue/` folder in File Explorer.

You can also copy video files directly into `queue/`. The app automatically recognizes newly added videos.

### Title Workshop

Title Workshop generates 10 or more platform-style title candidates for each platform. Click a candidate to fill the title field.

Credit cost: 1 credit per use. Video duration does not affect the title workshop cost.

Workflow:

1. Open a plan in Publishing Plans.
2. Find the candidate-title button beside the title field.
3. Click it to generate platform-specific title candidates.
4. Click any candidate to fill the corresponding platform title.
5. Optionally use a custom prompt to adjust title style and direction.

### Cover Workshop

Cover Workshop is a separate cover regeneration panel in the plan editor.

Credit cost depends on selected platforms and horizontal or vertical cover variants. The minimum is 1 credit per use. The UI shows an estimated cost before the action.

Functions:

- Modify the video description used for cover generation.
- Upload a reference image to guide style.
- Generate horizontal and vertical cover variants for multiple platforms.
- Preview generated versions.
- Apply the selected cover version.
- See estimated credit cost before confirming.

### Fixed Description Schemes

Fixed description schemes automatically add opening and closing text to descriptions so you do not need to copy and paste the same text every time.

Configure them in Settings -> Description Schemes.

Supported behavior:

- Global schemes.
- Platform-specific schemes.
- Multiple schemes for different content types.
- Switching between schemes, such as brand promotion versus daily posting.
- Preview of the final combined description in the publishing effect area.
- Per-plan override of the global scheme.

## Dashboard

The Dashboard is the control center for monitoring publishing status and controlling the scheduler.

### Scheduler Control

- Start Scheduler: starts automatic scheduling. The app publishes videos at configured times.
- Stop Scheduler: pauses automatic scheduling. It does not interrupt a task that is already running.

After the scheduler starts, it keeps running. If the close-button behavior is set to minimize to tray, closing the window does not stop scheduling.

### Statistics Cards

The top of the dashboard shows today's publishing status.

| Statistic | Meaning |
| --- | --- |
| Today's plans | Total publishing tasks scheduled for today. |
| Published | Tasks successfully published today. |
| Pending | Tasks still waiting today. |
| Failed | Tasks that failed today. |

### Today's Publishing Plans

The left timeline shows today's plans.

Each item shows:

- Time.
- Video name.
- Platforms.
- Status.
- Platform-level result after completion.

Click Refresh to sync the latest status.

### Scheduler Logs

The right side shows real-time scheduler logs.

Each log line includes:

- Timestamp.
- Operation description.

Use Copy to copy logs to the clipboard when reporting a problem.

### Publish Now

Use manual publishing when you do not want to wait for a scheduled time.

1. Click Publish Now.
2. Choose a video from the queue.
3. Select target platforms. All platforms may be selected by default.
4. Click the publish button for the selected platform count.
5. Watch progress on the dashboard.

### AI Progress Display

During publishing, the top area can show AI analysis progress:

- Current progress percentage.
- Current processing step, such as generating cover `2/5`.

### Failed Task Handling

When publishing fails, the dashboard may show a red warning bar.

| Action | Function |
| --- | --- |
| Retry All | Retry all failed tasks. |
| Ignore All | Mark failures as handled and stop reminding. |
| Clear Failed List | Remove all failure records. |
| Single-task action | Retry, ignore, or delete a specific failed task. |

### Pending Confirmations

Before publishing, the app may ask for confirmation if copy or cover assets are missing.

| Option | Effect |
| --- | --- |
| Use automatic analysis | Run AI analysis before publishing. |
| Force publish | Publish immediately with the current content. |
| Ignore | Skip this plan. |

## AI Analysis

AI analysis is a core feature of Tutu Video Publisher. It helps generate content suited to each platform.

### What AI Can Generate

- Title: platform-adapted titles based on video content.
- Description: platform-style descriptions or intros.
- Tags: relevant keywords and tags.
- Cover images: multiple high-resolution cover candidates in different sizes.
- Title candidates: 10 or more title options per platform through Title Workshop.
- Regenerated covers: cover versions through Cover Workshop, with reference image support and variant previews.

### Three Ways to Trigger AI Analysis

#### Automatic After Upload

Enable automatic AI pre-analysis after upload in Settings.

After a video is uploaded into the queue, it enters the AI analysis queue automatically. This is useful for batch upload before scheduling.

#### Manual Trigger

In Publishing Plans, click AI Auto-Complete beside a slot. This runs analysis for that one plan.

#### Automatic Before Publishing

Enable automatic AI completion before publishing in Settings.

When a publish task is missing copy or cover content, the app triggers AI analysis first and continues publishing after analysis is complete.

### Language and Style Settings

You can configure these in Settings or while adding a plan.

| Setting | Options | Applies to |
| --- | --- | --- |
| Overseas platform cover language | English or Chinese | TikTok and YouTube |
| Title generation style | Mixed Chinese-English, Chinese only, or English only | TikTok and YouTube |

Use English-language settings for English-speaking audiences unless you intentionally publish bilingual content.

### Review and Edit AI Output

1. Find an analyzed plan in Publishing Plans.
2. Click Edit.
3. Review generated title, description, tags, and cover.
4. Modify any content you want.
5. Click Save.

AI output should be reviewed before public publishing. It may miss context, platform rules, product claims, or small visual details.

### Credit Cost for AI Analysis

AI analysis charges by video duration. Credits are deducted after successful analysis. Failed analysis does not consume credits.

| Video duration | Credits | Approximate cost at 0.6 CNY per credit |
| --- | --- | --- |
| 0 to 1 minute | 3 credits | About 1.8 CNY |
| 1 to 3 minutes | 4 credits | About 2.4 CNY |
| 3 to 10 minutes | 5 credits | About 3.0 CNY |
| 10 to 30 minutes | 6 credits | About 3.6 CNY |
| 30 to 55 minutes | 10 credits | About 6.0 CNY |
| Over 55 minutes | Not supported | Not supported |

Large credit packages have a lower unit cost, so the actual cost can be lower.

Workshop credit rules:

- Title Workshop: 1 credit per use, independent of video duration.
- Cover Workshop: 1 to 4 credits per use depending on selected platforms and horizontal or vertical variants. The interface shows the estimate before confirmation.

## System Settings

### AI Automation Settings

Open Settings -> AI Automation.

| Switch | Meaning | Recommendation |
| --- | --- | --- |
| Automatic plan assignment | Assign uploaded videos to empty slots automatically. | Enable |
| Automatic AI pre-analysis after upload | Start AI analysis after a video is uploaded. | Enable |
| Automatic AI completion before publishing | Fill missing copy or cover before publishing. | Enable |
| Scheduler auto-restore | Restore scheduler state after app restart. | As needed |

AI analysis concurrency limit: up to 3 videos can be analyzed in parallel. If the queue is longer, the app may show an estimated waiting time. The same video can be forced to analyze again.

### Daily Publishing Times

Daily publishing times define when the scheduler should publish.

1. Click Add Time.
2. Enter a time, such as `11:00`.
3. Click an existing time to edit it.
4. Hover and click the delete icon to remove a time.
5. Click Save for changes to take effect.

Recommendations:

- Configure 2 to 4 time slots.
- Leave at least 2 hours between slots.
- Choose active audience times, such as `11:00`, `17:00`, and `20:00`.

### Close Button Behavior

You can configure what happens when you click the window close button.

| Option | Effect |
| --- | --- |
| Close directly | Exit the app and stop all tasks. |
| Minimize to tray | Keep the app running in the background. Automatic publishing can continue. |

If you want scheduled publishing to continue after closing the window, choose minimize to tray.

### Platform Configuration

Each platform card can include:

- Enable switch: disabled platforms are not used for publishing.
- Active account: current account name and status.
- Verify: check login state.
- Re-login: scan or authorize again.
- Manage accounts: view, switch, delete, or re-authenticate accounts.
- Login guide: view platform-specific login instructions.

## FAQ

### Publishing failed. What should I do?

Open the Dashboard and read the failure reason in the red prompt.

Common causes:

- Account invalid: re-login to that platform in Settings.
- Not enough credits: recharge credits in Account & Credits.
- Network problem: check network access and retry.
- Platform restriction: read the platform error message and wait before retrying if needed.

### How long does platform login stay valid?

Typical validity:

- Douyin, Kuaishou, TikTok, and Weibo: about 5 days.
- Bilibili: usually longer than one week.
- WeChat Channels: about 24 hours.
- YouTube: OAuth is long-term and usually does not need frequent reauthorization.

### How long does AI analysis take?

It depends on video duration and server load. It usually takes about 30 seconds to 5 minutes. Watch the AI progress bar on the dashboard for live progress.

### Will automatic publishing continue after I close the app window?

It depends on close-button behavior.

- Minimize to tray: the app keeps running in the background and automatic publishing continues.
- Close directly: the app exits and automatic publishing stops.

Use minimize to tray if you want scheduled publishing to continue.

### What video formats are supported?

The app supports common formats such as MP4, MOV, AVI, and MKV. If a non-MP4 file is uploaded, the app can convert it to MP4. Conversion progress appears in the queue.

### Where are uploaded videos stored?

Uploaded videos are stored in the `queue/` folder under the application directory. Successfully published videos are archived under `queue/published/`.

### Can one video be published to multiple platforms?

Yes. Select multiple platforms when adding or editing a plan. AI can generate different copy for different platforms.

### Why does WeChat Channels need daily re-login?

This is caused by WeChat Channels session validity. The cookie usually lasts about 24 hours and cannot currently be bypassed. If you publish to WeChat Channels often, verify and re-login before publishing each day.

### What if I do not have enough credits?

Open Account & Credits, click recharge, select a package, and pay through the supported payment method. Recharge is usually reflected quickly.

### The scheduler is running but did not publish at the configured time.

Check:

1. Dashboard shows the scheduler is running.
2. A video is scheduled for that time in Publishing Plans.
3. The plan status is Pending, not Completed or Failed.
4. The platform account is valid.
5. Scheduler logs show no blocking error.

## Credit Rules

### What Credits Are Used For

Credits are used for AI analysis services, including generating copy, tags, and cover images.

### How to Get Credits

| Source | Credits | Condition |
| --- | --- | --- |
| Registration gift | 10 credits | Automatically issued to new accounts. |
| First recharge gift | 20 credits | One-time gift after first recharge. |
| Invitation reward | 10 credits for each side | Issued after the invited user consumes 10 credits. |
| Recharge purchase | Depends on package | Paid through supported payment methods. |

### Recharge Packages

| Package | Price | Unit price | Saving |
| --- | --- | --- | --- |
| 20 credits | 12 CNY | 0.60 CNY per credit | None |
| 100 credits | 48 CNY | 0.48 CNY per credit | Save 20 percent |
| 200 credits | 84 CNY | 0.42 CNY per credit | Save 30 percent |
| 1000 credits | 360 CNY | 0.36 CNY per credit | Save 40 percent |

Batch recharge has a lower unit price and is more cost-effective for long-term use.

### Credit Records

In Account & Credits, you can view credit history.

Records include:

- Time.
- Transaction type.
- Credit change.
- Balance after change.
- Notes.

Credit records include Title Workshop and Cover Workshop consumption, so you can track workshop usage separately.

### Credit Notes

- Credits do not expire after recharge.
- Failed AI analysis does not deduct credits.
- If recharge has a problem, contact support through the official website.

## API and Agent Integration

While the application is running, it starts a local HTTP service at:

```text
http://localhost:8899
```

The service exposes REST APIs that can be used by AI agents, automation scripts, or third-party programs. This makes it possible to control many app functions without manually operating the graphical interface.

### Function Coverage

The API can operate major app workflows, including:

- Video queue: upload videos, delete videos, and list queue items. Non-MP4 formats can be converted when supported by the app.
- AI analysis: trigger analysis, check credit requirements, poll status, and get title, description, tag, and cover results.
- Title Workshop and Cover Workshop: generate title candidates or regenerate covers, including cover version switching when supported.
- Publishing plans: view weekly or date-specific plans, create slots, edit slots, delete slots, and automatically assign queued videos.
- Scheduler: start or stop scheduler, publish immediately, publish a specified video to selected platforms, retry failures, and handle pending confirmations.
- Platform and account management: view platforms, enable or disable platforms, switch active accounts, and batch-verify cookies or sessions.
- Account groups: create, edit, delete, assign members, and switch account groups.
- Tag library, description templates, and description schemes: create, read, update, and delete records.
- Global settings: view and modify cover prompts, title language, automation switches, and other settings exposed by the app.
- Credits and recharge: query balance, view credit records, create supported recharge orders, and poll payment status.

### Authentication

Interfaces that require login use Bearer Token authentication.

1. Call `POST /api/auth/login` with `email` and `password`.
2. Read the returned token.
3. Include the token in later requests:

```text
Authorization: Bearer <token>
```

### Interactive API Docs

While the app is running, open:

```text
http://localhost:8899/docs
```

This opens interactive Swagger documentation. You can inspect endpoints, parameters, response formats, and test requests from the browser.

### API Notes

- Platform account login that requires QR-code scanning must still be completed through the GUI.
- After platform login succeeds, the saved session can be used by API-controlled publishing.
- Publishing, AI analysis, and Cover Workshop operations are asynchronous. The API may return immediately; poll status endpoints to confirm completion.
- `http://localhost:8899` is only available while the app is running. If the app exits, the local API is unavailable.

## Contact and Feedback

Official website: https://zhaotutu.xyz

Inside the app, use Suggestions and Feedback in Settings to submit usage feedback. Contact information is optional there.

Public contact information from the original Chinese guide:

- QQ: 331506796
- WeChat: tujiang0411

Thank you for using Tutu Video Publisher. We hope your publishing workflow goes smoothly.
