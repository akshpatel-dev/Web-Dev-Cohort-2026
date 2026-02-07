# 🖥️ Cursor Website Clone

A  recreation of the [Cursor](https://cursor.com) landing page built with **pure HTML & CSS**. This project demonstrates modern web development techniques, responsive design principles, and attention to detail in recreating a premium tech product's marketing page.

Demo Link [Click here](https://cursor-clone-akshpatel.vercel.app/)

Note: This website is deploy on vercel. if the click here is not working then go with this link: https://cursor-clone-akshpatel.vercel.app/



# Clone vs Actual 


<img width="1920" height="1080" alt="ss1" src="https://github.com/user-attachments/assets/771f5034-efd9-4eee-ae25-c9310e4546fe" />


 For Hole Website Screenshort: [Click Here](Cursor-Website-Clone/Assets/images/Cursor.png).


---

## 📖 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [How I Built This - Step by Step](#-how-i-built-this---step-by-step)
- [Getting Started](#-getting-started)
- [Key Learnings](#-key-learnings)

---

## 🎯 Overview

This project is a frontend clone of the Cursor AI code editor's landing page. The goal was to practice and demonstrate skills in:

- Semantic HTML5 structure
- Modern CSS techniques (CSS Variables, Flexbox, Grid)
- Custom font implementation
- Responsive design patterns
- UI/UX attention to detail

---

## ✨ Features

| Section                | Description                                               |
| ---------------------- | --------------------------------------------------------- |
| **Navigation Bar**     | Sticky navigation with logo, menu links, and CTA buttons  |
| **Hero Section**       | Eye-catching headline with download button and hero image |
| **Trusted By Section** | Company logos carousel showing social proof               |
| **Agent Features**     | Three feature highlight cards with alternating layouts    |
| **Testimonials**       | Grid of user testimonials from industry leaders           |
| **Frontier Section**   | Three-column feature cards with images                    |
| **Changelog**          | Recent updates displayed in card format                   |
| **Team Section**       | Company mission statement with team image                 |
| **Recent Highlights**  | Blog post previews in a two-column layout                 |
| **Download CTA**       | Final call-to-action section                              |
| **Footer**             | Multi-column footer with links and theme switcher         |

---

## 🛠️ Tech Stack

| Technology        | Purpose                             |
| ----------------- | ----------------------------------- |
| **HTML5**         | Semantic structure and content      |
| **CSS3**          | Styling, layouts, and animations    |
| **CSS Variables** | Theming and consistent color scheme |
| **CSS Flexbox**   | Component-level layouts             |
| **CSS Grid**      | Page-level grid layouts             |
| **Custom Fonts**  | CursorGothic brand typography       |

---

## 📂 Project Structure

```
Cursor Website Clone/
├── index.html          # Main HTML file (473 lines)
├── style.css           # All styles (612 lines)
├── README.md           # Project documentation
└── Assets/
    ├── fonts/          # Custom CursorGothic font files (32 files)
    │   └── CursorGothic_Regular-s.p.a361088d.woff2
    └── images/         # All images and SVGs (27 files)
        ├── brand_logo.png
        ├── logo.png
        ├── Hero.png
        ├── agent.png
        ├── magically_section.png
        ├── everywhere.png
        ├── author-1.webp ... author-6.webp
        ├── frontier-first.png
        ├── frontier-second.png
        ├── frontier-third.webp
        ├── hero3.webp
        └── asset-*.svg (company logos)
```


## 🚀 How I Built This - Step by Step

### Step 1: Project Setup & Analysis

**What I did:**

1. Created the project folder structure
2. Analyzed the original Cursor website to understand the layout
3. Identified all the sections and components needed
4. Downloaded/extracted necessary assets (images, fonts, logos)

**Files created:**

- `index.html` - Main HTML structure
- `style.css` - Stylesheet
- `Assets/fonts/` - Custom fonts
- `Assets/images/` - All visual assets

---

### Step 2: CSS Foundation & Variables

**What I did:**

1. Set up CSS reset (`* { margin: 0; padding: 0; box-sizing: border-box; }`)
2. Imported the custom CursorGothic font using `@font-face`
3. Created CSS variables for consistent theming

```css
:root {
  --bg-color: #13120b; /* Dark brown/black background */
  --secondary-bg-color: #1b1913; /* Slightly lighter for cards */
  --font-color: #ffff; /* White text */
  --secondary-font-color: #f54e00; /* Orange accent color */
  --font-primary: "CursorGothic"; /* Brand font */
  --border-default: 0.5px solid gray;
}
```

**Key decisions:**

- Used CSS variables for easy theme management
- Dark color scheme to match Cursor's branding
- Orange accent color for CTAs and links

---

### Step 3: Navigation Bar

**What I did:**

1. Created a sticky `<nav>` element
2. Split navigation into three parts: logo, center links, right CTAs
3. Used Flexbox for horizontal alignment

**HTML Structure:**

```html
<nav>
  <div class="nav-container">
    <div class="logo">...</div>
    <div class="center-anchor">...</div>
    <div class="right-anchor">...</div>
  </div>
</nav>
```

**CSS Techniques:**

- `position: sticky` for fixed navigation on scroll
- `display: flex; justify-content: space-between;` for layout
- Hover effects on links and buttons
- Rounded pill-shaped CTA buttons

---

### Step 4: Hero Section

**What I did:**

1. Created the main headline with two `<h1>` tags
2. Added a download button with an inline SVG icon
3. Included the hero image

**Key styling:**

```css
.hero-section {
  margin-top: 15vh;
  font-size: 14px;
  letter-spacing: 0.0125;
}

.download button {
  padding: 11px 22px;
  border-radius: 30px;
  background-color: var(--font-color);
  color: var(--bg-color);
}
```

**Techniques used:**

- SVG icon embedded inline for the download icon
- CSS transitions for hover effects
- Responsive spacing with `vh` units

---

### Step 5: Trusted By Section (Social Proof)

**What I did:**

1. Added a centered text paragraph
2. Created a horizontal row of company logo boxes
3. Each box contains an SVG logo image

**CSS Layout:**

```css
.trusted-container {
  display: flex;
  align-items: center;
  gap: 10px;
}

.box {
  width: 160px;
  height: 100px;
  background-color: var(--secondary-bg-color);
  border-radius: 7px;
}
```

---

### Step 6: Agent Features Section

**What I did:**

1. Created three feature blocks with image + text
2. Used a `.reverse` class to alternate layouts
3. Each block contains a heading, description, and "Learn more" link

**HTML Pattern:**

```html
<div class="agent-container common">
  <div class="agent-text">...</div>
  <div class="agent-image">...</div>
</div>

<div class="agent-container common reverse">
  <!-- Same structure, reversed order -->
</div>
```

**Key CSS:**

```css
.agent-container {
  height: 90vh;
  display: flex;
  justify-content: space-between;
}

.agent-container.reverse {
  flex-direction: row-reverse;
}
```

---

### Step 7: Testimonials Grid

**What I did:**

1. Created a grid of testimonial cards
2. Each card has a quote and author info (image + name + title)
3. Used CSS Flexbox for card layout

**Card structure:**

```html
<div class="testimonial-box">
  <p class="details">Quote text...</p>
  <div class="testimonial-author">
    <img src="..." alt="..." />
    <div class="author-info">
      <p>Name</p>
      <p>Title</p>
    </div>
  </div>
</div>
```

**Layout approach:**

- `display: flex; flex-wrap: wrap;` for responsive grid
- Fixed card dimensions (`430px × 280px`)
- `justify-content: space-between` to distribute content

---

### Step 8: Frontier Features Section

**What I did:**

1. Created three equal-width feature cards
2. Each card has a title, description, link, and image
3. Used percentage-based widths for responsive layout

**CSS Grid:**

```css
.frontier-box {
  width: 32.8%; /* ~1/3 of container */
  display: flex;
  flex-direction: column;
}
```

---

### Step 9: Changelog Section

**What I did:**

1. Created four changelog entry cards
2. Each shows version number, date, and update description
3. Added a "See what's new" link at the bottom

**Card structure:**

```html
<div class="changelog-box">
  <div class="changelog-info">
    <span class="changelog-rating">2.4</span>
    <p>Jan 22, 2026</p>
  </div>
  <div class="changelog-content">
    <p>Update description...</p>
  </div>
</div>
```

---

### Step 10: Team/Company Section

**What I did:**

1. Added a mission statement with "Join us" CTA
2. Included a full-width team image

**CSS:**

```css
.hero-3 {
  margin-top: 15vh;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.hero-3 img {
  width: 100%;
  border-radius: 5px;
}
```

---

### Step 11: Recent Highlights (Blog Section)

**What I did:**

1. Created a full-width section with CSS Grid
2. Two-column layout: title on left, posts on right
3. Used the "breakout" technique to span full viewport width

**Full-width technique:**

```css
.highlights-container {
  width: 100vw;
  position: relative;
  left: 50%;
  margin-left: -50vw;
}
```

---

### Step 12: Footer

**What I did:**

1. Created a 5-column grid for links
2. Added bottom bar with copyright, SOC 2 badge, and theme switcher
3. Implemented theme toggle buttons (non-functional, UI only)

**CSS Grid:**

```css
.footer-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 2rem;
}
```

---

### Step 13: Polish & Refinements

**Final touches:**

1. Added hover effects to all interactive elements
2. Fine-tuned spacing and margins for visual balance
3. Ensured consistent use of CSS variables throughout
4. Added smooth transitions (`transition: 0.2s ease`)

---

## 🏃 Getting Started

### Prerequisites

- Any modern web browser (Chrome, Firefox, Safari, Edge)
- A code editor (VS Code, Cursor, etc.) for viewing/editing

### Installation

1. **Clone or download this repository**

   ```bash
   git clone https://github.com/akshpatel-dev/Web-Dev-cohort-26.git
   ```

2. **Navigate to the project folder**

   ```bash
   cd Cursor Website Clone
   ```

3. **Open in browser**
   - Simply double-click `index.html`, or
   - Use a local server (Live Server extension in VS Code)

---

## 📚 Key Learnings

### 1. CSS Variables for Theming

Using `:root` variables made it easy to maintain a consistent color scheme and would make adding a light theme straightforward.

### 2. Flexbox vs Grid

- **Flexbox**: Used for navigation, cards, and component-level layouts
- **Grid**: Used for footer columns and the blog section

### 3. Full-Width Sections

The "breakout" technique (`width: 100vw; margin-left: -50vw;`) allowed sections to span the full viewport while the parent has padding.

### 4. Custom Fonts

Using `@font-face` with `.woff2` files ensured the brand typography was consistent with the original.

### 5. Semantic HTML

Used appropriate tags (`<nav>`, `<main>`, `<section>`, `<footer>`, `<article>`) for accessibility and SEO.

---


