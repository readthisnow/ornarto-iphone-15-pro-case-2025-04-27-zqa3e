# Ornarto Landing Page - Maintenance Guide

This guide will help you maintain and customize the Ornarto iPhone case landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the navigation menu and logo. To modify:

```html
<!-- Located at the top of the page -->
<header class="fixed w-full bg-white/95 backdrop-blur-sm z-50 border-b border-gray-100">
    <nav class="container mx-auto px-4 sm:px-6 lg:px-8 py-4">
        <!-- Change logo text here -->
        <a href="#" class="text-2xl font-bold text-gray-800">Ornarto</a>
```

To update:
1. Change logo text by modifying "Ornarto"
2. Adjust logo size by changing `text-2xl` to `text-3xl` or `text-xl`
3. Modify background transparency by changing `bg-white/95`

### Hero Section
The main promotional section appears below the header:

```html
<section class="pt-32 pb-20 bg-gradient-to-b from-blue-50 to-white">
    <!-- Main heading -->
    <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
        Koop Ornarto iPhone 15 Pro Case Met Korting
    </h1>
```

To customize:
1. Update heading text between the `<h1>` tags
2. Modify text size using Tailwind classes:
   - `text-4xl`: Mobile size
   - `md:text-5xl`: Tablet size
   - `lg:text-6xl`: Desktop size

### Feature Cards
Located in the features section:

```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Maximale Bescherming</h3>
    <p class="text-gray-600">Militaire valbeveiliging voor optimale bescherming...</p>
</div>
```

To modify feature cards:
1. Change heading text in `<h3>` tags
2. Update description in `<p>` tags
3. Adjust spacing using `mb-4` (margin-bottom) classes
4. Modify shadow effects using `shadow-lg` or `shadow-xl`

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors">FAQ</a>
</div>
```

To update links:
1. Change internal section links by modifying `href="#section-name"`
2. For external links, replace with full URL: `href="https://example.com"`
3. Update link text between `<a>` tags

### Call-to-Action Buttons
Currently using Amazon affiliate links:

```html
<a href="https://amzn.to/42PiMQ7" class="bg-blue-600 text-white px-6 py-2 rounded-full hover:bg-blue-700 transition-colors">
    Koop Nu
</a>
```

To update:
1. Replace `href` with your new product link
2. Modify button text between `<a>` tags
3. Adjust button styling using Tailwind classes:
   - `bg-blue-600`: Background color
   - `px-6 py-2`: Padding
   - `rounded-full`: Border radius

## Adding Privacy and Terms Pages

### Footer Links
Located at the bottom of the page:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Links</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Terms & Conditions</a></li>
    </ul>
</div>
```

To add policy pages:
1. Create new files:
   ```
   privacy.html
   terms.html
   ```

2. Update footer links:
   ```html
   <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
   <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors">Terms & Conditions</a></li>
   ```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in section names
   - Section IDs should be lowercase with no spaces

2. **Responsive Design Issues**
   - Check mobile-first classes (no prefix)
   - Verify tablet classes (md: prefix)
   - Confirm desktop classes (lg: prefix)

3. **Style Changes Not Appearing**
   - Verify Tailwind CSS CDN link is working
   - Check class spelling matches Tailwind conventions
   - Clear browser cache

For additional help:
- Consult [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools (F12) to inspect elements
- Test on multiple devices and browsers

Remember to always make a backup before making significant changes to the code.