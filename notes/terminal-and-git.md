# Terminal & Git

Type these in the **VS Code terminal**, inside your cloned project. Use zsh/bash on Mac or Git Bash on Windows. Run one command at a time.

**Save** writes your file. **Add** stages changes for the next commit. **Commit** records a local version. **Push** sends commits to GitHub.

```bash
pwd                           # Check your current folder
git status                    # Check changed and staged files
git remote -v                 # Check your GitHub SSH address
```

For the initial file setup, run from the project folder:

```bash
git add *
git status
git commit -m "Set up project files"
```

For later commits, name the files belonging to that change:

```bash
git add README.md global-event.md ai-event.md notes/process.md
git commit -m "Add Markdown content and links"
```

After the image commit, push and inspect the history:

```bash
git push origin main
git log --oneline -4
```

Use your branch name from `git status` if it differs from `main`.

**Stash** puts aside an unfinished edit. Add a temporary line to README.md and save, then:

```bash
git stash push -m "Practice README change"
git stash list
```

The line disappears. `git stash pop` restores it and removes that stash. On the exam, show both actions live. Remove the temporary line afterward and save.

Stuck? Give Codex the command and its output. Ask for one next step, then check the result.

[Back to the practice guide](../assignment.md)
