# In-Class Build: Do the Whole Workflow

**AI is allowed. Codex is required.** Your job is to repeat the workflow we used in class: clone, build, use Codex, save with Git, and publish.

> “Do. Or do not. There is no try.” — Yoda

## 1. Make Sure Your Setup Works

Open VS Code and make sure Codex is available. Then run:

```bash
git --version
ssh -T git@github.com
```

You should see Git working and a GitHub SSH success message. Never share your private key, password, or token.

## 2. Clone Your Repo

Use the **SSH** URL from GitHub:

```bash
git clone git@github.com:YOUR-USERNAME/current-events-mini-site.git
cd current-events-mini-site
git remote -v
git status
```

## 3. Make the Files

```bash
mkdir images notes
touch README.md index.html styles.css global-event.md ai-event.md notes/process.md
rg --files
```

Keep images in `images/`. Keep your AI prompts and quick notes in `notes/process.md`.

## 4. Ask Codex to Help You Build

Create sample pages and assets:

- One Global Events Markdown page
- One AI Events Markdown page
- One image for each page
- A homepage that links to both pages

Each page needs a title, date, useful alt text, and a small Mermaid diagram. Keep the text short. The topic and words do not matter; the goal is to show that you can make and format the files.

In `notes/process.md`, save:

- One text-generation prompt
- One image prompt
- One revision prompt
- One short note about what Codex changed

Use Codex, then make sure you can explain the files and steps.

## 5. Use Git Like We Did in Class

Make two real commits:

```bash
git status
git add .
git commit -m "Set up mini site"

git add .
git commit -m "Add pages and visuals"
```

Show that you can stash unfinished work:

```bash
git stash push -m "WIP change"
git stash list
git stash pop
```

Push your work:

```bash
git push origin main
git log --oneline -3
```

## 6. Publish

Turn on GitHub Pages with **GitHub Actions**, then add the live site link to your README.

## You Pass When You Can Show

- Codex in VS Code
- SSH working with GitHub
- Your cloned repository and organized files
- Two Markdown pages with images and Mermaid
- Your prompts in `notes/process.md`
- Two commits, a stash, and a push
- A live GitHub Pages link

If something breaks, use Codex, your terminal, docs, and your classmates to fix it. Then show it working.
