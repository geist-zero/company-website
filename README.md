# Geist 0 — Company website

Static website for [geist0.com](https://geist0.com), hosted on **GitHub Pages** (free).

**Repo:** [github.com/geist-zero/company-website](https://github.com/geist-zero/company-website)

---

## Deploy to GitHub Pages

### 1. Push this folder to your repo

From your machine, copy the contents of `website/` into the `company-website` repo root, then push:

```bash
git clone https://github.com/geist-zero/company-website.git
cd company-website

# Copy site files from Geist-0 (adjust path if needed)
cp -R /path/to/Geist-0/website/* .
cp /path/to/Geist-0/website/.nojekyll .

git add .
git commit -m "Add Geist 0 company website for GitHub Pages"
git push origin main
```

Or push directly from this monorepo by making `website/` the repo root (see below).

### 2. Enable GitHub Pages

1. Open **github.com/geist-zero/company-website** → **Settings** → **Pages**
2. **Source:** Deploy from branch
3. **Branch:** `main` → folder **`/ (root)`**
4. Save

GitHub will build the site at `https://geist-zero.github.io/company-website/` within a few minutes.

### 3. Custom domain (geist0.com)

The repo includes a `CNAME` file set to `geist0.com`.

1. In **Settings → Pages → Custom domain**, enter `geist0.com` and save
2. Enable **Enforce HTTPS** when available
3. Update DNS at your domain registrar (remove Squarespace records first)

**DNS records for apex domain `geist0.com`:**

| Type | Name | Value |
|------|------|-------|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `geist-zero.github.io` |

Optional IPv6 (AAAA) records are listed in [GitHub’s docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

### 4. Contact form (optional)

The contact page uses [Formspree](https://formspree.io) (free tier).

1. Create a form at formspree.io → destination `contact@geist0.com`
2. Edit `contact/index.html` → replace `YOUR_FORM_ID` in the form action URL

Until then, visitors can still use the email link.

### 5. Cancel Squarespace

Once `https://geist0.com` loads correctly in an incognito window, cancel Squarespace to stop billing.

---

## Local preview

```bash
cd website
python3 -m http.server 8080
```

Open [http://localhost:8080](http://localhost:8080)

---

## Site structure

```
index.html          Home
about/index.html    About Geist 0
software/index.html Products (in development)
contact/index.html  Contact + form
privacy/index.html  Privacy policy
terms/index.html    Terms of use
assets/css/site.css Styles
CNAME               geist0.com
.nojekyll           Skip Jekyll processing
```

---

## Reply to Apple

> Hello Krisztina,
>
> Our website is now live and functional at https://www.geist0.com. It includes company information, contact details, and a privacy policy for Geist 0, Hilversum, Netherlands.
>
> Please continue processing our enrollment request.
>
> Best regards,
> Mahmut
