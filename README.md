# Darkfield

A minimal, dark Jekyll theme built for developers and technical writers. Clean typography, syntax highlighting, tag system, and GitHub Pages deployment out of the box.

![Jekyll](https://img.shields.io/badge/Jekyll-4.3+-red)
![License](https://img.shields.io/badge/license-MIT-green)

## Overview

Darkfield is a static blog theme powered by Jekyll. It features a dark color palette with green and purple accents, a responsive layout, and everything you need to publish technical content.

## Features

- Dark color palette with green (#c8f464) and purple (#7b6ef6) accents
- Responsive layout with sticky navigation
- Hero section with configurable featured tag pills
- Featured post card on the homepage
- Post list with tags and date metadata
- Tag index page (`/tags`)
- Archive page grouped by year (`/archives`)
- Customizable About page
- Syntax highlighting via Rouge (dark theme)
- RSS feed, XML sitemap, and SEO tags via plugins
- GitHub Actions workflow for automatic deployment
- Dependabot for weekly gem updates

## Typography

Darkfield uses three Google Fonts:

- **Outfit** (300, 400, 500) — body text
- **DM Mono** (400, 500) — UI elements and code
- **DM Serif Display** (regular, italic) — headings and post titles

## Prerequisites

Make sure you have the following installed before getting started:

- **Ruby 3.1+** — [ruby-lang.org/en/downloads](https://www.ruby-lang.org/en/downloads/)
  - Windows: use [RubyInstaller](https://rubyinstaller.org/) (recommended)
  - macOS: Ruby is pre-installed, or install via `brew install ruby`
  - Linux: `sudo apt install ruby-full` (Debian/Ubuntu)
- **Bundler** — Ruby gem manager:
  ```bash
  gem install bundler
  ```

Verify your installation:

```bash
ruby --version    # should be 3.1 or higher
bundle --version
```

## Running the Project Locally

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/darkfield.git my-blog
cd my-blog
```

### 2. Install dependencies

```bash
bundle install
```

> **Windows users:** The `Gemfile.lock` already includes both Windows and Linux platform entries, so no extra steps are needed.

### 3. Start the development server

```bash
bundle exec jekyll serve
```

Open your browser at `http://localhost:4000`.

Jekyll watches your files and recompiles the site on every change. Just refresh your browser to see updates.

#### Useful options

```bash
# Include draft posts (_drafts/)
bundle exec jekyll serve --drafts

# Use a different port
bundle exec jekyll serve --port 5000

# Make the site accessible on your local network
bundle exec jekyll serve --host 0.0.0.0
```

### 4. Build the static site (optional)

To generate production files into the `_site/` folder:

```bash
bundle exec jekyll build
```

## Configuration

Edit `_config.yml` to customize your site:

```yaml
title: "My Blog"
description_short: "Personal Blog"
hero_title: "Writing on code, tech, and ideas"
url: "https://yourusername.github.io"

author:
  name: "Your Name"
  email: "you@example.com"

github_username: yourusername

featured_tags:
  - Technology
  - Code
  - Research
```

> **Note:** Restart `jekyll serve` after any changes to `_config.yml`.

## Writing Posts

Create a file in `_posts/` following the naming convention:

```
_posts/YYYY-MM-DD-your-post-title.markdown
```

Minimal YAML front matter:

```yaml
---
layout: post
title: "Your Post Title"
date: 2024-06-15 12:00:00 -0500
tags: your-tag
---

Post content in Markdown...
```

## Project Structure

```
darkfield/
├── _config.yml          # Main configuration
├── Gemfile              # Ruby dependencies
├── _layouts/
│   ├── default.html     # Base template (HTML, nav, footer)
│   ├── home.html        # Homepage layout
│   └── post.html        # Individual post layout
├── _includes/
│   ├── nav.html         # Navigation bar
│   └── footer.html      # Footer
├── _sass/
│   ├── _variables.scss  # Color and layout variables
│   ├── _base.scss       # Base styles
│   ├── _nav.scss        # Navigation styles
│   ├── _home.scss       # Homepage styles
│   ├── _post.scss       # Post styles
│   └── _syntax.scss     # Syntax highlighting
├── assets/css/
│   └── main.scss        # Stylesheet entry point
├── _posts/              # Blog posts (Markdown)
├── archives.html        # Archive page
├── tags.html            # Tag index page
├── about.md             # About page
└── .github/
    ├── dependabot.yml
    └── workflows/
        └── deploy.yml   # Automatic GitHub Pages deployment
```

## Customization

### Colors

All colors are defined as Sass variables in [_sass/_variables.scss](_sass/_variables.scss):

```scss
$bg:      #0c0c0f;   // page background
$accent:  #c8f464;   // green accent (links, tags, highlights)
$accent2: #7b6ef6;   // purple accent (secondary tags)
$text:    #e8e6e1;   // body text
$muted:   #6b6a72;   // secondary text, dates, labels
```

### Layout width

```scss
$max-width: 860px;
$gutter: 2rem;
```

### Navigation links

Edit [_includes/nav.html](_includes/nav.html) to add or remove nav items.

## Deploy to GitHub Pages

1. Push your repository to GitHub.
2. Go to **Settings → Pages**.
3. Set **Source** to **GitHub Actions**.
4. Push to `main` — the included workflow handles the build and deploy automatically.

## License

MIT — see [LICENSE](LICENSE).
