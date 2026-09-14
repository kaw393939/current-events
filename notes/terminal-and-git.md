# Terminal, Filesystem & Git

The terminal lets you work with files using text commands. Run commands from the project folder, and read each command before you press Enter.

## Safe Filesystem Commands

```bash
pwd                 # Show the current folder
ls                  # List files and folders
ls -lh images       # List image files with sizes
mkdir notes         # Create a folder
cp source.png images/hero.png  # Copy a file
rg "source" .       # Search project files for text
```

Use `rg` (ripgrep) to find text quickly. Be careful with commands that remove or overwrite files. Do not use a recursive delete command unless you understand exactly what it targets.

## Git Commands Used in This Type of Project

```bash
git status           # See changed and untracked files
git add README.md index.html styles.css
git add .            # Stage all intended changes after reviewing git status
git commit -m "Build student guide and GitHub Pages site"
git push origin main # Send the commit to GitHub
```

## A Good Git Habit

Use this loop:

1. Make a small set of related changes.
2. Run `git status`.
3. Read what you are about to stage.
4. Commit with a message that explains the change.
5. Push only when the project is ready to share.

This guide documents commands commonly used to build this project. It does not reproduce private shell history, which may contain unrelated or sensitive information.
