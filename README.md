# Strangers · Beirut — Landing Page

A single-file static site (`index.html`). No build step, no dependencies.
Just open it, or deploy it as-is.

---

## Option A — Fastest, no terminal (GitHub web + Vercel)

**1. Make the repo**
- Go to https://github.com/new
- Name it `strangers-beirut` → **Create repository**
- On the empty repo page, click **“uploading an existing file”**
- Drag in `index.html` → **Commit changes**

**2. Publish on Vercel**
- Go to https://vercel.com → **Add New… → Project**
- **Import** your `strangers-beirut` repo
- Framework preset: **Other** · leave everything default → **Deploy**
- ~20 seconds later you get a live URL like `strangers-beirut.vercel.app`

That’s it — every future push to the repo auto-redeploys.

---

## Option B — Terminal (git + Vercel CLI)

```bash
# in the folder that contains index.html
git init
git add index.html
git commit -m "Strangers · Beirut landing page"
git branch -M main
git remote add origin https://github.com/<your-username>/strangers-beirut.git
git push -u origin main

# deploy
npm i -g vercel
vercel            # follow prompts → accept defaults
vercel --prod     # promote to production
```

---

## Custom domain (optional)
In Vercel → your project → **Settings → Domains** → add `strangers-beirut.com` (or your domain) and follow the DNS steps.

## Editing
Everything lives in `index.html` (HTML + CSS + inline SVG logo). The email form is a front-end placeholder — wire it to Mailchimp/Formspree/Resend when you’re ready to actually collect addresses.
