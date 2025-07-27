# Deployment Guide for CharityConnect Website

This guide will help you deploy the CharityConnect website to various hosting platforms.

## 🚀 Quick Deploy Options

### 1. Netlify (Recommended - Free)

**Option A: Drag & Drop**
1. Go to [netlify.com](https://netlify.com)
2. Sign up/Login with GitHub
3. Drag and drop the entire `charity-website` folder to the deploy area
4. Your site will be live in seconds!

**Option B: Git Integration**
1. Push your code to GitHub
2. Connect your GitHub repository to Netlify
3. Set build settings:
   - Build command: (leave empty)
   - Publish directory: `/` (root)
4. Deploy!

### 2. Vercel (Free)

1. Install Vercel CLI:
   ```bash
   npm i -g vercel
   ```

2. Deploy:
   ```bash
   cd charity-website
   vercel
   ```

3. Follow the prompts and your site will be live!

### 3. GitHub Pages (Free)

1. Push your code to GitHub
2. Go to repository Settings > Pages
3. Select source: "Deploy from a branch"
4. Choose branch: `main` or `master`
5. Click Save
6. Your site will be at: `https://username.github.io/repository-name`

### 4. Firebase Hosting (Free)

1. Install Firebase CLI:
   ```bash
   npm install -g firebase-tools
   ```

2. Login to Firebase:
   ```bash
   firebase login
   ```

3. Initialize Firebase:
   ```bash
   firebase init hosting
   ```

4. Deploy:
   ```bash
   firebase deploy
   ```

## 🌐 Custom Domain Setup

### Netlify
1. Go to Site Settings > Domain Management
2. Click "Add custom domain"
3. Enter your domain (e.g., `charityconnect.app`)
4. Follow DNS instructions

### Vercel
1. Go to Project Settings > Domains
2. Add your domain
3. Update DNS records as instructed

### GitHub Pages
1. Go to repository Settings > Pages
2. Add custom domain
3. Update DNS records

## 📱 PWA Setup (Optional)

To make your website a Progressive Web App:

1. Add a `manifest.json` file:
```json
{
  "name": "CharityConnect",
  "short_name": "CharityConnect",
  "description": "Connecting hearts, building communities",
  "start_url": "/",
  "display": "standalone",
  "background_color": "#667eea",
  "theme_color": "#2563eb",
  "icons": [
    {
      "src": "assets/icons/icon-192.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "assets/icons/icon-512.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ]
}
```

2. Add service worker for offline functionality

## 🔧 Environment Variables

If you need to add environment variables:

### Netlify
1. Go to Site Settings > Environment Variables
2. Add your variables

### Vercel
1. Go to Project Settings > Environment Variables
2. Add your variables

## 📊 Analytics Setup

### Google Analytics
1. Create a Google Analytics account
2. Get your tracking ID
3. Add the tracking code to `index.html`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_TRACKING_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_TRACKING_ID');
</script>
```

### Google Search Console
1. Go to [Google Search Console](https://search.google.com/search-console)
2. Add your property
3. Verify ownership (usually via HTML tag or DNS)
4. Submit your sitemap

## 🔍 SEO Optimization

1. **Meta Tags**: Already included in `index.html`
2. **Sitemap**: Create `sitemap.xml`:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://charityconnect.app/</loc>
    <lastmod>2024-01-01</lastmod>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
</urlset>
```

3. **Robots.txt**: Create `robots.txt`:
```
User-agent: *
Allow: /
Sitemap: https://charityconnect.app/sitemap.xml
```

## 🚨 Common Issues & Solutions

### Images Not Loading
- Check file paths in HTML
- Ensure images are in the correct folder
- Verify file permissions

### CSS Not Loading
- Check file paths
- Clear browser cache
- Verify CSS file exists

### JavaScript Errors
- Check browser console for errors
- Verify all script files are loaded
- Test on different browsers

### Mobile Issues
- Test responsive design
- Check viewport meta tag
- Verify touch interactions

## 📞 Support

If you encounter issues:
1. Check the browser console for errors
2. Verify all files are uploaded correctly
3. Test on different devices/browsers
4. Contact support with specific error messages

## 🎉 Post-Deployment Checklist

- [ ] Website loads correctly
- [ ] All images display properly
- [ ] Navigation works on all devices
- [ ] Contact form functions
- [ ] Download buttons work
- [ ] Mobile menu works
- [ ] Analytics tracking
- [ ] SEO meta tags
- [ ] Social media sharing
- [ ] Performance optimization

---

**Your CharityConnect website is now live! 🚀** 