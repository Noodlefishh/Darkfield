---
layout: post
title: "Hello World: Getting Started with Darkfield"
date: 2024-01-01 12:00:00 -0500
categories: general
tags: general
---

Welcome to your new blog powered by **Darkfield**, a minimal dark Jekyll theme built for writers who care about typography and readability.

## Writing Your First Post

To create a new post, add a file to the `_posts` directory with this naming convention:

```
YYYY-MM-DD-your-post-title.markdown
```

Every post needs front matter at the top:

```yaml
---
layout: post
title: "Your Post Title"
date: 2024-01-01 12:00:00 -0500
tags: your-tag
---
```

## Markdown Support

Darkfield renders standard Markdown cleanly. A few examples:

**Bold** and *italic* work as expected. You can include `inline code` or full fenced code blocks:

```python
def greet(name):
    return f"Hello, {name}!"
```

> Blockquotes are styled with a left accent border — useful for quotes or callouts.

Lists work too:

- Item one
- Item two
- Item three

## Customizing the Theme

Open `_config.yml` and update these fields to make the theme yours:

- `title` — your blog's name
- `hero_title` — the headline on the homepage
- `description_short` — the small label above the headline
- `url` — your GitHub Pages URL (`https://yourusername.github.io`)
- `github_username` — your GitHub handle
- `featured_tags` — tags shown as pills in the hero section

Then update `about.md` with your bio.

Delete this post when you're ready to start fresh. Happy writing.
