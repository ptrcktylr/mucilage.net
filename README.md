# MUCILAGE - Tabletop RPG Module Portfolio

A clean, static HTML site showcasing your tabletop RPG modules with a dark, vintage D&D aesthetic.

## 🎲 Quick Start

1. **View the site locally:**
   - Simply open `public/index.html` in your browser
   - No build step required!

2. **Add your module cover images:**
   - Place images in `public/images/modules/`
   - Recommended size: 600x900px (2:3 aspect ratio)
   - Format: JPG or PNG
   - Example filenames: `veiled-city.jpg`, `dungeon-delvers.jpg`, etc.

3. **Update the HTML to use your images:**
   - Edit `public/index.html` and replace the placeholder divs with:
     ```html
     <img src="images/modules/veiled-city.jpg" alt="The Veiled City">
     ```

## 📁 File Structure

```
public/
├── index.html              # Homepage with module grid
├── about.html              # About page
├── modules/
│   └── veiled-city.html   # Individual module page (template)
├── css/
│   └── styles.css         # All styling
└── images/
    └── modules/           # Your module cover images go here
```

## ✏️ How to Edit

### Adding a New Module

1. **Create a new module page:**
   - Copy `public/modules/veiled-city.html`
   - Rename it (e.g., `my-new-module.html`)
   - Update the content inside

2. **Add it to the homepage:**
   - Edit `public/index.html`
   - Add a new module card in the grid:
     ```html
     <a href="modules/my-new-module.html" class="module-card">
       <div class="module-cover">
         <img src="images/modules/my-new-module.jpg" alt="My New Module">
       </div>
       <h3 class="module-title">My New Module</h3>
       <p class="module-description">A brief one-sentence description.</p>
     </a>
     ```

### Updating Content

- **Homepage intro text:** Edit the `<div class="intro">` section in `index.html`
- **About page:** Edit `about.html`
- **Module details:** Edit individual files in `modules/`
- **Footer links:** Update URLs in the footer section of any HTML file
- **Social links:** Replace placeholder URLs with your actual Itch.io, Patreon, Discord links

### Styling Customization

All styles are in `public/css/styles.css`. Key color variables at the top:

```css
:root {
  --bg-primary: #2a2520;      /* Main background */
  --bg-secondary: #252018;    /* Header/footer background */
  --text-primary: #c9b896;    /* Main text color */
  --text-secondary: #8b7355;  /* Secondary text */
  /* ... more colors */
}
```

## 🚀 Deployment to Cloudflare Pages

1. **Connect your domain on Porkbun:**
   - Log in to Porkbun
   - Go to your domain's DNS settings
   - Change nameservers to Cloudflare's (you'll get these in step 2)

2. **Set up Cloudflare:**
   - Create free account at [cloudflare.com](https://cloudflare.com)
   - Add your domain
   - Cloudflare will scan your DNS records
   - Copy the nameservers Cloudflare provides
   - Go back to Porkbun and update your domain's nameservers

3. **Deploy to Cloudflare Pages:**
   - Push this repo to GitHub (or GitLab/Bitbucket)
   - Go to Cloudflare Dashboard → Pages
   - Click "Create a project" → "Connect to Git"
   - Select your repository
   - **Build settings:**
     - Build command: (leave empty)
     - Build output directory: `public`
   - Click "Save and Deploy"

4. **Set up custom domain:**
   - In Cloudflare Pages, go to your project
   - Click "Custom domains"
   - Add your domain: `mucilage.net`
   - Cloudflare will automatically configure DNS

That's it! Your site will be live at `mucilage.net` and will auto-deploy whenever you push to GitHub.

## 🎨 Design Notes

- **Dark vintage aesthetic** inspired by old D&D modules
- **Parchment color palette** with warm browns and creams
- **Serif fonts:** Cinzel for headings, Lora for body text
- **Fully responsive** - works on mobile, tablet, and desktop
- **Zero JavaScript dependencies** - just vanilla JS for mobile menu toggle

## 📝 To-Do for Joe

- [ ] Add your actual module cover images to `public/images/modules/`
- [ ] Update the image placeholders in HTML files to use real images
- [ ] Fill in your about section in `about.html`
- [ ] Add real content to `veiled-city.html` (or delete if not needed)
- [ ] Create pages for your other modules (copy the template)
- [ ] Update social media links with your actual URLs
- [ ] Update contact email in navigation
- [ ] Push to GitHub and deploy to Cloudflare Pages

## 🆘 Need Help?

- **Local testing:** Just open `public/index.html` in any browser
- **Image not showing?** Check the file path matches exactly
- **Styling broken?** Make sure `styles.css` is in `public/css/`
- **Deployment issues?** Check that Cloudflare Pages build output is set to `public`

---

Built with plain HTML, CSS, and a sprinkle of vanilla JavaScript. No frameworks, no build tools, just clean code.
