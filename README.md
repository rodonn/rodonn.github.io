# Rob Donnelly's Website

This is the source code for my personal website built with [Quarto](https://quarto.org/).

## Building the Website

### Prerequisites

1. Install [Quarto](https://quarto.org/docs/get-started/)
2. If using R code in any `.qmd` files, install [R](https://www.r-project.org/)

### Development

To preview the website locally with live reloading:

```bash
quarto preview
```

This will start a local server and open the website in your default browser. Changes to source files will automatically trigger a rebuild and refresh.

### Building for Production

To build the website without previewing:

```bash
quarto render
```

This will generate the static website in the `docs/` directory, which can then be deployed to GitHub Pages or another hosting service.

## Project Structure

- `_quarto.yml`: Main configuration file for the website
- `*.qmd`: Quarto markdown files for various pages
- `images/`: Directory containing images used throughout the site
- `files/`: Directory containing downloadable files like PDFs
- `docs/`: Generated output directory (not checked into source control)
- `styles.css`: Custom CSS styling

## Deployment

The site is configured to build to the `docs/` directory for [GitHub Pages](https://pages.github.com/) hosting.

After building with `quarto render`, commit and push the changes to GitHub:

```bash
git add docs/
git commit -m "Update website build"
git push
```

GitHub Pages will automatically serve the content from the `docs/` directory.