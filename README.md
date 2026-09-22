# Hosting Your Portfolio on GitHub Pages for Free

This guide will walk you through hosting your portfolio (which we've created in this folder) for free using GitHub Pages.

## Prerequisites
1. You need a free account on [GitHub](https://github.com/join).
2. You need to have `git` installed on your computer. If you don't have it, download it from [git-scm.com](https://git-scm.com/downloads) and install it.

## Step 1: Create a New Repository on GitHub
1. Log in to your GitHub account.
2. In the top-right corner of the page, click the `+` icon and select **New repository**.
3. **Repository name:** 
   - If you want the URL to be exactly `https://yourusername.github.io`, name the repository **`yourusername.github.io`** (replace `yourusername` with your actual GitHub username). 
   - Otherwise, you can name it something like `portfolio`.
4. Make sure it is set to **Public**.
5. Do *not* check any boxes to initialize with a README, .gitignore, or license (leave it completely empty).
6. Click **Create repository**.

## Step 2: Push Your Local Code to GitHub (Via Terminal)
On your computer, open **PowerShell** or **Command Prompt** (or Git Bash) and navigate to the folder where your portfolio is located.

```powershell
# Go to your portfolio folder
cd C:\Users\nites\Downloads\nitesh-portfolio

# Initialize Git
git init

# Add all files (index.html, profile.png, etc.)
git add .

# Save the files in your local history
git commit -m "Initial portfolio commit"

# Tell Git where your online repository is (Replace YOUR-USERNAME and YOUR-REPO-NAME below)
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git

# Set the main branch
git branch -M main

# Push the code to GitHub
git push -u origin main
```
*(Note: When you run `git push`, you might be asked to log in to GitHub in your browser).*

## Step 3: Enable GitHub Pages
1. Go back to your repository page on GitHub.com.
2. Click on the **Settings** tab (the gear icon near the top middle).
3. On the left sidebar, click on **Pages**.
4. Under **Build and deployment** -> **Source**, make sure "Deploy from a branch" is selected.
5. Under **Branch**, select `main` from the dropdown and click **Save**.

## Step 4: View Your Live Site!
Wait about 1 to 2 minutes. GitHub is currently processing your site behind the scenes. 
You can refresh the **Pages** settings screen, and eventually, a message will appear at the top saying:
> **"Your site is live at https://yourusername.github.io/..."**

Click the link, and your portfolio will be visible to the entire internet!

---
*If you ever want to update your portfolio (e.g., editing `index.html`), simply open your terminal in this folder again and type:*
```bash
git add .
git commit -m "Updated portfolio"
git push
```