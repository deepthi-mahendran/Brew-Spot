# The Brew Spot – Cozy Neighborhood Café Website

A fully responsive, feature-rich single-page website for "The Brew Spot" – a warm and inviting neighborhood café. This modern web application showcases the café's atmosphere, menu, gallery, and reservation system with interactive elements, dark/light mode, and offline support.

---

## Overview

**The Brew Spot** is a complete café website designed to create an immersive brand experience. It combines aesthetic design with practical functionality, allowing visitors to:

- Browse menu items organized by categories (Coffee, Tea, Pastries, Specials)
- Add items to a shopping cart and place orders
- View a gallery of café images with a lightbox preview
- Make table reservations through a validated form
- Subscribe to a newsletter
- Toggle between dark and light themes
- Experience a smooth, interactive loading animation

The site is built as a single HTML file with embedded CSS and JavaScript, making it easy to deploy and maintain.

---
## Screenshot
<img width="1912" height="917" alt="image" src="https://github.com/user-attachments/assets/8743d30e-7a75-43a0-a5ea-81096f3792cf" />


## Live Demo
https://deepthi-mahendran.github.io/Brew-Spot/

---

## Features

| Feature                    | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| **Interactive Loading**    | Animated coffee cup with rising liquid and steam, simulating a "brewing" experience |
| **Typing Hero Headline**   | Dynamic typing effect with rotating phrases ("Welcome to", "The Brew Spot", "Your cozy corner") |
| **Parallax Hero Background** | Smooth parallax scrolling effect on the hero background image              |
| **Menu Tabs**              | Four categories (Coffee, Tea, Pastries, Specials) with smooth transitions   |
| **Add to Cart**            | Each menu item has an "Add to Order" button with shake animation feedback   |
| **Shopping Cart**          | Slide-out panel with item list, total calculation, remove functionality, and order placement |
| **Gallery**                | Masonry-style image grid with lazy loading, blur-up effect, and lightbox preview |
| **Reservation Form**       | Validated form with fields for name, email, date, time, guests, and special requests |
| **Newsletter Signup**      | Footer subscription form with email validation and confirmation toast      |
| **Dark/Light Mode**        | Toggle switch with smooth transition, preference saved in localStorage     |
| **Responsive Design**      | Optimized for desktop, tablet, and mobile devices with adaptive layouts    |
| **Accessibility**          | ARIA labels, semantic HTML, keyboard navigation, and focus indicators      |
| **Offline Support**        | Service worker registration for basic offline caching (inline via blob URL) |
| **Back to Top Button**     | Fades in after scrolling, scrolls smoothly to the top                      |
| **Toast Notifications**    | Non-intrusive popup notifications for user actions (cart, reservations, newsletter) |

---

## Technology Stack

- **HTML5** – Semantic markup, ARIA attributes
- **CSS3** – Custom properties (variables), Grid/Flexbox layouts, animations, transitions
- **Vanilla JavaScript** – ES6+, DOM manipulation, Intersection Observer, localStorage
- **Google Fonts** – Playfair Display (headings) & Nunito (body)
- **Service Worker** – Inline registration for offline support
- **Unsplash** – High-quality free stock images for café visuals

**No frameworks, no build tools, no dependencies** – everything is self-contained in one file.

---

## Installation & Usage

### 1. Download the file

Save `index.html` to your local machine.

### 2. Open in a browser

Double-click the file or open it in your favorite browser (Chrome, Firefox, Edge, Safari).

### 3. Offline usage

The site includes a minimal service worker that enables basic offline caching – once loaded, you can revisit without an internet connection.

### 4. Hosting

For live deployment, simply upload the file to any static hosting service (Netlify, Vercel, GitHub Pages, etc.).

---

## Project Structure

The entire application is contained in a **single HTML file** with well-organized sections:

