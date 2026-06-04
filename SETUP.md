# Setup Instructions for Students

Follow these steps to get your research website up and running!

## Prerequisites

- A GitHub account (free at [github.com](https://github.com))
- Git installed on your computer ([git-scm.com](https://git-scm.com))
- (Optional) R and RStudio for local preview

## Step-by-Step Setup

### 1. Create Your Repository

**Option A: If your instructor gave you a template link**

1. Click the **"Use this template"** button
2. Click **"Create a new repository"**
3. Name your repository (e.g., `my-research-site` or `[YourName]-research-profile`)
4. Make it **Public** (so GitHub Pages can publish it)
5. Click **"Create repository"**

**Option B: If you're forking**

1. Click the **"Fork"** button
2. Click **"Create fork"**

### 2. Clone to Your Computer

1. On your new repository page, click the green **"Code"** button
2. Copy the HTTPS URL
3. Open Terminal (Mac/Linux) or Git Bash (Windows)
4. Run:
   ```bash
   git clone [paste the URL]
   cd [your-repo-name]
   ```

### 3. Edit Your Files

Open the repository folder in your text editor:

#### Edit `index.qmd`
- Replace "Your Name" with your actual name
- Update the "About Me" section
- Add your research interests
- Add your email

#### Edit `projects/final-report.qmd`
- Change the title to your actual project title
- Write your final report content
- Replace placeholder text with your actual work

#### (Optional) Edit `projects.qmd`
- Customize the description of your projects
- You can add more project links as you create them

#### (Optional) Edit `styles.css`
- Customize colors, fonts, etc. if you want

### 4. Preview Locally (Optional)

If you have R/RStudio installed:

```r
# In RStudio Console:
quarto::quarto_render()
```

Then open `docs/index.html` in your browser.

### 5. Push to GitHub

When you're happy with your changes:

```bash
git add .
git commit -m "Initial setup: Add my profile and final report"
git push
```

### 6. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top right)
3. Click **Pages** (left sidebar)
4. Under "Build and deployment":
   - Source: Select **Deploy from a branch**
   - Branch: Select **main**
   - Folder: Select **/docs**
5. Click **Save**

### 7. View Your Site

1. Wait 1-2 minutes for GitHub to deploy
2. Go back to **Settings** → **Pages**
3. You'll see a link like: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`
4. Click it to view your site!

## Updating Your Site

Every time you want to update your site:

1. Edit your `.qmd` files
2. Run:
   ```bash
   git add .
   git commit -m "Update: [describe your changes]"
   git push
   ```
3. Wait 1-2 minutes
4. Your site updates automatically!

## Checking the Build Status

If your site isn't updating:

1. Go to your repository on GitHub
2. Click the **Actions** tab
3. You'll see the build history
4. Click on the latest one to see if there were any errors

## Troubleshooting

### "Push rejected" error

Make sure you're in the correct folder:
```bash
cd [your-repo-name]  # Navigate to your repo
git push
```

### Site looks broken or plain

- Hard refresh: `Cmd+Shift+R` (Mac) or `Ctrl+Shift+R` (Windows/Linux)
- Check the Actions tab for build errors
- Make sure all `.qmd` files have proper formatting

### GitHub Pages not enabled

- Go to Settings → Pages
- Make sure branch is set to `main` and folder is `/docs`
- Site URL should be shown there

### File paths not working

Always use forward slashes `/` in links, even on Windows:
```
# Good:
[Link](projects/final-report.qmd)

# Bad:
[Link](projects\final-report.qmd)  # Windows backslash
```

## Adding More Pages

Want to add a poster, publication, or another project?

1. Create a new `.qmd` file in the `projects/` folder
2. Edit `projects.qmd` and add a link to it
3. Push and your site updates automatically!

## Resources

- [Quarto Documentation](https://quarto.org/)
- [GitHub Pages Help](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)
- [Git Basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)

---

**Need help?** Ask your instructor or check the resources above.
