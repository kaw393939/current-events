# Filesystem Commands & Project Organization

An organized project is easier to understand, edit, grade, and publish. Before writing code or content, decide where each kind of file belongs.

## A Useful Folder Plan

```text
current-events/
├── README.md              # Project overview and links
├── index.html             # Published homepage
├── styles.css             # Site design rules
├── global_events.md       # Global article draft
├── ai_events.md           # AI article draft
├── images/                # Images used by the project
├── notes/                 # Student documentation pages
└── .github/workflows/     # GitHub Pages publishing workflow
```

## Why Organization Matters

- **Predictability:** Anyone can guess where images, articles, and notes belong.
- **Fewer broken links:** A consistent `images/` folder makes image paths easier to write and check.
- **Cleaner commits:** Related files can be reviewed and saved together.
- **Easier publishing:** GitHub Pages needs a clear homepage and supporting files in the repository.

## Core Filesystem Commands

Run these inside the project folder.

```bash
pwd                         # Print the folder you are currently in
ls                          # List files and folders
ls -lah                     # List hidden files and useful details
cd images                   # Move into the images folder
cd ..                       # Move up one folder
mkdir notes                 # Create a new folder
touch draft.md              # Create an empty file
cp draft.md notes/draft.md  # Copy a file
mv draft.md notes/article.md # Move or rename a file
rg --files                  # List project files quickly
rg "Strait of Hormuz" .    # Find text anywhere in the project
```

## Before Moving or Renaming Files

1. Run `pwd` to confirm you are in the correct project.
2. Run `ls` to confirm the exact filename.
3. Use `rg "old-file-name" .` to find links that must be updated.
4. Move or rename the file with `mv`.
5. Update any Markdown or HTML links.
6. Run `git status` so you can see the change before committing it.

For example, if you rename an image, the image may disappear from the website until you update every `src="..."` or Markdown image path that used its old name.

## Naming Rules That Help

- Use lowercase letters and hyphens: `world-news-hero.png`, not `World News Hero FINAL.png`.
- Use descriptive names: `ai-news-hero.png` explains the file’s purpose.
- Avoid duplicate names like `image1.png` or `final-final.md`.
- Keep generated or downloaded assets in a dedicated folder such as `images/`.
- Keep notes in `notes/`, instead of mixing them with website assets.

## Be Careful with Destructive Commands

Commands such as `rm` remove files. Do not use recursive delete commands until you understand exactly which folder will be affected. In class, prefer moving an unwanted file to a temporary folder or ask for help before deleting it.
