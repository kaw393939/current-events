# Prompting with Codex

**Where:** Codex chat in VS Code, with your cloned repository open. AI is allowed throughout the exercise.

After the setup commit, try:

```text
Edit global-event.md and ai-event.md. Give each a title,
date, two short sentences, a list, and a three-box Mermaid diagram.
Add relative links to both pages in README.md and a link
back to README.md on each page. Leave images for the next
stage. I will run the Git commands myself.
```

Ask for one revision, such as “Make both pages shorter.” Save both prompts in `notes/process.md`, preview your files, and commit this stage before adding images.

**Image stage:** use an available AI image tool. Try this for the global image, then request an AI-themed version:

```text
Create a small, wide illustration of a globe for a news
page. Use simple shapes and bright colors. No text.
```

Save actual PNG files as `images/global-event.png` and `images/ai-event.png`; changing another format's extension does not convert it. Then ask Codex:

```text
Add each PNG to its matching Markdown page with
descriptive alt text and a relative image path.
```

Add your image prompt to `notes/process.md` before the image commit.

**Stuck?** Paste the command and its output into Codex: “Explain what happened and give me the next step.”
