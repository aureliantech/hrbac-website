# Hrbac Intellectual Property Law — Website

Static site, no build step. 11 pages:

```
index.html                                          → /
about.html                                          → /about
contact.html                                        → /contact
faq.html                                             → /faq
copyright.html                                       → /copyright
pricing.html                                         → /pricing
process.html                                         → /process
patents/prosecution-overview.html                    → /patents/prosecution-overview
patents/medical-device-patent-attorney.html           → /patents/medical-device-patent-attorney
patents/software-patent-attorney.html                → /patents/software-patent-attorney
patents/machine-learning-ai-patent-attorney.html     → /patents/machine-learning-ai-patent-attorney
trademarks/trademark-attorney.html                   → /trademarks/trademark-attorney
hrbac-catherine-headshot.jpeg                        → shared headshot, referenced by several pages
vercel.json                                          → enables clean URLs (strips .html)
```

## Deploy to GitHub

```bash
cd hrbac-law-website
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

## Deploy to Vercel

Option A — Vercel CLI (fastest, no GitHub needed first):
```bash
npm i -g vercel      # if you don't already have it
cd hrbac-law-website
vercel               # first deploy, follow the prompts
vercel --prod        # promote to production
```

Option B — via GitHub (auto-deploys on every push):
1. Push this folder to a GitHub repo (see above).
2. Go to https://vercel.com/new, import that repo.
3. Framework preset: "Other" (no build command, no output directory needed — it's static HTML).
4. Deploy.

No environment variables, no build command, and no `package.json` are required — these are plain static HTML files.

## Notes
- Only one real photo is used site-wide: `hrbac-catherine-headshot.jpeg`. A few sections use verified stock photography already live on the original homepage; a couple of spots are clearly-labeled on-brand placeholders where no real photo was available — search for `photo-placeholder-label` if you want to find and replace those once you have real photography.
- All phone links point to `tel:3152171673` and the address in the footer/contact page is `210 E. Fayette St., Syracuse, NY 13202` — update these if they're placeholders.
