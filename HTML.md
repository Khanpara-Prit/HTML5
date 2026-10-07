# HTML Notes

> Use Emmet (`!` + Enter) to generate a basic HTML boilerplate structure.

## Well-Managed Project Structure

```
project/
├── index.html
├── about.html
├── contact.html
├── css/
│   └── style.css
├── js/
│   └── script.js
├── images/
│   ├── logo.png
│   └── banner.jpg
└── assets/
    └── fonts/
```

## What is HTML?

**HTML** = HyperText Markup Language

HTML is the standard markup language for creating web pages. It provides the structure and content of web pages.

- **HTML**: Standard markup language
- **HTML5**: Latest version with new features (video, audio, canvas, semantic elements)

## Basic Tips Before You Start

### 1. Use Lowercase Tags

```html
<!-- Good -->
<div class="container">
    <p>Content</p>
</div>

<!-- Bad -->
<DIV CLASS="CONTAINER">
    <P>Content</P>
</DIV>
```

### 2. Close All Tags

```html
<!-- Good -->
<p>Paragraph</p>
<br>
<img src="image.jpg" alt="Image">

<!-- Bad -->
<p>Paragraph
<br
<img src="image.jpg">
```

### 3. Use Meaningful Class and ID Names

```html
<!-- Good -->
<div class="navigation-header">Navigation</div>
<button id="submit-button">Submit</button>

<!-- Bad -->
<div class="div1">Navigation</div>
<button id="btn">Submit</button>
```

### 4. Use Comments to Navigate Code (Increase Readability)

```html
<!-- Main navigation -->
<nav>
    <!-- Primary menu -->
    <ul>
        <li><a href="/">Home</a></li>
    </ul>
</nav>
```

## Basic HTML Document

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
</head>
<body>
    <h1>Hello, World!</h1>
    <p>This is my first HTML page.</p>
</body>
</html>
```

### Key Elements Explained

- `<!DOCTYPE html>` — Declares document type (HTML5)
- `<html>` — Root element
- `<head>` — Contains metadata
- `<body>` — Contains visible content
- `<title>` — Page title (shown in browser tab)

## Head Elements

### `<meta>` — Metadata

```html
<!-- Character encoding -->
<meta charset="UTF-8">

<!-- Viewport for responsive design -->
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### `<link>` — External Resources

```html
<!-- Link stylesheets -->
<link rel="stylesheet" href="styles.css">

<!-- Link alternate language -->
<link rel="alternate" hreflang="es" href="https://example.com/es/">
```

## Headings

> Don't use headings just for text size.

```html
<h1>Heading 1 - Main title</h1>
<h2>Heading 2 - Subtitle</h2>
<h3>Heading 3 - Sub-subtitle</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6 - Smallest heading</h6>
```

**Best practice:** Use only ONE `<h1>` per page.

## Paragraphs and Line Breaks

```html
<p>This is a paragraph of text.</p>

<!-- Line break --> <!-- next line -->
<p>First line<br>Second line</p>

<!-- Horizontal rule -->
<hr>

<!-- Preformatted text (preserves spacing) - prints as it is -->
<pre>
    Preserved    spacing
    and line breaks
</pre>
```

## Text Formatting (Preferred)

```html
<!-- Strong importance -->
<strong>This is important</strong>

<!-- Emphasized -->
<em>This is emphasized</em>

<!-- Marked/highlighted -->
<mark>This is highlighted</mark>

<!-- Deleted text -->
<del>This text is deleted</del>

<!-- Inserted text -->
<ins>This text is inserted</ins>

<!-- Smaller text -->
<small>This is small text</small>

<!-- Subscript -->
H<sub>2</sub>O

<!-- Superscript -->
E=mc<sup>2</sup>
```

## Text Containers

### `<span>` — Inline Container
Inline means it takes only the required space.

```html
<p>This is <span class="highlight">highlighted</span> text.</p>
```

### `<div>` — Block Container
Block container means it takes the full line.

```html
<div class="container">
    <h2>Section Title</h2>
    <p>Section content</p>
</div>
```

## Links

`<a></a>` is called the anchor tag.

```html
<!-- Simple link -->
<a href="https://example.com">Visit Example</a>

<!-- Link to page -->
<a href="about.html">About Us</a>
```

### Link Attributes

```html
<!-- Absolute URL -->
<a href="https://example.com">External</a>

<!-- Relative URL -->
<a href="about.html">About</a>

<!-- Email -->
<a href="mailto:email@example.com">Send Email</a>

<!-- Anchor/Section -->
<a href="#section2">Go to Section 2</a>
```

### `target` — Where the Link Opens

