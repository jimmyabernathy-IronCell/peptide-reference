# Peptide Reference (private)

One-file site: open `index.html` in a browser. Full setup guide: Peptide-Reference-GitHub-Setup-Guide.pdf.

# Part 1: Put the site in a private GitHub repository

1. Unzip **peptide-reference-github.zip** on your computer. You'll get a folder with the three files.
2. Go to **github.com** and sign in (or click **Sign up** to make a free account).
3. Click the **+** at the top right, then **New repository**.
4. Fill in:
   - **Repository name:** `peptide-reference`
   - **Visibility:** **Private**
   - Leave **Add a README file** unticked.
5. Click **Create repository**.
6. On the empty repository page, click the link **uploading an existing file**.
7. Drag `index.html`, `robots.txt` and `README.md` from the unzipped folder into the box. Drag the files themselves, not the folder.
8. Scroll down and click **Commit changes**.

You'll see the three files listed. This is your master copy. GitHub keeps every version you upload.

# Part 2, Option A: Run it on your computer

1. In your repository, click **index.html**.
2. Click the **Download raw file** button (the downward arrow at the top right of the file view).
3. Save it somewhere you'll find it, such as **Documents**.
4. Double-click the file. It opens in your web browser.
5. Bookmark the page (**Ctrl+D** on Windows, **Cmd+D** on Mac) so you can reopen it in one click.

The calculator works offline. The reconstitution video link needs internet. Open it in Chrome, Safari or Edge; file-preview windows may not run the calculator.

# Part 2, Option B: Publish it with GitHub Pages

**Step 1: Make the repository public (free plan only).** Skip this if you pay for GitHub Pro.

1. In the repository, click **Settings** (top menu, gear icon).
2. Stay on **General** and scroll to the bottom section, **Danger Zone**.
3. Click **Change visibility**, choose **Make public** and confirm.

**Step 2: Turn on Pages.**

1. In **Settings**, click **Pages** in the left sidebar (under *Code and automation*).
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Under **Branch**, pick **main** and the folder **/ (root)**, then click **Save**.
4. Wait a minute or two and refresh the page. A box appears: *"Your site is live at https://YOUR-USERNAME.github.io/peptide-reference/"*. Click **Visit site**.

**Step 3: Put it on your phone.**

- **iPhone:** open the site in Safari, tap **Share**, then **Add to Home Screen**.
- **Android:** open it in Chrome, tap the **⋮** menu, then **Add to Home screen**.

**To take the site down later:** set the repository back to **Private** (Settings → General → Danger Zone → Change visibility). On the free plan that turns the site off.

# Part 3: Updating the site

**When I send you a new version of `index.html`:**

1. Open your repository on github.com.
2. Click **Add file → Upload files**.
3. Drag in the new `index.html`. It replaces the old one.
4. Click **Commit changes**.
5. Option B updates itself in a minute or two. For Option A, download the file again (Part 2, Option A).

**To fix a small typo yourself:** click **index.html**, click the **pencil icon** (Edit), make the change, then click **Commit changes**.

**To see or restore an older version:** click **index.html**, then **History**. Click any version to view it; use **⋯ → View file** and **Download raw file** to get it back.

# Optional: using Git on the command line

Only if you're comfortable with a terminal and have Git installed.

```
git clone https://github.com/YOUR-USERNAME/peptide-reference.git
cd peptide-reference
```

Copy the new `index.html` into that folder, then:

```
git add index.html
git commit -m "Update peptide reference"
git push
```

To preview it the way Pages serves it, run this inside the folder and open http://localhost:8000:

```
python3 -m http.server 8000
```

# Troubleshooting

| Problem | Fix |
|---|---|
| "404 There isn't a GitHub Pages site here" | Wait 2 to 5 minutes after turning Pages on. Check that `index.html` sits at the top of the repository, not inside a folder, and is spelled exactly `index.html`. |
| No **Pages** option, or Pages says to upgrade | On the free plan the repository has to be public (Option B, Step 1). |
| Calculator doesn't respond | Open the file in Chrome, Safari or Edge, not a preview window or email attachment viewer. |
| Upload box won't take a folder | Open the folder and drag the files inside it instead. |
| Changes not showing on the website | Wait two minutes, then reload. On a phone, close the tab and reopen it. |
