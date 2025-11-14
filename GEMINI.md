# Project Overview

This project is a modern, responsive static website for "Unmanned Systems Engineering," a fictional organization focused on UAV technology. The website showcases the company's services, platforms, and team.

**Technologies Used:**

*   **HTML5:** For the structure and content of the website.
*   **CSS3:** For styling, layout, and responsive design. It utilizes modern features like Flexbox, Grid, and custom properties.
*   **JavaScript (ES6):** For interactive features such as a mobile navigation menu, smooth scrolling, scroll-based animations, and a mock contact form.
*   **Google Fonts:** The "Poppins" font is used for typography.

**Architecture:**

The project follows a simple and clean architecture with three main files:

*   `index.html`: The single HTML file containing the entire website's content, structured semantically with sections for Home, About, Platforms, etc.
*   `styles.css`: A single CSS file that styles the entire website. It is well-organized with base styles, utility classes, and component-specific styles.
*   `script.js`: A single JavaScript file that adds interactivity to the website.

# Building and Running

This is a static website, so there is no build process required. To run the website, simply open the `index.html` file in a web browser.

For a better development experience, you can use a local web server with live reload capabilities. For example, you can use the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension for Visual Studio Code.

# Development Conventions

*   **Code Style:** The code is well-formatted and follows standard conventions for HTML, CSS, and JavaScript.
*   **CSS:** The CSS uses a BEM-like naming convention for some classes (e.g., `hero-content`, `hero-text`). It also makes good use of CSS custom properties for theming.
*   **JavaScript:** The JavaScript code is clean, modern, and uses event listeners to add behavior to the page. It is wrapped in a `DOMContentLoaded` event listener to ensure the DOM is fully loaded before the script runs.
*   **Animations:** Simple fade-in animations are implemented using CSS transitions and are triggered by JavaScript using the Intersection Observer API for better performance.
*   **Responsive Design:** The website is designed to be responsive and work on different screen sizes, from mobile to desktop. Media queries are used to adjust the layout and styling accordingly.
