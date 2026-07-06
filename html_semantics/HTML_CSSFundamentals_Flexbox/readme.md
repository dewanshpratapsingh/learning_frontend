# HTML 

- HTML is a markup language.Instead of telling a computer to perform actions or calculations, it uses tags to mark up plain text so a web browser knows how to structure and display it.

<!DOCTYPE html> It tells the browser, Render this page using modern HTML5 standards. Without it, browsers may enter quirks mode and behave like Internet Explorer from years ago. Always include it.

- <html> Root element. Everything lives inside it.

- <html lang="en"> This tells Screen readers, Search engines, Translators what language the document is in.

- <head> Contains metadata. Not visible on the page.Like title, favicon, css, fonts, meta tags

- <body> Everything users actually see.Buttons, Images, Headings, Cards, Paragraphs, Everything.

# HTML Elements
- some tags in html dont have closing tags and are called void elements, ex - <br>, <img>, <hr>, <input>

- most tags have opening and closing, <p>Hello,world</p>
- Nesting : Elements live inside other elements.
<div>
    <h1>Portfolio</h1>
    <p>Hello</p>
</div>

Tree structure
div
├── h1
└── p

- Browsers internally convert HTML into something called the DOM(Document Object Model), which is this tree representation.

- Block Element : Take the full width, Always start on a new line.
Ex :<div>
<p>
<section>
<header>
<footer>
<article>
<nav>

- Inline elements : Only take the required width.
Ex : <a>
<span>
<strong>
<em>

-Instead of using multiple <div> tags use <header>, <nav>, <main>, <section>, <footer>. This is semantic html i,e tag carries meaning.
Ex - <div class = "header"> -> <header></header>

-Semantic HTML provides accessibility meaning screen reader knows this is navigation, this is footer, this is main content, SEO engines understands your page better, Readability increases i,e coder can understand why he wrote this peice of code.

- Good page structure
Ex - 
body
├── header
│      └── nav
│
├── main
│      ├── section (About)
│      ├── section (Experience)
│      ├── section (Projects)
│      └── section (Contact)
│
└── footer

