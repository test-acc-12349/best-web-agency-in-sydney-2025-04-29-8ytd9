# Landing Page Maintenance Guide

This guide will help you maintain and customize the WebAgency landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this section in the header -->
<div class="text-2xl font-bold text-white">
    WebAgency  <!-- Change this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update text here -->
    <a href="#benefits">Benefits</a>  <!-- Update text here -->
    <a href="#faq">FAQ</a>           <!-- Update text here -->
    <a href="#contact">Contact</a>    <!-- Update text here -->
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 bg-gradient-to-r from-blue-400 to-purple-500 text-transparent bg-clip-text">
    Best Web Agency In Sydney  <!-- Change headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-400 mb-12">
    Grow your business with clicks  <!-- Change subheading here -->
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-4`, `mb-8`)
- `py-[size]`: Adds padding top and bottom
- `px-[size]`: Adds padding left and right
- `bg-[color]`: Sets background color

Example of modifying a button:
```html
<!-- Original button -->
<button class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-2 rounded-full">

<!-- To make button larger -->
<button class="bg-blue-600 hover:bg-blue-700 text-white px-8 py-4 rounded-full">
```

## Fixing Broken Links

### Navigation Menu Links
All internal links use anchor tags (#):
```html
<!-- Current internal links -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>

<!-- To link to external page, replace # with full URL -->
<a href="https://your-site.com/features">Features</a>
```

### Social Media Links
Located in the footer, update these placeholder links:
```html
<!-- Find these in the footer section -->
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white">
        <i class="fab fa-twitter"></i>
    </a>
    <!-- Replace # with your social media URLs -->
    <!-- Example: -->
    <a href="https://twitter.com/your-handle" class="text-gray-400 hover:text-white">
```

### Contact Email
Update the email address in two locations:
```html
<!-- In the contact section -->
<a href="mailto:contact@example.com">
    contact@example.com
</a>

<!-- In the footer -->
<p class="text-gray-400">contact@example.com</p>
```

## Adding Privacy and Terms Pages

### Step 1: Add Links to Footer
Insert new links in the Quick Links section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Add these new lines -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
        <!-- Existing links -->
        <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
```

### Step 2: Create New Pages
Create `privacy.html` and `terms.html` in your root directory using the same styling:
```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="bg-gray-900 text-gray-100">
    <!-- Copy header from index.html -->
    
    <main class="pt-32 px-6">
        <div class="container mx-auto max-w-3xl">
            <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
            <!-- Add your privacy policy content here -->
        </div>
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

### Common Issues:

1. **Broken Layout:**
   - Check that all Tailwind CSS classes are spelled correctly
   - Verify container divs are properly closed
   - Ensure responsive classes (md:, lg:) are used correctly

2. **Links Not Working:**
   - Verify href attributes start with # for internal links
   - Check that section IDs match href values
   - Ensure external URLs include https://

3. **Icons Not Showing:**
   - Verify Font Awesome CDN link in head section
   - Check icon class names against Font Awesome documentation

Need help? Contact your developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).