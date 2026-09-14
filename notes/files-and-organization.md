# Files & Folders

**Where:** VS Code's terminal. Use zsh or bash on Mac, or Git Bash on Windows.

Open your cloned repository in VS Code. Use `current-events-practice` before Thursday and `current-events-exam` during the exam. Your finished project will look like this:

```text
current-events-exam/
├── README.md
├── global-event.md
├── ai-event.md
├── images/
│   ├── global-event.png
│   └── ai-event.png
└── notes/
    └── process.md
```

From the repository's top-level folder:

```bash
pwd
ls
mkdir -p images notes
touch global-event.md ai-event.md notes/process.md
ls -R
```

`pwd` shows your location; `ls` lists files; `mkdir` makes folders; `touch` creates empty files; `ls -R` includes subfolders.

**Check:** the new files appear in VS Code's Explorer. Add a title to each Markdown file and save before your setup commit. GitHub already created `README.md`. Git tracks files, so the empty `images/` folder will appear on GitHub after you add images.

`cd images` enters that folder; `cd ..` returns to the project. `cp SOURCE DESTINATION` copies a file; `mv SOURCE DESTINATION` moves or renames it. Replace those uppercase words with actual paths.

Keep filenames lowercase and consistent. If you move or rename a file, update the Markdown links that point to it.
