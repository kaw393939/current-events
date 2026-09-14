# In-Class Build: Do the Whole Workflow

**Pass / fail. Use AI and Codex.** Repeat the workflow from class: clone, organize files, make Markdown with AI, commit, stash, and push.

> “Do. Or do not. There is no try.” — Yoda

## 1. Make Sure Your Setup Works

Open VS Code and make sure Codex is available. Open **Terminal → New Terminal**, then run:

```bash
git --version
ssh -T git@github.com
```

You should see Git working and a GitHub SSH success message. Never share your private key, password, or token.

## 2. Clone Your Repo

Use the **SSH** URL from GitHub:

```bash
git clone git@github.com:YOUR-USERNAME/current-events-practice.git
cd current-events-practice
git remote -v
git status
```

Replace the example with your own repository's SSH URL and folder name. Open the cloned folder with **File → Open Folder** in VS Code.

## 3. Make the Files

```bash
pwd
ls
mkdir -p images notes
touch README.md global-event.md ai-event.md notes/process.md
ls -R
```

Keep images in `images/`. Keep your AI prompts and quick notes in `notes/process.md`.

Add a title to your README and save it. Make your first commit:

```bash
git add .
git commit -m "Set up Markdown project"
```

## 4. Ask Codex to Help You Build

Create sample pages and assets:

- One Global Events Markdown page
- One AI Events Markdown page
- One image for each page
- A README that links to both Markdown pages

Each page needs a title, date, useful alt text, and a small Mermaid diagram. Keep the text short. The topic and words do not matter; the goal is to show that you can make and format the files.

In `notes/process.md`, save:

- One text-generation prompt
- One image prompt
- One revision prompt
- One short note about what Codex changed

Save your edits and open **Markdown: Open Preview to the Side** from the VS Code Command Palette. Check the formatting. Check Mermaid on GitHub after pushing.

## 5. Use Git Like We Did in Class

Save the new text, images, and links in your second commit:

```bash
git status
git add .
git commit -m "Add pages and visuals"
```

Add a temporary line to your README and save it without committing. Stash that change:

```bash
git stash push -m "WIP change"
git stash list
```

Check that the line disappeared. Bring it back:

```bash
git stash pop
```

Check that the line returned, then remove the temporary line and save. Push your commits:

```bash
git push origin main
git log --oneline -3
```

Open your repository on GitHub. Click the README links and check that the images and diagrams display.

## You Pass When You Can Show

- Codex in VS Code
- SSH working with GitHub
- Your cloned repository and organized files
- Two Markdown pages with images and Mermaid
- Your prompts in `notes/process.md`
- Two commits, a stash, and a push
- Your GitHub repository with working Markdown links and images

If something breaks, use Codex, your terminal, docs, and your classmates to fix it. Then show it working.
