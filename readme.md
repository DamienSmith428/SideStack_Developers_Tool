SideStack Developer Release Tool


The SideStack Developer Release Tool is a desktop app for developers who want to publish their Android apps to the SideStack app store. It handles everything — generating your store page, creating GitHub repos, uploading APKs, and pushing releases — from one UI.


What's Included in the ZIP

The release ZIP contains two tools you'll need:


SideStackTool.exe — the main release tool (this app)
[Second Tool Name] — required companion tool, also included


Both must be present and set up before you start.


Requirements


A GitHub account
Git installed on your machine
Your APK file(s) ready to upload



First-Time Setup (Settings Tab)

Open the app and go to the Settings tab. Fill in the following:

GitHub Personal Access Token

Generate a token from your own GitHub account at:
Settings → Developer Settings → Personal Access Tokens → Tokens (classic)

Required permissions: repo, write:packages


Privacy note: This tool communicates exclusively with GitHub's API. No data is sent to SideStack servers or any third party. Your token is stored locally on your machine only.



GitHub Username

Enter your GitHub username. This is the account your repos and releases will be created under.

Issue Assignee

Enter your GitHub username here as well. This field sets who gets assigned to bug reports opened on your app's repo. In most cases this will be the same as your username.

SideStack Web Repo Name

Leave this as-is. Do not change the default value. This points to the correct SideStack store repo and changing it will break your store listing.

Store Config URL

Leave this as-is. This URL is pre-configured to point to the SideStack store config. It does not need to be changed.

Output Directory

This is a local folder on your PC where a copy of your generated app page files will be saved. It's just for your own reference — the real work happens on GitHub. The tool will automatically create the repo on your GitHub account and push everything there. The local output is just a convenience copy.


Creating a New App (New App Tab)

Fill in your app's details — name, repo info, APK architectures, SDK versions, description, and so on. The tool will:


Generate your app's store page
Create the necessary GitHub repository under your account
Push all the page files
Upload your APK(s) as a GitHub release
Register your app with the SideStack store


⚠️ The Red Box at the Bottom

At the bottom of the New App form there is a large red section.

Do not check the option inside it unless you have been explicitly told to by the SideStack team.

This option is reserved for developers who have been issued an Authorized Official SideStack Dev Release Token — a separate special-purpose token issued directly by SideStack for internal and verified publisher use. It is not your standard GitHub token.

If you're a developer publishing your own app to the store, you will not need this. You would already know if this applies to you. Leave the red box unchecked and proceed normally.


Updating an Existing App (Update App Tab)

Use the Update App tab any time you're releasing a new version of an app already in the store. Select your app from the dropdown, enter the new version number, describe what changed, attach the new APK(s), and publish. This is completely separate from the New App flow.


Need Help?

Open an issue on this repo or reach out through the SideStack community.