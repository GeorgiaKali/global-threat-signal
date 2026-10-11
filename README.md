# Global Threat Signal

Articles and research notes by Georgia Kali, published with Jekyll on GitHub Pages.

- Site: https://georgiakali.github.io/global-threat-signal/
- Project and map: https://globalthreatsignal.org
- Author hub: https://georgiakali.github.io

GitHub Pages builds this repository from the `main` branch, folder `/` (root). There is no Actions workflow and no secrets.

## Add a post

1. Create `_posts/YYYY-MM-DD-short-title.md`. The date in the name is the publication date.
2. Start the file with this front matter, then write the article in Markdown:

```yaml
---
layout: post
title: "Title of the article"
date: 2026-10-11 12:00:00 +0000
author: Georgia Kali
categories:
  - Notes
tags:
  - one-tag
  - another-tag
description: One or two plain sentences. This is the summary on the home page, in RSS, and in search results.
---
```

3. Commit the file to `main` and push. The home page lists posts newest first. Each tag and category gets a section on its own page. The post shows the author, date, tags, and reading time.

In a post, an internal link needs the project path:

```liquid
[related note]({{ '/about/' | relative_url }})
```

To show Liquid inside a fenced code block, wrap the example in `{% raw %}` and `{% endraw %}`.

Delete `_posts/2026-10-11-sample-delete-me.md` before you publish real work. It only shows the layout. Do not copy `sample: true` or `sitemap: false` from that file. Those lines keep the placeholder out of the sitemap.

## Preview locally

```bash
bundle install
bundle exec jekyll serve
```

Pages are under `http://127.0.0.1:4000/global-threat-signal/` because `baseurl` is `/global-threat-signal`.
