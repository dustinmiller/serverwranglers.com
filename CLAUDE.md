# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website for "Server Wranglers" - a company offering premium managed server services. The project is built using Zola, a fast static site generator written in Rust, and includes a blog with server management insights.

## Architecture

- **Static Site Generator**: Built with Zola (https://www.getzola.org/)
- **Templates**: Tera templating engine with base template inheritance
- **Content**: Markdown files for pages and blog posts
- **Styling**: Embedded CSS in base template with dark theme
- **External Dependencies**: 
  - Font Awesome icons (CDN)
  - Google Fonts (Inter)

## Project Structure

```
├── config.toml           # Zola configuration
├── content/              # Markdown content files
│   ├── _index.md        # Homepage content
│   └── blog/            # Blog section
│       ├── _index.md    # Blog listing page
│       └── *.md         # Individual blog posts
├── templates/           # Tera templates
│   ├── base.html       # Base template with navigation and styling
│   ├── index.html      # Homepage template
│   ├── blog.html       # Blog listing template
│   └── blog-page.html  # Individual blog post template
└── static/             # Static assets (currently empty)
```

## Styling System

The CSS is embedded in `templates/base.html` and uses a dark theme with CSS custom properties:
- Primary colors: Dark purple/blue theme (`--bg-primary: #282a36`)
- Accent colors: Purple (`--accent-primary: #bd93f9`) and cyan (`--accent-cyan: #8be9fd`)
- Responsive design with mobile-first approach
- Animations for server rack visualization and hover effects

## Development Commands

To work with this Zola site:

```bash
# Serve the site locally with hot reload
zola serve

# Build the site for production
zola build

# Check the site for issues
zola check
```

## Content Management

- **Homepage**: Edit `content/_index.md` for metadata, `templates/index.html` for structure
- **Blog Posts**: Create new `.md` files in `content/blog/` with frontmatter
- **Navigation**: Configure in `config.toml` under `[extra.nav]`
- **Site Settings**: Modify `config.toml` for title, description, base URL, etc.

## Blog Features

- Automatic post listing with pagination support
- Taxonomy support for tags and categories
- Reading time calculation
- RSS/Atom feed generation
- SEO-friendly URLs
- Responsive design with sidebar widgets