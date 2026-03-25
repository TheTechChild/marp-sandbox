# AGENTS.md — Marp Sandbox

> Agentic coding guide for this repository.

## Project Overview

A playground for experimenting with Marp (Markdown Presentation Ecosystem). Enables creating beautiful slide presentations using Markdown syntax with support for custom themes, code highlighting, and multi-format export (HTML, PDF, PowerPoint).

## Project Structure

```
marp-sandbox/
├── presentations/
│   └── example-presentation.md          # Example presentation
├── themes/
│   └── custom-theme.css                 # Custom theme stylesheet
├── package.json                         # NPM scripts & dependencies
├── README.md                            # Project overview
├── USAGE.md                             # Detailed usage guide
└── .gitignore                           # Git exclusions
```

## Build & Run Commands

### Setup
```bash
npm install
```

### Build Presentations
```bash
npm run build              # Generate HTML
npm run build:pdf          # Generate PDF
npm run build:pptx         # Generate PowerPoint
npm run build:all          # Generate HTML + PDF
npm run theme              # Build with custom theme
```

### Development
```bash
npm run serve              # Live preview server
npm run watch              # Auto-rebuild on changes
```

## Conventions

- **Frontmatter**: YAML config block at start of each presentation
- **Slide separator**: Three hyphens `---` between slides
- **Themes**: Built-in (default, gaia, uncover) or custom CSS
- **Directives**: Slide-specific control via HTML comments (e.g., `<!-- _class: lead -->`)
- **Assets**: Images in `assets/images/`, relative paths from presentation file
- **Output**: Generated files in `output/` directory (gitignored)

## Known Limitations / Gotchas

- **PDF export**: Requires Chromium/Chrome installed for PDF generation
- **Image paths**: Must use relative paths; absolute paths may fail
- **Theme CSS**: Custom themes require valid CSS syntax; invalid CSS silently fails
- **Single presentation**: Current npm scripts hardcoded to `example-presentation.md`
- **No output directory**: Must create `output/` manually or via build script
- **Math rendering**: Requires proper LaTeX syntax; complex expressions may not render
