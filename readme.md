# SideStack Developer Release Tool

A desktop app for developers who want to publish their Android apps to the SideStack store. It handles everything — generating your store page, creating GitHub repos, uploading APKs, and pushing releases — all from one UI.

---

## Downloads

Download the latest version of each tool directly from the newest GitHub release.

<p align="center">

<a href="https://github.com/DamienSmith428/SideStack_Developers_Tool/releases/latest/download/Side.Stack.Tool.exe">
    <img src="https://img.shields.io/badge/Download-SideStack%20Developer%20Tool-blue?style=for-the-badge" alt="Download SideStack Developer Tool">
</a>

&nbsp;&nbsp;&nbsp;

<a href="https://github.com/DamienSmith428/SideStack_Developers_Tool/releases/latest/download/SideStackSubmissionTool.exe">
    <img src="https://img.shields.io/badge/Download-App%20Submission%20Tool-green?style=for-the-badge" alt="Download App Submission Tool">
</a>

</p>

> Replace `YOUR_USERNAME` and `YOUR_REPO` with your GitHub repository information.

---

## What's Included

The project includes two tools:

- **SideStackTool.exe** — the main developer release tool
- **SideStackSubmissionTool.exe** — companion tool used to submit app URLs for store review and approval

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

Enter your GitHub username here as well. This sets who gets assigned to bug reports opened on your app's repo.

### SideStack Web Repo Name

**Leave this as-is.** Do not change the default value. This points to the correct SideStack store repo and changing it will break your store listing.

### Store Config URL

**Leave this as-is.** This URL is pre-configured to point to the SideStack store configuration and does not need to be changed.

### Output Directory

A local folder on your PC where a copy of your generated app page files will be saved. The tool automatically creates the repository on your GitHub account and pushes everything there. The local output is simply a convenience copy.

---

## Creating a New App — New App Tab

Fill in your app's details including name, repository information, APK architectures, SDK versions, description, and other metadata.

The tool will:

1. Generate your app's store page
2. Create the required GitHub repository
3. Push all page files to GitHub
4. Upload APK files as GitHub releases
5. Register the app with the SideStack store configuration

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

The SideStack Submission Tool is used by developers who do not possess an Authorized Official SideStack Dev Release Token.

This tool allows you to submit your application URL directly for review and approval.

### Submission Process

1. Publish your app using the SideStack Developer Release Tool.
2. Copy your generated application URL.
3. Open the SideStack Submission Tool.
4. Submit the application URL for review.
5. Upon approval, the application will automatically be added to the SideStack Android App Store.

Developers without an Authorized Official SideStack Dev Release Token must use this submission process before their app becomes publicly visible in the store.

---

## Updating an Existing App — Update App Tab

Use the **Update App** tab whenever releasing a new version of an existing application.

1. Select your app from the dropdown list.
2. Enter the new version number.
3. Add release notes describing changes.
4. Attach updated APK files.
5. Publish the update.

This workflow is separate from creating a new app.

---

## Initial Release

**Release Title**

SideStack Developer Release Tool v1.0.0 — Initial Public Release

**Tag**

v1.0.0

---

## Need Help?

Open an issue on this repository or reach out through the SideStack community.
