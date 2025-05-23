# CloudHost Landing Page Maintenance Guide

This guide will help you maintain and customize the CloudHost landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text**: Find this line in the header section:
```html
<div class="text-2xl font-bold text-blue-600">CloudHost</div>
```
Simply replace "CloudHost" with your desired text.

2. **Navigation Menu Items**: Located in:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
</div>
```
To change menu items, modify the text between `<a>` tags.

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Best Cloud Hosting for Non-Technical Users & Agencies 2025
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Powerful cloud hosting without the complexity
</p>
```

### Tailwind CSS Tips
- Font sizes use this pattern: `text-[size]` (e.g., `text-xl`, `text-2xl`)
- Colors follow: `[type]-[color]-[shade]` (e.g., `text-blue-600`, `bg-gray-50`)
- Spacing uses: `m[direction]-[size]` or `p[direction]-[size]` (e.g., `mb-6`, `px-6`)
- Responsive classes start with screen sizes: `md:` or `lg:`

## Managing Links

### Navigation Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```

To update:
1. Keep the `#` for same-page section links
2. Remove the `#` for links to other pages
3. Add the full path: `href="about.html"`

### Call-to-Action (CTA) Links
Located in multiple places:
```html
<a href="https://www.cloudways.com/en/?id=1384181" class="inline-block px-8 py-4 bg-blue-600...">
```

To update:
1. Replace the URL in `href=""`
2. Keep the existing classes to maintain styling
3. Test the link after updating

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in file names
   - Verify files are in the correct directory

2. **Styling Problems**
   - Don't remove `class=""` attributes
   - Keep responsive classes (`md:`, `lg:`)
   - Maintain spacing between Tailwind classes

3. **Layout Issues**
   - Keep the container classes: `container mx-auto px-6`
   - Don't remove grid classes: `grid grid-cols-1 md:grid-cols-3`
   - Preserve responsive hiding classes: `hidden md:flex`

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct location
3. Ensure all HTML tags are properly closed
4. Compare against the original code provided above

Remember to always test your changes across different screen sizes using browser developer tools.

---

This guide covers the basics of maintaining your landing page. For additional help or specific customizations, refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or consult with a web developer.