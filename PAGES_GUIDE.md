# Pages Guide

## Overview of All Pages

### 🏠 **Home Page** (`/index.astro`)
**URL:** `/` or `/index.html`

**Sections:**
- **Hero Section** - Large banner with business tagline and CTA button
- **Why Choose ProFix** - 4 feature cards showcasing key benefits
- **Call-to-Action** - Secondary CTA encouraging contact

**Key Elements:**
- Responsive hero with gradient background
- Feature cards with icons and hover effects
- Contact button links to `/contact`

**Customization:**
- Change tagline in `<h1>` tag
- Update feature descriptions
- Modify button text

---

### 🔧 **Services Page** (`/services.astro`)
**URL:** `/services` or `/services/index.html`

**Sections:**
- **Header** - Page title and description
- **Services Grid** - 8 service cards with descriptions
- **Service Process** - 4-step process explanation

**Services Included:**
1. Plumbing Repairs 🚿
2. Electrical Work ⚡
3. Drywall & Patching 🧱
4. Carpentry 🪵
5. Painting 🎨
6. Flooring 🏠
7. Door & Window Repair 🪟
8. General Maintenance 🔍

**How to Add/Remove Services:**
```astro
const services = [
    {
        name: "Service Name",
        description: "Description of the service",
        icon: "🔧"  // Use emoji or HTML entity
    },
    // Add more...
];
```

**Customization:**
- Change service names and descriptions
- Update icons (emojis or Unicode)
- Modify the 4-step process
- Update colors and styling

---

### ℹ️ **About Page** (`/about.astro`)
**URL:** `/about` or `/about/index.html`

**Sections:**
- **Header** - Page title
- **Who We Are** - Company information and mission
- **Statistics** - 4 key stats (years in business, customers, satisfaction rate, emergency support)
- **Team Section** - Team member profiles with avatars

**Team Members Included:**
- John Davis - Owner & Lead Technician
- Sarah Martinez - Master Plumber
- Mike Chen - Electrical Specialist
- Tom Johnson - Carpenter

**Statistics:**
- 10+ Years in Business
- 5000+ Happy Customers
- 98% Satisfaction Rate
- 24/7 Emergency Support

**How to Update Team:**
```astro
<div class="team-member">
    <div class="member-avatar">JD</div>  <!-- Initials -->
    <h3>Name</h3>
    <p class="role">Position</p>
    <p>Bio/description</p>
</div>
```

**Customization:**
- Update company history
- Change statistics
- Modify mission statement
- Add/remove team members
- Update team member details

---

### 📞 **Contact Page** (`/contact.astro`)
**URL:** `/contact` or `/contact/index.html`

**Sections:**
- **Header** - Page title
- **Contact Form** - Customer inquiry form
- **Contact Information** - Business details and hours
- **Business Hours** - Operating hours
- **Social Media Links** - Social media icons

**Form Fields:**
- Name (required)
- Email (required)
- Phone (required)
- Service Needed (dropdown with all services)
- Message (textarea)

**Contact Information Displayed:**
- Address
- Phone number (linked for calling)
- Email (linked for mailing)
- Business hours
- Social media links

**Contact Info to Update:**
```astro
<!-- In contact.astro -->
<p>123 Main Street<br>Anytown, ST 12345</p>
<a href="tel:+15551234567">(555) 123-4567</a>
<a href="mailto:info@profix.com">info@profix.com</a>
```

**Business Hours:**
```astro
Monday - Friday: 8:00 AM - 6:00 PM
Saturday: 9:00 AM - 4:00 PM
Sunday: Closed
```

**Note:** The form currently shows fields but doesn't submit anywhere. To make it functional, you'll need to:
- Set up a backend service (Node.js, Python, etc.)
- Use a third-party service (Formspree, Netlify Forms, etc.)
- Implement form handling JavaScript

---

## Navigation Structure

**Main Navigation (in navbar):**
```
ProFix (Logo/Home)
├── Home
├── Services
├── About
└── Contact
```

All pages are linked in the sticky navigation bar.

---

## Customization Checklist

- [ ] Update business name (appears in navbar logo and footer)
- [ ] Change all phone numbers and email addresses
- [ ] Update business address
- [ ] Modify business hours
- [ ] Update team member names and roles
- [ ] Change service list to match your offerings
- [ ] Update statistics on About page
- [ ] Customize colors in Layout.astro
- [ ] Add social media links
- [ ] Test all links work correctly
- [ ] Test responsive design on mobile
- [ ] Update favicon in public folder

---

## Color Customization

All colors use CSS custom properties. Edit in `src/layouts/Layout.astro`:

```css
:root {
    --primary-color: #2563eb;      /* Main blue - headers, buttons */
    --primary-dark: #1e40af;       /* Darker blue - hover states */
    --secondary-color: #f97316;    /* Orange - accents, secondary buttons */
    --dark-bg: #1f2937;            /* Dark background - navbar, footer */
    --light-bg: #f9fafb;           /* Light background - cards, sections */
    --text-dark: #111827;          /* Dark text - body text */
    --text-light: #6b7280;         /* Gray text - descriptions */
    --border-color: #e5e7eb;       /* Border color - separators */
}
```

Change these to match your brand colors.

---

## Adding New Pages

1. Create a new file in `src/pages/` (e.g., `gallery.astro`)
2. Use this template:
```astro
---
import Layout from '../layouts/Layout.astro';
---

<Layout title="Page Title">
    <section class="hero">
        <div class="container">
            <h1>Page Title</h1>
        </div>
    </section>

    <!-- Your content here -->
</Layout>
```
3. It will automatically create a route at `/gallery`
4. Add link to navigation in `src/layouts/Layout.astro`

---

## Layout Component

The `Layout.astro` file contains:
- Navigation bar (sticky)
- Footer
- Global styles
- Meta tags
- CSS custom properties for colors

All pages use this layout, so changes here apply everywhere.

---

## Tips for Effective Pages

1. **Keep it Simple** - Users prefer clear, easy-to-scan content
2. **Use Headings** - Help users navigate and improve SEO
3. **Short Paragraphs** - Break up text into digestible chunks
4. **Call-to-Action Buttons** - Guide users to contact or services
5. **Mobile First** - Test on phones and tablets
6. **Fast Loading** - Astro builds static sites (very fast!)

Happy customizing! 🎉
