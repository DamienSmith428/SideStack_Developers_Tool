# SideStack Developer Release Tool

A desktop app for developers who want to publish their Android apps to the SideStack store. It handles everything — generating your store page, creating GitHub repos, uploading APKs, and pushing releases — all from one UI.

---

## What's Included in the ZIP

The release ZIP contains two tools:

- **SideStackTool.exe** — the main release tool (this app)
- **SideStack App Submission Tool** — required companion tool for submitting app URLs for store review and approval

Both must be present and set up before you start.

---

## Requirements

- A GitHub account
- Git installed on your machine
- Your APK file(s) ready to upload

---

## First-Time Setup — Settings Tab

Open the app and go to the **Settings** tab. Fill in the following fields:

### GitHub Personal Access Token

Generate a token from your own GitHub account at:

> **Settings → Developer Settings → Personal Access Tokens → Tokens (classic)**

Required permissions: `repo`, `write:packages`

> **Privacy note:** This tool communicates exclusively with GitHub's API. No data is sent to SideStack servers or any third party. Your token is stored locally on your machine only.

### GitHub Username

Enter your GitHub username. This is the account your repos and releases will be created under.

### Issue Assignee

Enter your GitHub username here as well. This sets who gets assigned to bug reports opened on your app's repo — in most cases this will be the same as your username.

### SideStack Web Repo Name

**Leave this as-is.** Do not change the default value. This points to the correct SideStack store repo and changing it will break your store listing.

### Store Config URL

**Leave this as-is.** This URL is pre-configured to point to the SideStack store config and does not need to be changed.

### Output Directory

A local folder on your PC where a copy of your generated app page files will be saved. This is for your own reference only — the real work happens on GitHub. The tool automatically creates the repo on your GitHub account and pushes everything there. The local output is just a convenience copy.

---

## Creating a New App — New App Tab

Fill in your app's details: name, repo info, APK architectures, SDK versions, description, and so on. The tool will:

1. Generate your app's store page
2. Create the necessary GitHub repository under your account
3. Push all page files to that repo
4. Upload your APK(s) as a GitHub release
5. Register your app with the SideStack store configuration

---

## App Submission & Store Approval Process

### ⚠️ The Red Box at the Bottom

At the bottom of the New App form there is a large red section with a release authorization checkbox.

**Checking this box does NOT automatically publish your app to the SideStack Android App Store.**

Your app will only be automatically added to the store if BOTH of the following conditions are met:

1. You have been issued a valid **Authorized Official SideStack Dev Release Token**
2. You have checked the red authorization box during app creation

The Authorized Official SideStack Dev Release Token is a special token issued directly by SideStack and is completely separate from your GitHub Personal Access Token.

If you do not have this special token, leave the red box unchecked. Your app will not be automatically listed in the store, even if all other publishing steps complete successfully.

Only verified developers and authorized publishers who have received this token from SideStack can use the automatic release system.

---

## Companion Submission Tool

The ZIP package also includes a second tool used for app store submission requests.

This companion tool allows developers to submit their application URL directly to the SideStack review system for manual approval.

The submission process is simple:

1. Publish your app using the main release tool.
2. Copy your generated application URL.
3. Open the included submission tool.
4. Submit your application URL for review.
5. Once approved, your application will be automatically added to the SideStack Android App Store.

Developers who do not possess an Authorized Official SideStack Dev Release Token should use this submission tool to request inclusion in the store.

Automatic store listing through the red authorization box is reserved exclusively for authorized token holders. All other developers must submit their app URL through the companion submission tool and wait for approval before their listing becomes publicly visible in the store.

---

## Updating an Existing App — Update App Tab

Use the **Update App** tab any time you're releasing a new version of an app already in the store. Select your app from the dropdown, enter the new version number, describe what changed, attach the new APK(s), and publish. This flow is completely separate from the New App tab.

---

## Need Help?

Open an issue on this repo or reach out through the SideStack community.
