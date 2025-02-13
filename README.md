# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this line in the header -->
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">TWD</a>
```
Simply replace "TWD" with your desired text.

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-purple-400 transition-colors">Features</a>
    <a href="#benefits" class="hover:text-purple-400 transition-colors">Benefits</a>
    <!-- Add or modify menu items here -->
</div>
```

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-6 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">Best Websites In Texas</p>
```
- Replace "Texas Web Design" with your main heading
- Update "Best Websites In Texas" with your tagline

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-4xl`: Large text size
- `md:text-6xl`: Larger text on medium screens
- `bg-gray-900`: Dark background color
- `text-gray-100`: Light text color
- `hover:scale-105`: Slight enlargement on hover
- `transition-colors`: Smooth color transitions

To modify styles:
1. Find the element you want to change
2. Locate its class attribute
3. Add or modify Tailwind classes
4. Test on different screen sizes

Example:
```html
<!-- Original -->
<div class="bg-gray-800 rounded-2xl p-8">

<!-- Modified for lighter background -->
<div class="bg-gray-700 rounded-2xl p-8">
```

## Managing Links

### External Links
Current external links that need updating:
```html
<!-- Header CTA button -->
<a href="https://twd.com" class="bg-gradient-to-r from-purple-600 to-pink-600">Get Started</a>

<!-- Hero CTA button -->
<a href="https://twd.com" class="inline-block bg-gradient-to-r">Transform Your Online Presence</a>
```
Replace `https://twd.com` with your actual website URL.

### Internal Links
Navigation menu links to sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
These link to sections using IDs. Ensure section IDs match:
```html
<section id="features">
<section id="benefits">
<section id="faq">
<section id="contact">
```

## Adding Policy Pages

### Footer Policy Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-purple-400 transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-purple-400 transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

To link to policy pages:
1. Create privacy.html and terms.html in your project folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-purple-400 transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-purple-400 transition-colors">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
- Check that section IDs match href attributes exactly
- IDs are case-sensitive
- Remove any spaces in IDs

2. **Responsive Design Issues**
- Test on multiple screen sizes
- Look for `md:` and `lg:` prefixes in classes
- Use browser developer tools to test responsiveness

3. **Gradient Text Not Showing**
- Ensure all three classes are present:
  ```html
  bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
  ```

4. **Hover Effects Not Working**
- Verify `hover:` classes are present
- Check that `transition-` classes are included
- Test in different browsers

Need more help? Contact admin@twd.com for technical support.