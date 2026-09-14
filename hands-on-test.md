# Thursday: Hands-On Exam

Recreate the class workflow in your own new repository. **Individual demonstration. Pass / fail. Use AI, Codex, and these notes.**

> “Do. Or do not. There is no try.” — Yoda

Need the commands? Follow the [practice guide](assignment.md), using `current-events-exam` as your repository and folder name.

## 1. Create, authenticate, and clone

- On GitHub, create `current-events-exam` in your account with **Add README** enabled.
- In the VS Code terminal, verify Git and run `ssh -T git@github.com`.
- Clone your new repository with its **SSH** address and open the cloned folder in VS Code.

## 2. Make three purposeful commits

Complete and commit each stage before starting the next. GitHub's initial README commit is already there.

| Commit message | What to do before committing |
| --- | --- |
| `Set up project files` | Use file commands to make `images/`, `notes/`, `global-event.md`, `ai-event.md`, and `notes/process.md`. Add titles to the new Markdown files. Stage from the project folder with `git add *`. |
| `Add Markdown content and links` | Use Codex for both pages and one revision. Include a title, date, short text, a list, a small Mermaid diagram, and links between the README and pages. Save your prompts in `notes/process.md`. Stage the changed Markdown files by name. |
| `Add images to Markdown pages` | Generate two images with AI, save them in `images/`, and display them in the matching pages with alt text. Save the image prompt. Stage the images and changed Markdown files by name. |

Use `git status` to check each stage. Preview your Markdown in VS Code.

## 3. Push and check GitHub

Push your commits. Check that your README links, images, and diagrams work on GitHub.

## 4. Show the instructor

Have your project open in VS Code with Codex available, and your repository open on GitHub. Run:

```bash
ssh -T git@github.com
git remote -v
git log --oneline -4
git status
```

Show your SSH username, SSH remote, three local commits plus GitHub's initial commit, and a clean working tree. Open your Markdown pages and organized files.

**Demonstrate stash live:** Add a temporary README line and save. Run `git stash push -m "Exam README change"` and `git stash list`. Show the line disappearing, then run `git stash pop` and show it returning. Remove the temporary line, save, and run `git status` again.

You're done when you've shown the complete workflow working.
