# Files & Folders

Keep your project easy to read:

```text
project/
├── README.md
├── index.html
├── styles.css
├── global-event.md
├── ai-event.md
├── images/
└── notes/
```

Use simple names: `ai-news-hero.png`, not `finalfinal2.png`.

```bash
pwd            # Where am I?
ls -lah        # What is here?
mkdir images   # Make a folder
touch draft.md # Make a file
cp old new     # Copy a file
mv old new     # Move or rename a file
rg --files     # List project files
```

Before renaming a file, search for its old name with `rg "old-name" .`. Then update any links that use it. Broken image? Check the filename and path first.