- `target="_self"` → Open in current tab
- `target="_blank"` → Open in new tab
- `target="_top"` → Open in full window

### Anchor Links (Internal Navigation)

```html
<!-- At the top of page -->
<a href="#section2">Jump to Section 2</a>
```

## Images

### Basic Images

```html
<!-- Simple image -->
<img src="image.jpg" alt="Description of image">

<!-- With title -->
<img src="image.jpg" alt="Description" title="Hover text">
```

### Image Formats

```html
<!-- JPEG - Photos -->
<img src="photo.jpg" alt="Photo">

<!-- PNG - Images with transparency -->
<img src="icon.png" alt="Icon">

<!-- GIF - Animations -->
<img src="animation.gif" alt="Animation">
```

### Alternative Text

```html
<!-- Images -->
<img src="logo.jpg" alt="Company Logo">

<!-- Icon images -->
<img src="star.jpg" alt="Rating: 5 stars">
```

## Lists

### Unordered Lists

```html
<!-- Bullet points -->
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>

<!-- Different bullet styles -->
<ul style="list-style-type: disc;">    <!-- • (default) -->
<ul style="list-style-type: circle;">  <!-- ○ -->
<ul style="list-style-type: square;">  <!-- ■ -->
<ul style="list-style-type: none;">    <!-- No bullet -->
```

### Ordered Lists

```html
<!-- Numbered list -->
<ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ol>

<!-- Different numbering -->
<ol type="1">       <!-- 1, 2, 3... (default) -->
<ol type="A">       <!-- A, B, C... -->
<ol type="a">       <!-- a, b, c... -->
<ol type="I">       <!-- I, II, III... -->
<ol type="i">       <!-- i, ii, iii... -->

<!-- Reverse order -->
<ol reversed>
    <li>Last item</li>
    <li>Second-to-last item</li>
</ol>
```

## Tables

### Basic Table Structure

```html
<table>
    <thead>
        <tr>
            <th>Header 1</th>
            <th>Header 2</th>
            <th>Header 3</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Data 1</td>
            <td>Data 2</td>
            <td>Data 3</td>
        </tr>
        <tr>
            <td>Data 4</td>
            <td>Data 5</td>
            <td>Data 6</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>Footer 1</td>
            <td>Footer 2</td>
            <td>Footer 3</td>
        </tr>
    </tfoot>
</table>
```

### Table Elements Explained

- `<table>` — Container
- `<thead>` — Table header (semantic)
- `<tbody>` — Table body (semantic)
- `<tfoot>` — Table footer (semantic)
- `<tr>` — Table row
- `<th>` — Header cell
- `<td>` — Data cell

### Table Attributes

1. **border** — Visible borders
2. **colspan** (Column Span) — Use when you want a single cell to stretch sideways over two or more columns.
3. **rowspan** (Row Span) — Use when you want a single cell to stretch downwards over two or more rows.

```html
<table border="1">
    <tr>
        <th colspan="2">Merged Header</th>
    </tr>
    <tr>
        <td>Cell 1</td>
        <td>Cell 2</td>
    </tr>
    <tr>
        <td rowspan="2">Merged Cell</td>
        <td>Cell 3</td>
    </tr>
    <tr>
        <td>Cell 4</td>
    </tr>
</table>
```

## Forms

### Form Structure

```html
<form action="submit.php" method="POST">
    <!-- Form fields here -->
    <button type="submit">Submit</button>
</form>
```

### Form Attributes

**action** — Where to send data
```html
<form action="process.php">
```

**method** — How to send (GET or POST)
```html
<form method="POST">      <!-- Secure, hidden data -->
<form method="GET">       <!-- Visible in URL -->
```

**name** — Form identifier
```html
<form name="contactForm">
```

### Input Types (Text Input)

```html
<input type="text" name="username" placeholder="Enter username">
<input type="password" name="password" placeholder="Enter password">
<input type="email" name="email" placeholder="Enter email">
<input type="url" name="website" placeholder="Enter URL">
<input type="number" name="age" min="0" max="120">
<input type="range" name="volume" min="0" max="100">
<input type="date" name="birthday">
<input type="time" name="event-time">
<input type="search" name="search" placeholder="Search...">
<input type="tel" name="phone" placeholder="Phone number">
```

### Buttons and Checkboxes

```html
<!-- Radio buttons (single choice) -->
<label>
    <input type="radio" name="gender" value="male"> Male
</label>
<label>
    <input type="radio" name="gender" value="female"> Female
</label>

<!-- Checkboxes (multiple choice) -->
<label>
    <input type="checkbox" name="interests" value="sports"> Sports
</label>
<label>
    <input type="checkbox" name="interests" value="music"> Music
</label>
<label>
    <input type="checkbox" name="interests" value="reading"> Reading
</label>

<!-- Submit button -->
<button type="submit">Submit</button>

<!-- Reset button -->
<button type="reset">Reset</button>

<!-- Regular button -->
<button type="button">Click Me</button>

<!-- Hidden input -->
<input type="hidden" name="userId" value="12345">
```

