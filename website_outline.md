# Prompt: Static Website for **Unmanned Systems Engineering**

You are a front-end developer.  
Generate a modern, responsive **static website** with **three files**:

1. `index.html`
2. `styles.css`
3. `script.js`

The site is for a UAV-focused organisation called **Unmanned Systems Engineering** that works on advanced drone / unmanned systems projects (e.g. logistics UAVs, surveillance UAVs, hobby FPV kits).

---

## Overall Design Requirements

- Clean, modern, engineering/tech aesthetic.
- Color palette:
  - Dark navy / charcoal background
  - White / light gray for text areas
  - Accent color: cyan / electric blue for buttons, highlights.
- Typography:
  - Use a Google Font (e.g. `Poppins` or `Inter`) for all text.
  - Clear hierarchy: bold headings, readable body text.
- Layout:
  - Responsive design (desktop, tablet, mobile).
  - Max-width container with centered content on large screens.
  - Use CSS Flexbox / Grid appropriately.
- Effects:
  - Smooth scrolling to sections.
  - Subtle hover effects on buttons and cards.
  - Simple fade-in animation on scroll for key sections (implemented via `script.js`).

---

## 1. `index.html`

Create a semantic HTML5 page with the following structure:

### 1.1 Document Setup

- `<!DOCTYPE html>`, `<html lang="en">`
- `<head>`:
  - Proper `<meta charset="UTF-8">`
  - Responsive `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
  - `<title>Unmanned Systems Engineering</title>`
  - Link `styles.css`
  - Link Google Fonts (e.g. Poppins)
  - Include basic SEO meta description about UAV / unmanned systems engineering.
- `<body>`:
  - Wrap main content inside `<div class="page-wrapper">`.

### 1.2 Header & Navigation

- Fixed or sticky top navigation bar.
- Contents:
  - Left: Simple text logo: **Unmanned Systems Engineering**.
  - Right: Navigation links that scroll to sections:
    - Home
    - About
    - Platforms
    - Ecosystem
    - Roadmap
    - Team
    - Contact
- For mobile:
  - A hamburger menu icon that toggles a slide-down nav via `script.js`.

### 1.3 Hero Section (`id="home"`)

- Full-width hero near the top.
- Left side (text):
  - Main headline:  
    **Building the Future of Unmanned Systems**
  - Subheadline describing the mission (e.g. UAV design, logistics drones, persistent surveillance, hobby FPV).
  - Two CTA buttons:
    - **View Platforms** (scroll to Platforms section)
    - **Contact Us**
- Right side (optional):
  - Abstract illustration placeholder (e.g. simple SVG shape or UAV silhouette using CSS).

### 1.4 About Section (`id="about"`)

- Title: **About Unmanned Systems Engineering**
- Short paragraphs describing:
  - Focus on engineering design, composite structures, autonomous systems.
  - Mission: developing sovereign UAV capabilities and nurturing talent.
- Use a two-column layout on desktop (text + small info list or stats).
- Include a small “Key Focus Areas” list (bulleted):
  - Long-range logistics UAVs
  - 24/7 surveillance VTOL systems
  - Hobby FPV & education kits
  - Research & industry collaboration

### 1.5 Platforms Section (`id="platforms"`)

- Title: **Core Platforms**
- Subtitle: brief line like “From heavy-lift logistics to 24/7 surveillance and hobby FPV.”
- Display **three cards** in a responsive grid:

  1. **BADANG – Logistics UAV**
     - Short description (10 kg payload, long-range logistics, island/offshore use).
     - Bullet points for key specs (range, payload, VTOL, use cases).

  2. **MAHSURI – Surveillance VTOL**
     - Short description (24/7 automated surveillance, battery swap base, industrial and border monitoring).
     - Bullet points for endurance, automation, typical missions.

  3. **Hobby FPV & Education**
     - Short description (3D-printed FPV wings, modular Li-ion packs, learning platform).
     - Bullet points: KIT/RTF options, workshops, learning outcomes.

- Each card:
  - Has icon or simple graphic placeholder (e.g. a circle with letters).
  - Shows a “Learn more” button that scrolls to Ecosystem section or opens no link (static placeholder).

### 1.6 Ecosystem Section (`id="ecosystem"`)

- Title: **Unmanned Systems Ecosystem**
- Brief description of how the three segments connect (R&D, services, hobby community).
- Use a **3-column info layout** (stacked on mobile):

  - **R&D & Innovation**
    - Text about advanced engineering, composites, autonomy, flight testing.

  - **Commercial Operations**
    - Text about UAV-as-a-service, logistics, inspection, surveillance contracts.

  - **Community & Education**
    - Text about workshops, student clubs, maker community and FPV kits.

- Optionally include a simple horizontal infographic-style layout showing flow:
  - Hobby → Talent → R&D Platforms → Commercial Services.

### 1.7 Roadmap Section (`id="roadmap"`)

- Title: **Roadmap**
- Use a vertical timeline layout (can be simple cards stacked vertically) showing phases:

  - **Phase 1 – Foundation**
    - Partnered operations, early pilots, platform prototyping.

  - **Phase 2 – Certification & Scaling**
    - Regulatory approvals, system reliability, initial commercial contracts.

  - **Phase 3 – Ecosystem Expansion**
    - Export to ASEAN, more platforms, larger community and education programs.

- Each phase is a card with:
  - Small heading
  - 2–3 bullet points
  - A subtle left border or icon to indicate timeline.

### 1.8 Team Section (`id="team"`)

- Title: **Our Team**
- Short intro text (multidisciplinary engineers, pilots, software developers).
- Show **3–4 team member cards** (static placeholders):

  - Name
  - Role (e.g. Lead Airframe Engineer, Autonomy & AI, Operations & Safety)
  - One-sentence description.

- Use simple circular avatar placeholders (e.g. letters, no real photos).

### 1.9 Contact Section (`id="contact"`)

- Title: **Get in Touch**
- Subtext: Invite collaboration with universities, industry, government.
- Include:

  - Short explanatory text.
  - A simple contact form:
    - Name (input)
    - Email (input)
    - Organization (input)
    - Message (textarea)
    - Submit button
  - Below the form, static contact info:
    - Placeholder email: `info@unmannedsystems.engineering`
    - Placeholder location: `Kuala Lumpur, Malaysia`

- The form does not need real back-end; just HTML structure and JS to show a “Thank you” message on submit.

### 1.10 Footer

- Simple footer with:
  - © Current year and “Unmanned Systems Engineering”
  - Small text links: “Privacy”, “Terms” (non-functional).
  - Optional: “Made with ❤️ by the Unmanned Systems Club” text.

---

## 2. `styles.css`

Implement the following styling:

### 2.1 Base Styles

- Set global box-sizing to `border-box`.
- Set body background color to dark navy/charcoal and text color to light gray.
- Apply the chosen Google Font to `body`.
- Define utility classes:
  - `.container` with max-width (e.g. 1200px) and horizontal padding.
  - `.btn` for buttons (primary style and outline/secondary if needed).
  - `.section` for vertical spacing between sections.

### 2.2 Header & Navigation

- Create a fixed or sticky header with:
  - Slight background blur or solid dark background.
  - Box-shadow for separation from content.
- Navigation links:
  - Inline on desktop.
  - On hover: underline or bottom border with accent color.
- Mobile:
  - Hide nav links by default, show a hamburger icon.
  - When active, show a vertical menu.

### 2.3 Hero Section

- Use a two-column layout on larger screens; stack on mobile.
- Large, bold headline; slightly smaller subheadline.
- Buttons styled with:
  - Rounded corners
  - Hover state (background change, subtle scale).

### 2.4 Sections

- Each section has:
  - Adequate padding and spacing.
  - Clear headings with consistent margins.
- Cards (`platforms`, `ecosystem`, `roadmap`, `team`):
  - Background slightly lighter than body.
  - Rounded corners, subtle shadow.
  - Hover: slight lift (transform) and shadow increase.

### 2.5 Timeline / Roadmap

- Simple vertical timeline style:
  - Left border or line.
  - Each phase card aligned with the line (dot or icon at the start).

### 2.6 Contact Form

- Styled inputs:
  - Full width on mobile.
  - Rounded corners.
  - Outline or border accent on focus.

### 2.7 Animations

- Define a `.fade-in` class with keyframe animation for opacity and slight upward motion.
- Elements that will fade in on scroll should start with `opacity: 0` and become visible with the animation.

### 2.8 Responsive Rules

- Use media queries for:
  - Nav layout changes (hamburger for small screens).
  - Converting multi-column sections to single-column on narrow screens.
  - Adjusting font sizes and paddings.

---

## 3. `script.js`

Add simple, unobtrusive JavaScript to enhance UX:

### 3.1 Mobile Navigation Toggle

- Add event listener for the hamburger icon.
- On click, toggle a CSS class on the nav menu to open/close it.

### 3.2 Smooth Scrolling

- For internal nav links (`href="#section"`), intercept click and use `scrollIntoView({ behavior: 'smooth' })` or equivalent.

### 3.3 Scroll-Based Animations

- Use `IntersectionObserver` (if available) or scroll listener to:
  - Detect when elements with `.fade-in` class enter the viewport.
  - Add an extra class (e.g. `.visible`) to trigger the CSS fade-in animation.

### 3.4 Contact Form Handling

- Prevent default form submission.
- On submit:
  - Validate that required fields are not empty.
  - Show a simple thank-you message (e.g. an alert or a
