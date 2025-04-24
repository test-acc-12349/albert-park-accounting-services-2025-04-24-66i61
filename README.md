# Modern Landing Page - Maintenance Guide

This guide will help you maintain and customize the Modern Landing Page template. Whether you're new to web development or need a quick reference, follow these instructions to make updates while preserving the design integrity.

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
<a href="#" class="text-xl font-bold">Logo</a>
```
Replace "Logo" with your company name. Example:
```html
<a href="#" class="text-xl font-bold">MyCompany</a>
```

2. **Navigation Menu Items**
```html
<a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Home</a>
```
- Update text between `<a>` tags
- Keep the classes to maintain hover effects
- Don't remove `transition-colors duration-200` as it ensures smooth color changes

### Hero Section
Located right below the header, this is your main attention-grabbing area:

1. **Main Heading**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">
    Welcome to Our Modern Platform
</h1>
```
- Replace the text while keeping the classes
- The different text sizes (`text-4xl`, `text-5xl`, `text-6xl`) ensure proper scaling on different devices

2. **Subheading**
```html
<p class="text-xl text-gray-600 max-w-2xl mx-auto mb-12">
    Transform your digital experience with our cutting-edge solution.
</p>
```
- Update the text between the `<p>` tags
- Keep `max-w-2xl` and `mx-auto` to maintain centered alignment

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl border border-gray-100 hover:shadow-lg transition-all duration-200">
    <div class="w-12 h-12 bg-blue-100 rounded-xl flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Lightning Fast</h3>
    <p class="text-gray-600">Experience blazing fast performance with our optimized platform.</p>
</div>
```
To add new feature cards:
1. Copy the entire `<div>` block
2. Paste within the grid container
3. Update the heading and description text
4. Modify the icon SVG as needed

## Managing Links

### Navigation Menu Links
Current placeholder links are marked with `#`:
```html
<a href="#" class="text-gray-600 hover:text-gray-900">Home</a>
```
To update:
1. Replace `#` with your actual URL:
   ```html
   <a href="/home.html" class="text-gray-600 hover:text-gray-900">Home</a>
   ```
2. For external links, use complete URLs:
   ```html
   <a href="https://example.com" class="text-gray-600 hover:text-gray-900">External Link</a>
   ```

### Call-to-Action (CTA) Links
Located in the hero and CTA sections:
```html
<a href="#" class="px-8 py-4 bg-blue-600 text-white rounded-full">Get Started</a>
```
- Update `href="#"` to point to your signup or contact page
- Keep all styling classes to maintain button appearance

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the footer section:

1. Locate the footer links section:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Company</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-200">About</a></li>
        <!-- Add new links here -->
    </ul>
</div>
```

2. Add new links with matching styles:
```html
<li><a href="/privacy.html" class="hover:text-white transition-colors duration-200">Privacy Policy</a></li>
<li><a href="/terms.html" class="hover:text-white transition-colors duration-200">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Styles**
- Make sure the Tailwind CDN link is present in the header:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
- Check that all class names are spelled correctly
- Verify that classes haven't been accidentally deleted

2. **Responsive Design Issues**
- Look for classes starting with `md:` or `lg:` - these control tablet and desktop layouts
- Don't remove these classes as they ensure proper scaling
- Test your page at different screen sizes

3. **Link Problems**
- Verify all file paths are correct
- Use relative paths (`/about.html`) for internal pages
- Use full URLs (`https://...`) for external links

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for styling references
- Validate your HTML using [W3C Validator](https://validator.w3.org/)
- Test all links before deploying changes

Remember to always backup your files before making significant changes, and test your updates across different browsers and devices.