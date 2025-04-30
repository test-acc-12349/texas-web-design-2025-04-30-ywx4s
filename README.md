# Texas Web Design Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Logo (TWD)**
```html
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```
- Replace "TWD" with your company name
- Adjust text size using `text-2xl` (options: text-lg, text-xl, text-3xl)
- Change color using `text-blue-600` (options: text-red-600, text-green-600)

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">Best Websites In Texas</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Professional web design services tailored for Texas businesses</p>
```
To modify:
1. Change headline text between `<h1>` tags
2. Update subheading between `<p>` tags
3. Responsive text sizes are defined as:
   - Mobile: `text-4xl`
   - Tablet: `md:text-5xl`
   - Desktop: `lg:text-6xl`

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 rounded-2xl bg-white shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included with every website package at no additional cost.</p>
</div>
```
To update:
1. Change feature title between `<h3>` tags
2. Modify description between `<p>` tags
3. Keep the existing classes for consistent styling

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Replace `href="#features"` with your desired URL
2. For internal page sections, keep the `#` prefix
3. For external links, use complete URLs (e.g., `href="https://example.com"`)

### Call-to-Action Buttons
Current placeholder link:
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">Start Your Project</a>
```
Replace `https://twd.com` with your actual website URL or contact page.

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your website directory
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Example: `href="#FAQ"` won't work if section is `id="faq"`

2. **Responsive Design Issues**
   - Check that you maintain the responsive classes:
     - `md:` prefix for tablet
     - `lg:` prefix for desktop
   - Don't remove `container` and `mx-auto` classes from section wrappers

3. **Social Media Icons Not Showing**
   - Verify SVG paths are complete
   - Keep the `currentColor` fill attribute for proper color inheritance

### Need Help?
If you encounter issues:
1. Check class names match exactly (Tailwind is case-sensitive)
2. Verify all opening tags have corresponding closing tags
3. Maintain the existing structure of container divs
4. Keep the responsive design classes intact

Remember to test all changes across different screen sizes using your browser's developer tools (F12 or right-click → Inspect).