### Form Elements

**`<label>`** — Associate with input

```html
<!-- Using 'for' attribute -->
<label for="username">Username:</label>
<input id="username" type="text" name="username">
```

**`<textarea>`** — Multi-line text

```html
<textarea name="message" rows="4" cols="50" placeholder="Enter your message">
</textarea>
```

**`<select>` and `<option>`** — Dropdown list

```html
<label for="country">Country:</label>
<select id="country" name="country">
    <option value="">-- Select --</option>
    <option value="usa">United States</option>
    <option value="uk">United Kingdom</option>
    <option value="canada">Canada</option>
</select>

<!-- Multiple selection -->
<select name="languages" multiple>
    <option value="html">HTML</option>
    <option value="css">CSS</option>
    <option value="js">JavaScript</option>
</select>
```

### Input Attributes

**required** — Must be filled
```html
<input type="text" name="username" required>
```

**disabled** — Cannot be used
```html
<input type="text" name="username" disabled>
```

**readonly** — Cannot be edited
```html
<input type="text" name="username" readonly value="John">
```

**placeholder** — Hint text
```html
<input type="email" placeholder="example@email.com">
```

**value** — Default value
```html
<input type="text" name="username" value="default">
```

**minlength and maxlength** — Text length
```html
<input type="text" name="username" minlength="3" maxlength="20">
```

**min and max** — Number range
```html
<input type="number" name="age" min="18" max="120">
<input type="range" name="volume" min="0" max="100">
```

**pattern** — Validation pattern
```html
<!-- Only numbers -->
<input type="text" name="phone" pattern="[0-9]{10}">

<!-- Email pattern -->
<input type="email" name="email" pattern="[a-z0-9._%+\-]+@[a-z0-9.\-]+\.[a-z]{2,}$">
```

**step** — Input increments
```html
<input type="number" name="quantity" step="5" min="0">
```

**autocomplete** — Autocomplete attribute
```html
<input type="text" name="name" autocomplete="name">
<input type="email" name="email" autocomplete="email">
<input type="text" name="address" autocomplete="street-address">
```

### Form Accessibility

```html
<!-- Proper labels -->
<label for="email">Email:</label>
<input id="email" type="email" name="email">

<!-- Required indication -->
<label for="name">Name <span aria-label="required">*</span>:</label>
<input id="name" type="text" required>

<!-- Error messages -->
<input id="age" type="number" aria-describedby="age-error">
<span id="age-error" role="alert">Age must be 18+</span>
```

## Semantic Elements

**`<header>`** — Header section
```html
<header>
    <h1>Website Title</h1>
    <p>Website tagline</p>
</header>
```

**`<nav>`** — Navigation
```html
<nav>
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
    </ul>
</nav>
```

**`<main>`** — Main content
```html
<main>
    <!-- Main page content -->
</main>
```

**`<article>`** — Independent content
```html
<article>
    <h2>Blog Post Title</h2>
    <p>Post content...</p>
</article>
```

**`<section>`** — Thematic grouping
```html
<section>
    <h2>Section Title</h2>
    <p>Section content...</p>
</section>
```

**`<aside>`** — Sidebar content
```html
<aside>
    <h3>Related Articles</h3>
    <ul>
        <li><a href="#">Article 1</a></li>
    </ul>
</aside>
```

**`<footer>`** — Footer section
```html
<footer>
    <p>&copy; 2024 Company Name</p>
    <p><a href="/privacy">Privacy Policy</a></p>
</footer>
```

**`<address>`** — Contact information
```html
<address>
    name<br>
    123 Main St<br>
    Rajkot<br>
    <a href="mailto:name@example.com">name@example.com</a>
</address>
```

## Multimedia

### Audio

```html
<!-- Basic audio -->
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    Your browser doesn't support audio.
</audio>

<!-- With multiple formats -->
<audio controls>
    <source src="audio.webm" type="audio/webm">
    <source src="audio.mp3" type="audio/mpeg">
    Your browser doesn't support audio.
</audio>

<!-- Attributes -->
<audio controls autoplay loop muted>
    <source src="audio.mp3" type="audio/mpeg">
</audio>

<!-- With dimensions -->
<audio controls width="300">
    <source src="audio.mp3" type="audio/mpeg">
</audio>
```

