# Unshure.github.io

Personal GitHub Pages site built with [Jekyll](https://jekyllrb.com/).

## Structure

```
├── _config.yml          # Site configuration (title, description, nav, collections, plugins)
├── _layouts/
│   ├── default.html     # Base layout (header, nav, footer)
│   ├── page.html        # Layout for static pages (wraps default)
│   ├── project.html     # Layout for individual project pages
│   └── presentation.html # Layout for individual presentation pages
├── _projects/           # Project collection (one .md per project)
├── _presentations/      # Presentation collection (one .md per presentation)
├── assets/
│   ├── css/
│   │   └── style-dusk.css # All custom styles (dark theme, grid, cards)
│   ├── images/          # Site images
│   └── presentations/   # Presentation slide PDFs
├── index.md             # Homepage / About
├── projects.md          # Project listing
├── presentations.md     # Presentation listing
├── Gemfile              # Ruby/Jekyll dependencies
└── .gitignore
```

## Local Development

**Prerequisites:** Ruby and Bundler installed.

```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve --livereload
```

The site will be available at `http://localhost:4000`.

## How It Works

- **Jekyll** reads Markdown files (`index.md`, `projects.md`, `presentations.md`) and renders them into static HTML using the layouts in `_layouts/`.
- **Collections** (`_projects/`, `_presentations/`) each generate individual pages with structured front matter.
- **Front matter** (the `---` block at the top of each `.md` file) controls which layout is used, the page title, and the permalink.
- **`_config.yml`** sets global options: site title, description, collections, which pages appear in the nav (`header_pages`), and which plugins to load.
- **`assets/css/style-dusk.css`** provides all styling — no theme CSS is inherited. The site uses a custom dark color scheme with sky blue accents.

## Adding a New Page

1. Create a new `.md` file in the project root (e.g. `blog.md`).
2. Add front matter:
   ```yaml
   ---
   layout: page
   title: Blog
   permalink: /blog/
   ---
   ```
3. Add the filename to `header_pages` in `_config.yml` to include it in the nav.

## Deployment

This repo is configured for [GitHub Pages](https://pages.github.com/). Any push to the `main` branch triggers a build and deploy. The site is served at `https://unshure.github.io`.

To enable Pages: **Settings → Pages → Source → Deploy from a branch → `main` / `/ (root)`**.
