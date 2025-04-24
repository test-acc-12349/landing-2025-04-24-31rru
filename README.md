# Modern Landing Page - Maintenance Guide

This guide will help you customize and maintain your landing page, even if you're new to web development. Follow these detailed instructions to make common updates while preserving the design integrity.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this line in the header section -->
<a href="#" class="text-2xl font-bold text-gray-900">Logo</a>
```
Replace "Logo" with your company name or brand.

2. **Navigation Links**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#" class="text-gray-600 hover:text-gray-900">Features</a>
    <a href="#" class="text-gray-600 hover:text-gray-900">Benefits</a>
    <a href="#" class="text-gray-600 hover:text-gray-900">Testimonials</a>
</div>
```
Modify the text between `<a>` tags to change menu items.

### Hero Section
The main headline and subheading are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Transform Your Digital Presence
</h1>
<p class="text-xl text-gray-600 mb-12">
    Create stunning experiences that convert visitors into customers...
</p>
```

To modify:
- Replace the h1 text for your main headline
- Update the paragraph text for your subheading
- Keep the existing classes to maintain responsive sizing

### Understanding Tailwind Classes

Key class patterns used in this page:
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-{number}`: Adds margin bottom (4, 8, 12, etc.)
- `py-{number}`: Adds padding top and bottom
- `px-{number}`: Adds padding left and right
- `bg-{color}-{shade}`: Sets background color

Example modification:
```html
<!-- Original -->
<div class="bg-blue-600 text-white px-6 py-3">

<!-- Modified for green theme -->
<div class="bg-green-600 text-white px-6 py-3">
```

## Managing Links

### Navigation Menu Links

1. Locate the navigation section:
```html
<nav class="container mx-auto px-4 sm:px-6 lg:px-8">
```

2. Update href attributes:
```html
<!-- Before -->
<a href="#" class="text-gray-600">Features</a>

<!-- After -->
<a href="/features.html" class="text-gray-600">Features</a>
```

### Button Links

Find call-to-action buttons:
```html
<a href="#" class="inline-flex items-center justify-center px-8 py-4">
    Get Started Now
</a>
```

Replace "#" with your target URL:
```html
<a href="https://your-signup-page.com" class="inline-flex items-center justify-center px-8 py-4">
    Get Started Now
</a>
```

## Adding Privacy and Terms Pages

### Footer Link Setup

1. Locate the legal section in the footer:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

2. Update the href attributes:
```html
<li><a href="/privacy.html" class="hover:text-white">Privacy Policy</a></li>
<li><a href="/terms.html" class="hover:text-white">Terms of Service</a></li>
```

3. Create matching HTML files:
- Create `privacy.html` and `terms.html` in your root directory
- Copy the header and footer from `index.html` to maintain consistent styling
- Add your policy content between the header and footer

## Troubleshooting

Common issues and solutions:

1. **Broken Responsive Design**
   - If elements look wrong on mobile, check that you've kept all `md:` and `lg:` prefixed classes
   - Don't remove the `container` class from parent elements

2. **Inconsistent Button Styling**
   - When adding new buttons, copy the entire class string from an existing button
   - Example button class string:
   ```html
   class="inline-flex items-center justify-center px-8 py-4 text-lg font-semibold text-white bg-blue-600 rounded-full hover:bg-blue-700 transition-all duration-300 transform hover:scale-105"
   ```

3. **Missing Fonts**
   - Ensure the Inter font link remains in the head section:
   ```html
   <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
   ```

Remember to:
- Test all links after updating
- View changes on both desktop and mobile devices
- Keep backup copies of working files before making changes
- Maintain consistent spacing and indentation in your HTML

Need more help? Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your web development team.