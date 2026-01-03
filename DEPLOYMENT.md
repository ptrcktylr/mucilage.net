# Deploying to Cloudflare Pages

## Step-by-Step Guide

### 1. Point Your Domain to Cloudflare

1. Go to [cloudflare.com](https://cloudflare.com) and create a free account
2. Click "Add a Site" and enter `mucilage.net`
3. Select the **Free plan**
4. Cloudflare will scan your DNS records (this takes ~1 minute)
5. Review the detected DNS records and click "Continue"
6. Cloudflare will show you **2 nameservers** (they look like: `elsa.ns.cloudflare.com` and `tim.ns.cloudflare.com`)

7. **Update nameservers at Porkbun:**
   - Log in to [porkbun.com](https://porkbun.com)
   - Go to "Domain Management"
   - Click on `mucilage.net`
   - Find "Nameservers" section
   - Change from Porkbun's nameservers to the **Cloudflare nameservers**
   - Click "Submit"

8. Go back to Cloudflare and click "Done, check nameservers"
   - This can take up to 24 hours, but usually happens in 5-15 minutes
   - You'll get an email when it's active

### 2. Push Code to GitHub

If you haven't already:

```bash
# Initialize git (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit - Mucilage portfolio site"

# Create a new repository on GitHub, then:
git remote add origin https://github.com/YOUR_USERNAME/mucilage.net.git
git branch -M main
git push -u origin main
```

### 3. Deploy to Cloudflare Pages

1. In Cloudflare Dashboard, click **"Pages"** in the left sidebar
2. Click **"Create a project"**
3. Click **"Connect to Git"**
4. Select **GitHub** and authorize Cloudflare
5. Select your `mucilage.net` repository
6. Configure build settings:
   - **Project name:** `mucilage` (or whatever you want)
   - **Production branch:** `main`
   - **Build command:** *(leave empty)*
   - **Build output directory:** `public`
7. Click **"Save and Deploy"**

Your site will build in ~30 seconds!

### 4. Add Custom Domain

1. Once deployed, click on your project in Cloudflare Pages
2. Go to **"Custom domains"** tab
3. Click **"Set up a custom domain"**
4. Enter `mucilage.net`
5. Click **"Continue"**
6. Cloudflare will automatically configure DNS
7. Also add `www.mucilage.net` (optional but recommended)

### 5. Done!

Your site is now live at:
- `https://mucilage.net`
- `https://YOUR_PROJECT.pages.dev` (Cloudflare's free subdomain)

## Automatic Deployments

Every time you push to GitHub, Cloudflare Pages will automatically rebuild and deploy your site. It takes about 30 seconds.

```bash
# Make changes to your site
# Then:
git add .
git commit -m "Updated module content"
git push

# Site auto-deploys in ~30 seconds!
```

## Troubleshooting

**Problem:** Site shows 404 errors
- **Solution:** Make sure build output directory is set to `public`

**Problem:** Images not loading
- **Solution:** Check image paths are relative (e.g., `images/modules/veiled-city.jpg` not `/images/...`)

**Problem:** Nameserver changes taking too long
- **Solution:** Can take up to 24 hours, but usually 5-15 minutes. Check status at Cloudflare dashboard.

**Problem:** CSS not loading
- **Solution:** Clear browser cache or open in incognito mode

## Free SSL Certificate

Cloudflare automatically provides a free SSL certificate, so your site will always use `https://` - no configuration needed!

## Cost

Everything is **100% free**:
- ✅ Cloudflare DNS (free forever)
- ✅ Cloudflare Pages hosting (free for unlimited sites)
- ✅ SSL certificate (free)
- ✅ Unlimited bandwidth (free)
- ✅ Automatic deployments (free)

You only pay for your domain name at Porkbun (~$10/year).
