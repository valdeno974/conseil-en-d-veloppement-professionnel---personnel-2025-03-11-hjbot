# Landing Page Maintenance Guide

This guide will help you maintain and customize the Valdeno Consulting landing page. It's designed for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections to Update

#### 1. Header/Navigation
```html
<header class="fixed w-full bg-white/95 backdrop-blur-sm z-50 border-b border-gray-100">
    <nav class="container mx-auto px-6 py-4">
        <!-- To update company name -->
        <a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">Valdeno</a>
```
To modify:
- Change "Valdeno" to your company name
- Keep the classes intact to maintain the gradient effect

#### 2. Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Conseil en développement professionnel & personnel
</h1>
```
To modify:
- Update the heading text while maintaining the HTML structure
- The `text-4xl md:text-5xl lg:text-6xl` classes control text size across different screen sizes

#### 3. Services Section
Each service card follows this structure:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Coaching</h3>
    <p class="text-gray-600">Accompagnement personnalisé pour atteindre vos objectifs</p>
</div>
```
To modify:
- Update the `h3` text for service titles
- Update the `p` text for service descriptions
- Keep all classes to maintain styling and hover effects

### Understanding Tailwind Classes

Key classes explained:
- `container mx-auto`: Centers content with automatic margins
- `px-6 py-4`: Padding (x-axis: 6 units, y-axis: 4 units)
- `text-gray-600`: Text color
- `hover:scale-105`: Grows element to 105% on hover
- `md:`: Applies styles on medium screens and up
- `lg:`: Applies styles on large screens and up

## Managing Links

### Current Link Structure

#### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Avantages</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. Replace `#services` with your desired anchor or URL
3. Update the link text between `<a>` tags

#### Call-to-Action Button
```html
<a href="https://www.valdeno-consulting.com" class="inline-block px-8 py-4 text-lg font-semibold text-white bg-gradient-to-r from-blue-600 to-purple-600 rounded-full">
```
To update:
1. Replace the URL in `href`
2. Keep all classes to maintain button styling

#### Email Link
```html
<a href="mailto:coachpersonnel@mac.com" class="text-gray-400 hover:text-white transition-colors duration-300">
```
To update:
1. Replace `coachpersonnel@mac.com` with your email address

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the footer's "Liens rapides" section:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Politique de confidentialité</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Conditions d'utilisation</a></li>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your privacy/terms content between them

## Troubleshooting

Common issues and solutions:

1. **Broken Gradient Text**
   - Ensure all classes in the gradient text are present:
   ```html
   bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent
   ```

2. **Responsive Issues**
   - Check that `md:` and `lg:` prefixed classes are intact
   - Test on different screen sizes using browser dev tools

3. **Missing Styles**
   - Verify the Tailwind CSS CDN link is present in the head:
   ```html
   <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
   ```

Remember to:
- Test all changes in multiple browsers
- Maintain consistent spacing and indentation
- Keep backup copies before making major changes
- Test all links after updating

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your web development team.