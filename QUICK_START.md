# Quick Start Guide - ProFix Handyman Website

## 🚀 Getting Started in 30 Seconds

### 1. Install & Run
```bash
cd handyman-website
npm install
npm run dev
```

Then open http://localhost:3000 in your browser.

## 📝 Quick Customization

### Change Business Name
In `src/layouts/Layout.astro`, find:
```astro
<a href="/">ProFix</a>
```
Replace "ProFix" with your business name.

### Change Contact Info
In `src/pages/contact.astro`, update:
- Phone number
- Email address
- Business address
- Hours of operation

### Change Colors
In `src/layouts/Layout.astro`, update the CSS variables:
```css
:root {
    --primary-color: #2563eb;      /* Your main color */
    --secondary-color: #f97316;    /* Your accent color */
}
```

### Update Services
In `src/pages/services.astro`, modify the services array with your offerings.

### Update Team
In `src/pages/about.astro`, add your team members to the team-grid section.

## 📤 Building & Deploying

### Build for Production
```bash
npm run build
```
Creates optimized files in the `dist/` folder.

### Preview Production Build
```bash
npm run preview
```

### Deploy Options

**Netlify:**
- Connect GitHub repo to Netlify
- Build command: `npm run build`
- Publish directory: `dist`

**Vercel:**
- Import GitHub repo to Vercel
- It auto-detects Astro
- Deploy!

**GitHub Pages:**
- Build locally: `npm run build`
- Push `dist` folder to `gh-pages` branch

## 🎨 File Structure Reference

```
src/
├── layouts/Layout.astro    ← Main layout, navbar, footer
├── pages/
│   ├── index.astro        ← Home page
│   ├── services.astro     ← Services listing
│   ├── about.astro        ← About company
│   └── contact.astro      ← Contact form
```

## 💡 Pro Tips

1. **Test Responsive Design:** Use browser DevTools (F12) to test mobile view
2. **SEO Titles:** Each page has a unique title in the Layout component
3. **Links:** Update the navbar links if you add/remove pages
4. **Styling:** All CSS is embedded in components for simplicity

## 🆘 Troubleshooting

**"Port 3000 already in use":**
```bash
npm run dev -- --port 3001
```

**Build errors:**
```bash
rm -rf dist node_modules
npm install
npm run build
```

**Changes not showing:**
- Restart dev server (Ctrl+C then `npm run dev`)
- Clear browser cache

## 📚 Learn More

- [Astro Docs](https://docs.astro.build)
- [Astro Tutorial](https://docs.astro.build/en/tutorial/0-introduction/)

## Next Steps

1. ✅ Update business information
2. ✅ Change colors to match your branding
3. ✅ Add photos/images to `public` folder
4. ✅ Customize services list
5. ✅ Test on mobile
6. ✅ Deploy!

Happy building! 🎉
