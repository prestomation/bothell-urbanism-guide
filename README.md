# Bothell Urbanism Guide

A practical reference guide for Bothell urbanists and advocates. Understand the issues, learn the terms, and show up to community meetings ready to contribute.

## What's in here

- **Quick Start** -- Plain-language overview of Bothell's urban landscape, governance, and active debates
- **Glossary** -- Definitions of urbanist terms (ADU, SEPA, FAR, BRT, etc.) with Bothell-specific context
- **Timeline** -- Key events in Bothell's urbanism history, from 1909 incorporation to the 2024 comprehensive plan update
- **Blog** -- Deeper dives and analysis on specific topics

## Tech stack

- [Hugo](https://gohugo.io/) static site generator
- [hugo-book](https://github.com/alex-shpak/hugo-book) theme (wiki/documentation style)
- GitHub Pages for hosting
- GitHub Actions for automated deployment
- Content is standalone Markdown + YAML data files (portable to other generators)

## Local development

```bash
# Clone with submodules (for the theme)
git clone --recurse-submodules https://github.com/prestomation/bothell-urbanism-guide.git
cd bothell-urbanism-guide

# Run local dev server
hugo server -D

# Build for production
hugo --gc --minify
```

## Content structure

```
content/
  _index.md              # Homepage
  quick-start/
    _index.md            # Bothell overview
  glossary/
    _index.md            # Glossary landing page
    housing-zoning.md    # Housing & zoning terms
    transportation.md    # Transportation terms
    land-use.md          # Land use & planning terms
    funding-policy.md    # Funding & policy terms
  guides/
    _index.md            # Guides landing page
  blog/
    _index.md            # Blog listing
    welcome.md           # First post
  timeline/
    _index.md            # Timeline page
data/
  timeline.yaml          # Timeline event data (structured, portable)
```

## Contributing

Content is in Markdown. You don't need to know Hugo to contribute -- just edit the `.md` files.

1. Fork the repo
2. Create a branch
3. Edit or add content
4. Submit a pull request

### Adding a glossary term

Add it to the appropriate category file in `content/glossary/`. Follow the existing format:

```markdown
## Term Name

A plain-language definition.

**Why it matters:** Bothell-specific context.

**See also:** Related Term 1, Related Term 2
```

### Adding a timeline event

Add an entry to `data/timeline.yaml`:

```yaml
- year: 2025
  title: "Event Title"
  description: "What happened."
  legacy: "Why it matters today."
  sources:
    primary:
      name: "Source Name"
      url: "https://..."
```

### Adding a blog post

Create a new file in `content/blog/`:

```bash
hugo new blog/your-post-title.md
```

## License

MIT
