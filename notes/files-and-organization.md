# Files & Folders

Keep your project easy to read:

```text
project/
├── README.md
├── global-event.md
├── ai-event.md
├── images/
└── notes/
    └── process.md
```

Use simple names: `ai-news-hero.png`, not `finalfinal2.png`.

```bash
pwd            # Where am I?
ls -lah        # What is here?
cd images      # Go into a folder
cd ..          # Go up one folder
mkdir images   # Make a folder
touch draft.md # Make a file
cp old new     # Copy a file
mv old new     # Move or rename a file
ls -R          # List files in subfolders
```

Before renaming a file, search for its old name with `rg "old-name" .`. Then update any links that use it. Broken image? Check the filename and path first.
