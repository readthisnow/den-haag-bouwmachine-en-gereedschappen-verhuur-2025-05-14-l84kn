# Den Haag Verhuur Landing Page - Maintenance Guide

This guide will help you maintain and customize the Den Haag Verhuur landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. Change company name:
```html
<!-- Find this section in the header -->
<div class="text-xl font-bold text-gray-800">
    Den Haag Verhuur  <!-- Replace this text -->
</div>
```

2. Modify navigation items:
```html
<div class="hidden md:flex space-x-8">
    <!-- Each link can be modified here -->
    <a href="#diensten" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Diensten</a>
```

### Hero Section
The main banner section at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8">
    Den Haag Bouwmachine en Gereedschappen Verhuur  <!-- Main title -->
</h1>
<p class="text-xl text-gray-600 mb-12">
    Professionele verhuur van bouwmaterieel en gereedschappen voor vakman en particulier  <!-- Subtitle -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this page:

- Text sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-gray-800`, `bg-blue-600`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-8` (margin bottom)
- Responsive design: `md:text-5xl` (applies at medium screens and up)

To modify styling, replace these classes while maintaining the same format.

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#diensten">Diensten</a>
<a href="#voordelen">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. The `#` symbol indicates an internal page link
2. The text after `#` must match the `id` of the target section
3. Example: To link to a new section, add `id="nieuwe-sectie"` to that section and use `href="#nieuwe-sectie"`

### Call-to-Action Button
Update the main button link:
```html
<a href="https://hansschuiling.nl" class="inline-block bg-blue-600...">
    Bekijk ons aanbod
</a>
```
Replace `https://hansschuiling.nl` with your desired URL.

### Email Link
Update the contact email:
```html
<a href="mailto:info@denhaagverhuur.nl">
    info@denhaagverhuur.nl
</a>
```
Replace both the `href` and displayed email with your business email.

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
</ul>
```

To link to new pages:

1. Create your privacy policy page (`privacy.html`)
2. Create your terms page (`terms.html`)
3. Update the footer links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section `id` attributes match the `href` values exactly
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Responsive Design Problems**
   - If mobile layout looks wrong, check for `md:` and `lg:` prefixed classes
   - The mobile menu requires Alpine.js to work - don't remove the script tag

3. **Styling Issues**
   - Make sure Tailwind CSS is properly loaded (check the link in `<head>`)
   - Keep the `class="scroll-smooth"` on the HTML tag for smooth scrolling
   - Maintain the existing class structure when making changes

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for styling options
- Verify all external links start with `https://`
- Test the page on different screen sizes using browser dev tools
- Keep a backup copy of the original HTML before making changes

Remember to test all changes in multiple browsers and on different devices to ensure everything works as expected.