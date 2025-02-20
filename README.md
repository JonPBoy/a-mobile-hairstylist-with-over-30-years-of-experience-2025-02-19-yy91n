# Mobile Hairstylist Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Mobile Hairstylist landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and logo text. To update:

```html
<!-- Located at the top of the page -->
<div class="text-xl font-semibold text-gray-800">Mobile Stylist</div>
```

To change the business name:
1. Locate this line in the header section
2. Replace "Mobile Stylist" with your desired text
3. Adjust font size by modifying `text-xl` to `text-lg` (smaller) or `text-2xl` (larger)

### Hero Section
The main headline and subheading are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    A Mobile Hairstylist With Over 30 Years of Experience
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">
    I am Mobile... I come to YOU! Your Home or Office
</p>
```

To update:
1. Replace the text between the `<h1>` tags for the main headline
2. Replace the text between the `<p>` tags for the subheading
3. Maintain the responsive text sizes (`text-4xl`, `md:text-5xl`, `lg:text-6xl`)

### Services Section
Each service card follows this structure:

```html
<div class="bg-gray-50 rounded-2xl p-8 hover:shadow-lg transition-shadow duration-300">
    <h3 class="text-xl font-semibold text-gray-900 mb-4">Hair Extensions</h3>
    <p class="text-gray-600">Professional installation and maintenance...</p>
</div>
```

To add or modify services:
1. Copy the entire `<div>` block above
2. Paste it within the `grid grid-cols-1 md:grid-cols-2 gap-8` container
3. Update the heading and description text
4. Maintain the class structure for consistent styling

## Fixing Broken Links

### Navigation Menu Links
The main navigation uses anchor links to scroll to page sections:

```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. The `href="#services"` format links to sections with matching IDs
2. Ensure section IDs match exactly (e.g., `id="services"`)
3. For external links, replace with full URLs (e.g., `href="https://example.com"`)

### Contact Information
Update phone and email links:

```html
<a href="tel:9493072748">Call (949) 307-2748</a>
<a href="mailto:jonpboy@gmail.com">Email Us</a>
```

To modify:
1. Update the `tel:` number in the href
2. Update the displayed phone number text
3. Change the `mailto:` email address
4. Maintain the same format to ensure proper functionality

## Adding Privacy and Terms Pages

Add privacy and terms links to the footer:

```html
<!-- Add this within the Quick Links section -->
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To implement:
1. Create `privacy.html` and `terms.html` files in your root directory
2. Copy the above code into the footer's Quick Links section
3. Maintain consistent styling with existing footer links
4. Ensure the new pages use the same styling as the main page

## Troubleshooting

Common issues and solutions:

1. **Broken Scroll Links**
   - Verify that section IDs match navigation href values exactly
   - Check for extra spaces or special characters

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Maintain the existing grid structure (`grid-cols-1 md:grid-cols-2`)

3. **Contact Links Not Working**
   - Ensure proper formatting: `tel:` for phone numbers
   - Remove any spaces or special characters from href values

4. **Styling Inconsistencies**
   - Copy existing class structures when adding new elements
   - Keep the color scheme using existing Tailwind classes

Remember to test all changes across different screen sizes using your browser's developer tools.

For additional help or specific customizations, refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or contact your web developer.