**Audio Attributes:**
- `controls` — Show player controls
- `autoplay` — Start playing automatically
- `loop` — Repeat when finished
- `muted` — Muted by default
- `preload` — `none`, `metadata`, or `auto`

### Video

```html
<!-- Basic video -->
<video controls>
    <source src="video.mp4" type="video/mp4">
    Your browser doesn't support video.
</video>

<!-- With multiple formats -->
<video controls width="640" height="360">
    <source src="video.webm" type="video/webm">
    <source src="video.mp4" type="video/mp4">
    Your browser doesn't support video.
</video>

<!-- Attributes -->
<video controls autoplay loop muted width="640" height="360" poster="poster.jpg">
    <source src="video.mp4" type="video/mp4">
</video>

<!-- With subtitles -->
<video controls>
    <source src="video.mp4" type="video/mp4">
    <track src="subtitles.vtt" kind="subtitles" srclang="en" label="English">
    <track src="subtitles-es.vtt" kind="subtitles" srclang="es" label="Spanish">
</video>
```

**Video Attributes:**
- `controls` — Show player controls
- `width`, `height` — Video dimensions
- `poster` — Image shown before playing
- `autoplay` — Start playing automatically
- `loop` — Repeat when finished
- `muted` — Muted by default
- `preload` — `none`, `metadata`, or `auto`

### SVG (Scalable Vector Graphics)

```html
<!-- Inline SVG -->
<svg width="200" height="200" xmlns="http://www.w3.org/2000/svg">
    <!-- Circle -->
    <circle cx="100" cy="100" r="50" fill="red"/>
    
    <!-- Rectangle -->
    <rect x="20" y="20" width="160" height="50" fill="blue"/>
    
    <!-- Line -->
    <line x1="0" y1="0" x2="200" y2="200" stroke="black" stroke-width="2"/>
    
    <!-- Polygon -->
    <polygon points="100,10 40,198 190,78" fill="green"/>
    
    <!-- Text -->
    <text x="50" y="100" font-size="20" fill="white">SVG Text</text>
</svg>
```

## Complete Website Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Professional web design services">
    <meta name="keywords" content="web design, development, responsive">
    
    <title>Web Design Studio - Your Website Here</title>
    
    <link rel="icon" href="favicon.ico">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <h1>Web Design Studio</h1>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Main Content -->
    <main>
        <!-- Hero Section -->
        <section id="home" class="hero">
            <div class="container">
                <h1>Welcome to Our Studio</h1>
                <p>Creating beautiful, responsive websites</p>
                <a href="#contact" class="button">Get Started</a>
            </div>
        </section>

        <!-- Services Section -->
        <section id="services" class="services">
            <div class="container">
                <h2>Our Services</h2>
                
                <div class="service-grid">
                    <article class="service">
                        <h3>Web Design</h3>
                        <p>Beautiful, modern website designs</p>
                    </article>
                    
                    <article class="service">
                        <h3>Development</h3>
                        <p>Fast, secure web applications</p>
                    </article>
                    
                    <article class="service">
                        <h3>Responsive</h3>
                        <p>Mobile-first approach to design</p>
                    </article>
                </div>
            </div>
        </section>

        <!-- Portfolio Section -->
        <section id="portfolio" class="portfolio">
            <div class="container">
                <h2>Our Work</h2>
                
                <div class="portfolio-grid">
                    <figure>
                        <img src="project1.jpg" alt="Project 1">
                        <figcaption>Project 1</figcaption>
                    </figure>
                    
                    <figure>
                        <img src="project2.jpg" alt="Project 2">
                        <figcaption>Project 2</figcaption>
                    </figure>
                    
                    <figure>
                        <img src="project3.jpg" alt="Project 3">
                        <figcaption>Project 3</figcaption>
                    </figure>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="contact">
            <div class="container">
                <h2>Contact Us</h2>
                
                <form action="submit.php" method="POST">
                    <fieldset>
                        <legend>Contact Form</legend>
                        
                        <label for="name">Name:</label>
                        <input id="name" type="text" name="name" required>
                        
                        <label for="email">Email:</label>
                        <input id="email" type="email" name="email" required>
                        
                        <label for="message">Message:</label>
                        <textarea id="message" name="message" rows="5" required></textarea>
                        
                        <button type="submit">Send Message</button>
                    </fieldset>
                </form>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2024 Web Design Studio. All rights reserved.</p>
            <address>
                <p>Email: <a href="mailto:info@example.com">info@example.com</a></p>
                <p>Phone: <a href="tel:+1234567890">+1 (234) 567-8900</a></p>
            </address>
        </div>
    </footer>

    <script src="script.js"></script>
</body>
</html>
```
# <center>Thank you!</center>
#### <p align = 'right'>- Prit Khanpara</p>