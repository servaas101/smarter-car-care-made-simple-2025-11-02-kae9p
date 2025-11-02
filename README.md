# AutoMind Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain, customize, and improve your AutoMind landing page. Whether you're a complete beginner or have some HTML/CSS experience, you'll find detailed instructions for every common task.

---

## Table of Contents

1. [Quick Start Overview](#quick-start-overview)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
7. [Common Customizations](#common-customizations)
8. [Troubleshooting Guide](#troubleshooting-guide)
9. [Best Practices](#best-practices)

---

## Quick Start Overview

### What This Landing Page Contains

Your AutoMind landing page (`index.html`) is a modern, responsive website built with:

- **Tailwind CSS** - A utility-first CSS framework (no separate CSS files needed)
- **Font Awesome Icons** - For visual icons throughout the page
- **Vanilla JavaScript** - For interactive features like mobile menu and FAQ accordion
- **Responsive Design** - Works on phones, tablets, and desktop computers

### File Structure You'll Need

```
your-project-folder/
├── index.html (your main landing page)
├── privacy.html (create this for privacy policy)
├── terms.html (create this for terms of service)
└── blog.html (create this for blog page)
```

### Key Colors Used in Your Design

- **Primary Purple**: `#667eea` (used in gradients)
- **Secondary Pink**: `#764ba2` and `#a855f7` (used in gradients)
- **Text Gray**: `#111827` (dark gray for body text)
- **Light Gray**: `#f3f4f6` (for backgrounds)

---

## Understanding the Page Structure

### Main Sections Breakdown

Your landing page is organized into these main sections:

```
1. HEADER/NAVIGATION (sticky at top)
   ├── Logo and brand name
   ├── Desktop navigation menu
   └── Mobile menu (hidden on small screens)

2. HERO SECTION (large banner with main message)
   ├── Headline and subheadline
   ├── Call-to-action buttons
   └── Decorative mobile phone mockup

3. FEATURES SECTION (3 feature cards)
   ├── Smart Diagnostics
   ├── Live Alerts
   └── Auto Insights

4. BENEFITS SECTION (3 benefit cards)
   ├── Save Money
   ├── Prevent Issues
   └── Stay Informed

5. CTA SECTION (call-to-action with background image)

6. ABOUT US SECTION (company information)

7. TESTIMONIALS SECTION (4 customer reviews)

8. FAQ SECTION (5 frequently asked questions)

9. FINAL CTA SECTION (last call-to-action)

10. FOOTER (links, contact info, social media)
```

### How to Find Specific Sections

Each major section in your HTML starts with an HTML comment and an ID:

```html
<!-- Features Section -->
<section id="features" class="py-24 bg-gray-50">
```

**To find a section quickly:**
1. Open `index.html` in your text editor
2. Press `Ctrl+F` (Windows) or `Cmd+F` (Mac)
3. Type the section name (e.g., "Features Section")
4. Press Enter to jump to that location

---

## Updating Text Content

This section shows you exactly where and how to change text on your landing page.

### Hero Section Text (Main Headline)

**Location:** Near the top of the file, inside the `<section class="hero-gradient">` tag

**Current text:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-6">
    Smarter Car Care Made Simple
</h1>
```

**How to change it:**

1. Open `index.html` in any text editor (Notepad, VS Code, Sublime Text, etc.)
2. Find the line containing `Smarter Car Care Made Simple`
3. Replace the text between `>` and `</h1>` with your new headline
4. Save the file (Ctrl+S or Cmd+S)

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-6">
    Your New Headline Here
</h1>
```

**Important:** Keep the HTML tags (`<h1>` and `</h1>`) exactly as they are. Only change the text between them.

---

### Hero Section Subheadline

**Current text:**
```html
<p class="text-xl md:text-2xl text-purple-100 mb-8 leading-relaxed font-light">
    Drive smarter, safer, stress-free
</p>
```

**How to change it:**
Replace `Drive smarter, safer, stress-free` with your new subheadline.

**Example:**
```html
<p class="text-xl md:text-2xl text-purple-100 mb-8 leading-relaxed font-light">
    Your new tagline here
</p>
```

---

### Hero Section Description

**Current text:**
```html
<p class="text-lg text-purple-100 mb-8 leading-relaxed">
    Experience the future of vehicle maintenance with AutoMind's intelligent diagnostics system...
</p>
```

**How to change it:**
Replace the entire paragraph text with your own description.

---

### Feature Cards (Smart Diagnostics, Live Alerts, Auto Insights)

Each feature card has three parts: title, description, and bullet points.

**Location:** Search for `<!-- Smart Diagnostics Card -->` in your file

**Changing the feature title:**
```html
<h3 class="text-2xl font-bold text-gray-900 mb-4">Smart Diagnostics</h3>
```

Replace `Smart Diagnostics` with your new title.

**Changing the feature description:**
```html
<p class="text-gray-600 leading-relaxed mb-4">
    Our advanced AI-powered diagnostic system...
</p>
```

Replace the paragraph text with your new description.

**Changing feature bullet points:**
```html
<ul class="space-y-2 text-gray-600">
    <li class="flex items-center"><i class="fas fa-check text-purple-600 mr-3"></i> Real-time system monitoring</li>
    <li class="flex items-center"><i class="fas fa-check text-purple-600 mr-3"></i> Predictive failure detection</li>
    <li class="flex items-center"><i class="fas fa-check text-purple-600 mr-3"></i> Multi-sensor analysis</li>
</ul>
```

To change a bullet point, replace the text after `</i>` but before `</li>`:

**Example:**
```html
<li class="flex items-center"><i class="fas fa-check text-purple-600 mr-3"></i> Your new feature here</li>
```

---

### Benefits Section Text

**Location:** Search for `<!-- Benefits Section -->` or `Why Choose AutoMind?`

**Changing section title:**
```html
<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">
    Why Choose AutoMind?
</h2>
```

**Changing benefit titles:**
```html
<h3 class="text-2xl font-bold text-gray-900 mb-4">Save Money</h3>
```

**Changing benefit descriptions:**
```html
<p class="text-gray-600 leading-relaxed mb-6">
    Prevent expensive repairs by addressing issues early...
</p>
```

**Changing the statistics box:**
```html
<div class="bg-green-50 border-l-4 border-green-500 px-4 py-3 rounded">
    <p class="text-green-700 font-semibold">Average savings: $1,200/year</p>
</div>
```

Replace `Average savings: $1,200/year` with your statistic.

---

### Testimonials Section

**Location:** Search for `<!-- Testimonials Section -->` or `What Our Users Say`

**Changing testimonial quote:**
```html
<p class="text-gray-700 leading-relaxed mb-6">
    "AutoMind saved me from a major engine failure..."
</p>
```

Replace the text inside the quotes.

**Changing customer name:**
```html
<p class="font-semibold text-gray-900">James Mitchell</p>
```

**Changing customer title/company:**
```html
<p class="text-gray-600 text-sm">Fleet Manager, Logistics Plus</p>
```

**Changing customer initials (the circle avatar):**
```html
<div class="w-12 h-12 bg-gradient-to-br from-purple-600 to-pink-600 rounded-full flex items-center justify-center text-white font-bold mr-4">
    JM
</div>
```

Replace `JM` with the customer's initials.

---

### FAQ Section

**Location:** Search for `<!-- FAQ Section -->` or `Frequently Asked Questions`

**Changing FAQ question:**
```html
<h3 class="text-lg font-semibold text-gray-900 flex-1">
    How does AutoMind connect to my vehicle?
</h3>
```

**Changing FAQ answer:**
```html
<div class="faq-answer hidden px-6 pb-5 border-t border-gray-200 transition-all duration-300">
    <p class="text-gray-700 leading-relaxed">
        AutoMind connects to your vehicle through a small, discreet device...
    </p>
</div>
```

Replace the text inside the `<p>` tag with your answer.

---

### Footer Text and Links

**Location:** Search for `<!-- Footer -->` near the end of the file

**Changing footer company description:**
```html
<p class="text-gray-400 leading-relaxed">
    Smarter car care for modern drivers. Intelligent diagnostics, real-time alerts, and actionable insights.
</p>
```

**Changing footer section titles:**
```html
<h4 class="text-white font-bold mb-6 text-lg">Product</h4>
```

**Changing contact email:**
```html
<a href="mailto:support@automindza.co.za" class="text-purple-400 hover:text-purple-300 transition-colors duration-300 font-semibold">support@automindza.co.za</a>
```

Replace `support@automindza.co.za` with your email address (appears twice in footer).

**Changing copyright text:**
```html
<p class="text-gray-400 text-sm mb-4 md:mb-0">
    &copy; 2025 AutoMind. All rights reserved. Powered by intelligent vehicle diagnostics.
</p>
```

---

## Modifying Tailwind CSS Classes

Tailwind CSS uses utility classes to style elements. This section explains how to modify the design without needing to write custom CSS.

### Understanding Tailwind Classes

Tailwind classes are short, descriptive names that control specific styling properties. Here's a breakdown:

```html
<button class="px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 text-white rounded-lg font-bold text-lg">
```

Let's break this down:

| Class | What It Does | Example |
|-------|------------|---------|
| `px-8` | Horizontal padding (left & right) | Adds space inside the button |
| `py-4` | Vertical padding (top & bottom) | Adds space inside the button |
| `bg-gradient-to-r` | Background gradient (left to right) | Creates the color transition |
| `from-purple-600` | Starting gradient color | Purple color |
| `to-pink-600` | Ending gradient color | Pink color |
| `text-white` | Text color | Makes text white |
| `rounded-lg` | Border radius | Rounds the corners |
| `font-bold` | Font weight | Makes text bold |
| `text-lg` | Font size | Makes text larger |

### Common Tailwind Classes You'll Use

#### Spacing (Padding & Margin)

**Padding (space inside):**
- `p-4` = padding all sides
- `px-8` = horizontal padding only
- `py-6` = vertical padding only
- `pt-4` = padding top only
- `pb-4` = padding bottom only

**Margin (space outside):**
- `m-4` = margin all sides
- `mx-auto` = center horizontally
- `mb-6` = margin bottom only
- `mt-8` = margin top only

**Numbers:** 1, 2, 3, 4, 6, 8, 12, 16, 20, 24, 32, etc.

#### Colors

**Text colors:**
- `text-gray-900` = dark gray text
- `text-purple-600` = purple text
- `text-white` = white text
- `text-pink-600` = pink text

**Background colors:**
- `bg-white` = white background
- `bg-gray-50` = very light gray
- `bg-purple-600` = purple background

**Format:** `text-{color}-{shade}` or `bg-{color}-{shade}`

Shades go from 50 (lightest) to 900 (darkest): 50, 100, 200, 300, 400, 500, 600, 700, 800, 900

#### Text Styling

- `text-xl` = extra large text
- `text-lg` = large text
- `text-base` = normal text
- `text-sm` = small text
- `font-bold` = bold text
- `font-semibold` = semi-bold text
- `font-light` = light weight text

#### Borders & Corners

- `rounded-lg` = slightly rounded corners
- `rounded-2xl` = very rounded corners
- `rounded-full` = circle
- `border` = 1px border
- `border-2` = 2px border
- `border-gray-200` = light gray border

#### Display & Layout

- `flex` = flexbox layout (arranges items in a row)
- `grid` = grid layout
- `hidden` = hide element
- `block` = display as block
- `inline-block` = display inline

#### Responsive Design

Tailwind uses prefixes to make classes responsive:

- `md:` = medium screens (tablets)
- `lg:` = large screens (desktop)
- `sm:` = small screens (large phones)

**Example:**
```html
<h1 class="text-2xl md:text-4xl lg:text-6xl">
```

This means:
- On phones: text-2xl (size 24px)
- On tablets: text-4xl (size 36px)
- On desktop: text-6xl (size 60px)

### Common Customizations with Tailwind

#### Changing Button Colors

**Original button:**
```html
<a href="/get-started" class="px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 text-white rounded-lg font-bold text-lg">
    Start Free Trial
</a>
```

**To change to solid green button:**
```html
<a href="/get-started" class="px-8 py-4 bg-green-600 text-white rounded-lg font-bold text-lg">
    Start Free Trial
</a>
```

**To change to solid blue button:**
```html
<a href="/get-started" class="px-8 py-4 bg-blue-600 text-white rounded-lg font-bold text-lg">
    Start Free Trial
</a>
```

#### Changing Card Styling

**Original feature card:**
```html
<div class="feature-card bg-white rounded-2xl p-8 shadow-md hover:shadow-xl transition-all duration-300 border border-gray-100">
```

**To make cards more rounded:**
```html
<div class="feature-card bg-white rounded-3xl p-8 shadow-md hover:shadow-xl transition-all duration-300 border border-gray-100">
```

**To add more padding:**
```html
<div class="feature-card bg-white rounded-2xl p-12 shadow-md hover:shadow-xl transition-all duration-300 border border-gray-100">
```

**To make shadow darker:**
```html
<div class="feature-card bg-white rounded-2xl p-8 shadow-lg hover:shadow-2xl transition-all duration-300 border border-gray-100">
```

#### Changing Background Colors of Sections

**Original Features section:**
```html
<section id="features" class="py-24 bg-gray-50">
```

**To change to white background:**
```html
<section id="features" class="py-24 bg-white">
```

**To change to light blue background:**
```html
<section id="features" class="py-24 bg-blue-50">
```

#### Changing Text Sizes

**Original heading:**
```html
<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">
```

**To make smaller:**
```html
<h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
```

**To make larger:**
```html
<h2 class="text-5xl md:text-6xl font-bold text-gray-900 mb-4">
```

#### Changing Spacing

**Original section spacing:**
```html
<section class="py-24 bg-gray-50">
```

**To reduce vertical spacing:**
```html
<section class="py-16 bg-gray-50">
```

**To increase vertical spacing:**
```html
<section class="py-32 bg-gray-50">
```

### Adding Custom Colors to Tailwind

If you want to use a custom color that Tailwind doesn't have, you can modify the `<style>` section at the top of the file:

**Find this section:**
```html
<style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
    
    * {
        font-family: 'Inter', sans-serif;
    }
    
    .hero-gradient {
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    }
    
    /* ... more styles ... */
</style>
```

**To add a custom color class, add this before the closing `</style>` tag:**

```html
<style>
    /* ... existing styles ... */
    
    .bg-custom-teal {
        background-color: #14b8a6;
    }
    
    .text-custom-teal {
        color: #14b8a6;
    }
</style>
```

Then use it in your HTML:
```html
<div class="bg-custom-teal text-white p-4">
    Your custom colored box
</div>
```

### Responsive Design Best Practices

When modifying classes, always maintain responsive design:

**Good practice:**
```html
<h1 class="text-2xl md:text-4xl lg:text-6xl">
```

**Don't do this:**
```html
<h1 class="text-6xl">
```

Always include mobile-first sizing, then add tablet and desktop sizes.

---

## Fixing and Managing Links

This section shows you how to update all the links on your landing page.

### Understanding Links in HTML

Links are created with the `<a>` tag:

```html
<a href="destination-page.html" class="styling-classes">Link Text Here</a>
```

**Parts of a link:**
- `<a>` = opening tag
- `href="..."` = where the link goes
- `class="..."` = styling
- `Link Text Here` = what the user sees and clicks
- `</a>` = closing tag

### Navigation Menu Links (Header)

**Location:** Find `<!-- Desktop Menu -->` in the header

**Current desktop menu links:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Benefits</a>
    <a href="#testimonials" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Testimonials</a>
    <a href="#faq" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">FAQ</a>
    <a href="/get-started" class="px-6 py-2 bg-gradient-to-r from-purple-600 to-pink-600 text-white rounded-lg font-semibold hover:shadow-lg transition-all duration-300 hover:scale-105">Get Started</a>
</div>
```

**Understanding each link:**
- `href="#features"` = jumps to the section with `id="features"` on the same page
- `href="#benefits"` = jumps to the section with `id="benefits"`
- `href="/get-started"` = goes to a page called "get-started" (needs to exist)

**How to fix broken links:**

If a link is broken, it's usually because:
1. The page doesn't exist
2. The URL is incorrect
3. The ID on the page is spelled differently

**To fix the "Get Started" link:**

1. Find this line in the desktop menu:
```html
<a href="/get-started" class="...">Get Started</a>
```

2. Replace `/get-started` with the correct path:

   - **If the page is in the same folder:** `href="get-started.html"`
   - **If the page is in a subfolder:** `href="pages/get-started.html"`
   - **If it's an external website:** `href="https://example.com/get-started"`

**Example - pointing to a file in the same folder:**
```html
<a href="get-started.html" class="...">Get Started</a>
```

### Mobile Menu Links

**Location:** Find `<!-- Mobile Menu -->` in the header

The mobile menu has the same links but appears on small screens:

```html
<div class="mobile-menu hidden absolute top-full left-0 right-0 bg-white border-t border-gray-200 md:hidden">
    <div class="flex flex-col space-y-4 px-4 py-6">
        <a href="#features" class="...">Features</a>
        <a href="#benefits" class="...">Benefits</a>
        <a href="#testimonials" class="...">Testimonials</a>
        <a href="#faq" class="...">FAQ</a>
        <a href="/get-started" class="...">Get Started</a>
    </div>
</div>
```

**Important:** Update the mobile menu links the same way as the desktop menu. They should point to the same places.

### Hero Section CTA Buttons

**Location:** Find `<!-- Hero Section -->` and look for the buttons

**Current buttons:**
```html
<a href="/get-started" class="btn-primary px-8 py-4 bg-white text-purple-600 rounded-lg font-bold text-lg hover:shadow-2xl transition-all duration-300 text-center">
    Start Free Trial
</a>
<button class="px-8 py-4 border-2 border-white text-white rounded-lg font-bold text-lg hover:bg-white hover:bg-opacity-10 transition-all duration-300">
    Watch Demo
</button>
```

**To fix the "Start Free Trial" button:**
```html
<a href="get-started.html" class="btn-primary px-8 py-4 bg-white text-purple-600 rounded-lg font-bold text-lg hover:shadow-2xl transition-all duration-300 text-center">
    Start Free Trial
</a>
```

**To make the "Watch Demo" button functional:**

Change it from a `<button>` to a link:
```html
<a href="https://www.youtube.com/watch?v=your-video-id" class="px-8 py-4 border-2 border-white text-white rounded-lg font-bold text-lg hover:bg-white hover:bg-opacity-10 transition-all duration-300 text-center">
    Watch Demo
</a>
```

Or add a click handler with JavaScript:
```html
<button class="px-8 py-4 border-2 border-white text-white rounded-lg font-bold text-lg hover:bg-white hover:bg-opacity-10 transition-all duration-300" onclick="alert('Demo coming soon!')">
    Watch Demo
</button>
```

### CTA Section Buttons

**Location:** Search for `<!-- CTA Section with Background -->`

**Current button:**
```html
<a href="/get-started" class="btn-primary inline-block px-10 py-4 bg-gradient-to-r from-purple-600 to-pink-600 text-white rounded-lg font-bold text-lg hover:shadow-2xl transition-all duration-300">
    Start Your Free Trial Today
</a>
```

**To fix:**
```html
<a href="get-started.html" class="btn-primary inline-block px-10 py-4 bg-gradient-to-r from-purple-600 to-pink-600 text-white rounded-lg font-bold text-lg hover:shadow-2xl transition-all duration-300">
    Start Your Free Trial Today
</a>
```

### Final CTA Section Button

**Location:** Search for `<!-- Final CTA Section -->`

**Current button:**
```html
<a href="/get-started" class="btn-primary inline-block px-10 py-4 bg-white text-purple-600 rounded-lg font-bold text-lg hover:shadow-2xl transition-all duration-300">
    Get Started Free Today
</a>
```

**To fix:**
```html
<a href="get-started.html" class="btn-primary inline-block px-10 py-4 bg-white text-purple-600 rounded-lg font-bold text-lg hover:shadow-2xl transition-all duration-300">
    Get Started Free Today
</a>
```

### Footer Links

**Location:** Find `<!-- Footer -->` near the end

The footer has several groups of links:

#### Product Links
```html
<ul class="space-y-3">
    <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
    <li><a href="#benefits" class="text-gray-400 hover:text-white transition-colors duration-300">Benefits</a></li>
    <li><a href="#testimonials" class="text-gray-400 hover:text-white transition-colors duration-300">Testimonials</a></li>
    <li><a href="#faq" class="text-gray-400 hover:text-white transition-colors duration-300">FAQ</a></li>
    <li><a href="/get-started" class="text-gray-400 hover:text-white transition-colors duration-300">Get Started</a></li>
</ul>
```

**These are correct** - they link to sections on the same page (using `#`) or to the get-started page.

#### Company Links
```html
<ul class="space-y-3">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">About Us</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Contact</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Careers</a></li>
</ul>
```

**These need to be fixed** - they currently use `href="#"` which is a placeholder.

**To fix Company links:**
```html
<ul class="space-y-3">
    <li><a href="about.html" class="text-gray-400 hover:text-white transition-colors duration-300">About Us</a></li>
    <li><a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
    <li><a href="contact.html" class="text-gray-400 hover:text-white transition-colors duration-300">Contact</a></li>
    <li><a href="careers.html" class="text-gray-400 hover:text-white transition-colors duration-300">Careers</a></li>
</ul>
```

#### Social Media Links
```html
<a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">
    <i class="fab fa-facebook-f text-lg"></i>
</a>
```

**To fix social links, replace `href="#"` with actual URLs:**

```html
<!-- Facebook -->
<a href="https://facebook.com/automind" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">
    <i class="fab fa-facebook-f text-lg"></i>
</a>

<!-- Twitter -->
<a href="https://twitter.com/automind" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">
    <i class="fab fa-twitter text-lg"></i>
</a>

<!-- LinkedIn -->
<a href="https://linkedin.com/company/automind" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">
    <i class="fab fa-linkedin-in text-lg"></i>
</a>

<!-- Instagram -->
<a href="https://instagram.com/automind" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">
    <i class="fab fa-instagram text-lg"></i>
</a>
```

### Email Links

**Location:** Footer contact section

**Current email link:**
```html
<a href="mailto:support@automindza.co.za" class="text-purple-400 hover:text-purple-300 transition-colors duration-300 font-semibold">support@automindza.co.za</a>
```

**To change the email:**
```html
<a href="mailto:your-email@example.com" class="text-purple-400 hover:text-purple-300 transition-colors duration-300 font-semibold">your-email@example.com</a>
```

**Note:** The `mailto:` part is important - it tells the browser to open the user's email client.

### All Links Summary Table

Here's a quick reference of all links that need updating:

| Link Text | Current | What It Should Be | Location |
|-----------|---------|------------------|----------|
| Get Started (nav) | `/get-started` | `get-started.html` | Header |
| Get Started (hero) | `/get-started` | `get-started.html` | Hero section |
| Start Your Free Trial | `/get-started` | `get-started.html` | CTA section |
| Get Started Free Today | `/get-started` | `get-started.html` | Final CTA |
| About Us | `#` | `about.html` | Footer |
| Blog | `#` | `blog.html` | Footer |
| Contact | `#` | `contact.html` | Footer |
| Careers | `#` | `careers.html` | Footer |
| Facebook | `#` | `https://facebook.com/yourpage` | Footer |
| Twitter | `#` | `https://twitter.com/yourpage` | Footer |
| LinkedIn | `#` | `https://linkedin.com/company/yourpage` | Footer |
| Instagram | `#` | `https://instagram.com/yourpage` | Footer |
| Email | `support@automindza.co.za` | `your-email@example.com` | Footer |

---

## Linking Privacy and Terms Pages

This section provides step-by-step instructions for creating and linking your privacy policy and terms of service pages.

### Step 1: Create the Privacy Policy Page

**What you need to do:**

1. Create a new file in your project folder called `privacy.html`
2. Copy the code below into that file
3. Save it

**Basic Privacy Policy Template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="AutoMind Privacy Policy">
    <title>Privacy Policy - AutoMind</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        * {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header/Navigation (same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-car text-white text-lg"></i>
                </div>
                <span class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">AutoMind</span>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#faq" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">FAQ</a>
                <a href="index.html#contact" class="px-6 py-2 bg-gradient-to-r from-purple-600 to-pink-600 text-white rounded-lg font-semibold hover:shadow-lg transition-all duration-300">Get Started</a>
            </div>
        </nav>
    </header>

    <!-- Content -->
    <section class="py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            <p class="text-gray-600 mb-8">Last updated: January 2025</p>

            <div class="space-y-8 text-gray-700 leading-relaxed">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
                    <p>
                        AutoMind ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website and use our services.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Information We Collect</h2>
                    <p>We collect information in the following ways:</p>
                    <ul class="list-disc list-inside space-y-2 mt-4">
                        <li>Information you provide directly (name, email, phone number)</li>
                        <li>Vehicle diagnostic data through our connected device</li>
                        <li>Usage data and analytics</li>
                        <li>Cookies and similar tracking technologies</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. How We Use Your Information</h2>
                    <p>We use the information we collect to:</p>
                    <ul class="list-disc list-inside space-y-2 mt-4">
                        <li>Provide and improve our services</li>
                        <li>Send you diagnostic alerts and recommendations</li>
                        <li>Communicate with you about your account</li>
                        <li>Comply with legal obligations</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Data Security</h2>
                    <p>
                        We implement appropriate technical and organizational measures to protect your personal information against unauthorized access, alteration, disclosure, or destruction. All data transmitted between your vehicle and our servers is encrypted using 256-bit SSL encryption.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Your Rights</h2>
                    <p>You have the right to:</p>
                    <ul class="list-disc list-inside space-y-2 mt-4">
                        <li>Access your personal data</li>
                        <li>Correct inaccurate data</li>
                        <li>Request deletion of your data</li>
                        <li>Opt-out of marketing communications</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Contact Us</h2>
                    <p>
                        If you have questions about this Privacy Policy or our privacy practices, please contact us at:
                    </p>
                    <p class="mt-4">
                        <strong>Email:</strong> <a href="mailto:support@automindza.co.za" class="text-purple-600 hover:text-purple-700">support@automindza.co.za</a>
                    </p>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer (same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center border-t border-gray-800 pt-8">
                <p class="text-gray-400 text-sm">
                    &copy; 2025 AutoMind. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

**What you need to do:**

1. Create a new file in your project folder called `terms.html`
2. Copy the code below into that file
3. Save it

**Basic Terms of Service Template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="AutoMind Terms of Service">
    <title>Terms of Service - AutoMind</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        * {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header/Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-car text-white text-lg"></i>
                </div>
                <span class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">AutoMind</span>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#faq" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">FAQ</a>
                <a href="index.html#contact" class="px-6 py-2 bg-gradient-to-r from-purple-600 to-pink-600 text-white rounded-lg font-semibold hover:shadow-lg transition-all duration-300">Get Started</a>
            </div>
        </nav>
    </header>

    <!-- Content -->
    <section class="py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            <p class="text-gray-600 mb-8">Last updated: January 2025</p>

            <div class="space-y-8 text-gray-700 leading-relaxed">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Acceptance of Terms</h2>
                    <p>
                        By accessing and using the AutoMind website and services, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Use License</h2>
                    <p>
                        Permission is granted to temporarily download one copy of the materials (information or software) on AutoMind's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside space-y-2 mt-4">
                        <li>Modify or copy the materials</li>
                        <li>Use the materials for any commercial purpose or for any public display</li>
                        <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                        <li>Remove any copyright or other proprietary notations from the materials</li>
                        <li>Transmit the materials to anyone else or "mirror" the materials on any other server</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Disclaimer</h2>
                    <p>
                        The materials on AutoMind's website are provided on an 'as is' basis. AutoMind makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Limitations</h2>
                    <p>
                        In no event shall AutoMind or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on AutoMind's website.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Accuracy of Materials</h2>
                    <p>
                        The materials appearing on AutoMind's website could include technical, typographical, or photographic errors. AutoMind does not warrant that any of the materials on its website are accurate, complete, or current. AutoMind may make changes to the materials contained on its website at any time without notice.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Links</h2>
                    <p>
                        AutoMind has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by AutoMind of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Modifications</h2>
                    <p>
                        AutoMind may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Governing Law</h2>
                    <p>
                        These terms and conditions are governed by and construed in accordance with the laws of the jurisdiction in which AutoMind operates, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">9. Contact Information</h2>
                    <p>
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="mt-4">
                        <strong>Email:</strong> <a href="mailto:support@automindza.co.za" class="text-purple-600 hover:text-purple-700">support@automindza.co.za</a>
                    </p>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center border-t border-gray-800 pt-8">
                <p class="text-gray-400 text-sm">
                    &copy; 2025 AutoMind. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 3: Update Links in index.html Footer

Now that you have `privacy.html` and `terms.html` files, update the links in your main `index.html` file.

**Location:** Find the Legal Column in the footer (search for `<!-- Legal Column -->`)

**Current code:**
```html
<div>
    <h4 class="text-white font-bold mb-6 text-lg">Legal</h4>
    <ul class="space-y-3">
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
        <li><a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Support</a></li>
    </ul>
</div>
```

**Good news:** The privacy and terms links are already correct! They point to `privacy.html` and `terms.html`.

**However, you still need to fix:**
1. The blog link - either create `blog.html` or remove it
2. The support link - either create a support page or change it to an email link

**Option 1: Change Support to Email Link**
```html
<li><a href="mailto:support@automindza.co.za" class="text-gray-400 hover:text-white transition-colors duration-300">Support</a></li>
```

**Option 2: Create a support.html page**
```html
<li><a href="support.html" class="text-gray-400 hover:text-white transition-colors duration-300">Support</a></li>
```

### Step 4: Add Links to Bottom Footer Links

**Location:** Search for the bottom footer section (near the very end of the file)

**Current code:**
```html
<div class="flex space-x-6 text-sm">
    <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy</a>
    <a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms</a>
    <a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a>
</div>
```

**These are already correct!** Privacy and terms links point to the right files.

### Step 5: Verify Everything Works

**To test your links:**

1. Open `index.html` in your web browser
2. Scroll to the footer
3. Click on "Privacy Policy" - it should open `privacy.html`
4. Click on "Terms of Service" - it should open `terms.html`
5. Use the back button to return to the homepage

**If links don't work:**
- Make sure `privacy.html` and `terms.html` are in the same folder as `index.html`
- Check that the file names are spelled exactly the same (including lowercase/uppercase)
- Refresh your browser (Ctrl+F5 or Cmd+Shift+R)

### Step 6: Customize Your Policy Pages

Now that the pages are created and linked, customize them with your actual policies:

**For privacy.html:**
- Replace placeholder text with your actual privacy practices
- Update the contact email
- Add any specific data handling procedures
- Include information about cookies if you use them

**For terms.html:**
- Replace placeholder text with your actual terms
- Add any specific service limitations
- Include your refund policy
- Add dispute resolution procedures
- Update jurisdiction information

**Example customization in privacy.html:**

Find this section:
```html
<section>
    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
    <p>
        AutoMind ("we," "us," "our," or "Company") is committed to protecting your privacy...
    </p>
</section>
```

Replace with your specific information:
```html
<section>
    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
    <p>
        Your Company Name ("we," "us," "our," or "Company") is committed to protecting your privacy. 
        We operate the AutoMind vehicle diagnostics platform and are dedicated to providing transparent 
        and secure data handling practices...
    </p>
</section>
```

### Important Notes About Legal Pages

**These templates are basic examples.** For your actual business, you should:

1. **Consult a lawyer** - Legal requirements vary by location
2. **Check local regulations** - GDPR (Europe), CCPA (California), etc.
3. **Be specific** - Include your actual data practices
4. **Keep updated** - Review and update policies regularly
5. **Make them findable** - Ensure they're linked from every page

---

## Common Customizations

This section covers frequently requested changes to your landing page.

### Changing the Brand Name and Logo

#### Update the Logo Text

**Location:** Find the header logo area

**Current code:**
```html
<div class="flex items-center space-x-2">
    <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
        <i class="fas fa-car text-white text-lg"></i>
    </div>
    <span class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">AutoMind</span>
</div>
```

**To change the brand name:**

Replace `AutoMind` with your brand name:
```html
<span class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">Your Brand Name</span>
```

**Appears in 2 places:**
1. Header (top of page)
2. Footer (bottom of page)

Make sure to update both!

#### Change the Logo Icon

The logo uses Font Awesome icons. To change the car icon to something else:

**Current:**
```html
<i class="fas fa-car text-white text-lg"></i>
```

**Alternative icons:**
```html
<!-- Wrench icon -->
<i class="fas fa-wrench text-white text-lg"></i>

<!-- Gear icon -->
<i class="fas fa-cog text-white text-lg"></i>

<!-- Speedometer icon -->
<i class="fas fa-tachometer-alt text-white text-lg"></i>

<!-- Shield icon -->
<i class="fas fa-shield-alt text-white text-lg"></i>

<!-- Lightning bolt icon -->
<i class="fas fa-bolt text-white text-lg"></i>
```

**To find more icons:**
Visit [Font Awesome Icons](https://fontawesome.com/icons) and search for what you need. Replace `fa-car` with the icon name.

#### Change the Logo Colors

**Current gradient:**
```html
<div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg...">
```

**To change to solid color:**
```html
<div class="w-10 h-10 bg-blue-600 rounded-lg...">
```

**To change to different gradient:**
```html
<div class="w-10 h-10 bg-gradient-to-br from-green-600 to-emerald-600 rounded-lg...">
```

### Changing Color Scheme

Your page uses purple and pink throughout. Here's how to change it:

#### Primary Color Changes

**Current purple color:** `from-purple-600 to-pink-600`

**Replace with:**
- **Blue theme:** `from-blue-600 to-cyan-600`
- **Green theme:** `from-green-600 to-emerald-600`
- **Orange theme:** `from-orange-600 to-red-600`
- **Indigo theme:** `from-indigo-600 to-blue-600`

**Where to change:**
1. Header button: `bg-gradient-to-r from-purple-600 to-pink-600`
2. Hero section background: `.hero-gradient`
3. Feature card icons: `bg-gradient-to-br from-purple-600 to-pink-600`
4. All buttons throughout the page
5. Footer links hover effect

**Example: Change entire color scheme to blue**

In the `<style>` section, find:
```html
.hero-gradient {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

Replace with:
```html
.hero-gradient {
    background: linear-gradient(135deg, #2563eb 0%, #0891b2 100%);
}
```

Then find and replace all instances of:
- `from-purple-600` → `from-blue-600`
- `to-pink-600` → `to-cyan-600`
- `text-purple-600` → `text-blue-600`
- `text-purple-100` → `text-blue-100`

### Changing Feature Icons

Each feature card has an icon. To change them:

**Location:** Search for `<!-- Smart Diagnostics Card -->`

**Current:**
```html
<div class="w-16 h-16 bg-gradient-to-br from-purple-600 to-pink-600 rounded-xl flex items-center justify-center mb-6">
    <i class="fas fa-brain text-white text-2xl"></i>
</div>
```

**To change the brain icon to something else:**

```html
<!-- For Smart Diagnostics, try: -->
<i class="fas fa-microchip text-white text-2xl"></i>

<!-- For Live Alerts, try: -->
<i class="fas fa-exclamation-circle text-white text-2xl"></i>

<!-- For Auto Insights, try: -->
<i class="fas fa-chart-bar text-white text-2xl"></i>
```

### Changing Button Text

**To change "Get Started" button text:**

Find all instances (there are several):
```html
<a href="/get-started" class="...">Get Started</a>
```

Replace `Get Started` with your new text:
```html
<a href="/get-started" class="...">Sign Up Free</a>
```

**Other button text examples:**
- "Start Free Trial"
- "Join Now"
- "Try It Free"
- "Get Access"

### Adding a New Feature Card

**To add a 4th feature card:**

1. Find the Features section grid:
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
```

2. Change `md:grid-cols-3` to `md:grid-cols-4`:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
```

3. Copy one of the existing feature cards:
```html
<div class="feature-card bg-white rounded-2xl p-8 shadow-md hover:shadow-xl transition-all duration-300 border border-gray-100">
    <div class="w-16 h-16 bg-gradient-to-br from-purple-600 to-pink-600 rounded-xl flex items-center justify-center mb-6">
        <i class="fas fa-brain text-white text-2xl"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-4">Smart Diagnostics</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Our advanced AI-powered diagnostic system...
    </p>
    <ul class="space-y-2 text-gray-600">
        <li class="flex items-center"><i class="fas fa-check text-purple-600 mr-3"></i> Real-time system monitoring</li>
        <li class="flex items-center"><i class="fas fa-check text-purple-600 mr-3"></i> Predictive failure detection</li>
        <li class="flex items-center"><i class="fas fa-check text-purple-600 mr-3"></i> Multi-sensor analysis</li>
    </ul>
</div>
```

4. Paste it after the last feature card
5. Update the title, description, icon, and bullet points

### Changing Testimonials

**To edit a testimonial:**

Find the testimonial you want to change:
```html
<!-- Testimonial 1 -->
<div class="testimonial-card bg-white rounded-2xl p-8 shadow-md hover:shadow-xl transition-all duration-300 border border-gray-100">
```

Update these parts:
- **Quote:** `<p class="text-gray-700 leading-relaxed mb-6">...`
- **Name:** `<p class="font-semibold text-gray-900">James Mitchell</p>`
- **Title:** `<p class="text-gray-600 text-sm">Fleet Manager, Logistics Plus</p>`
- **Initials:** `<div>...JM</div>`
- **Stars:** Keep the 5 stars or remove some

### Adding More Testimonials

**To add a 5th testimonial:**

1. Find the testimonials grid:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-8">
```

2. Change to:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

3. Copy one of the existing testimonial cards and paste it at the end
4. Update the content

### Changing FAQ Questions and Answers

**To edit a FAQ item:**

Find the FAQ item you want to change:
```html
<!-- FAQ Item 1 -->
<div class="faq-item bg-white rounded-xl border border-gray-200 overflow-hidden">
    <div class="faq-question px-6 py-5 flex items-center justify-between hover:bg-gray-50 transition-all duration-300">
        <h3 class="text-lg font-semibold text-gray-900 flex-1">
            How does AutoMind connect to my vehicle?
        </h3>
        <i class="faq-icon fas fa-chevron-down text-purple-600 transition-transform duration-300"></i>
    </div>
    <div class="faq-answer hidden px-6 pb-5 border-t border-gray-200 transition-all duration-300">
        <p class="text-gray-700 leading-relaxed">
            AutoMind connects to your vehicle through...
        </p>
    </div>
</div>
```

Update:
- **Question:** Replace text after `<h3>`
- **Answer:** Replace text in the `<p>` tag inside `faq-answer`

### Adding More FAQ Questions

**To add a 6th FAQ item:**

Copy one of the existing FAQ items and paste it at the end of the FAQ section. Update the question and answer.

### Changing Section Backgrounds

**Current feature section background:**
```html
<section id="features" class="py-24 bg-gray-50">
```

**To change to different colors:**
```html
<!-- White background -->
<section id="features" class="py-24 bg-white">

<!-- Light blue background -->
<section id="features" class="py-24 bg-blue-50">

<!-- Light purple background -->
<section id="features" class="py-24 bg-purple-50">
```

### Changing Section Spacing

**Current:**
```html
<section class="py-24 bg-gray-50">
```

The `py-24` controls vertical spacing (padding top and bottom).

**To reduce spacing:**
```html
<section class="py-16 bg-gray-50">
```

**To increase spacing:**
```html
<section class="py-32 bg-gray-50">
```

---

## Troubleshooting Guide

### Problem: Page Looks Broken After Editing

**Symptoms:** Text overlapping, buttons misaligned, sections look weird

**Solutions:**

1. **Check for unclosed tags:**
   - Make sure every `<div>` has a closing `</div>`
   - Make sure every `<p>` has a closing `</p>`
   - Make sure every `<a>` has a closing `</a>`

   **Example of correct code:**
   ```html
   <p class="text-lg">This is correct</p>
   ```

   **Example of incorrect code:**
   ```html
   <p class="text-lg">This is incorrect
   ```

2. **Undo your changes:**
   - If you're not sure what went wrong, use Ctrl+Z (or Cmd+Z on Mac) to undo
   - Or copy the original HTML again

3. **Check for typos in class names:**
   - `text-lg` ✓ (correct)
   - `text-lg` ✓ (correct)
   - `text-lgg` ✗ (wrong - extra 'g')
   - `textlg` ✗ (wrong - no hyphen)

4. **Validate your HTML:**
   - Visit [HTML Validator](https://validator.w3.org/)
   - Copy and paste your HTML
   - It will show you errors

### Problem: Links Don't Work

**Symptoms:** Clicking a link does nothing or shows 404 error

**Solutions:**

1. **Check the file exists:**
   - Make sure the file you're linking to actually exists in your folder
   - File names are case-sensitive (privacy.html ≠ Privacy.html)

2. **Check the file path:**
   - If file is in same folder: `href="privacy.html"` ✓
   - If file is in subfolder: `href="pages/privacy.html"` ✓
   - If external URL: `href="https://example.com"` ✓

3. **Check for typos:**
   - `privacy.html` ✓
   - `privacyy.html` ✗ (wrong)
   - `Privacy.html` ✗ (wrong case)

4. **Test in different browser:**
   - Try Chrome, Firefox, Safari, or Edge
   - Clear browser cache (Ctrl+Shift+Delete)

### Problem: Images or Icons Don't Show

**Symptoms:** Broken image icons or missing Font Awesome icons

**Solutions:**

1. **For Font Awesome icons:**
   - Make sure the Font Awesome link is in the `<head>`:
   ```html
   <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
   ```

2. **Check internet connection:**
   - Font Awesome loads from the internet
   - Make sure you're connected
   - Try refreshing the page

3. **Check icon name:**
   - `<i class="fas fa-car"></i>` ✓
   - `<i class="fas fa-carr"></i>` ✗ (wrong)
   - Visit [Font Awesome](https://fontawesome.com/icons) to find correct names

### Problem: Text Colors Look Wrong

**Symptoms:** Text is hard to read or color doesn't match

**Solutions:**

1. **Check color class:**
   - `text-gray-900` = dark gray (good for body text)
   - `text-white` = white (good for light backgrounds)
   - `text-gray-400` = light gray (good for secondary text)

2. **Check background color:**
   - If background is dark, use light text: `text-white`
   - If background is light, use dark text: `text-gray-900`

3. **Check contrast:**
   - Make sure text is readable
   - Use [Contrast Checker](https://webaim.org/resources/contrastchecker/) to verify

### Problem: Mobile Menu Doesn't Work

**Symptoms:** Mobile menu button doesn't open menu on phone

**Solutions:**

1. **Check JavaScript is enabled:**
   - Make sure JavaScript isn't disabled in browser settings
   - Check browser console for errors (F12 key)

2. **Check HTML structure:**
   - Make sure mobile menu HTML is present
   - Make sure button has class `mobile-menu-button`
   - Make sure menu has class `mobile-menu`

3. **Test on actual mobile:**
   - Use browser developer tools (F12)
   - Click the phone icon in top left
   - Test responsive view

### Problem: FAQ Accordion Doesn't Work

**Symptoms:** Clicking FAQ question doesn't expand answer

**Solutions:**

1. **Check JavaScript:**
   - Make sure JavaScript code is at bottom of HTML
   - Check for errors in browser console (F12)

2. **Check HTML structure:**
   - Make sure each FAQ item has `faq-item` class
   - Make sure question has `faq-question` class
   - Make sure answer has `faq-answer` class

3. **Test in different browser:**
   - Try different browser to isolate problem

### Problem: Page Doesn't Look Right on Mobile

**Symptoms:** Content is too small, text overlaps, buttons are hard to click

**Solutions:**

1. **Check viewport meta tag:**
   - Should be in `<head>`:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

2. **Check responsive classes:**
   - Make sure you're using `md:` and `lg:` prefixes
   - Example: `<h1 class="text-2xl md:text-4xl lg:text-6xl">`

3. **Test in browser:**
   - Open DevTools (F12)
   - Click phone icon (toggle device toolbar)
   - Test different screen sizes

### Problem: Tailwind CSS Classes Aren't Working

**Symptoms:** Classes like `text-lg` or `bg-white` don't apply

**Solutions:**

1. **Check Tailwind CDN link:**
   - Should be in `<head>`:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

2. **Check internet connection:**
   - Tailwind loads from internet
   - Make sure you're connected

3. **Clear browser cache:**
   - Press Ctrl+Shift+Delete
   - Clear all cache
   - Refresh page

4. **Check class name spelling:**
   - Tailwind classes are very specific
   - `text-lg` ✓
   - `textlg` ✗
   - `text-large` ✗

### Problem: Gradient Colors Look Different

**Symptoms:** Gradient doesn't match what you see in preview

**Solutions:**

1. **Check gradient syntax:**
   - `from-purple-600 to-pink-600` ✓
   - `from-purple-600 to-pink` ✗ (missing shade number)

2. **Check browser support:**
   - Gradients work in all modern browsers
   - Update your browser if needed

3. **Clear cache:**
   - Browser might be showing old version
   - Press Ctrl+Shift+Delete and clear cache

### Problem: Email Link Doesn't Work

**Symptoms:** Clicking email link does nothing

**Solutions:**

1. **Check mailto syntax:**
   - `href="mailto:email@example.com"` ✓
   - `href="email@example.com"` ✗ (missing mailto:)
   - `href="mailto: email@example.com"` ✗ (space after colon)

2. **Check email format:**
   - Must have @ symbol
   - Must have domain
   - `support@automindza.co.za` ✓
   - `support automindza.co.za` ✗

3. **Test on different device:**
   - Email clients must be configured
   - Test on computer and phone

---

## Best Practices

Follow these guidelines to maintain a professional, functional landing page.

### Code Organization

**Keep your HTML organized:**

1. **Use comments to mark sections:**
   ```html
   <!-- Header/Navigation -->
   <header>...</header>

   <!-- Hero Section -->
   <section class="hero-gradient">...</section>

   <!-- Features Section -->
   <section id="features">...</section>
   ```

2. **Indent nested elements:**
   ```html
   <!-- Good indentation -->
   <div class="container">
       <div class="row">
           <div class="col">
               <p>Content</p>
           </div>
       </div>
   </div>
   ```

3. **Keep one element per line:**
   ```html
   <!-- Good -->
   <div class="container">
       <p>Text</p>
       <button>Click me</button>
   </div>

   <!-- Avoid -->
   <div class="container"><p>Text</p><button>Click me</button></div>
   ```

### Naming Conventions

**Use descriptive names:**

- Link names: `href="privacy.html"` (not `href="p.html"`)
- Section IDs: `id="testimonials"` (not `id="t"`)
- Class names: `class="feature-card"` (not `class="fc"`)

### Consistency

**Keep consistent throughout your page:**

1. **Use same colors:**
   - If you use purple-600 in header, use it elsewhere too
   - Consistent branding looks professional

2. **Use same spacing:**
   - If sections have `py-24`, keep that consistent
   - Don't mix `py-16` and `py-32` randomly

3. **Use same fonts:**
   - Page uses Inter font throughout
   - Don't add multiple different fonts

4. **Use same button styles:**
   - All primary buttons should look the same
   - All secondary buttons should look the same

### Performance

**Keep your page fast:**

1. **Minimize changes:**
   - Don't add unnecessary code
   - Remove unused classes

2. **Optimize images:**
   - Use compressed images
   - Use appropriate file formats

3. **Avoid external scripts:**
   - Only use necessary external libraries
   - This page uses Tailwind and Font Awesome (both essential)

### Accessibility

**Make your page accessible to everyone:**

1. **Use descriptive link text:**
   ```html
   <!-- Good -->
   <a href="privacy.html">Read our privacy policy</a>

   <!-- Avoid -->
   <a href="privacy.html">Click here</a>
   ```

2. **Use semantic HTML:**
   ```html
   <!-- Good -->
   <h1>Main heading</h1>
   <h2>Subheading</h2>
   <button>Click me</button>

   <!-- Avoid -->
   <div class="h1">Main heading</div>
   <div class="h2">Subheading</div>
   <div onclick="...">Click me</div>
   ```

3. **Include alt text for images:**
   ```html
   <img src="car.jpg" alt="Mechanic checking car engine">
   ```

4. **Use proper color contrast:**
   - Text should be easily readable
   - Use [Contrast Checker](https://webaim.org/resources/contrastchecker/)

### Security

**Keep your page secure:**

1. **Use HTTPS links:**
   - Always use `https://` for external links
   - `https://example.com` ✓
   - `http://example.com` ✗

2. **Validate all input:**
   - If you add forms, validate user input
   - Don't trust user-submitted data

3. **Keep software updated:**
   - Update Tailwind CSS periodically
   - Update Font Awesome periodically

### SEO (Search Engine Optimization)

**Help your page rank in search results:**

1. **Use descriptive titles:**
   ```html
   <title>AutoMind - Smarter Car Care Made Simple</title>
   ```

2. **Use meta descriptions:**
   ```html
   <meta name="description" content="Intelligent vehicle diagnostics and maintenance insights">
   ```

3. **Use heading hierarchy:**
   ```html
   <h1>Main title (one per page)</h1>
   <h2>Section titles</h2>
   <h3>Subsection titles</h3>
   ```

4. **Use descriptive anchor text:**
   ```html
   <!-- Good -->
   <a href="privacy.html">Privacy Policy</a>

   <!-- Bad for SEO -->
   <a href="privacy.html">Click here</a>
   ```

### Testing Checklist

**Before publishing, test:**

- [ ] All links work (internal and external)
- [ ] Page looks good on mobile (test with F12 DevTools)
- [ ] Page looks good on tablet
- [ ] Page looks good on desktop
- [ ] All buttons work
- [ ] Mobile menu opens and closes
- [ ] FAQ accordion works
- [ ] All text is readable
- [ ] All images load
- [ ] No console errors (F12 → Console)
- [ ] Email links work
- [ ] Social media links work
- [ ] Page loads reasonably fast

### Version Control

**Keep track of changes:**

1. **Save backups:**
   - Before making big changes, save a copy
   - Name it: `index-backup.html`

2. **Document changes:**
   - Keep notes of what you changed
   - Helps if you need to revert

3. **Use a version control system:**
   - Consider using Git/GitHub
   - Tracks all changes automatically

### Regular Maintenance

**Keep your page up to date:**

1. **Update content regularly:**
   - Refresh testimonials
   - Update statistics
   - Add new features

2. **Monitor links:**
   - Check links monthly
   - Fix broken links immediately

3. **Update policies:**
   - Review privacy policy yearly
   - Update terms if needed

4. **Check analytics:**
   - See how visitors use your page
   - Improve based on data

---

## Quick Reference Guide

### File Locations

```
your-project-folder/
├── index.html (main landing page)
├── privacy.html (privacy policy)
├── terms.html (terms of service)
├── about.html (about page - optional)
├── blog.html (blog page - optional)
├── contact.html (contact page - optional)
└── support.html (support page - optional)
```

### Key Section IDs

```html
id="features"        <!-- Features section -->
id="benefits"        <!-- Benefits section -->
id="testimonials"     <!-- Testimonials section -->
id="faq"             <!-- FAQ section -->
```

### Important Classes

```html
.hero-gradient       <!-- Hero section background -->
.feature-card        <!-- Feature cards -->
.btn-primary         <!-- Primary buttons -->
.testimonial-card    <!-- Testimonial cards -->
.faq-item            <!-- FAQ items -->
.faq-question        <!-- FAQ questions -->
.faq-answer          <!-- FAQ answers -->
```

### Common Tailwind Classes

```html
text-{size}          <!-- text-lg, text-2xl, text-4xl -->
bg-{color}-{shade}   <!-- bg-white, bg-purple-600 -->
text-{color}-{shade} <!-- text-gray-900, text-white -->
px-{size}            <!-- px-4, px-8 (horizontal padding) -->
py-{size}            <!-- py-4, py-8 (vertical padding) -->
rounded-{size}       <!-- rounded-lg, rounded-2xl -->
shadow-{size}        <!-- shadow-md, shadow-lg -->
hover:               <!-- hover:text-purple-600 -->
md:                  <!-- md:text-4xl (tablet and up) -->
lg:                  <!-- lg:text-6xl (desktop and up) -->
```

### Common Tasks

| Task | How To |
|------|--------|
| Change headline | Find `<h1>` and replace text |
| Change button color | Change `bg-gradient-to-r from-purple-600 to-pink-600` |
| Change section background | Change `bg-gray-50` to `bg-white` or other color |
| Add feature card | Copy existing card and paste, update content |
| Add testimonial | Copy existing testimonial and paste, update content |
| Fix link | Change `href="/page"` to `href="page.html"` |
| Hide element | Add class `hidden` |
| Show element | Remove class `hidden` |
| Change text size | Change `text-lg` to `text-2xl` or `text-sm` |
| Change spacing | Change `py-24` to `py-16` or `py-32` |

---

## Getting Help

### Resources

- **Tailwind CSS Documentation:** https://tailwindcss.com/docs
- **Font Awesome Icons:** https://fontawesome.com/icons
- **HTML Validator:** https://validator.w3.org/
- **CSS Validator:** https://jigsaw.w3.org/css-validator/
- **Color Picker:** https://www.w3schools.com/colors/colors_picker.asp
- **Contrast Checker:** https://webaim.org/resources/contrastchecker/

### Common Questions

**Q: Can I use this on a mobile app?**
A: This is HTML/CSS/JavaScript, designed for web browsers. For mobile apps, you'd need different technology.

**Q: Can I sell this design?**
A: This is a template for your own use. Selling the design itself may violate license terms. Check Font Awesome and Tailwind licenses.

**Q: How do I add a shopping cart?**
A: This requires backend development (server-side code). You'd need to integrate with payment systems like Stripe or PayPal.

**Q: How do I add user accounts?**
A: This requires backend development. You'd need a database and server-side code.

**Q: Can I use this for multiple websites?**
A: Yes, you can use this template for multiple projects.

**Q: How do I deploy this online?**
A: Upload the HTML files to a web host (like Bluehost, GoDaddy, Netlify, or Vercel).

---

## Conclusion

You now have a comprehensive guide to maintaining and customizing your AutoMind landing page. Remember:

1. **Always backup** before making big changes
2. **Test thoroughly** on all devices
3. **Keep it consistent** in design and content
4. **Update regularly** to stay fresh
5. **Monitor links** to ensure everything works

Good luck with your landing page! If you have questions, refer back to this guide or consult the resources listed above.

---

**Last Updated:** January 2025
**Version:** 1.0