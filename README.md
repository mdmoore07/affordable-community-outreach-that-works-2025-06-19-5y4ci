# Incite Local Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Incite Local landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To modify:

1. **Company Name:**
```html
<div class="text-2xl font-bold text-gray-800">Incite Local</div>
```
- Replace "Incite Local" with your company name
- Adjust size using `text-2xl` (options: text-lg, text-xl, text-3xl)

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
</div>
```
- Change menu text by editing the text between `<a>` tags
- Maintain the `href` attributes to preserve section linking

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">Affordable Community Outreach That Works</h1>
<p class="text-xl md:text-2xl text-gray-600">Connect Directly. Grow Locally. Advertise Affordably.</p>
```
- Update heading text between `<h1>` tags
- Modify subheading between `<p>` tags
- Keep responsive classes (`md:` and `lg:` prefixes) to maintain mobile compatibility

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl">
    <h3 class="text-xl font-semibold">End-to-End Service</h3>
    <p class="text-gray-600">Complete campaign management...</p>
</div>
```
To modify:
1. Change feature title between `<h3>` tags
2. Update description between `<p>` tags
3. Keep styling classes to maintain visual consistency

## Managing Links

### Navigation Links
Current links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://incitelocal.com/signup">Get Started</a>
```

To update:
1. Internal links (starting with #):
   - Match the `href` value with the corresponding section's `id`
   - Example: `href="#features"` links to `<section id="features">`

2. External links:
   - Replace `https://incitelocal.com/signup` with your desired URL
   - Always include `https://` for external links

### Footer Links
Located at the bottom of the page:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <!-- Quick Links -->
    <ul class="space-y-2">
        <li><a href="#features">Features</a></li>
        <li><a href="#benefits">Benefits</a></li>
        <li><a href="#faq">FAQ</a></li>
    </ul>
</div>
```

To modify:
1. Update href attributes to match your page sections
2. Ensure consistency with navigation menu links
3. Test all links after modification

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new HTML files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the placeholder `#` with proper file paths:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href values
   - Check for typos in both the link and section ID
   - IDs are case-sensitive

2. **Styling Problems**
   - Keep all Tailwind classes on elements
   - Don't remove responsive prefixes (sm:, md:, lg:)
   - Maintain spacing classes (mb-4, py-2, etc.)

3. **Layout Issues**
   - Preserve container classes: `container mx-auto px-6`
   - Keep grid classes: `grid grid-cols-1 md:grid-cols-3`
   - Don't remove flex utilities: `flex items-center justify-between`

### Getting Help
- Review Tailwind CSS documentation for styling classes
- Use browser inspection tools to identify styling issues
- Test on multiple devices and screen sizes
- Maintain regular backups before making changes

Remember to test all changes thoroughly before deploying to a live site. When in doubt, make one change at a time and verify its impact before proceeding with additional modifications.