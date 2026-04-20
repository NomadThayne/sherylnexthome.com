# Ojai Homes — Real Estate Site

A neighborhood real estate site for Ojai, CA — modeled after [laiepoint.com](https://laiepoint.com), featuring NextHome branding.

## Files

```
index.html        — Main page (hero, listings, neighborhood, about, agent, contact)
resources.html    — Buyer/seller resource links
README.md         — This file
```

---

## Deploying to GitHub Pages + Cloudflare

This is the same setup used for laiepoint.com. Here's the exact workflow:

### Step 1 — Create a GitHub Repository

1. Go to [github.com/new](https://github.com/new)
2. Name it something like `ojai-homes` (or your custom domain name, e.g. `ojairealestate`)
3. Set it to **Public** (required for free GitHub Pages)
4. Don't initialize with a README (you already have files)
5. Click **Create repository**

### Step 2 — Push your files

In your terminal (or GitHub Desktop):

```bash
cd /path/to/ojai-realestate
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

Or use **GitHub Desktop** — drag the folder in, commit, and push.

### Step 3 — Enable GitHub Pages

1. In your repo on GitHub, go to **Settings → Pages**
2. Under "Source", select **Deploy from a branch**
3. Branch: `main` / Folder: `/ (root)`
4. Click **Save**
5. GitHub will give you a URL like `https://yourusername.github.io/ojai-homes/`

---

### Step 4 — Set up your domain in Cloudflare

Assuming you've purchased your domain through Cloudflare (same as laiepoint.com):

1. Log in to [dash.cloudflare.com](https://dash.cloudflare.com)
2. Select your domain → go to **DNS → Records**
3. Add these 4 **A records** pointing to GitHub Pages IPs:

| Type | Name | Content         | Proxy |
|------|------|-----------------|-------|
| A    | @    | 185.199.108.153 | DNS only (gray cloud) |
| A    | @    | 185.199.109.153 | DNS only |
| A    | @    | 185.199.110.153 | DNS only |
| A    | @    | 185.199.111.153 | DNS only |

4. Add a **CNAME record** for `www`:

| Type  | Name | Content                          | Proxy |
|-------|------|----------------------------------|-------|
| CNAME | www  | yourusername.github.io           | DNS only |

> ⚠️ Set DNS records to **DNS only** (gray cloud), NOT proxied. GitHub Pages handles HTTPS itself and Cloudflare proxying can cause certificate issues.

---

### Step 5 — Add custom domain in GitHub Pages

1. Back in GitHub → Settings → Pages
2. Under "Custom domain", enter your domain (e.g. `ojairealestate.com`)
3. Click **Save**
4. GitHub will add a `CNAME` file to your repo automatically
5. Check "Enforce HTTPS" once the certificate is issued (takes ~10 min)

---

### Step 6 — Verify

- Visit `https://yourdomain.com` — you should see the site
- Visit `https://www.yourdomain.com` — should redirect to root

---

## Making Updates

Any changes you push to the `main` branch on GitHub will automatically redeploy via GitHub Pages (usually within 1–2 minutes).

```bash
# Edit a file, then:
git add .
git commit -m "Updated listings"
git push
```

---

## Customization Checklist

Before going live, update these placeholders in `index.html`:

- [ ] **Sheryl's last name** — search for `[Last Name]` and replace
- [ ] **Sheryl's phone number** — search for `(805) 000-0000`
- [ ] **Sheryl's email** — search for `sheryl@nexthome.com`
- [ ] **DRE license number** — search for `#XXXXXXX`
- [ ] **NextHome office address** — update in the contact section
- [ ] **Listing details** — replace placeholder listings with real MLS data
- [ ] **Agent photo** — replace the 👩 emoji placeholder with a real `<img>` tag
- [ ] **Property photos** — replace gradient placeholders with real photos

### Adding a real agent photo

Replace the `<div class="agent-photo">👩</div>` with:

```html
<img src="images/sheryl.jpg" alt="Sheryl [Last Name], Realtor" class="agent-photo" style="object-fit: cover;">
```

And add `images/sheryl.jpg` to the repo.

### Adding real listing photos

Replace `<div class="listing-img lavender">` with:

```html
<div class="listing-img" style="padding: 0;">
  <img src="images/lavender-ridge.jpg" alt="Lavender Ridge" style="width:100%; height:100%; object-fit:cover;">
  <span class="listing-badge available">Active</span>
</div>
```

---

## Notes

- The site is **pure HTML/CSS** — no build tools, no dependencies, no CMS needed
- Fonts load from Google Fonts (requires internet connection)
- The contact form is **not wired up** — you'll need to connect it to a form service like [Formspree](https://formspree.io), [Netlify Forms](https://docs.netlify.com/forms/setup/), or a mailto link

### Quick contact form via Formspree (free tier)

1. Sign up at formspree.io
2. Create a new form, get your endpoint URL
3. Replace `<form onsubmit="return false;">` in index.html with:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

And change the submit button to `type="submit"`.

---

*Built to match the laiepoint.com structure. Hosted on GitHub Pages, domain via Cloudflare.*