```
cafe.html
├── <head>
│   ├── Meta tags (viewport, charset)
│   ├── Google Fonts link
│   ├── Inline manifest (base64-encoded)
│   ├── Service worker registration script
│   └── <style> (all CSS – ~600 lines)
├── <body>
│   ├── Loading screen (animated coffee cup)
│   ├── Toast notification
│   ├── Back to top button
│   ├── Cart overlay & slide-out panel
│   ├── Lightbox
│   ├── Navbar (fixed, with theme toggle, cart, hamburger)
│   ├── Hero section (parallax, typing effect, CTA)
│   ├── About section (scroll-reveal)
│   ├── Menu section (tabs, dynamic grid, order buttons)
│   ├── Gallery section (masonry grid, lightbox)
│   ├── Contact/Reservation section (form + map iframe)
│   ├── Footer (brand, hours, newsletter, social links)
│   └── <script> (all JavaScript – ~400 lines)
└── (end)
```

---

## Key Components

### Loading Screen

- Animated coffee cup with a filling liquid (progress bar) and rising steam
- Simulates the "brewing" experience while assets load
- Auto-dismisses after a short delay

### Hero Section

- Full-viewport background image with parallax on scroll
- Typing effect that cycles through welcoming phrases
- Floating particles (coffee-themed floating circles)
- Call-to-action button linking to the menu

### Menu System

- Data-driven menu stored in a JavaScript object (`menuData`)
- Four tabs with dynamic rendering
- Each item includes: name, description, price, and image
- "Add to Order" buttons with shake feedback

### Shopping Cart

- Slide-out panel from the right
- Real-time item count badge on the cart icon
- Item list with remove buttons
- Total cost calculation
- "Place Order" button with confirmation toast

### Gallery with Lightbox

- Masonry-style grid with responsive columns
- Lazy-loaded images with blur-up effect
- Click any image to open a full-screen lightbox
- Close with ✕ button, overlay click, or Escape key

### Reservation Form

- All required fields (Name, Email, Date, Time, Guests)
- Date picker with minimum date set to today
- Email validation
- Special requests textarea
- Success message via toast notification

### Dark/Light Mode

- Toggle button in the navbar (☀️/🌙)
- CSS custom properties control all colors
- Preference saved to `localStorage` for persistence across sessions
- Smooth transitions on background and text colors

---

## Customization

You can easily adapt the website for your own café or business:

### Change Colors

Edit the CSS custom properties in the `:root` block:

```css
:root {
    --color-terracotta: #D4764A;      /* Primary accent */
    --color-brown-rich: #5C3D2E;      /* Dark text */
    --color-cream: #FDF6F0;           /* Background */
}
```

### Update Menu Items

Modify the `menuData` object in the JavaScript section:

```javascript
const menuData = {
    coffee: [
        { name: 'Your Coffee', desc: 'Description', price: 4.50, img: 'image-url.jpg' },
        // ...
    ],
    // ...
};
```

### Change Gallery Images

Replace the `galleryImages` array with your own image URLs.

### Update Map Location

Replace the `src` attribute of the iframe in the contact section with your own Google Maps embed URL.

### Modify Opening Hours

Edit the `.footer-hours ul` HTML content.

### Change Typing Phrases

Update the `phrases` array inside the `initTyping()` function.

---

## Browser Support

| Browser          | Version | Support |
|------------------|---------|---------|
| Chrome           | 60+     | ✅ Fully supported |
| Firefox          | 60+     | ✅ Fully supported |
| Safari           | 14+     | ✅ Fully supported |
| Edge             | 79+     | ✅ Fully supported |
| Opera            | 50+     | ✅ Fully supported |
| Internet Explorer| 11-     | ❌ Not supported |

The site uses modern CSS features (Grid, Custom Properties, `backdrop-filter`) and ES6 JavaScript, so it works best in modern browsers.

---

## License

This project is created to demonstrate modern front‑end web development techniques including responsive design, CSS animations, DOM manipulation, and progressive enhancement. You are free to use, modify, and distribute this code for learning and personal projects.

---

*"Where every cup tells a story."* ☕
