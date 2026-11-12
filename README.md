# TextForge

A lightweight text formatter that runs entirely in the browser. It's a single HTML file built with [Alpine.js](https://alpinejs.dev/), with no build step, no backend and no data leaving your machine.

Paste some text, pick a tool in the sidebar, copy the result.

## Features

**Format**
- **Wrap text** to a configurable line width (existing line breaks are kept)
- **Slugify / Unslugify** with a custom separator (handles accents, `ß`, `œ`, `æ`; one slug per line)
- **Hashtags ⇄ List**: `Learn English, Idioms` ⇄ `#LearnEnglish #Idioms`

**Change case**
- UPPERCASE, lowercase, Title Case, Sentence case
- camelCase, PascalCase, snake_case, kebab-case, CONSTANT_CASE (applied line by line)

**Lists** (one item per line)
- **Sort:** A → Z, Z → A (ignores accents and case, natural order so `item 2` comes before `item 10`), by length, reverse, shuffle
- **Clean:** remove duplicates, remove empty lines, trim spaces, number lines
- **Convert:** lines ⇄ comma-separated list

**Stats**
- Live word, character, character (no spaces), line and sentence counts, plus estimated reading time

**UX**
- Input and output side by side, with the tools in a sidebar
- **Use as input** to chain several operations
- One-click copy with feedback
- Keyboard-accessible, responsive down to mobile

## Usage

No installation needed. Open `text-formatter.html` in a browser.

Alpine.js is loaded from a CDN, so an internet connection is required on first load. To work fully offline, download Alpine and change the `<script>` tag to point to the local file.

## Customization

- **Styles** are inlined in the `<style>` block. Move them to a separate `.css` file if you prefer.
- **Add a case or list operation:**
  1. Add an entry to `cases` or `listGroups` (this adds the button).
  2. Handle the new id in `convertCase()` or `listOp()`.
- **Sidebar width** is the first value of `grid-template-columns` in `.app`.

## Tech

- HTML, CSS, JavaScript
- [Alpine.js](https://alpinejs.dev/) 3

## License

MIT