# Terminal & Git

Use the terminal from inside your project folder.

```bash
git status                    # See changes
git add .                     # Stage reviewed changes
git commit -m "Explain change" # Save a version
git push origin main          # Send it to GitHub
git log --oneline -3          # See recent commits
```

Need to switch tasks but keep an unfinished change?

```bash
git stash push -m "WIP change"
git stash list
git stash pop
```

`stash` temporarily puts away uncommitted work. `pop` brings it back.

Always run `git status` before you add, commit, stash, or push. Do not use delete commands unless you know exactly what they remove.
