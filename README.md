# Landing Page Maintenance Guide

This guide will help you maintain and customize the Atiq-ur-Rehman Khattak landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">AK</a>
```
- Replace `AK` with your desired logo text
- Keep the classes to maintain the gradient effect

### Hero Section
Located at the top of the page with the main headline:

1. **Main Headline**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Atiq-ur-Rehman Khattak
</h1>
```
- Replace the name while keeping the classes
- The `text-4xl md:text-5xl lg:text-6xl` classes control text size on different screen sizes

2. **Subheading**
```html
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Empowering Institutions, Transforming Enterprises.
</p>
```
- Update the tagline text
- Maintain the responsive text classes

### Tailwind CSS Tips for Beginners
- `text-{size}`: Controls text size (xs, sm, base, lg, xl, 2xl, etc.)
- `mb-{number}`: Adds margin bottom (1-16)
- `py-{number}`: Adds padding top and bottom
- `bg-{color}-{shade}`: Sets background color
- Don't remove `md:` or `lg:` prefixes as they control responsive design

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#about" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">About</a>
    <a href="#services" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Services</a>
    <!-- Additional menu items -->
</div>
```
To update links:
1. Locate the `href` attribute
2. For internal sections, use `#section-name`
3. For external pages, use the full URL: `https://example.com/page`

### Contact Button Links
```html
<a href="https://atiqkhattak.com/contact" class="hidden md:block px-6 py-2 bg-gradient-to-r from-blue-600 to-purple-600 text-white rounded-full">
    Contact
</a>
```
- Update the `href` with your contact page URL
- Keep the classes to maintain the button styling

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <!-- Social media icons -->
    </a>
</div>
```
- Replace `#` with your social media profile URLs
- Example: `href="https://linkedin.com/in/your-profile"`

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Insert these links in the footer's Quick Links section:
```html
<ul class="space-y-4">
    <!-- Existing links -->
    <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them

### Step 3: Maintain Consistent Styling
```html
<!-- Example privacy.html structure -->
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body>
    <!-- Copy header section -->
    
    <section class="pt-32 pb-24">
        <div class="container mx-auto px-6">
            <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
            <!-- Add your privacy policy content here -->
        </div>
    </section>

    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Links**
   - Check for typos in URLs
   - Ensure file names match exactly
   - Verify file locations in your directory

2. **Styling Issues**
   - Don't remove Tailwind classes unless you're sure about their purpose
   - Keep responsive prefixes (`md:`, `lg:`)
   - Maintain the gradient classes for consistent branding

3. **Layout Problems**
   - Keep the `container` class on main sections
   - Maintain padding classes (`px-6`, `py-24`)
   - Don't remove `flex` and `grid` classes

Need help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).