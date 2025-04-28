# Landing Page Maintenance Guide
## 101 Headshots Website Documentation

This guide provides detailed instructions for maintaining and customizing the 101 Headshots landing page. Perfect for beginners learning HTML and CSS.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and logo:

```html
<a href="/" class="text-2xl font-bold tracking-tighter text-white hover:text-purple-400">
    101 Headshots
</a>
```

To update:
1. Change logo text: Replace "101 Headshots" with your brand name
2. Modify colors: 
   - `text-white` controls text color
   - `hover:text-purple-400` controls hover state color
   - Example: Change to blue: `text-white hover:text-blue-400`

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tighter mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Independence, Missouri Corporate Headshot Photography Services
</h1>
```

To update:
1. Replace headline text between the `<h1>` tags
2. Adjust text size:
   - `text-4xl` (mobile)
   - `md:text-5xl` (tablet)
   - `lg:text-6xl` (desktop)
3. Modify gradient colors:
   - `from-purple-400` (starting color)
   - `to-pink-400` (ending color)

### Services Cards
Each service card follows this structure:

```html
<div class="bg-gray-800 rounded-2xl p-8 hover:bg-gray-800/80">
    <h3 class="text-xl font-semibold mb-4">Service Title</h3>
    <p class="text-gray-400">Service description</p>
</div>
```

To update:
1. Change service title between `<h3>` tags
2. Update description between `<p>` tags
3. Modify card appearance:
   - `bg-gray-800` (background color)
   - `rounded-2xl` (corner roundness)
   - `p-8` (padding)

## Fixing Broken Links

### Current Link Inventory
The page contains these links:

1. Navigation Menu:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="https://www.101headshots.com">Book Now</a>
```

2. Footer Links:
```html
<a href="mailto:bryan@101headshots.com">bryan@101headshots.com</a>
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="https://www.101headshots.com">Visit our booking site →</a>
```

To update links:
1. Internal links (starting with #):
   - Ensure corresponding ID exists in HTML
   - Example: `href="#services"` needs `id="services"` on target section
2. External links:
   - Replace placeholder URLs with actual URLs
   - Example: Change booking link URL in both navigation and footer

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer's Quick Links section:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <li><a href="#services" class="text-gray-400 hover:text-white transition-colors duration-300">Services</a></li>
        <li><a href="#benefits" class="text-gray-400 hover:text-white transition-colors duration-300">Benefits</a></li>
        <!-- Add these new lines -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`
2. Use the same header and footer as index.html
3. Maintain consistent styling with Tailwind classes

## Troubleshooting

Common Issues:
1. **Broken Internal Links**
   - Check that section IDs match href attributes
   - Example: `href="#services"` needs matching `id="services"`

2. **Responsive Design Issues**
   - Check mobile-first classes (without prefix)
   - Verify breakpoint classes (md:, lg:)
   - Example: `text-4xl md:text-5xl lg:text-6xl`

3. **Color Inconsistencies**
   - Maintain color scheme throughout:
   - Primary: `purple-600`
   - Hover: `purple-700`
   - Text: `gray-400`
   - Background: `gray-800`, `gray-900`

4. **Missing Hover States**
   - Ensure interactive elements have hover classes
   - Example: `hover:bg-purple-700 hover:scale-105`

Need help? Contact technical support or refer to [Tailwind CSS documentation](https://tailwindcss.com/docs).