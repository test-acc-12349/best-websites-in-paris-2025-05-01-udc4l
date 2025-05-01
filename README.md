# Landing Page Maintenance Guide

This guide will help you maintain and customize the Paris Web landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections Overview
The landing page is divided into these key sections:
- Header (navigation)
- Hero section
- Features
- Benefits
- FAQ
- CTA (Call to Action)
- Footer

### Updating Text Content

#### Hero Section
```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">Best Websites In Paris</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Custom Websites For Your Business</p>

<!-- Example change -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">Your New Heading Here</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Your New Subheading Here</p>
```

#### Features Section
Each feature card follows this structure:
```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-600 leading-relaxed">Intuitive interface designed for the best user experience.</p>
</div>
```

### Understanding Tailwind Classes

Key class patterns used throughout:
- Text sizes: `text-sm`, `text-xl`, `text-2xl`, etc.
- Colors: `text-gray-600`, `bg-blue-600`, etc.
- Spacing: `p-8` (padding), `mb-4` (margin-bottom)
- Responsive design: `md:text-5xl` (applies at medium screens)

Example of modifying a button:
```html
<!-- Original -->
<a href="#" class="inline-block px-6 py-2 bg-blue-600 text-white rounded-full hover:bg-blue-700">

<!-- Making it larger -->
<a href="#" class="inline-block px-8 py-3 bg-blue-600 text-white rounded-full hover:bg-blue-700">
```

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the text between the tags

Example:
```html
<!-- Original -->
<a href="#features">Features</a>

<!-- Updated -->
<a href="#services">Services</a>
```

### External Links
The landing page contains these external links:
- "Get Started" button: `https://sigmaseo.io`
- "Start Your Project" button: `https://sigmaseo.io`
- "Contact Us Today" button: `https://sigmaseo.io`

To update:
```html
<!-- Original -->
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">

<!-- Updated -->
<a href="https://yournewdomain.com" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">
```

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Creating Policy Pages
1. Create new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

Common issues and solutions:

### Broken Links
- Check for typos in `href` attributes
- Ensure file names match exactly (case-sensitive)
- Verify file locations relative to index.html

### Styling Issues
- Make sure Tailwind CDN link is present in the head section
- Check for missing or mistyped class names
- Verify responsive classes use correct breakpoints (`sm:`, `md:`, `lg:`)

### Layout Problems
- Inspect container widths and padding
- Verify grid column settings
- Check for missing closing tags

Need more help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).