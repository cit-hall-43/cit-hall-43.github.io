# Copilot Instructions for Taipei Church Hall 43 Website

This repository is a Jekyll-based static site for Taipei Church Hall 43, hosted on GitHub Pages. AI coding agents should follow these guidelines to be productive:

## Architecture Overview
- **Jekyll Structure:** Content is organized using Jekyll conventions: `_layouts/`, `_includes/`, `_pages/`, `_sass/`, and `assets/`.
- **Content Organization:**
  - Sermon notes, presentations, and study guides are in `_pages/主日資料/` and subfolders by year.
  - Hymn lyrics and collections are in `_pages/詩歌/` and `assets/docs/` (PDFs).
  - Study guides and special topics are in `_pages/導讀卡/` and `_pages/從羅馬書看神完全的救恩/`.
- **Styling:** SCSS files are in `_sass/` and `assets/css/`. Use Jekyll's built-in SASS pipeline.
- **Assets:** Images, fonts, PDFs, and JS are in `assets/`.

## Developer Workflows
- **Local Development:**
  1. Install Ruby and Jekyll.
  2. Run `bundle install` to install dependencies.
  3. Start the server with `bundle exec jekyll serve` (site at `http://localhost:4000`).
- **No Automated Tests:** This repo does not use automated tests or CI/CD pipelines.
- **Deployment:** Pushed changes to `main` are automatically published via GitHub Pages.
- **Git Commit Messages**: All commit messages must follow the Conventional Commits format (see https://www.conventionalcommits.org/).

## Project-Specific Conventions
- **Language:** Content is primarily in Traditional Chinese; filenames and folder names may use Chinese characters.
- **File Naming:** Weekly sermon files use the format `YYYYMMDD主日*.md` for easy chronological sorting.
- **Navigation:** `_includes/navigation.html` and `_includes/sidebar.html` control site navigation; update these for new sections.
- **PDFs:** Sermon slides and study guides are uploaded to `assets/docs/` and linked from markdown pages.
- **Custom Layouts:** Use `_layouts/default.html` for most pages; `_layouts/page.html` for special layouts.

## Integration Points
- **External Libraries:**
  - Uses `mermaid.js` for diagrams (`_includes/mermaid.html`).
  - Uses `highlight.js` for code syntax highlighting (`assets/js/highlight.min.js`).
- **Fonts:** Custom fonts are loaded from `assets/fonts/`.

## Examples
- To add a new sermon:
  1. Place markdown in `_pages/主日資料/YYYY/`.
  2. Add related PDF to `assets/docs/`.
  3. Update navigation includes if needed.
- To add a new hymn collection:
  1. Add markdown to `_pages/詩歌/`.
  2. Add PDF to `assets/docs/`.

## Key Files & Directories
- `_config.yml`: Jekyll configuration.
- `Gemfile`: Ruby dependencies.
- `_includes/`, `_layouts/`, `_pages/`: Core site structure.
- `assets/`: Static assets (docs, images, fonts, JS).

---
For questions about conventions or missing documentation, check `README.md` or ask for clarification.
