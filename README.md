# Relia Product Catalogue

The online product catalogue for Relia: 241 products across 20 brands, with filters by
division, brand and category, search by name / item code / barcode, and a downloadable PDF.

Everything runs in the browser from a single file. There is no server, no database and no
build step, so it can be hosted on GitHub Pages for free.

---

## Publish it (about 10 minutes, no software to install)

### 1. Create the repository

1. Sign in at **github.com** (create a free account if you don't have one).
2. Click **+** (top right) → **New repository**.
3. Name it `catalogue`.
4. Choose **Public**. GitHub Pages is free only for public repositories.
5. Click **Create repository**.

> "Public" means the website is public, which is what you want. It does not publish
> anything private; this folder contains only the catalogue.

### 2. Upload these files

1. On the new repository page, click **uploading an existing file**.
2. Select **all** the files in this folder and drag them in, including the file named
   `.nojekyll`. It starts with a dot and is easy to miss.
3. Click **Commit changes**.

> If `.nojekyll` doesn't upload from your computer, create it in GitHub instead:
> **Add file → Create new file**, name it `.nojekyll`, leave it empty, commit.

### 3. Turn on GitHub Pages

1. Go to **Settings** → **Pages** (left sidebar).
2. Under **Source**, choose **Deploy from a branch**.
3. Branch: **main**, folder: **/ (root)**. Click **Save**.
4. Wait 1–2 minutes, then refresh. Your address appears at the top:

```
https://YOUR-USERNAME.github.io/catalogue/
```

That link opens for anyone, on any device, with no login and no account.

### 4. Check it

Open the link on a phone that is not signed in to anything and confirm:

- the first page, brand logos and all product pictures load
- the Division / Brand / Category filters and the search work
- **Download PDF** produces the PDF file
- the arrow button at the bottom right returns you to the top

---

## Use your own address (optional but recommended)

To serve the catalogue at `catalogue.relia-me.com` instead:

1. Ask whoever manages the `relia-me.com` domain to add a **CNAME** record:

   | Type  | Name        | Value                     |
   |-------|-------------|---------------------------|
   | CNAME | `catalogue` | `YOUR-USERNAME.github.io` |

2. In the repository: **Settings → Pages → Custom domain**, enter
   `catalogue.relia-me.com` and click **Save**. GitHub adds a `CNAME` file for you.
3. Once the check passes, tick **Enforce HTTPS**.

DNS changes can take anything from a few minutes to a few hours to take effect.

---

## Updating the catalogue later

The catalogue lives entirely in `index.html`. To publish a new version:

1. Open the repository on GitHub.
2. Click `index.html` → the **⋯** menu → **Delete file** → **Commit changes**.
3. **Add file → Upload files**, upload the new `index.html`, then **Commit changes**.

The site updates in about a minute. **The web address never changes**, so any printed QR
codes keep working.

---

## What each file does

| File                   | Purpose                                                          |
|------------------------|------------------------------------------------------------------|
| `index.html`           | The entire catalogue: products, pictures, logos, PDF generator    |
| `404.html`             | Friendly page shown if someone mistypes the address               |
| `.nojekyll`            | Tells GitHub to serve the files as-is. **Required, don't delete** |
| `social-preview.png`   | The image shown when the link is shared on WhatsApp or email      |
| `icon-512.png`         | App icon when someone adds the catalogue to their home screen     |
| `apple-touch-icon.png` | The same icon, for iPhone and iPad                                |
| `favicon-32.png`       | The small icon in the browser tab                                 |

---

## Notes

- **Pictures are inside `index.html`.** They are embedded in the file, which is why it is
  around 6.9 MB. There is no separate images folder to manage.
- **The PDF is built on demand.** It is created in the visitor's browser when they tap
  **Download PDF**, so it always matches whatever the catalogue currently shows. No PDF
  file needs to be kept up to date here.
- **Link previews.** If WhatsApp doesn't show the preview image, edit `index.html` and
  replace `content="social-preview.png"` with the full address, for example
  `content="https://catalogue.relia-me.com/social-preview.png"` (there are two of them).
- **Anyone can view, nobody can edit.** Visitors only read the page. Changes are made by
  uploading a new `index.html` to this repository.

---

## Ordering contacts shown in the catalogue

- info@relia-me.com
- +966 12 697 0779
- Dilan: +966 53 391 1086
- Hesham: +966 54 778 1006
- www.relia-me.com
