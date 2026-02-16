# AGENTS.md - Agent Guidelines for quanttide-profile-of-founder

## Project Overview

This is a **Jupyter Book documentation project** containing founder profile and knowledge management content. The project is written in Markdown and built using Jupyter Book.

- **Project type**: Documentation site (Jupyter Book)
- **Content language**: Chinese (Simplified)
- **No Python code**: This is a pure documentation repository

---

## Build Commands

### Build the Book

```bash
# Build HTML version
jupyter-book build .

# Build and serve locally
jupyter-book build . --builder htmlserve
```

### Clean Build

```bash
# Clean previously built files
jupyter-book clean .
```

### Single Page Build (for faster iteration)

```bash
# Build specific file
jupyter-book build . --page path/to/file.md
```

---

## Linting

This project uses **Markdownlint** for Markdown files:

```bash
# Install markdownlint-cli (if not present)
npm install -g markdownlint-cli

# Run linting
markdownlint "**/*.md"
```

---

## Testing

No traditional code tests exist. For documentation quality:

- Verify all internal links work: `jupyter-book build . --verbose`
- Check table of contents validity in `_toc.yml`
- Validate YAML syntax in config files

---

## Code Style Guidelines

### Markdown Formatting

- Use ATX-style headers (`#`, `##`, `###`)
- One blank line between block elements
- Code blocks with language specifiers: ```python, ```bash, etc.
- Use fenced code blocks instead of indented code

### File Naming

- Use lowercase with hyphens: `my-section-name.md`
- Use descriptive, SEO-friendly names
- Directory names: lowercase, plural (e.g., `think/`, `knowl/`)

### Content Structure (_toc.yml)

- Use `jb-book` format
- Use `parts` and `chapters` for hierarchical structure
- Each file must exist before adding to TOC
- Keep TOC depth reasonable (max 3-4 levels)

### YAML Conventions (_config.yml, _toc.yml)

- Use 2-space indentation
- No tabs
- Quote strings with special characters
- Use lowercase for keys

### Chinese Content

- Use Chinese punctuation: `。`，`，`，`？`，`！`
- No extra spaces between Chinese and English text
- Use full-width characters where appropriate
- Keep consistent terminology throughout

### Internal Linking

```markdown
[Link Text](path/to/file.md)
[Anchor Link](file.md#section-anchor)
```

### Images

- Store in `_static/` directory
- Use relative paths: `../_static/image.png` or `_static/image.png`
- Optimize images before adding

---

## Project Structure

```
.
├── _config.yml          # Jupyter Book configuration
├── _toc.yml             # Table of contents
├── index.md             # Home page
├── think/               # Thinking documents
├── knowl/               # Knowledge documents
├── code/                # Code-related docs
├── write/               # Reports and writing
├── stdn/                # Standards documents
├── agent/               # Agent-related docs
└── _static/             # Static assets (images, etc.)
```

---

## Error Handling

- **Broken links**: Always verify links point to existing files
- **TOC errors**: Ensure all files in `_toc.yml` exist
- **Build errors**: Check YAML syntax, file paths, and image references
- **Chinese encoding**: Ensure UTF-8 encoding for all files

---

## Common Tasks

### Adding a New Document

1. Create the `.md` file in appropriate directory
2. Add proper frontmatter if needed (title, etc.)
3. Update `_toc.yml` to include the file
4. Test build: `jupyter-book build .`

### Updating Navigation

Edit `_toc.yml` following the jb-book format. Remember:
- Files must exist before adding to TOC
- Test build after each TOC change

### Local Preview

```bash
jupyter-book build . --builder htmlserve
# Then open http://localhost:8000
```

---

## Notes for Agents

- This is a documentation-only repository - do not add Python code
- Always verify build succeeds after making changes
- Maintain consistent Chinese terminology
- Keep Markdown files well-structured and readable
- Do not modify `_toc.yml` without ensuring all referenced files exist
