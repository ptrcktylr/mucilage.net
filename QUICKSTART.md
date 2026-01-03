# Mucilage Site - Quick Start Guide

## 🎉 Your site is ready!

I've built you a clean, simple portfolio site for your RPG modules. **No frameworks, no build tools** - just HTML, CSS, and a sprinkle of JavaScript.

## 📂 What's Inside

```
public/
├── index.html              ← Homepage with module grid
├── about.html              ← About page (update with your story)
├── modules/
│   └── veiled-city.html   ← Example module page (copy this template)
├── css/
│   └── styles.css         ← All styling (dark vintage aesthetic)
└── images/
    └── modules/           ← Put your module cover images here
```

## ✅ Next Steps for Joe

### 1. View It Locally (Right Now!)
Just open `public/index.html` in your browser. That's it!

### 2. Add Your Module Cover Images
- Put your cover images in `public/images/modules/`
- Recommended size: **600×900px** (2:3 ratio, like book covers)
- Name them: `veiled-city.jpg`, `dungeon-delvers.jpg`, etc.

### 3. Update the HTML to Show Your Images
In `public/index.html`, replace this:
```html
<div class="module-cover-placeholder">
  [veiled-city.jpg]<br>
  <small>Module Cover Art</small>
</div>
```

With this:
```html
<img src="images/modules/veiled-city.jpg" alt="The Veiled City">
```

Do this for each module card.

### 4. Customize Your Content
- **About page:** Edit `public/about.html` with your story
- **Homepage intro:** Edit the intro text in `public/index.html`
- **Module pages:** Copy `public/modules/veiled-city.html` for each module
- **Social links:** Replace placeholder URLs with your real Itch.io, Patreon, Discord links
- **Contact email:** Update `mailto:` link in navigation

### 5. Push to GitHub
```bash
# If you haven't pushed yet:
git remote add origin https://github.com/YOUR_USERNAME/mucilage.net.git
git push -u origin main
```

### 6. Deploy to Cloudflare Pages
See [DEPLOYMENT.md](DEPLOYMENT.md) for the complete step-by-step guide.

**TL;DR:**
1. Point your Porkbun domain to Cloudflare (change nameservers)
2. Connect GitHub repo to Cloudflare Pages
3. Set build output to `public`
4. Done! Auto-deploys on every git push

## 🎨 Design Features

✅ Dark vintage D&D aesthetic (like your screenshot)
✅ Module cards with title + description below (not overlaid)
✅ Fully responsive (mobile, tablet, desktop)
✅ Clean typography (Cinzel + Lora fonts)
✅ Parchment color palette (#c9b896, #8b7355, #2a2520)
✅ Fast loading (no frameworks, minimal CSS)
✅ SEO-friendly with semantic HTML

## 💡 How to Add a New Module

1. **Copy the template:**
   ```bash
   cp public/modules/veiled-city.html public/modules/my-new-module.html
   ```

2. **Edit the new file** with your module's content

3. **Add it to homepage** (`public/index.html`):
   ```html
   <a href="modules/my-new-module.html" class="module-card">
     <div class="module-cover">
       <img src="images/modules/my-new-module.jpg" alt="My New Module">
     </div>
     <h3 class="module-title">My New Module</h3>
     <p class="module-description">One sentence description here.</p>
   </a>
   ```

## 🆘 Need Help?

Check out:
- [README.md](README.md) - Full documentation
- [DEPLOYMENT.md](DEPLOYMENT.md) - Cloudflare deployment guide

## 🚀 Ready to Go Live?

1. Add your images
2. Update the content
3. Push to GitHub
4. Follow [DEPLOYMENT.md](DEPLOYMENT.md)

Your site will be live at `mucilage.net` in about 30 minutes!

---

**The site is already committed to git and ready to push.** Once you push to GitHub, you can deploy to Cloudflare Pages in minutes.
