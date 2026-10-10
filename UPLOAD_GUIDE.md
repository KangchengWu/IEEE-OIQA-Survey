# Uploading to GitHub

[← Back to the resource hub](README.md)

## Update an Existing Repository

1. Extract the archive and open the `OIQA-Resource-Hub-English` folder.
2. Open your GitHub repository and choose **Add file → Upload files**.
3. Upload the **contents** of this folder into the repository root: `README.md`, `assets/`, `docs/`, `data/`, `CONTRIBUTING.md`, and any preview pages you want to retain. Do not upload the enclosing folder itself, or GitHub will not use its README as the repository homepage.
4. Enter a commit message such as `Update OIQA resource hub in English`, review the uploaded files, and choose **Commit changes**.
5. Open the repository homepage and check the figures, dataset links, and method links.

Preserve the repository's existing source files and LICENSE. If you already have a local Git clone, copy these files into its root, review the diff, and commit and push the changes through your usual workflow.

## Files and Preview

| Path | Purpose |
| :--- | :--- |
| `README.md` | GitHub repository homepage |
| `assets/` | Cover, four survey figures, and attribution |
| `docs/` | Dataset access, method details, comparisons, and source records |
| `data/` | Machine-readable resource index and benchmark values |
| `CONTRIBUTING.md` | Contribution conventions |
| `preview.html` and supporting `.html` pages | Local English preview with light and dark themes |

All document and image links are relative to the repository. Keep the directory structure intact. The HTML preview approximates the reading layout; GitHub applies its own renderer and does not use the preview's CSS or JavaScript.

The raw manuscript PDF is not required for the repository homepage. Once a final publication URL and citation are available, add them to the README and update the citation entry.
