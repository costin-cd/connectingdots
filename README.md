# Connecting Dots — Website

Static website for connectingdots.tech. Built with plain HTML/CSS — no build tools, no dependencies.

## Files
- `index.html` — Homepage
- `about.html` — About page
- `contact.html` — Contact page with form
- `shipping-accelerator.html` — Service page
- `guidance-program.html` — Service page
- `launchpad.html` — Service page
- `vcs.html` — For VCs landing page
- `flash-audit.html` — VC service page
- `due-diligence.html` — VC service page
- `style.css` — All styles
- `logo.png` — Your logo (ADD THIS FILE — export from Wix or use your own)

## Add Your Logo
Export your logo from Wix (or use your existing file) and place it as `logo.png` in this folder.
If no logo file is present, the site gracefully falls back to the text "Connecting Dots".

## Deploying to Cloudflare Pages (free)

### Step 1 — Create a GitHub repository
1. Go to https://github.com and create a free account if you don't have one
2. Click "New repository" → name it `connectingdots-website` → set it to Private → Create
3. Upload all the files from this folder to the repository

### Step 2 — Connect Cloudflare Pages
1. Go to https://dash.cloudflare.com and create a free account
2. Go to "Workers & Pages" → "Create" → "Pages" → "Connect to Git"
3. Select your GitHub repository
4. Build settings: leave everything blank (no build command needed — it's plain HTML)
5. Click "Save and Deploy" — your site goes live in ~30 seconds

### Step 3 — Connect your domain
1. In Cloudflare Pages, go to your project → "Custom domains" → "Set up a custom domain"
2. Enter `connectingdots.tech` and follow the instructions
3. If your domain is registered elsewhere (e.g. GoDaddy, Namecheap), you'll update the nameservers to point to Cloudflare
4. Cloudflare handles HTTPS automatically — no SSL certificates to manage

### Step 4 — Set up the contact form
The contact form uses `data-netlify="true"` which works if you host on Netlify instead of Cloudflare.

**Option A — Use Netlify (also free, equally easy):**
Same as above but use https://netlify.com instead of Cloudflare Pages.
Netlify automatically detects and handles forms — no extra setup needed.
Form submissions land in your Netlify dashboard and can be emailed to you.

**Option B — Use Formspree (works with Cloudflare):**
1. Go to https://formspree.io and create a free account
2. Create a new form → get your form endpoint URL (looks like `https://formspree.io/f/xxxxxxxx`)
3. In `contact.html`, replace the `<form>` tag's `action` attribute with your Formspree URL
   and remove `data-netlify="true"`

## Making edits
Just edit the HTML files directly in any text editor (even Notepad).
Then push the changes to GitHub — Cloudflare/Netlify will redeploy automatically in ~30 seconds.

## Blog
The Wix blog is not included in this static version.
Options for adding a blog later:
- Use a free service like **Substack** or **Ghost** and link to it from the nav
- Add Markdown-based blogging via **Hugo** or **Eleventy** (Claude can help you set this up)

## Cost summary
| Item | Cost |
|------|------|
| GitHub | Free |
| Cloudflare Pages hosting | Free |
| Cloudflare SSL certificate | Free |
| Formspree (up to 50 submissions/month) | Free |
| Your domain (connectingdots.tech) | ~€10–15/year |
| **Total** | **~€10–15/year** |
