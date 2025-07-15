---
marp: true
theme: default
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

<!-- _class: lead -->

# Welcome to Marp

## Markdown Presentation Ecosystem

**Created with Marp CLI**
📅 2025

---

# What is Marp?

Marp (Markdown Presentation) lets you create beautiful slide decks using:

- 📝 **Markdown** - Simple and familiar syntax
- 🎨 **Themes** - Customizable and reusable
- 🚀 **Fast** - Lightning quick rendering
- 📦 **Portable** - Export to HTML, PDF, or PPTX

> The markdown-driven presentation ecosystem

---

# Code Syntax Highlighting

Marp supports syntax highlighting for various languages:

```javascript
// JavaScript example
function greet(name) {
  return `Hello, ${name}!`;
}

const message = greet('Marp');
console.log(message); // Output: Hello, Marp!
```

```python
# Python example
def calculate_fibonacci(n):
    if n <= 1:
        return n
    return calculate_fibonacci(n-1) + calculate_fibonacci(n-2)

print(f"Fibonacci(10) = {calculate_fibonacci(10)}")
```

---

# Images and Layouts

![bg right:40% 80%](https://raw.githubusercontent.com/marp-team/marp/master/marp.png)

## Flexible Image Positioning

You can position images in various ways:

- Background images
- Split layouts
- Inline images
- Custom sizing

The image on the right shows the Marp logo using the `![bg right:40% 80%]` directive.

---

<!-- _class: lead -->
<!-- _backgroundColor: #2B3A67 -->
<!-- _color: white -->

# Custom Styling

## This slide uses custom directives

- Custom background color: `#2B3A67`
- White text color
- Lead class for centered content

You can customize individual slides or create reusable themes!

---

# Lists and Tables

## Unordered Lists
- First item
  - Nested item 1
  - Nested item 2
- Second item
- Third item

## Tables

| Feature | Marp | PowerPoint | Keynote |
|---------|------|------------|---------|
| Markdown | ✅ | ❌ | ❌ |
| Version Control | ✅ | ⚠️ | ⚠️ |
| Free | ✅ | ❌ | ❌ |

---

# Advanced Features

## Math Expressions (KaTeX)

Inline math: $E = mc^2$

Block math:
$$
\sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$

## Diagrams with Mermaid

```mermaid
graph LR
    A[Write Markdown] --> B[Run Marp CLI]
    B --> C[Generate Slides]
    C --> D[Present!]
```

---

<!-- _class: lead -->

# Thank You! 🎉

## Ready to create amazing presentations?

**Resources:**
- [Marp Official Site](https://marp.app)
- [GitHub Repository](https://github.com/marp-team/marp)
- [Documentation](https://marpit.marp.app)

---