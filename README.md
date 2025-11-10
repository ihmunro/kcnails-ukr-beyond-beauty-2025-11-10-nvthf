# KCNails UKR Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize the KCNails UKR landing page. Whether you're updating text, fixing links, or connecting policy pages, we'll walk you through each step with clear, beginner-friendly instructions.

---

## Table of Contents

1. [Quick Start Overview](#quick-start-overview)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Section 1: Updating Text and Tailwind CSS Classes](#section-1-updating-text-and-tailwind-css-classes)
4. [Section 2: Fixing Broken Links](#section-2-fixing-broken-links)
5. [Section 3: Linking Privacy and Terms Pages](#section-3-linking-privacy-and-terms-pages)
6. [Troubleshooting Tips](#troubleshooting-tips)
7. [Best Practices](#best-practices)

---

## Quick Start Overview

### What You'll Need

- A text editor (such as VS Code, Sublime Text, or even Notepad)
- The `index.html` file open in your editor
- Basic understanding of HTML tags (don't worry, we'll explain everything!)
- A web browser to preview your changes

### How to Preview Changes

After making edits to your `index.html` file:

1. Save the file (Ctrl+S on Windows, Cmd+S on Mac)
2. Open the file in your web browser (double-click the file or drag it into your browser)
3. Refresh the page (F5 or Cmd+R) to see your changes

---

## Understanding the Page Structure

Before making changes, let's understand how this landing page is organized:

### Main Sections (In Order)

| Section | Purpose | Location in HTML |
|---------|---------|-----------------|
| **Header Navigation** | Logo, menu links, "Shop Now" button | Lines 41-98 |
| **Hero Section** | Main headline and call-to-action | Lines 100-127 |
| **Features Section** | Three feature cards (Colors, Gels, Starter Kits) | Lines 129-272 |
| **Benefits Section** | Three benefit cards with icons | Lines 274-371 |
| **About Us Section** | Company story and mission | Lines 373-396 |
| **Testimonials Section** | Customer reviews and ratings | Lines 398-543 |
| **FAQ Section** | Expandable questions and answers | Lines 545-706 |
| **Call-to-Action Section** | Final conversion section | Lines 708-732 |
| **Footer** | Contact info, links, copyright | Lines 734-850 |

### Key HTML Terms to Know

- **`<section>`** - A major area of content on the page
- **`<h1>, <h2>, <h3>`** - Headings (h1 is largest, h3 is smaller)
- **`<p>`** - Paragraph of text
- **`<a href="...">`** - A clickable link
- **`class="..."`** - Styling instructions that control how something looks
- **`id="..."`** - A unique identifier used for linking to sections

---

## Section 1: Updating Text and Tailwind CSS Classes

This section covers how to modify text content and styling throughout the page while maintaining the professional look.

### 1.1 Updating the Header/Logo

**Location:** Lines 48-50

**Current Code:**
```html
<div class="flex-shrink-0">
    <h1 class="text-3xl font-bold gradient-text">KCNails</h1>
</div>
```

**How to Change:**

1. Find the text `KCNails` inside the `<h1>` tag
2. Replace it with your company name
3. Save the file

**Example:**
```html
<h1 class="text-3xl font-bold gradient-text">MyBeautyBrand</h1>
```

**What the Classes Do:**
- `text-3xl` - Makes text large (3 times the base size)
- `font-bold` - Makes text bold/thick
- `gradient-text` - Applies the pink-to-orange gradient color

---

### 1.2 Updating Navigation Menu Items

**Location:** Lines 53-62 (Desktop Menu)

**Current Code:**
```html
<nav class="hidden md:flex items-center gap-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Benefits</a>
    <a href="#testimonials" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Testimonials</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">FAQ</a>
```

**How to Change Menu Text:**

1. Find the text between `>` and `</a>` for each menu item
2. Replace with your desired text
3. **Important:** Do NOT change the `href="#..."` part yet (we'll cover that in Section 2)

**Example - Changing "Features" to "Our Products":**
```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Our Products</a>
```

**What the Classes Do:**
- `text-gray-300` - Gray text color
- `hover:text-white` - Text turns white when you hover over it
- `transition-colors duration-300` - Color change happens smoothly over 300 milliseconds
- `font-medium` - Medium-weight font

**Note:** The same navigation menu appears twice in the code:
- **Desktop version** (Lines 53-62) - Shown on large screens
- **Mobile version** (Lines 71-80) - Shown on phones/tablets

Update both versions to keep them consistent!

---

### 1.3 Updating Hero Section Headline and Description

**Location:** Lines 107-114

**Current Code:**
```html
<h1 class="text-5xl sm:text-6xl lg:text-7xl font-bold mb-6 leading-tight tracking-tight">
    <span class="block text-white">KCNails UKR:</span>
    <span class="block gradient-text">Beyond Beauty</span>
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-8 max-w-3xl mx-auto leading-relaxed font-light">
    Elevate your nail game with products that tell a powerful story. Express your unique personality through vibrant, professional-quality nail solutions designed for everyone.
</p>
```

**How to Change:**

The headline is split into two lines:
- Line 1: `KCNails UKR:` (white text)
- Line 2: `Beyond Beauty` (gradient pink-to-orange text)

**To update the headline:**

1. Replace `KCNails UKR:` with your tagline (Line 109)
2. Replace `Beyond Beauty` with your main message (Line 110)

**Example:**
```html
<h1 class="text-5xl sm:text-6xl lg:text-7xl font-bold mb-6 leading-tight tracking-tight">
    <span class="block text-white">Your Brand:</span>
    <span class="block gradient-text">Your Message</span>
</h1>
```

**To update the description:**

1. Replace the entire paragraph text (Lines 111-113)
2. Keep the `<p>` tag and class names the same

**Example:**
```html
<p class="text-xl md:text-2xl text-gray-300 mb-8 max-w-3xl mx-auto leading-relaxed font-light">
    Your new description goes here. Keep it compelling and customer-focused!
</p>
```

**Understanding the Responsive Classes:**

These classes make text different sizes on different screen sizes:
- `text-5xl` - Base size (phones)
- `sm:text-6xl` - Larger on small screens (tablets)
- `lg:text-7xl` - Largest on large screens (desktops)

This ensures your page looks good on all devices!

---

### 1.4 Updating Feature Cards

**Location:** Lines 137-272

Each feature card has three parts: icon, title, and description.

**Current Structure (Feature 1 - Vibrant Color Palettes):**
```html
<div class="hover-lift bg-gray-800 border border-gray-700 rounded-2xl p-8 soft-shadow">
    <div class="mb-6">
        <!-- SVG Icon Here -->
    </div>
    <h3 class="text-2xl font-bold mb-4">Vibrant Color Palettes</h3>
    <p class="text-gray-400 leading-relaxed mb-4">
        Choose from an extensive spectrum...
    </p>
    <ul class="space-y-3 text-gray-300">
        <li class="flex items-center gap-2">
            <!-- Checkmark icon -->
            100+ curated color options
        </li>
        <!-- More list items -->
    </ul>
</div>
```

**How to Update Feature Title:**

1. Find the `<h3>` tag in each feature card
2. Replace the text between `>` and `</h3>`

**Example - Changing Feature 1 Title:**
```html
<h3 class="text-2xl font-bold mb-4">Endless Color Choices</h3>
```

**How to Update Feature Description:**

1. Find the `<p>` tag in each feature card
2. Replace the paragraph text
3. Keep it between 2-3 sentences for readability

**Example:**
```html
<p class="text-gray-400 leading-relaxed mb-4">
    Our premium gel collection offers over 100 stunning shades. Each color is specially formulated to resist fading and maintain brilliance throughout the month.
</p>
```

**How to Update Feature Bullet Points:**

Each bullet point is inside an `<li>` tag:

```html
<li class="flex items-center gap-2">
    <svg class="w-5 h-5 text-pink-500" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7"></path>
    </svg>
    100+ curated color options
</li>
```

**To update the bullet text:**
1. Find the text after the `</svg>` tag
2. Replace it with your new text

**Example:**
```html
<li class="flex items-center gap-2">
    <svg class="w-5 h-5 text-pink-500" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7"></path>
    </svg>
    Handpicked selection of trending colors
</li>
```

**⚠️ Important:** Do NOT delete or modify the `<svg>` code (the checkmark icon). Just replace the text after it.

**What the Classes Do:**
- `text-2xl` - Large heading size
- `font-bold` - Bold text
- `mb-4` - Margin (space) below the element
- `text-gray-400` - Gray text color
- `leading-relaxed` - Extra space between lines for readability

---

### 1.5 Updating Benefits Section

**Location:** Lines 318-371

The benefits section has three cards with icons and descriptions.

**Current Structure:**
```html
<div class="bg-gradient-to-br from-gray-800 to-gray-900 border border-gray-700 rounded-2xl p-8 hover-lift soft-shadow">
    <div class="flex items-start gap-4">
        <div class="flex-shrink-0">
            <div class="flex items-center justify-center h-14 w-14 rounded-full bg-pink-500 bg-opacity-20">
                <!-- Icon SVG -->
            </div>
        </div>
        <div class="flex-1">
            <h3 class="text-2xl font-bold mb-3">Express Your Personality</h3>
            <p class="text-gray-400 leading-relaxed">
                Your nails are a canvas...
            </p>
        </div>
    </div>
</div>
```

**How to Update Benefit Title and Description:**

1. Find the `<h3>` tag and replace the title text
2. Find the `<p>` tag and replace the description

**Example:**
```html
<h3 class="text-2xl font-bold mb-3">Show Your Style</h3>
<p class="text-gray-400 leading-relaxed">
    Make a statement with nails that reflect your unique personality and fashion sense.
</p>
```

**Changing Icon Colors:**

Each benefit card has a colored icon circle. To change the color:

1. Find the line with `bg-pink-500` or `bg-orange-500` or `bg-pink-400`
2. Replace with a different Tailwind color

**Available Colors:**
- `bg-pink-500` - Pink
- `bg-orange-500` - Orange
- `bg-blue-500` - Blue
- `bg-purple-500` - Purple
- `bg-green-500` - Green
- `bg-red-500` - Red

**Example - Changing first benefit icon to orange:**
```html
<div class="flex items-center justify-center h-14 w-14 rounded-full bg-orange-500 bg-opacity-20">
```

Also update the icon color inside (find `text-pink-400` and change to `text-orange-400`):
```html
<svg class="w-7 h-7 text-orange-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5">
```

---

### 1.6 Updating About Us Section

**Location:** Lines 373-396

**Current Code:**
```html
<h2 class="text-4xl md:text-5xl font-bold mb-4 leading-tight">
    About KCNails UKR
</h2>
<div class="w-16 h-1 bg-gradient-to-r from-pink-500 to-orange-500 mx-auto rounded-full"></div>

<div class="space-y-8">
    <p class="text-lg text-gray-300 leading-relaxed">
        KCNails UKR was founded on a simple yet powerful belief...
    </p>
    
    <p class="text-lg text-gray-300 leading-relaxed">
        Our mission is to empower individuals...
    </p>
</div>
```

**How to Update:**

1. Replace the heading text in the `<h2>` tag
2. Replace each paragraph text in the `<p>` tags
3. You can have as many paragraphs as needed

**Example:**
```html
<h2 class="text-4xl md:text-5xl font-bold mb-4 leading-tight">
    Our Story
</h2>

<div class="space-y-8">
    <p class="text-lg text-gray-300 leading-relaxed">
        We started with a simple idea: everyone deserves access to quality products.
    </p>
    
    <p class="text-lg text-gray-300 leading-relaxed">
        Today, we're proud to serve thousands of satisfied customers worldwide.
    </p>
</div>
```

**Note:** The decorative line (`<div class="w-16 h-1 ...">`) below the heading is optional. You can delete it or keep it.

---

### 1.7 Updating Testimonials

**Location:** Lines 421-543

Each testimonial card contains:
- Star rating
- Quote text
- Customer name
- Customer title/location

**Current Structure:**
```html
<div class="hover-lift bg-gradient-to-br from-gray-800 to-gray-900 border border-gray-700 rounded-2xl p-8 soft-shadow">
    <!-- 5 star SVGs (don't modify) -->
    <p class="text-gray-300 mb-6 leading-relaxed">
        "The colors are absolutely stunning..."
    </p>
    <div class="border-t border-gray-700 pt-4">
        <p class="font-bold text-white">Sarah Mitchell</p>
        <p class="text-gray-400 text-sm">Beauty Enthusiast, London</p>
    </div>
</div>
```

**How to Update Testimonial Quote:**

1. Find the `<p>` tag containing the quote
2. Replace the text (keep the quotation marks if desired)

**Example:**
```html
<p class="text-gray-300 mb-6 leading-relaxed">
    "Best products I've ever used! My nails look salon-perfect every time."
</p>
```

**How to Update Customer Name and Title:**

1. Find the name in the first `<p>` tag after `border-t`
2. Find the location/title in the second `<p>` tag

**Example:**
```html
<div class="border-t border-gray-700 pt-4">
    <p class="font-bold text-white">John Smith</p>
    <p class="text-gray-400 text-sm">Professional Stylist, New York</p>
</div>
```

**⚠️ Important:** Do NOT modify the star rating SVG code. It's the same for all testimonials and should stay as is.

---

### 1.8 Updating FAQ Questions and Answers

**Location:** Lines 567-706

**Current Structure:**
```html
<div class="faq-item bg-gray-800 border border-gray-700 rounded-2xl overflow-hidden soft-shadow">
    <button class="faq-question w-full px-8 py-6 flex items-center justify-between hover:bg-gray-750 transition-colors duration-300 cursor-pointer">
        <span class="text-lg font-bold text-white text-left">Are KCNails UKR products suitable for beginners?</span>
        <svg class="faq-icon w-6 h-6 text-pink-500 flex-shrink-0 ml-4 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
        </svg>
    </button>
    <div class="faq-answer hidden px-8 pb-6 border-t border-gray-700">
        <p class="text-gray-300 leading-relaxed">
            Absolutely! KCNails UKR is specifically designed with beginners in mind...
        </p>
    </div>
</div>
```

**How to Update FAQ Question:**

1. Find the text between `<span class="text-lg font-bold text-white text-left">` and `</span>`
2. Replace with your question

**Example:**
```html
<span class="text-lg font-bold text-white text-left">Can I use these products if I'm new to nails?</span>
```

**How to Update FAQ Answer:**

1. Find the `<p class="text-gray-300 leading-relaxed">` tag
2. Replace the answer text

**Example:**
```html
<p class="text-gray-300 leading-relaxed">
    Yes! Our products are designed for all skill levels. We provide detailed instructions and video tutorials to help you get started.
</p>
```

**⚠️ Important:** Do NOT modify the `<svg>` icon code. It animates when questions are clicked and needs to stay as is.

---

### 1.9 Updating Footer Text and Information

**Location:** Lines 788-850

**Current Contact Information:**
```html
<div class="flex items-center gap-4">
    <div class="flex-shrink-0">
        <svg class="w-6 h-6 text-pink-500" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
        </svg>
    </div>
    <div>
        <p class="text-gray-400 text-sm">Email Us</p>
        <p class="text-white font-semibold">
            <a href="mailto:iainhmunro@gmail.com" class="hover:text-pink-400 transition-colors duration-300">iainhmunro@gmail.com</a>
        </p>
    </div>
</div>
```

**How to Update Email Address:**

1. Find the email address in the `<a href="mailto:...">` link
2. Replace both the `href` value AND the displayed text

**Example:**
```html
<a href="mailto:your-email@yourcompany.com" class="hover:text-pink-400 transition-colors duration-300">your-email@yourcompany.com</a>
```

**How to Update Website URL:**

Find this section:
```html
<div>
    <p class="text-gray-400 text-sm">Visit Us</p>
    <p class="text-white font-semibold">
        <a href="https://kcnailsukr.com/" target="_blank" rel="noopener noreferrer" class="hover:text-pink-400 transition-colors duration-300">kcnailsukr.com</a>
    </p>
</div>
```

Replace:
1. The `href` value with your website URL
2. The displayed text with your domain name

**Example:**
```html
<a href="https://yourwebsite.com/" target="_blank" rel="noopener noreferrer" class="hover:text-pink-400 transition-colors duration-300">yourwebsite.com</a>
```

**How to Update Support Hours:**

Find this section:
```html
<div>
    <p class="text-gray-400 text-sm">Support Hours</p>
    <p class="text-white font-semibold">Mon-Fri, 9AM-6PM UTC</p>
</div>
```

Replace the hours text:
```html
<p class="text-white font-semibold">Mon-Fri, 10AM-8PM EST</p>
```

**How to Update Copyright Year:**

Find this at the bottom:
```html
<p class="text-gray-400">
    &copy; 2025 KCNails UKR. All rights reserved.
</p>
```

Replace the year:
```html
<p class="text-gray-400">
    &copy; 2024 Your Company Name. All rights reserved.
</p>
```

---

### 1.10 Color Scheme Customization

The page uses a pink-to-orange gradient as its primary color scheme. Here are all the color-related classes:

**Primary Gradient (Pink to Orange):**
- `from-pink-500 to-orange-500` - Used in buttons and gradients
- `gradient-text` - Custom gradient text (defined in CSS)

**To Change the Color Scheme:**

1. Replace all instances of `from-pink-500 to-orange-500` with your colors
2. Update hover states like `hover:from-pink-600 hover:to-orange-600`

**Available Tailwind Colors:**
- `pink-500`, `pink-600` → Pink shades
- `orange-500`, `orange-600` → Orange shades
- `blue-500`, `blue-600` → Blue shades
- `purple-500`, `purple-600` → Purple shades
- `green-500`, `green-600` → Green shades

**Example - Changing to Blue Theme:**

Find:
```html
<a href="..." class="bg-gradient-to-r from-pink-500 to-orange-500 hover:from-pink-600 hover:to-orange-600 ...">
```

Replace with:
```html
<a href="..." class="bg-gradient-to-r from-blue-500 to-purple-500 hover:from-blue-600 hover:to-purple-600 ...">
```

**Note:** There are approximately 15-20 instances of the pink-orange gradient throughout the page. Use Find & Replace in your text editor (Ctrl+H) to change them all at once!

---

## Section 2: Fixing Broken Links

This section explains how to update all the links in your navigation, buttons, and footer.

### 2.1 Understanding Link Structure

A link in HTML looks like this:
```html
<a href="DESTINATION">LINK TEXT</a>
```

- **`href`** - Where the link goes
- **LINK TEXT** - What users see and click on
- **`target="_blank"`** - Opens link in new tab
- **`rel="noopener noreferrer"`** - Security feature (always include with external links)

### 2.2 Types of Links on This Page

| Link Type | Example | Used For |
|-----------|---------|----------|
| **Internal (Section)** | `href="#features"` | Links to sections on same page |
| **External** | `href="https://kcnailsukr.com/"` | Links to other websites |
| **Email** | `href="mailto:email@example.com"` | Opens email client |
| **File** | `href="about.html"` | Links to other HTML files |

### 2.3 Navigation Menu Links

**Location:** Lines 53-62 (Desktop) and 71-80 (Mobile)

**Current Code:**
```html
<a href="#features" class="text-gray-300 hover:text-white ...">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-white ...">Benefits</a>
<a href="#testimonials" class="text-gray-300 hover:text-white ...">Testimonials</a>
<a href="#faq" class="text-gray-300 hover:text-white ...">FAQ</a>
```

**How These Links Work:**

These links use the `#` symbol, which means "jump to this section on the same page." The part after `#` must match an `id` attribute on the page.

**Checking if Links Work:**

1. Look for sections with matching `id` attributes:
   - `<section id="features">` ✓ (Line 129)
   - `<section id="benefits">` ✓ (Line 274)
   - `<section id="testimonials">` ✓ (Line 398)
   - `<section id="faq">` ✓ (Line 545)

2. All navigation links match these IDs, so they should work!

**If You Add a New Section:**

1. Add an `id` to your new section:
```html
<section id="my-new-section">
    <h2>My New Section</h2>
    <!-- content -->
</section>
```

2. Add a navigation link:
```html
<a href="#my-new-section" class="text-gray-300 hover:text-white ...">My Section</a>
```

**⚠️ Important:** Update BOTH desktop (Line 53-62) AND mobile (Line 71-80) navigation menus!

---

### 2.4 "Shop Now" Button Links

**Location:** Lines 65-67 (Header), 118-120 (Hero), 732 (CTA Section)

**Current Code:**
```html
<a href="https://kcnailsukr.com/" target="_blank" rel="noopener noreferrer" class="bg-gradient-to-r from-pink-500 to-orange-500 ...">
    Shop Now
</a>
```

**How to Update:**

1. Replace the URL in `href="..."`
2. Keep `target="_blank"` (opens in new tab)
3. Keep `rel="noopener noreferrer"` (security)

**Example - If your shop is at yoursite.com/shop:**
```html
<a href="https://yoursite.com/shop" target="_blank" rel="noopener noreferrer" class="bg-gradient-to-r from-pink-500 to-orange-500 ...">
    Shop Now
</a>
```

**⚠️ Important:** Update ALL instances of "Shop Now" buttons:
1. Header navigation (Line 66)
2. Desktop mobile menu (Line 79)
3. Hero section (Line 119)
4. CTA section (Line 731)

**Quick Find Method:**

1. Open Find & Replace (Ctrl+H or Cmd+H)
2. Find: `https://kcnailsukr.com/`
3. Replace with: `https://yoursite.com/shop`
4. Click "Replace All"

---

### 2.5 Footer Links - Quick Links Section

**Location:** Lines 793-811

**Current Code:**
```html
<div>
    <h4 class="text-lg font-bold text-white mb-6">Quick Links</h4>
    <ul class="space-y-3">
        <li>
            <a href="#features" class="text-gray-400 hover:text-pink-400 ...">Features</a>
        </li>
        <li>
            <a href="#benefits" class="text-gray-400 hover:text-pink-400 ...">Benefits</a>
        </li>
        <li>
            <a href="#testimonials" class="text-gray-400 hover:text-pink-400 ...">Testimonials</a>
        </li>
        <li>
            <a href="#faq" class="text-gray-400 hover:text-pink-400 ...">FAQ</a>
        </li>
        <li>
            <a href="https://kcnailsukr.com/" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-pink-400 ...">Shop</a>
        </li>
    </ul>
</div>
```

**These Links Are Already Correct:**
- Section links (`#features`, `#benefits`, etc.) match the section IDs ✓
- Shop link points to your store ✓

**If You Need to Change Section Names:**

1. Change the link text (what users see)
2. Keep the `href` the same

**Example - Changing "Features" to "Our Products":**
```html
<li>
    <a href="#features" class="text-gray-400 hover:text-pink-400 ...">Our Products</a>
</li>
```

---

### 2.6 Footer Links - Company Section

**Location:** Lines 813-831

**Current Code:**
```html
<div>
    <h4 class="text-lg font-bold text-white mb-6">Company</h4>
    <ul class="space-y-3">
        <li>
            <a href="about.html" class="text-gray-400 hover:text-pink-400 ...">About Us</a>
        </li>
        <li>
            <a href="blog.html" class="text-gray-400 hover:text-pink-400 ...">Blog</a>
        </li>
        <li>
            <a href="contact.html" class="text-gray-400 hover:text-pink-400 ...">Contact</a>
        </li>
        <li>
            <a href="careers.html" class="text-gray-400 hover:text-pink-400 ...">Careers</a>
        </li>
    </ul>
</div>
```

**What These Links Do:**

These links point to separate HTML files:
- `about.html` - About page
- `blog.html` - Blog page
- `contact.html` - Contact page
- `careers.html` - Careers page

**⚠️ These Files Don't Exist Yet!**

You need to create these files or update the links to point to real pages.

**Option A: Update Links to External URLs**

If your pages are hosted on a different website:

```html
<li>
    <a href="https://yoursite.com/about" class="text-gray-400 hover:text-pink-400 ...">About Us</a>
</li>
<li>
    <a href="https://yoursite.com/blog" class="text-gray-400 hover:text-pink-400 ...">Blog</a>
</li>
<li>
    <a href="https://yoursite.com/contact" class="text-gray-400 hover:text-pink-400 ...">Contact</a>
</li>
<li>
    <a href="https://yoursite.com/careers" class="text-gray-400 hover:text-pink-400 ...">Careers</a>
</li>
```

**Option B: Create the Missing Files**

If you want to create these pages locally:

1. Create a new file named `about.html` in the same folder as `index.html`
2. Create files: `blog.html`, `contact.html`, `careers.html`
3. The links will automatically work

**Option C: Remove Links You Don't Need**

If you don't want certain pages, delete the entire `<li>` block:

```html
<!-- Remove careers link -->
<!-- <li>
    <a href="careers.html" class="text-gray-400 hover:text-pink-400 ...">Careers</a>
</li> -->
```

---

### 2.7 Footer Links - Legal Section

**Location:** Lines 833-851

**Current Code:**
```html
<div>
    <h4 class="text-lg font-bold text-white mb-6">Legal</h4>
    <ul class="space-y-3">
        <li>
            <a href="privacy.html" class="text-gray-400 hover:text-pink-400 ...">Privacy Policy</a>
        </li>
        <li>
            <a href="terms.html" class="text-gray-400 hover:text-pink-400 ...">Terms of Service</a>
        </li>
        <li>
            <a href="shipping.html" class="text-gray-400 hover:text-pink-400 ...">Shipping Info</a>
        </li>
        <li>
            <a href="returns.html" class="text-gray-400 hover:text-pink-400 ...">Returns & Refunds</a>
        </li>
    </ul>
</div>
```

**⚠️ These Files Also Don't Exist Yet!**

We'll cover how to create and link these in Section 3.

---

### 2.8 Footer Contact Information

**Location:** Lines 853-893

**Email Link:**
```html
<a href="mailto:iainhmunro@gmail.com" class="hover:text-pink-400 ...">iainhmunro@gmail.com</a>
```

**How to Update:**
1. Replace the email in `href="mailto:..."`
2. Replace the displayed email text

**Example:**
```html
<a href="mailto:hello@yourcompany.com" class="hover:text-pink-400 ...">hello@yourcompany.com</a>
```

**Website Link:**
```html
<a href="https://kcnailsukr.com/" target="_blank" rel="noopener noreferrer" class="hover:text-pink-400 ...">kcnailsukr.com</a>
```

**How to Update:**
1. Replace the URL in `href="..."`
2. Replace the displayed domain name

**Example:**
```html
<a href="https://yoursite.com/" target="_blank" rel="noopener noreferrer" class="hover:text-pink-400 ...">yoursite.com</a>
```

---

### 2.9 Footer Copyright and Bottom Links

**Location:** Lines 897-903

**Current Code:**
```html
<p class="text-gray-400">
    &copy; 2025 KCNails UKR. All rights reserved. | 
    <a href="privacy.html" class="hover:text-pink-400 ...">Privacy Policy</a> | 
    <a href="terms.html" class="hover:text-pink-400 ...">Terms of Service</a> | 
    <a href="blog.html" class="hover:text-pink-400 ...">Blog</a>
</p>
```

**How to Update:**

1. Change the company name and year:
```html
&copy; 2024 Your Company. All rights reserved.
```

2. Update the privacy and terms links (we'll cover this in Section 3)

3. Update the blog link if needed

---

### 2.10 Social Media Links

**Location:** Lines 769-784

**Current Code:**
```html
<div class="flex gap-4">
    <a href="#" class="w-10 h-10 rounded-full bg-gray-800 hover:bg-pink-500 flex items-center justify-center transition-colors duration-300" aria-label="Facebook">
        <i class="fab fa-facebook-f text-white"></i>
    </a>
    <a href="#" class="w-10 h-10 rounded-full bg-gray-800 hover:bg-pink-500 flex items-center justify-center transition-colors duration-300" aria-label="Instagram">
        <i class="fab fa-instagram text-white"></i>
    </a>
    <!-- More social icons -->
</div>
```

**⚠️ Current Status:** All social links point to `#` (nowhere)

**How to Update:**

Replace the `#` with your social media URLs:

```html
<!-- Facebook -->
<a href="https://facebook.com/yourpage" class="w-10 h-10 rounded-full bg-gray-800 hover:bg-pink-500 flex items-center justify-center transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f text-white"></i>
</a>

<!-- Instagram -->
<a href="https://instagram.com/yourprofile" class="w-10 h-10 rounded-full bg-gray-800 hover:bg-pink-500 flex items-center justify-center transition-colors duration-300" aria-label="Instagram">
    <i class="fab fa-instagram text-white"></i>
</a>

<!-- Twitter -->
<a href="https://twitter.com/yourhandle" class="w-10 h-10 rounded-full bg-gray-800 hover:bg-pink-500 flex items-center justify-center transition-colors duration-300" aria-label="Twitter">
    <i class="fab fa-twitter text-white"></i>
</a>

<!-- Pinterest -->
<a href="https://pinterest.com/yourprofile" class="w-10 h-10 rounded-full bg-gray-800 hover:bg-pink-500 flex items-center justify-center transition-colors duration-300" aria-label="Pinterest">
    <i class="fab fa-pinterest-p text-white"></i>
</a>
```

**Don't Have a Social Profile?**

Delete the link entirely:
```html
<!-- Remove this entire section if you don't have Instagram -->
<!-- <a href="https://instagram.com/..." ...>
    <i class="fab fa-instagram text-white"></i>
</a> -->
```

---

## Section 3: Linking Privacy and Terms Pages

This section shows you exactly how to create and link privacy and terms pages.

### 3.1 Understanding What's Needed

**Current Situation:**
- Your `index.html` has links to `privacy.html` and `terms.html`
- These files don't exist yet
- Clicking these links will result in a 404 error

**Solution:**
Create these files and add your privacy/terms content.

---

### 3.2 Creating the Privacy Policy Page

**Step 1: Create the File**

1. Open your text editor
2. Create a new file
3. Save it as `privacy.html` in the same folder as `index.html`

**Step 2: Add Basic Structure**

Copy this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - KCNails UKR">
    <title>Privacy Policy - KCNails UKR</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            scroll-behavior: smooth;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #ec4899 0%, #f97316 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 backdrop-filter backdrop-blur-lg bg-gray-900 bg-opacity-80 border-b border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <!-- Logo -->
                <div class="flex-shrink-0">
                    <a href="index.html" class="text-3xl font-bold gradient-text hover:opacity-80 transition-opacity">KCNails</a>
                </div>
                
                <!-- Navigation -->
                <nav class="hidden md:flex items-center gap-8">
                    <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Home</a>
                    <a href="index.html#faq" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">FAQ</a>
                    <a href="contact.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Contact</a>
                </nav>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="py-24 md:py-32 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold mb-8 leading-tight">
                Privacy Policy
            </h1>
            
            <div class="space-y-8 text-gray-300 leading-relaxed">
                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">1. Introduction</h2>
                    <p>
                        KCNails UKR ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and otherwise process your personal information in connection with our website and services.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">2. Information We Collect</h2>
                    <p>
                        We collect information you provide directly to us, such as when you:
                    </p>
                    <ul class="list-disc list-inside ml-4 mt-2 space-y-2">
                        <li>Create an account or place an order</li>
                        <li>Fill out a form or survey</li>
                        <li>Contact us with inquiries</li>
                        <li>Subscribe to our newsletter</li>
                        <li>Leave a review or testimonial</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">3. How We Use Your Information</h2>
                    <p>
                        We use the information we collect to:
                    </p>
                    <ul class="list-disc list-inside ml-4 mt-2 space-y-2">
                        <li>Process and fulfill your orders</li>
                        <li>Send you promotional materials and updates</li>
                        <li>Respond to your inquiries</li>
                        <li>Improve our website and services</li>
                        <li>Comply with legal obligations</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">4. Data Security</h2>
                    <p>
                        We implement appropriate technical and organizational measures to protect your personal information against unauthorized access, alteration, disclosure, or destruction. However, no method of transmission over the Internet is 100% secure.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">5. Your Rights</h2>
                    <p>
                        Depending on your location, you may have certain rights regarding your personal information, including the right to access, correct, or delete your data. Please contact us at iainhmunro@gmail.com to exercise these rights.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">6. Contact Us</h2>
                    <p>
                        If you have questions about this Privacy Policy or our privacy practices, please contact us at:
                    </p>
                    <p class="mt-2">
                        <strong>Email:</strong> <a href="mailto:iainhmunro@gmail.com" class="text-pink-400 hover:text-pink-300">iainhmunro@gmail.com</a><br>
                        <strong>Website:</strong> <a href="https://kcnailsukr.com/" target="_blank" rel="noopener noreferrer" class="text-pink-400 hover:text-pink-300">kcnailsukr.com</a>
                    </p>
                </section>

                <section class="border-t border-gray-700 pt-8">
                    <p class="text-sm text-gray-400">
                        Last Updated: January 2024
                    </p>
                </section>
            </div>

            <!-- Back Button -->
            <div class="mt-12">
                <a href="index.html" class="inline-flex items-center text-pink-400 hover:text-pink-300 transition-colors">
                    <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M15 19l-7-7 7-7"></path>
                    </svg>
                    Back to Home
                </a>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-950 border-t border-gray-800 py-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400">
                &copy; 2024 KCNails UKR. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

**Step 3: Customize the Content**

Replace the placeholder content with your actual privacy policy. Key sections to customize:

1. **Company Name** - Replace "KCNails UKR" with your company name
2. **Email Address** - Replace `iainhmunro@gmail.com` with your email
3. **Website URL** - Replace `https://kcnailsukr.com/` with your website
4. **Policy Content** - Update all sections with your actual privacy policy

---

### 3.3 Creating the Terms of Service Page

**Step 1: Create the File**

1. Open your text editor
2. Create a new file
3. Save it as `terms.html` in the same folder as `index.html`

**Step 2: Add Basic Structure**

Copy this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - KCNails UKR">
    <title>Terms of Service - KCNails UKR</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            scroll-behavior: smooth;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #ec4899 0%, #f97316 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 backdrop-filter backdrop-blur-lg bg-gray-900 bg-opacity-80 border-b border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <!-- Logo -->
                <div class="flex-shrink-0">
                    <a href="index.html" class="text-3xl font-bold gradient-text hover:opacity-80 transition-opacity">KCNails</a>
                </div>
                
                <!-- Navigation -->
                <nav class="hidden md:flex items-center gap-8">
                    <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Home</a>
                    <a href="index.html#faq" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">FAQ</a>
                    <a href="contact.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Contact</a>
                </nav>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="py-24 md:py-32 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold mb-8 leading-tight">
                Terms of Service
            </h1>
            
            <div class="space-y-8 text-gray-300 leading-relaxed">
                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">1. Acceptance of Terms</h2>
                    <p>
                        By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">2. Use License</h2>
                    <p>
                        Permission is granted to temporarily download one copy of the materials (information or software) on KCNails UKR's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside ml-4 mt-2 space-y-2">
                        <li>Modifying or copying the materials</li>
                        <li>Using the materials for any commercial purpose or for any public display</li>
                        <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                        <li>Removing any copyright or other proprietary notations from the materials</li>
                        <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">3. Disclaimer</h2>
                    <p>
                        The materials on KCNails UKR's website are provided on an 'as is' basis. KCNails UKR makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">4. Limitations</h2>
                    <p>
                        In no event shall KCNails UKR or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on KCNails UKR's website.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">5. Accuracy of Materials</h2>
                    <p>
                        The materials appearing on KCNails UKR's website could include technical, typographical, or photographic errors. KCNails UKR does not warrant that any of the materials on its website are accurate, complete, or current. KCNails UKR may make changes to the materials contained on its website at any time without notice.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">6. Links</h2>
                    <p>
                        KCNails UKR has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by KCNails UKR of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">7. Modifications</h2>
                    <p>
                        KCNails UKR may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">8. Governing Law</h2>
                    <p>
                        These terms and conditions are governed by and construed in accordance with the laws of Ukraine and you irrevocably submit to the exclusive jurisdiction of the courts located in Ukraine.
                    </p>
                </section>

                <section class="border-t border-gray-700 pt-8">
                    <p class="text-sm text-gray-400">
                        Last Updated: January 2024
                    </p>
                </section>
            </div>

            <!-- Back Button -->
            <div class="mt-12">
                <a href="index.html" class="inline-flex items-center text-pink-400 hover:text-pink-300 transition-colors">
                    <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M15 19l-7-7 7-7"></path>
                    </svg>
                    Back to Home
                </a>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-950 border-t border-gray-800 py-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400">
                &copy; 2024 KCNails UKR. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

**Step 3: Customize the Content**

Update the same elements as the privacy policy:
1. Company name
2. Email address
3. Website URL
4. Policy content

---

### 3.4 Verifying Links Work

**Step 1: Test the Links**

1. Save all files (`index.html`, `privacy.html`, `terms.html`)
2. Open `index.html` in your browser
3. Scroll to the footer
4. Click on "Privacy Policy" and "Terms of Service" links
5. They should now open the new pages!

**Step 2: Check the Back Links**

1. On the privacy or terms page, click "Back to Home"
2. You should return to the main page

**Step 3: Test All Link Locations**

Privacy and Terms links appear in multiple places:
- Footer Legal section (Lines 833-851)
- Footer bottom links (Line 903)

Click all of them to ensure they work!

---

### 3.5 Customizing the Policy Pages

**Edit Company Information:**

In both `privacy.html` and `terms.html`, find and update:

```html
<!-- Change this email -->
<a href="mailto:iainhmunro@gmail.com" class="text-pink-400 hover:text-pink-300">iainhmunro@gmail.com</a>

<!-- Change this website -->
<a href="https://kcnailsukr.com/" target="_blank" rel="noopener noreferrer" class="text-pink-400 hover:text-pink-300">kcnailsukr.com</a>

<!-- Change this company name -->
KCNails UKR
```

**Update the "Last Updated" Date:**

Find this line in both files:
```html
<p class="text-sm text-gray-400">
    Last Updated: January 2024
</p>
```

Replace with current date:
```html
<p class="text-sm text-gray-400">
    Last Updated: December 2024
</p>
```

**Adding More Content:**

To add more sections, copy this structure:

```html
<section>
    <h2 class="text-2xl font-bold text-white mb-4">Your Section Title</h2>
    <p>
        Your content goes here. You can add multiple paragraphs.
    </p>
    <ul class="list-disc list-inside ml-4 mt-2 space-y-2">
        <li>Bullet point 1</li>
        <li>Bullet point 2</li>
        <li>Bullet point 3</li>
    </ul>
</section>
```

---

### 3.6 Making Policy Pages Mobile-Friendly

The templates provided are already mobile-responsive, but here are key responsive classes:

- `max-w-4xl` - Limits width on large screens
- `px-4 sm:px-6 lg:px-8` - Adds padding on all screen sizes
- `py-24 md:py-32` - Different padding for mobile vs desktop
- `text-4xl md:text-5xl` - Different font sizes

These classes automatically adjust the layout for phones, tablets, and desktops!

---

### 3.7 Optional: Creating Additional Policy Pages

You can create similar pages for other policies:

**Shipping Policy (`shipping.html`):**
```html
<h1 class="text-4xl md:text-5xl font-bold mb-8 leading-tight">
    Shipping Information
</h1>

<section>
    <h2 class="text-2xl font-bold text-white mb-4">Shipping Methods</h2>
    <p>
        We offer standard and express shipping options...
    </p>
</section>
```

**Returns & Refunds (`returns.html`):**
```html
<h1 class="text-4xl md:text-5xl font-bold mb-8 leading-tight">
    Returns & Refunds
</h1>

<section>
    <h2 class="text-2xl font-bold text-white mb-4">Return Policy</h2>
    <p>
        We offer a 30-day return policy...
    </p>
</section>
```

Then update the footer links in `index.html` to point to these new pages:

```html
<li>
    <a href="shipping.html" class="text-gray-400 hover:text-pink-400 ...">Shipping Info</a>
</li>
<li>
    <a href="returns.html" class="text-gray-400 hover:text-pink-400 ...">Returns & Refunds</a>
</li>
```

---

## Troubleshooting Tips

### Links Not Working

**Problem:** Clicking a link does nothing or shows an error

**Solutions:**

1. **Check the URL spelling:**
   - `href="privacy.html"` ✓ Correct
   - `href="privacy.Html"` ✗ Wrong (case-sensitive)
   - `href="privacy"` ✗ Wrong (missing .html)

2. **Check file location:**
   - All files must be in the same folder
   - Folder structure should look like:
     ```
     project-folder/
     ├── index.html
     ├── privacy.html
     ├── terms.html
     └── other-files.html
     ```

3. **Hard refresh your browser:**
   - Windows: Ctrl+Shift+R
   - Mac: Cmd+Shift+R
   - This clears cached files that might be outdated

4. **Check console for errors:**
   - Right-click → Inspect
   - Click "Console" tab
   - Look for red error messages

---

### Styling Issues

**Problem:** Text colors or layout looks wrong

**Solutions:**

1. **Check for typos in class names:**
   - `text-gray-300` ✓ Correct
   - `text-gray-30` ✗ Wrong (should be 300)
   - `text-gray300` ✗ Wrong (missing hyphen)

2. **Make sure you didn't delete CSS:**
   - The `<style>` section at the top should remain unchanged
   - If deleted, copy it back from the original

3. **Check for missing closing tags:**
   - Every `<div>` needs a `</div>`
   - Every `<p>` needs a `</p>`
   - Every `<a>` needs a `</a>`

---

### Text Not Displaying Correctly

**Problem:** Text appears cut off or overlapped

**Solutions:**

1. **Check for missing spaces:**
   ```html
   <!-- Wrong - no space between words -->
   <p>HelloWorld</p>
   
   <!-- Correct -->
   <p>Hello World</p>
   ```

2. **Check for proper line breaks:**
   - Long text should wrap naturally
   - Use `<br>` tag only when needed

3. **Check text length:**
   - Very long text might overflow containers
   - Consider breaking into multiple paragraphs

---

### Mobile Menu Not Working

**Problem:** Mobile menu doesn't open/close

**Solutions:**

1. **Check JavaScript section:**
   - Don't modify the JavaScript code (Lines 911-960)
   - Make sure it's not deleted

2. **Check mobile menu button:**
   - The button should have class `mobile-menu-button`
   - The menu should have class `mobile-menu`

3. **Test on actual mobile device:**
   - Use browser DevTools (F12) to view mobile version
   - Click the hamburger menu icon

---

### Page Layout Broken

**Problem:** Page looks completely wrong or elements are misaligned

**Solutions:**

1. **Check for accidental deletions:**
   - Compare your file with the original
   - Look for missing closing tags

2. **Validate HTML:**
   - Use online HTML validator: https://validator.w3.org/
   - Upload your HTML file
   - Fix any errors reported

3. **Check Tailwind CSS:**
   - Make sure this line is still in the `<head>`:
     ```html
     <script src="https://cdn.tailwindcss.com"></script>
     ```

4. **Clear browser cache:**
   - Ctrl+Shift+Delete (Windows)
   - Cmd+Shift+Delete (Mac)

---

## Best Practices

### 1. Always Make Backups

Before making major changes:
1. Copy the entire `index.html` file
2. Rename it to `index-backup.html`
3. Keep it safe in case you need to revert

**How to restore from backup:**
1. Delete the broken `index.html`
2. Rename `index-backup.html` to `index.html`
3. Start over with smaller changes

---

### 2. Make Changes Incrementally

Don't change everything at once. Instead:

1. Change one section
2. Save the file
3. Test in browser
4. If it looks good, move to next section
5. If it breaks, undo that change

---

### 3. Use Find & Replace Carefully

When using Find & Replace (Ctrl+H):

1. **Preview first:** Click "Find All" to see all matches
2. **Replace one at a time:** Don't use "Replace All" immediately
3. **Check context:** Make sure you're replacing the right things

**Example - Changing company name:**
- Find: `KCNails UKR`
- Replace with: `Your Company`
- Click "Find All" first to see all 20+ instances
- Verify they're all correct before replacing

---

### 4. Keep Consistent Formatting

**For text:**
- Use same capitalization throughout
- "Sign Up" or "sign up" - pick one and stick with it

**For colors:**
- Use same color scheme throughout
- If you change pink to blue, change all instances

**For spacing:**
- Keep similar margins and padding
- Don't mix `mb-4` and `mb-6` randomly

---

### 5. Test on Multiple Devices

After making changes:

1. **Desktop:** View at full width
2. **Tablet:** Resize browser to ~768px width
3. **Mobile:** Resize browser to ~375px width
4. **Real devices:** Test on actual phone if possible

Use browser DevTools (F12) → Click device icon to test different sizes.

---

### 6. Keep External Links Updated

When you update a link:
1. Make sure the destination page exists
2. Test the link works
3. Verify it opens in correct tab (new tab for external, same tab for internal)

---

### 7. Document Your Changes

Keep a simple list of what you changed:

```
CHANGES MADE:
- Updated hero headline
- Changed "Shop Now" URL to https://mysite.com/products
- Created privacy.html and terms.html
- Updated footer email to hello@mycompany.com
- Changed color scheme from pink/orange to blue/purple
```

This helps if you need to remember what you did later!

---

### 8. Version Control (Optional but Recommended)

If you're comfortable with Git:

```bash
git init
git add .
git commit -m "Initial landing page"
git commit -m "Updated company information"
git commit -m "Created policy pages"
```

This lets you revert to any previous version if needed.

---

### 9. Performance Optimization

**To keep your site fast:**

1. Don't add too many large images
2. Compress images before uploading
3. Minimize custom CSS
4. Use CDN links (already done in template)

---

### 10. Accessibility Considerations

**To make your site accessible:**

1. Always use proper heading hierarchy (h1, h2, h3)
2. Include `alt` text for images
3. Use sufficient color contrast
4. Test with keyboard navigation (Tab key)
5. Include `aria-label` on icon-only buttons

---

## Quick Reference Checklist

Use this checklist when making updates:

### Text Updates
- [ ] Header logo text
- [ ] Navigation menu items
- [ ] Hero headline (both lines)
- [ ] Hero description
- [ ] Feature titles (3 cards)
- [ ] Feature descriptions (3 cards)
- [ ] Feature bullet points (9 total)
- [ ] Benefit titles (3 cards)
- [ ] Benefit descriptions (3 cards)
- [ ] About Us heading and paragraphs
- [ ] Testimonial quotes (4)
- [ ] Customer names and titles (4)
- [ ] FAQ questions (5)
- [ ] FAQ answers (5)

### Link Updates
- [ ] Desktop navigation links
- [ ] Mobile navigation links
- [ ] All "Shop Now" buttons (4 instances)
- [ ] Footer Quick Links
- [ ] Footer Company Links
- [ ] Footer Legal Links
- [ ] Social media links
- [ ] Email link in footer
- [ ] Website URL in footer
- [ ] Copyright year

### Policy Pages
- [ ] Create `privacy.html`
- [ ] Create `terms.html`
- [ ] Update email in both files
- [ ] Update website URL in both files
- [ ] Update company name in both files
- [ ] Test all links from index.html

### Testing
- [ ] All internal section links work
- [ ] All external links open correctly
- [ ] Mobile menu opens/closes
- [ ] Responsive on phone, tablet, desktop
- [ ] No console errors (F12)
- [ ] All text displays correctly

---

## Final Thoughts

Congratulations! You now have a comprehensive understanding of how to maintain and customize the KCNails UKR landing page. 

**Remember:**
- Start small with simple text changes
- Test frequently as you make changes
- Keep backups of working versions
- Don't be afraid to experiment!
- Refer back to this guide whenever you need help

If you encounter any issues not covered in this guide, try:
1. Checking the HTML validator (validator.w3.org)
2. Using browser DevTools (F12) to inspect elements
3. Comparing your code with the original template
4. Taking a screenshot of the error for reference

Good luck with your landing page! 🎉