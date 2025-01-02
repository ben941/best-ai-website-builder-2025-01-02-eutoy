# Landing Page Maintenance Guide

Welcome to the maintenance guide for your AI Website Builder landing page. This document will help you make common updates and modifications safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Find this line and change "BAI":
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">BAI</a>
```

2. **Navigation Links**: Located in the header's `<nav>` element:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <!-- Add or modify links here -->
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-6xl font-bold mb-6">Best AI Website Builder for Non-Coders</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">Create stunning websites without writing a single line of code</p>
```

> 💡 Tip: The `md:text-6xl` means the text will be larger on medium-sized screens and above.

### Modifying Tailwind Classes

Common classes explained:
- `text-gray-300`: Light gray text
- `mb-6`: Margin bottom (spacing)
- `px-6`: Horizontal padding
- `py-4`: Vertical padding
- `rounded-full`: Circular corners
- `hover:scale-105`: Grows slightly on hover

To change colors, replace existing color classes:
```html
from-purple-500 to-pink-500  <!-- Current gradient -->
from-blue-500 to-green-500   <!-- Example alternative -->
```

## Fixing Broken Links

### Current Link Structure
1. **Navigation Links**:
   ```html
   <a href="#features">Features</a>
   <a href="#benefits">Benefits</a>
   <a href="#faq">FAQ</a>
   <a href="#contact">Contact</a>
   ```

2. **Call-to-Action Links**:
   ```html
   <a href="https://bai.com" class="...">Get Started</a>
   ```
   Replace `https://bai.com` with your actual website URL.

### How to Update Links:
1. For internal section links:
   ```html
   <a href="#sectionName">Link Text</a>
   ```
   Ensure the section has matching ID:
   ```html
   <section id="sectionName">
   ```

2. For external links:
   ```html
   <a href="https://your-actual-domain.com">Link Text</a>
   ```

> ⚠️ Warning: Always test links after updating them to ensure they work correctly.

## Linking Privacy and Terms Pages

### Current Footer Structure
```html
<div>
    <h4 class="font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages:
1. Create new files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

3. Maintain consistent styling by copying these classes:
```html
class="hover:text-white transition-colors duration-300"
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Layout**
   - Check for missing closing tags
   - Verify all `div` elements are properly nested
   - Ensure Tailwind CSS CDN is loading

2. **Links Not Working**
   - Confirm file names match exactly
   - Check for proper path structure
   - Verify IDs match href attributes

3. **Colors Not Showing**
   - Ensure gradient classes are properly formatted
   - Check for conflicting color classes
   - Verify class names are spelled correctly

> 🔍 Need Help? Use browser developer tools (F12) to inspect elements and identify issues.

Remember to always make a backup before making significant changes to your landing page.