# Buddhist Bible Study

A small, public Buddhist studies curriculum built with Jekyll and the Minimal Mistakes theme.

## Overview
- Live site: `https://millerms.github.io/book-study-group/`
- Theme: [`mmistakes/minimal-mistakes@4.27.3`](https://github.com/mmistakes/minimal-mistakes)
- Base URL: `_config.yml` uses `url: https://millerms.github.io` and `baseurl: /book-study-group` (links should respect this).

## Project Structure
- `_config.yml`: Site config, theme, footer links.
- `_data/navigation.yml`: Masthead and curriculum sidebar navigation.
- `_pages/`: About, methodology, curriculum overview, and resources.
- `_weeks/`: The twelve curriculum documents.
- `_layouts/week.html`: Shared weekly-page presentation and previous/next navigation.
- `_includes/week-outline.md`: Reusable placeholder structure for unfilled weekly guides.
- `index.md`: Home page.
- `assets/`, `_sass/`: Styles and assets.

## Local Development (Docker)
Prereqs: Docker Desktop with Compose v2 (`docker compose`).

- Start: `make serve`
- Open: `http://localhost:4000/book-study-group/`
- Stop: Ctrl+C
- Clean: `make clean`

What it does:
- Builds a Ruby 3.2 image and installs gems.
- Mounts the repo so edits live-reload (`35729` exposed).
- Caches gems in a Docker volume for faster subsequent runs.

## Local Development (Ruby)
If you prefer running locally without Docker:

1) Install Ruby 3.1 (via rbenv/asdf). GitHub Pages' pinned Liquid version is not compatible with Ruby 3.2.
2) Install Bundler: `gem install bundler:2.4.22`
3) Install gems: `bundle install`
4) Serve: `bundle exec jekyll serve`

Open `http://localhost:4000/book-study-group/`.

## Common Edits
- Navigation: Edit `_data/navigation.yml`; the theme prefixes `baseurl` for local links.
- Footer links: Edit `footer.links` in `_config.yml` and include both `label`, `icon`, and `url`.
- Pages: Add Markdown files in `_pages/` with front matter including `layout` and `permalink`.
- Weekly guides: Replace the placeholder include in a file under `_weeks/` with verified Markdown content while retaining the same section order.

## Deploying to GitHub Pages
This is configured as a GitHub project site. Push to `main`, then enable GitHub Pages in the repository settings. The simplest compatible option is **Deploy from a branch**, using `main` and `/ (root)`. GitHub Actions can be added later if the build needs unsupported plugins or custom processing.

`https://millerms.github.io/book-study-group/`

## Acknowledgements
- Theme: [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) by Michael Rose.

## License
MIT — see [`LICENSE`](LICENSE).
