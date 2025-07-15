# Marp Presentation Usage Guide

Welcome to the Marp Sandbox! This guide will help you create and manage presentations using Marp.

## Quick Start

1. **Create a new presentation**
   - Create a new `.md` file in the `presentations/` directory
   - Start with the Marp frontmatter:
   ```yaml
   ---
   marp: true
   theme: default
   paginate: true
   ---
   ```

2. **Build your presentation**
   ```bash
   npm run build    # Generate HTML
   npm run build:pdf    # Generate PDF
   npm run build:pptx   # Generate PowerPoint
   npm run build:all    # Generate HTML and PDF
   ```

3. **Preview your presentation**
   ```bash
   npm run serve    # Start live preview server
   npm run watch    # Auto-rebuild on changes
   ```

## Available NPM Scripts

| Script | Description |
|--------|-------------|
| `npm run build` | Convert presentation to HTML |
| `npm run build:pdf` | Convert presentation to PDF |
| `npm run build:pptx` | Convert presentation to PowerPoint |
| `npm run watch` | Watch for changes and auto-rebuild HTML |
| `npm run serve` | Start development server with live preview |
| `npm run build:all` | Build both HTML and PDF versions |
| `npm run theme` | Build with custom theme |

## Creating Presentations

### Basic Structure

Each presentation should start with frontmatter configuration:

```markdown
---
marp: true
theme: default
paginate: true
backgroundColor: #fff
---

# Your First Slide

Content goes here...

---

# Second Slide

More content...
```

### Slide Separators

Use `---` (three hyphens) to separate slides.

## Applying Themes

### Using Built-in Themes

Marp comes with three built-in themes:
- `default`
- `gaia`
- `uncover`

Set in frontmatter:
```yaml
---
theme: gaia
---
```

### Using Custom Themes

1. Create your theme in `themes/` directory
2. Apply it using the theme script:
   ```bash
   npm run theme
   ```
3. Or specify in the command:
   ```bash
   npx marp presentations/your-presentation.md --theme themes/custom-theme.css
   ```

## Marp Syntax Tips

### Slide Directives

Control individual slides with directives:

```markdown
<!-- _class: lead -->
<!-- _backgroundColor: #123456 -->
<!-- _color: white -->
```

### Images

**Background images:**
```markdown
![bg](image.jpg)
![bg right:40%](image.jpg)
```

**Inline images:**
```markdown
![width:200px](image.jpg)
```

### Lists and Tables

Standard Markdown syntax works:
```markdown
- Item 1
  - Nested item
- Item 2

| Column 1 | Column 2 |
|----------|----------|
| Data 1   | Data 2   |
```

### Code Blocks

Use triple backticks with language specification:
````markdown
```javascript
console.log('Hello, Marp!');
```
````

### Math Expressions

Inline: `$E = mc^2$`

Block:
```markdown
$$
\sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$
```

## Project Structure

```
marp-sandbox/
├── presentations/      # Your presentation files
├── themes/            # Custom themes
├── assets/            # Images and other resources
│   └── images/
├── output/            # Generated presentations (gitignored)
└── package.json       # NPM scripts and dependencies
```

## Tips and Best Practices

1. **Use version control**: Track your presentations in Git
2. **Organize assets**: Keep images in `assets/images/`
3. **Test exports**: Always preview HTML before generating PDF/PPTX
4. **Custom styling**: Create reusable themes for consistent branding
5. **Keyboard shortcuts**: Use arrow keys to navigate during presentation

## Troubleshooting

**Issue**: Images not loading
- Solution: Use relative paths from the presentation file

**Issue**: PDF generation fails
- Solution: Ensure Chromium/Chrome is installed (required for PDF export)

**Issue**: Custom theme not applying
- Solution: Check the theme path and ensure CSS syntax is valid

## Resources

- [Marp Official Documentation](https://marpit.marp.app/)
- [Marp CLI Documentation](https://github.com/marp-team/marp-cli)
- [Marpit Markdown](https://marpit.marp.app/markdown)
- [Theme CSS Properties](https://marpit.marp.app/theme-css)