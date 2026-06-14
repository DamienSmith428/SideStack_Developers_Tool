# SideStack Developer Release Tool

A desktop app for developers who want to publish their Android apps to the SideStack store. It handles everything — generating your store page, creating GitHub repos, uploading APKs, and pushing releases — all from one UI.

---

## Downloads

Download the latest version of each tool directly from the newest GitHub release.

<p align="center">
  <a href="https://github.com/DamienSmith428/SideStack_Developers_Tool/releases/latest/download/Side.Stack.Tool.exe">
    <img src="https://img.shields.io/badge/Download-SideStack%20Developer%20Tool-blue?style=for-the-badge" alt="Download SideStack Developer Tool">
  </a>
</p>

<p align="center">
  <a href="https://github.com/DamienSmith428/SideStack_Developers_Tool/releases/latest/download/SideStackSubmissionTool.exe">
    <img src="https://img.shields.io/badge/Download-App%20Submission%20Tool-green?style=for-the-badge" alt="Download App Submission Tool">
  </a>
</p>

---

## What's Included

The project includes two tools:

- **Side.Stack.Tool.exe** — the main developer release tool
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

> Settings → Developer Settings → Personal Access Tokens → Tokens (classic)

Required permissions: `repo`, `write:packages`

> Privacy note: This tool communicates exclusively with GitHub's API. No data is sent to SideStack servers or any third party. Your token is stored locally on your machine only.

### GitHub Username

Enter your GitHub username. This is the account your repos and releases will be created under.

### Issue Assignee

Enter your GitHub username here as well. This sets who gets assigned to bug reports opened on your app's repo.

### SideStack Web Repo Name

**Leave this as-is.** Do not change the default value.

### Store Config URL

**Leave this as-is.** This URL is only for authorized Developers who have a Authorized SideStack Token and are authorized to update our internal apps. Leave Blank and Ignore the Import From Store button in the My Apps tab. My apps tab will still populate with apps you create within the New App tab and allow you to update your apps. 

### Output Directory

A local folder on your PC where a copy of your generated app page files will be saved.

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

The Authorized Official SideStack Dev Release Token is separate from your GitHub Personal Access Token.

If you do not have this special token, leave the red box unchecked.

---

## Companion Submission Tool

The SideStack Submission Tool is used by developers who do not possess an Authorized Official SideStack Dev Release Token.

### Submission Process

1. Publish your app using the SideStack Developer Release Tool.
2. Copy your generated application URL. (or go to the repo for your new app then docs/config.json and click "raw" and copy the URL and   paste into the appropriate field in submission tool)
   (example URL: https://raw.githubusercontent.com/YOUR-GITHUB-USERNAME/YOUR-REPO/refs/heads/main/docs/config.json)
4. Open the SideStack Submission Tool.
5. Submit the application URL for review.
6. Upon approval, the application will automatically be added to the SideStack Android App Store.

---

## Updating an Existing App — Update App Tab

1. Select your app from the dropdown list.
2. Enter the new version number.
3. Add release notes describing changes.
4. Attach updated APK files.
5. Publish the update.

> Note: Updates to your app's dont require a submission for approval. The repo lives in your github account there for your apps page is your responsibility/under your ownership. Just use the tool to update and itll be auto pushed to the store with your apks and changelog notes. 

---

## Need Help?

Open an issue on this repository.
