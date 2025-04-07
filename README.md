# Rohan R. Portfolio Website

This is a **personal portfolio website** built using **HTML, CSS**, and a bit of **JavaScript**. It showcases my academic background, technical skills, achievements, and provides a way for visitors to connect with me through a contact form.

---

## 🌐 Structure Overview

The site consists of a single HTML file with embedded CSS and JavaScript. It is designed to be responsive and visually engaging, and is broken into logical, scroll-free sections. Below is a breakdown of the code's architecture and content.

---

## 📁 File Breakdown

### 1. **HTML Layout**

The entire webpage is contained within a single HTML file (`index.html`). The core sections are:

- **`<head>`**:
  - Imports Google Fonts (`Poppins`, `Bebas Neue`) and Font Awesome icons.
  - Embeds internal CSS inside a `<style>` tag for styling.

- **`<body>`**:
  Contains the visible sections of the page, divided into:
  - **Navbar**
  - **Home**
  - **About**
  - **Skills**
  - **My Works**
  - **Contact**
  - **Footer**

---

## 🧭 Navigation Bar

```html
<nav class="navbar">
  ...
</nav>
```

- **Fixed at the top**, uses Flexbox for layout.
- Contains links to different page sections via anchor tags (`#home`, `#about`, etc.).
- Collapses into a **hamburger menu** on screens below 768px using media queries.
- JavaScript toggles the `show` class to expand/collapse the menu.

---

## 🏠 Home Section

```html
<section class="section home" id="home">
  ...
</section>
```

- Features a split layout:
  - Left: Name and degree
  - Right: Profile image
- Uses **keyframe animations** (`fadeIn`, `slideInLeft`) to create entrance effects.
- Designed to be visually appealing and serve as a landing panel.

---

## 👤 About Section

```html
<section class="section" id="about">
  ...
</section>
```

- Describes educational journey and certifications.
- Uses basic paragraph tags with some line spacing for readability.

---

## 🧠 Skills Section

```html
<section class="section" id="skills">
  ...
</section>
```

- Organized in a **flexbox container**.
- Each `skill-box` highlights a skill/certification.
- Includes hover animations (e.g., color change, background glow).

---

## 🛠️ My Works Section

```html
<section class="section" id="myworks">
  ...
</section>
```

- Uses a **grid layout** to showcase:
  - Programming
  - Math foundations
  - Physics and engineering basics
- Includes a **"Download Resume"** button linking to an external PDF.

---

## 📬 Contact Section

```html
<section class="section" id="contact">
  ...
</section>
```

- Features a **contact form** with:
  - Name
  - Email
  - Message
- Includes input validation via the `required` attribute.
- Submits data using **Google Apps Script** to a connected Google Sheet.
- Success message is shown and then cleared using a timeout function.

---

## 🌐 Social Media Icons

```html
<div class="social-icons">
  ...
</div>
```

- Uses Font Awesome icons for GitHub, LinkedIn, Email, and Instagram.
- Icons change color on hover to match the primary theme (`#ff004f`).

---

## 🖼️ Background Design

```css
body::before {
  background-image: url('back.jpg');
}
```

- The background is rendered using a `::before` pseudo-element.
- This keeps the design consistent and ensures it doesn’t interfere with content flow.
- Different backgrounds for the home page vs. other pages using conditional `body.home-page` class.

---

## 🧾 Footer

```html
<div class="copyright">
  Copyright © Rohan R. Made with Visual Studio Code
</div>
```

- Fixed at the bottom of the viewport.
- Background in dark grey (`#333`) and a height less than 30px as per design preferences.

---

## 🧠 JavaScript Functions

There are two small JS scripts:

1. **Navigation Toggle** (for mobile):
   ```js
   function toggleMenu() {
     const nav = document.getElementById('navLinks');
     nav.classList.toggle('show');
   }
   ```

2. **Form Submission** (Google Apps Script integration):
   ```js
   form.addEventListener('submit', e => {
     e.preventDefault();
     fetch(scriptURL, { method: 'POST', body: new FormData(form)})
     ...
   });
   ```

   - Prevents default form submission
   - Sends data to Google Sheets
   - Displays a success message for 5 seconds

---

## 🎨 CSS Design Highlights

- **Primary color**: `#ff004f` (used for navbar, buttons, borders)
- **Background**: Light and medium grey, with image overlay at 30% opacity
- **Typography**:
  - `Bebas Neue` for headings
  - `Poppins` for body text
- **Responsive design**: Optimized for both desktop and mobile using media queries

---

## 🚀 Hosting Suggestions

To host this portfolio:
- Upload to GitHub Pages, Netlify, or Vercel
- Ensure `Resume.pdf`, `back.jpg`, `homebackground.jpg`, and `profile.jpg` are in the correct path
- Link Google Apps Script correctly for form submissions

---

## 📌 Conclusion

This code represents a clean, responsive, and animated portfolio for showcasing academic and technical achievements. It reflects a keen eye for design and a foundational understanding of front-end development. Feel free to fork and modify for your own portfolio use.