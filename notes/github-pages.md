# Publishing with GitHub Pages

GitHub Pages turns files in a GitHub repository into a public website.

## What This Repository Uses

This project is a static site: `index.html` is the homepage and `styles.css` controls the design. The workflow at `.github/workflows/deploy-pages.yml` runs whenever changes are pushed to the `main` branch.

## Publish Steps

1. Push your project to GitHub.
2. Open the repository on GitHub.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **GitHub Actions** as the source.
5. Push a change to `main` or run the workflow from the **Actions** tab.
6. Wait for the deployment to finish, then open the Pages URL.

For this repository, the expected URL is:

```text
https://kaw393939.github.io/current-events/
```

## Before You Publish

- Click every internal link.
- Confirm every image has alt text.
- Check that external sources open to the intended original article.
- Make sure your name, class information, and any required attribution are correct.
- Review your Git history so your commits describe your work clearly.
