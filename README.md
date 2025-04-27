# Delightful Bean Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Delightful Bean conference coffee service landing page.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Delightful Bean  <!-- Edit this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Edit menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
The main banner section contains:

1. **Main Heading:**
```html
<h1 class="text-4xl md:text-5xl lg:text-7xl font-extrabold mb-6 bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Clearwater Conference Coffee Service  <!-- Edit main headline -->
</h1>
```

2. **Subheading:**
```html
<p class="text-xl md:text-2xl lg:text-3xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Keeping Clearwater event attendees energized and engaged  <!-- Edit subheading -->
</p>
```

### Understanding Tailwind Classes

Key class patterns used throughout:
- Responsive prefixes: `md:`, `lg:` (applies styles at different screen sizes)
- Spacing: `px-6`, `py-4` (padding), `mb-6` (margin)
- Colors: `text-gray-300`, `bg-gray-900`
- Flexbox: `flex`, `items-center`, `justify-center`

Example of modifying responsive text size:
```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-7xl">

<!-- Making text smaller -->
<h1 class="text-3xl md:text-4xl lg:text-6xl">
```

## Managing Links

### Current Link Structure

1. **Navigation Menu Links:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

2. **Call-to-Action Links:**
```html
<a href="https://www.delightfulbean.com/" class="inline-block px-8 py-4...">
    Book Your Service
</a>
```

### Updating Links

1. Replace placeholder URLs:
```html
<!-- Find all instances of delightfulbean.com and replace with your domain -->
<a href="https://www.delightfulbean.com/" class="...">
<!-- Change to -->
<a href="https://www.your-domain.com/" class="...">
```

2. Update email links:
```html
<a href="mailto:info@delightfulbean.com">
<!-- Change to -->
<a href="mailto:your-email@domain.com">
```

## Adding Privacy and Terms Pages

### Footer Modification

1. Add new links to the Quick Links section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
        <!-- Add these new lines -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Alternative Footer Layout

For a dedicated legal links section:
```html
<!-- Add before the copyright notice -->
<div class="mt-8 text-center">
    <div class="space-x-4">
        <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
        <span class="text-gray-600">|</span>
        <a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
    </div>
</div>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links:**
- Ensure section IDs match href attributes
- Check for typos in href values
- Verify file paths are correct relative to index.html

2. **Responsive Design Issues:**
- Check responsive prefixes (md:, lg:) are properly ordered
- Verify container classes are present
- Test on multiple screen sizes

3. **Gradient Text Not Showing:**
- Ensure all three classes are present:
  ```html
  bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent
  ```

For additional help or questions, please refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Alpine.js Documentation](https://alpinejs.dev/)