# Repository Guidelines

- Think in English, but generate responses in Japanese. (思考は英語、回答の生成は日本語で行うように)
- Do not make any changes, until you have 95% confidence that you know what to build. Ask me follow up questions until you have that confidence.

## Project Structure & Module Organization

- `config.yml` holds Hugo site configuration (menus, params, permalinks, outputs).
- `content/` contains Markdown pages; posts live in `content/posts/`.
- `archetypes/` provides front matter templates for new content.
- `assets/css/extended/custom.css` is the main custom CSS entry.
- `static/` is for static files copied as-is (images, icons, etc.).
- `themes/archie` is a Git submodule for the site theme.

## Build, Test, and Development Commands

- `mise install` (or your preferred tool manager) installs versions from `.tool-versions`.
- `hugo server -D` runs the local dev server and includes drafts.
- `hugo` builds the site into `public/` using `config.yml`.
- `yarn install` installs PostCSS dependencies used by Hugo’s asset pipeline.

## Coding Style & Naming Conventions

- Content uses Markdown with YAML front matter; follow the existing keys and 2-space indentation.
- Post filenames and `slug` values should be kebab-case (e.g., `hello-world`).
- Keep posts under `content/posts/` and page entries under `content/`.
- Custom CSS belongs in `assets/css/extended/custom.css`.

## Testing Guidelines

- No automated tests are defined in this repository.
- Validate changes by running `hugo server -D` and checking the rendered pages.

## Commit & Pull Request Guidelines

- Commit messages are short and descriptive; the history includes both English and Japanese.
- Dependency bumps follow the pattern `Bump <pkg> from <old> to <new> (#NN)`.
- Pull requests should include a brief summary, affected paths, and screenshots for layout/style changes.
- Link related issues when applicable.

## Content Authoring Notes

- Typical front matter fields are `slug`, `title`, `date`, `draft`, and `tags`.
- Example:
  ```yaml
  ---
  slug: hello-world
  title: Hello world!
  date: 2021-08-19
  draft: false
  tags: []
  ---
  ```
- Use `archetypes/` templates when adding new posts.

## Theme & Submodules

- Initialize or update the theme submodule with `git submodule update --init --recursive`.
- Theme changes should be coordinated with the upstream Archie project.
