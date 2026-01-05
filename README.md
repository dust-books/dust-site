# Dust Marketing Site

Official marketing website for [Dust Media Server](https://github.com/dust-books/dust-server) - a free and open-source media server for eBooks and digital comics.

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 📁 Project Structure

```
dust-site/
├── src/
│   ├── layouts/
│   │   └── Layout.astro       # Main layout with navbar and footer
│   └── pages/
│       ├── index.astro         # Homepage
│       ├── features.astro      # Features page
│       ├── setup.astro         # Setup guide
│       ├── developers.astro    # API & developer docs
│       └── about.astro         # About page
├── public/
│   ├── favicon.svg             # Site favicon
│   └── images/                 # Add hero image and other assets here
└── astro.config.mjs            # Astro configuration
```

## 📸 Adding a Hero Image

Replace the placeholder on the homepage by adding your screenshot:

1. Take a screenshot of your Dust server
2. Save it as `public/images/hero.png` (or .jpg, .webp)
3. Update `src/pages/index.astro`:

```astro
<!-- Replace this: -->
<div class="hero-placeholder">
  <p>📚 Hero Image Placeholder</p>
</div>

<!-- With this: -->
<img src="/images/hero.png" alt="Dust Media Server" />
```

## 🎨 Customization

### Colors

Edit CSS variables in `src/layouts/Layout.astro`:

```css
:root {
  --color-primary: #3b82f6;      /* Primary blue */
  --color-primary-dark: #2563eb; /* Darker blue */
  --color-secondary: #8b5cf6;    /* Purple */
  --color-accent: #06b6d4;       /* Cyan */
  /* ... */
}
```

### Site Metadata

Update `astro.config.mjs`:

```js
export default defineConfig({
  site: 'https://your-domain.com',
  base: '/',
});
```

## 📦 Building for Production

```bash
npm run build
```

Output will be in `dist/` directory. Deploy to any static hosting:

- **GitHub Pages**: Push `dist/` to `gh-pages` branch
- **Netlify/Vercel**: Connect repo and auto-deploy
- **Own Server**: Copy `dist/` contents to web root

## 🔗 Links

- [Dust Server Repository](https://github.com/dust-books/dust-server)
- [API Documentation](https://github.com/dust-books/dust-server/blob/main/API-REFERENCE.md)
- [Astro Documentation](https://docs.astro.build)

## 📝 License

MIT - Same as Dust Media Server
