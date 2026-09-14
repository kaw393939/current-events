# Practice Before Thursday

Work through this once before the [hands-on exam](hands-on-test.md). Use AI and Codex throughout. Run terminal commands one line at a time.

## 1. Create your repository

**GitHub in your browser:** Open [New repository](https://github.com/new). Use your own account, name it `current-events-practice`, and turn on **Add README**. Leave the other initialization options alone, then create it.

**You should see:** Your repository with `README.md` and GitHub's initial commit. You'll add three commits of your own.

## 2. Check your tools and SSH

**VS Code:** Open Codex and send a short message to check that it responds. Use **File → Open Folder** to open your Documents folder, then **Terminal → New Terminal**.

Use **zsh/bash on Mac** or **Git Bash on Windows**. On Windows, select Git Bash from the terminal's new-terminal dropdown.

**VS Code terminal:**

```bash
git --version
ssh -T git@github.com
```

**You should see:** A Git version, then this message with your username:

```text
Hi USERNAME! You've successfully authenticated, but GitHub does not provide shell access.
```

That entire message means SSH worked. If you get a first-connection prompt or an SSH error, use [GitHub's SSH check instructions](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection).

## 3. Clone and open your project

**GitHub:** Open your new repository. Choose **Code → SSH** and copy its address.

**VS Code terminal:** Create a class folder inside Documents. Replace `YOUR-USERNAME` below with your GitHub username, or paste your copied SSH address after `git clone`.

```bash
mkdir -p is117
cd is117
git clone git@github.com:YOUR-USERNAME/current-events-practice.git
cd current-events-practice
pwd
git remote -v
git status
```

**VS Code:** Use **File → Open Folder** to open `Documents/is117/current-events-practice`. Open a new terminal there.

**You should see:** `README.md` in Explorer, your project path from `pwd`, an `origin` address beginning with `git@github.com:`, and a clean working tree.

## 4. Commit 1: set up project files

**VS Code terminal — inside your project:**

```bash
mkdir -p images notes
touch global-event.md ai-event.md notes/process.md
ls -R
```

**VS Code editor:** Add a `#` title to each new Markdown file and save. Keep the existing README. Git tracks files; the empty `images/` folder will appear on GitHub once you add images.

**VS Code terminal:**

```bash
git status
git add *
git status
git commit -m "Set up project files"
```

**You should see:** The new files under “Changes to be committed” before the commit, then a commit message with a short ID.

Need help? [Files and folders](notes/files-and-organization.md) · [What Git commands do](notes/terminal-and-git.md)

## 5. Commit 2: add Markdown content and links

**Codex chat:** Paste this prompt:

```text
Edit global-event.md and ai-event.md. Give each a title, date,
two short sentences, a list, a link back to README.md, and a tiny
three-box Mermaid diagram. Update README.md to link to both files.
Keep the text simple. Leave image work for the next step.
I will run the Git commands myself.
```

Ask for one revision, such as “Make both pages shorter.” Save the text prompt and revision prompt in `notes/process.md`.

**VS Code editor:** Save all files. Open a Markdown file, press **Ctrl+Shift+P** on Windows or **Cmd+Shift+P** on Mac, and select **Markdown: Open Preview to the Side**.

**You should see:** Formatted headings, text, and links. Check Mermaid on GitHub after pushing. [Tiny Markdown example](notes/markdown-and-mermaid.md)

**VS Code terminal:**

```bash
git status
git add README.md global-event.md ai-event.md notes/process.md
git commit -m "Add Markdown content and links"
```

## 6. Commit 3: add images

**AI image tool:** Generate one image for each page. Save the PNG files inside your project's `images/` folder as `global-event.png` and `ai-event.png`.

**Codex chat:** Ask it to add each image to its matching Markdown page using those paths and descriptive alt text. Save your image prompt in `notes/process.md`.

**You should see:** Both images in Explorer and in the Markdown preview. [Image prompt and file paths](notes/prompting-with-codex.md)

**VS Code terminal:**

```bash
git status
git add images/ global-event.md ai-event.md notes/process.md
git commit -m "Add images to Markdown pages"
```

## 7. Practice stash

**VS Code editor:** Add a temporary line `STASH PRACTICE` to README.md and save without committing.

**VS Code terminal:**

```bash
git status
git stash push -m "Practice README change"
git stash list
```

**You should see:** The line disappears from README.md and a stash appears in the list. Restore it:

```bash
git stash pop
```

The line returns. Remove just that temporary line and save. Run `git status`; your working tree should be clean. On Thursday, repeat this demonstration while the instructor watches.

## 8. Push and check

**VS Code terminal:** These commands assume your branch is `main`; use the branch name shown by `git status` if different.

```bash
git push origin main
git log --oneline -4
git status
```

**GitHub:** Refresh your repository. Open its commit history and click your README links.

**You should see:** Three purposeful commits plus the initial README commit, working links, images, and Mermaid diagrams. Your local working tree should be clean and up to date.

Stuck? Paste the command and error into Codex: “Explain what happened and give me the next step.”

[Ready for Thursday? See the exam →](hands-on-test.md)
