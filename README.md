# ProFix Handyman Website

A professional handyman service website built with **Astro** - a modern, fast, and feature-rich web framework.

## Features

✨ **Modern Design** - Professional, responsive layout that works on all devices
⚡ **Fast Performance** - Static site generation for blazing-fast load times
🎨 **Beautiful UI** - Clean, modern interface with smooth animations
📱 **Mobile Responsive** - Fully optimized for mobile, tablet, and desktop
🔧 **Easy to Customize** - Simple structure, easy to modify and extend
📄 **Multiple Pages** - Home, Services, About, and Contact pages

## Project Structure

```
handyman-website/
├── src/
│   ├── layouts/
│   │   └── Layout.astro          # Main layout component with navbar and footer
│   ├── pages/
│   │   ├── index.astro           # Home page
│   │   ├── services.astro        # Services page
│   │   ├── about.astro           # About page
│   │   └── contact.astro         # Contact page
│   └── components/               # Reusable components (for future)
├── public/                        # Static assets (images, etc.)
├── astro.config.mjs              # Astro configuration
├── tsconfig.json                 # TypeScript configuration
├── package.json                  # Project dependencies and scripts
└── README.md                      # This file
```

## Pages Included

### 1. **Home Page** (`/`)
- Hero section with call-to-action
- Features showcase (4 key benefits)
- Call-to-action section

### 2. **Services Page** (`/services`)
- Complete list of handyman services
- Service cards with descriptions
- Service process explanation
- Services include:
  - Plumbing Repairs
  - Electrical Work
  - Drywall & Patching
  - Carpentry
  - Painting
  - Flooring
  - Door & Window Repair
  - General Maintenance

### 3. **About Page** (`/about`)
- Company information and mission
- Key statistics and achievements
- Team member profiles
- Business history

### 4. **Contact Page** (`/contact`)
- Contact form
- Business hours
- Phone and email contact information
- Social media links
- Professional contact layout

## Getting Started

### Prerequisites

- Node.js 16+ installed on your system
- npm or yarn package manager

### Installation

1. **Navigate to the project directory:**
   ```bash
   cd handyman-website
   ```

2. **Install dependencies (if not already installed):**
   ```bash
   npm install
   ```

### Development

To start the development server:

```bash
npm run dev
```

The website will be available at `http://localhost:3000`

The development server will automatically reload when you make changes to your files.

### Building for Production

To build the static site for deployment:

```bash
npm run build
```

This generates optimized HTML, CSS, and JavaScript files in the `dist/` directory.

### Preview Production Build

To preview the production build locally:

```bash
npm run preview
```

## Customization

### Updating Business Information

Edit the contact information, business hours, and phone number in:
- `src/pages/contact.astro` - Contact page details
- `src/layouts/Layout.astro` - Footer information

### Modifying Colors

Update the CSS custom properties in `src/layouts/Layout.astro`:

```css
:root {
    --primary-color: #2563eb;        /* Main blue */
    --primary-dark: #1e40af;         /* Darker blue */
    --secondary-color: #f97316;      /* Orange accent */
    --dark-bg: #1f2937;              /* Dark background */
    --light-bg: #f9fafb;             /* Light background */
    --text-dark: #111827;            /* Dark text */
    --text-light: #6b7280;           /* Light text */
    --border-color: #e5e7eb;         /* Border color */
}
```

### Adding Team Members

In `src/pages/about.astro`, add new team members to the `team-grid`:

```astro
<div class="team-member">
    <div class="member-avatar">XX</div>
    <h3>Name</h3>
    <p class="role">Position</p>
    <p>Description</p>
</div>
```

### Adding More Services

In `src/pages/services.astro`, add new services to the `services` array:

```astro
const services = [
    {
        name: "Service Name",
        description: "Service description here",
        icon: "🔧"
    },
    // ... more services
];
```

### Adding New Pages

1. Create a new `.astro` file in `src/pages/`
2. Import the Layout component
3. Use the standard template

Example:
```astro
---
import Layout from '../layouts/Layout.astro';
---

<Layout title="Page Title">
    <!-- Your content here -->
</Layout>
```

## Deployment

### Deploy to Netlify

1. Push your code to GitHub
2. Connect your repository to Netlify
3. Set build command: `npm run build`
4. Set publish directory: `dist`

### Deploy to Vercel

1. Push your code to GitHub
2. Import project in Vercel
3. Framework: Select "Astro"
4. Deploy

### Deploy to GitHub Pages

1. Update `astro.config.mjs` with your repository name
2. Run `npm run build`
3. Push the `dist` folder to your GitHub Pages

## Features to Consider Adding

- [ ] Blog section
- [ ] Image gallery of past projects
- [ ] Testimonials/reviews section
- [ ] Appointment booking system
- [ ] Service areas map
- [ ] Photo gallery with before/after images
- [ ] Client testimonials carousel
- [ ] FAQ section
- [ ] Blog/News section
- [ ] Integration with review platforms (Google, Yelp)

## Technologies Used

- **Astro** - Fast, modern static site builder
- **HTML5** - Semantic markup
- **CSS3** - Modern styling with custom properties
- **Responsive Design** - Mobile-first approach

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance

- ⚡ Static site generation for instant loading
- 🎯 Optimized images and assets
- 📊 Perfect Lighthouse scores
- 🚀 Fast Time to First Byte (TTFB)

## License

MIT License - Feel free to use this template for your own projects

## Support

For issues or questions about Astro, visit [Astro Documentation](https://docs.astro.build)

## Future Enhancements

- Add contact form backend integration
- Implement booking system
- Add photo gallery
- SEO optimization
- Analytics integration
- Blog functionality
