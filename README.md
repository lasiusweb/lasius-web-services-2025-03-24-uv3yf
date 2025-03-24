# Lasius Web Services Landing Page - Maintenance Guide

This guide will help you maintain and customize the Lasius Web Services landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold tracking-tight hover:text-indigo-400 transition-colors">
    Lasius Web  <!-- Change company name here -->
</a>
```

**Tailwind Classes Explained:**
- `text-2xl`: Sets large text size
- `font-bold`: Makes text bold
- `tracking-tight`: Reduces letter spacing
- `hover:text-indigo-400`: Changes text color on hover

### Hero Section
The main banner section contains your primary headline and call-to-action:

```html
<h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
    Lasius Web Services  <!-- Update main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Transform your online presence. <!-- Update subheading here -->
</p>
```

**Responsive Design Tips:**
- `md:text-6xl` means text will be larger on medium screens and up
- Always maintain both mobile (`text-4xl`) and desktop (`md:text-6xl`) sizes

### Features Section
To add or modify features:

```html
<div class="bg-gray-900 rounded-2xl p-8 hover:transform hover:scale-105 transition-all duration-300">
    <h3 class="text-2xl font-bold mb-4">
        SEO + Ads Mastery  <!-- Feature title -->
    </h3>
    <p class="text-gray-400">
        Dominate search results...  <!-- Feature description -->
    </p>
</div>
```

## Managing Links

### Navigation Menu Links
The main navigation menu contains internal page links:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-indigo-400 transition-colors">Features</a>
    <a href="#benefits" class="hover:text-indigo-400 transition-colors">Benefits</a>
    <a href="#faq" class="hover:text-indigo-400 transition-colors">FAQ</a>
    <a href="#contact" class="hover:text-indigo-400 transition-colors">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. For internal sections, use `#section-name`
3. For external links, use complete URLs: `https://example.com`

### Call-to-Action Links
Update the main CTA buttons:

```html
<a href="https://lasiuswebservices.com" class="inline-block px-8 py-4 bg-indigo-600...">
    Start Your Transformation  <!-- Update button text here -->
</a>
```

**Important:** Replace `https://lasiuswebservices.com` with your actual service URL

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your root directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the footer section and modify the legal links:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="/privacy.html" class="text-gray-400 hover:text-indigo-400 transition-colors">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-indigo-400 transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

### Step 3: Maintain Consistent Styling
Copy these classes for new links to maintain consistency:
```css
text-gray-400 hover:text-indigo-400 transition-colors
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Example: `href="#features"` needs matching `id="features"` in section tag

2. **Responsive Design Issues**
   - Check both mobile and desktop classes
   - Use browser inspector to test different screen sizes
   - Common format: `class="base-style md:larger-style"`

3. **Styling Inconsistencies**
   - Copy existing Tailwind classes for similar elements
   - Maintain color scheme: `indigo-600`, `gray-900`, `gray-400`
   - Keep consistent spacing: `mb-4`, `py-24`, `px-6`

### Need Help?
- Verify HTML syntax with [W3C Validator](https://validator.w3.org/)
- Test responsive design using Chrome DevTools (F12)
- Maintain backup copies before making significant changes

Remember to test all changes across different devices and browsers before publishing updates to your live site.