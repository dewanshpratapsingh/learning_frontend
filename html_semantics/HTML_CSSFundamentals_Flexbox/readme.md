# HTML

HTML (**HyperText Markup Language**) is a **markup language**, not a programming language.

Instead of telling the computer to perform actions or calculations, HTML uses **tags** to describe the structure and meaning of content so that web browsers know how to display it.

---

## Basic HTML Document Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

</body>
</html>
```

### `<!DOCTYPE html>`

- Declares that the document uses **HTML5**.
- Tells the browser to render the page using modern HTML standards.
- Without it, browsers may enter **Quirks Mode**, causing inconsistent rendering.

> Always include it at the top of every HTML document.

---

### `<html>`

- The **root element** of an HTML document.
- Every other HTML element exists inside it.

Example:

```html
<html>
    ...
</html>
```

---

### `lang="en"`

```html
<html lang="en">
```

Specifies the language of the document.

It helps:

- Screen readers
- Search engines
- Translation tools

---

### `<head>`

Contains metadata about the webpage.

This content is **not displayed** to users.

Common elements inside `<head>`:

- `<title>`
- `<meta>`
- CSS files
- Fonts
- Favicon

---

### `<body>`

Contains everything visible on the webpage.

Examples:

- Headings
- Paragraphs
- Images
- Buttons
- Forms
- Cards
- Navigation

---

# HTML Elements

An HTML element usually consists of:

- Opening tag
- Content
- Closing tag

Example:

```html
<p>Hello, World!</p>
```

---

## Void Elements

Some HTML elements **do not have closing tags**.

Examples:

```html
<br>
<img>
<hr>
<input>
<meta>
<link>
```

These are called **void elements**.

---

## Nesting

HTML elements can contain other elements.

Example:

```html
<div>
    <h1>Portfolio</h1>
    <p>Hello</p>
</div>
```

Tree representation:

```text
div
├── h1
└── p
```

Browsers convert this structure into the **DOM (Document Object Model)**.

The DOM is a tree representation of the HTML document that JavaScript can interact with.

---

# Block vs Inline Elements

## Block Elements

Characteristics:

- Take the full available width.
- Always start on a new line.

Examples:

```html
<div>
<p>
<section>
<header>
<footer>
<article>
<nav>
<main>
```

---

## Inline Elements

Characteristics:

- Only occupy the width they need.
- Do not start on a new line.

Examples:

```html
<a>
<span>
<strong>
<em>
```

---

# Semantic HTML

Semantic HTML means using elements that **describe the meaning of the content** instead of generic containers.

Instead of writing:

```html
<div class="header">
```

Use:

```html
<header>
```

Other semantic elements include:

```html
<header>
<nav>
<main>
<section>
<article>
<aside>
<footer>
```

---

## Why Semantic HTML?

### Accessibility

Semantic elements help screen readers understand the page structure.

For example:

- Navigation
- Main content
- Footer

can all be identified automatically.

---

### SEO (Search Engine Optimization)

Search engines understand the purpose of each section more accurately, helping improve indexing.

---

### Readability

Semantic tags make the code easier to understand and maintain.

Compare:

```html
<div class="header">
```

vs

```html
<header>
```

The second is much more descriptive.

---

# Typical Page Structure

```text
body
├── header
│   └── nav
│
├── main
│   ├── section (About)
│   ├── section (Experience)
│   ├── section (Projects)
│   └── section (Contact)
│
└── footer
```

This is the basic structure followed by most modern websites.

---

# Key Takeaways

- HTML defines the **structure** of a webpage.
- HTML is a **markup language**, not a programming language.
- Use semantic elements whenever possible.
- Use only one `<h1>` per page.
- Always include `<!DOCTYPE html>`.
- Always specify the document language using `lang`.
- The browser converts HTML into the **DOM**, which JavaScript can manipulate.
- Prefer semantic tags over generic `<div>` elements whenever they accurately describe the content.