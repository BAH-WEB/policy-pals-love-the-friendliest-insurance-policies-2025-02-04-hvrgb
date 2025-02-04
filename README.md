# PolicyPals Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the PolicyPals landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">PolicyPals</a>
```
- Replace "PolicyPals" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Other menu items -->
</div>
```
- Update text between `>` and `</a>` tags
- Maintain the class structure for consistent styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 text-gray-900">
    Policy Pals Love The Friendliest Insurance Policies
</h1>
```
- Update heading text while preserving classes
- Classes explained:
  - `text-4xl`: Base size on mobile
  - `md:text-5xl`: Medium screen size
  - `lg:text-6xl`: Large screen size

### Features Section
To modify feature cards:
```html
<div class="p-8 rounded-2xl bg-white shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Personalised Policy Matching</h3>
    <p class="text-gray-600 leading-relaxed">Find the perfect insurance policy...</p>
</div>
```
- Update headings and descriptions
- Maintain padding (`p-8`) and margin (`mb-4`) classes for consistent spacing

## Managing Links

### Navigation Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. For internal sections:
   - Use `#section-name` format
   - Ensure section IDs match in the HTML
2. For external links:
   - Replace `#` with full URL
   - Example: `href="https://www.example.com"`

### Call-to-Action Buttons
```html
<a href="https://www.PolicyPals.Co.Uk" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">
    Find Your Perfect Policy
</a>
```
- Update href attribute with your destination URL
- Maintain button styling classes for consistent appearance

## Adding Privacy and Terms Pages

### Footer Link Setup
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To link to new pages:
1. Create privacy.html and terms.html in your root directory
2. Update links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Maintaining Consistent Styling
When creating privacy.html and terms.html:
1. Copy the header and footer from index.html
2. Use similar Tailwind classes for content:
```html
<main class="container mx-auto px-6 py-24">
    <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
    <div class="prose max-w-none">
        <!-- Your content here -->
    </div>
</main>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Verify that section IDs match href attributes
- Section IDs should be lowercase with no spaces
- Example: `href="#features"` matches `id="features"`

2. **Responsive Design Issues**
- Check mobile display using browser dev tools
- Verify Tailwind responsive classes (md:, lg:) are correct
- Example: `class="text-4xl md:text-5xl lg:text-6xl"`

3. **Styling Inconsistencies**
- Compare classes with original code
- Maintain spacing classes (p-8, mb-4, etc.)
- Keep transition classes for hover effects

### Need Help?
- Check Tailwind CSS documentation for class references
- Use browser inspector to identify specific elements
- Maintain a backup copy of the original HTML
- Test all changes in multiple browsers

Remember to always test your changes across different screen sizes and browsers before deploying to production.