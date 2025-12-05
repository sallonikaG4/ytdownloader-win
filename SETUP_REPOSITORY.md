# Setup Windows Repository on GitHub

## Step 1: Create the Repository on GitHub

1. Go to: https://github.com/new
2. **Repository name**: `ytdownloader-windows`
3. **Description**: `A simple YouTube downloader that works locally on Windows. No ads, no popups, no subscriptions.`
4. **Visibility**: Public (or Private if you prefer)
5. **DO NOT** initialize with README, .gitignore, or license (we already have these)
6. Click **"Create repository"**

## Step 2: Push the Code

After creating the repository, run these commands:

```bash
cd WINDOWS
git remote add origin https://github.com/sallonikaG4/ytdownloader-windows.git
git branch -M main
git push -u origin main
```

Or if the remote already exists:
```bash
cd WINDOWS
git push -u origin main
```

## Step 3: Verify

1. Go to: https://github.com/sallonikaG4/ytdownloader-windows
2. You should see all the files
3. Check the Actions tab - the build should start automatically

## Step 4: Wait for Build

The GitHub Actions workflow will:
1. Build the Windows application
2. Create the installer
3. Upload artifacts

Once complete, follow `CREATE_RELEASE.md` to create a release!

