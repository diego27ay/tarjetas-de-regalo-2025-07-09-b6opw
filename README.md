# Landing Page Maintenance Guide

This guide will help you maintain and customize the Tarjetas de Regalo landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

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
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Tarjetas de Regalo <!-- Change this text to update the logo -->
</a>
```

2. **Navigation Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#caracteristicas">Características</a> <!-- Update navigation text here -->
    <a href="#beneficios">Beneficios</a>
    <a href="#faq">FAQ</a>
    <a href="#contacto">Contacto</a>
</div>
```

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-8 bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Crea las mejores tarjetas de regalo <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl mb-12 text-gray-300">
    Diseña tarjetas únicas y personalizadas de forma gratuita <!-- Subheadline -->
</p>
```

### Tailwind CSS Tips
- Font sizes use this pattern: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Spacing uses this pattern: `m-4` (margin) or `p-4` (padding)
- Colors follow: `text-purple-400`, `bg-gray-900`, etc.
- Responsive classes start with: `sm:`, `md:`, `lg:`

Example of updating a responsive text size:
```html
<!-- Original -->
<h1 class="text-4xl md:text-6xl lg:text-7xl">

<!-- Making it smaller -->
<h1 class="text-3xl md:text-5xl lg:text-6xl">
```

## Managing Links

### Current Link Structure
The page contains these link types:

1. **Navigation Links:**
```html
<a href="#caracteristicas">Características</a>
<a href="#beneficios">Beneficios</a>
<a href="#faq">FAQ</a>
<a href="#contacto">Contacto</a>
```

2. **Call-to-Action Links:**
```html
<a href="https://adornosparacumple.com/" class="inline-block bg-gradient-to-r from-purple-500 to-pink-500...">
    Comenzar Ahora
</a>
```

### Updating Links
To update any link:

1. Find the `<a>` tag you want to modify
2. Change the `href` attribute:
   - For internal sections: `href="#section-name"`
   - For external pages: `href="https://example.com"`

Example:
```html
<!-- Original -->
<a href="https://adornosparacumple.com/">

<!-- Updated -->
<a href="https://your-new-domain.com/">
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer's "Enlaces Rápidos" section:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Enlaces Rápidos</h3>
    <ul class="space-y-2">
        <li><a href="#caracteristicas" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Características</a></li>
        <!-- Add these new lines -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Política de Privacidad</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Términos y Condiciones</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - Check for typos in both the link and section ID
   - Section IDs are case-sensitive

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify all responsive classes (sm:, md:, lg:) are correct
   - Test different screen sizes

3. **Gradient Text Not Showing**
   - Ensure these classes are present:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent
     ```

### Need Help?
Contact support at diego27ay@gmail.com for additional assistance.

Remember to:
- Always test changes in multiple browsers
- Back up files before making modifications
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test all links after making changes