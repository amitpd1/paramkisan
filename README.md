# Param Kisan Landing Page

Static single-page site for Param Kisan, hosted on GitHub Pages at **https://paramkisan.in/**.

## Project files

| File / folder | Purpose |
|---|---|
| `index.html` | The landing page (all HTML, CSS and JavaScript in one file) |
| `assets/` | Product photos and logo used by the page |
| `assets/logo.png` | Param Kisan logo (header, footer, hero badge, browser tab icon) |
| `robots.txt` | Tells search engines and bots what they may crawl, and where the sitemap is |
| `sitemap.xml` | Lists the pages for search engines |
| `llms.txt` | Plain-text guide for AI shopping agents: products, Amazon links, key facts |
| `README.md` | This guide |

## Required image files

Save these files in `assets/` with **exactly** these names (lowercase, `.jpg` unless noted):

- `triple-combo.jpg` – Turmeric, Chilli & Jaggery Combo
- `jaggery-cubes.jpg` – Jaggery Cubes
- `chilli-jaggery-combo.jpg` – Chilli & Jaggery Cubes Combo
- `turmeric-jaggery-combo.jpg` – Turmeric & Jaggery Cubes Combo
- `turmeric-powder.jpg` – Turmeric Powder
- `byadagi-chilli.jpg` – Byadagi Chilli Powder
- `turmeric-chilli-combo.jpg` – Turmeric & Byadagi Chilli Combo
- `logo.png` – Param Kisan logo

Tips: keep each image under about 500 KB. File names are case-sensitive on GitHub.

## Amazon product links (verified)

| Product on the page | ASIN | Link |
|---|---|---|
| Natural Jaggery Cubes | B0H837MKY8 | https://www.amazon.in/dp/B0H837MKY8 |
| Natural Turmeric Powder 100g | B0H82ZDRBS | https://www.amazon.in/dp/B0H82ZDRBS |
| Byadagi Chilli Powder 100g | B0H835DXRZ | https://www.amazon.in/dp/B0H835DXRZ |
| Turmeric, Chilli & Jaggery Trio 690g | B0H83FZLZC | https://www.amazon.in/dp/B0H83FZLZC |
| Chilli & Jaggery Combo 590g | B0H83NJCS3 | https://www.amazon.in/dp/B0H83NJCS3 |
| Turmeric & Jaggery Combo 590g | B0H832GR81 | https://www.amazon.in/dp/B0H832GR81 |
| Turmeric & Byadagi Chilli Combo 200g | B0H82QJDDH | https://www.amazon.in/dp/B0H82QJDDH |

If a listing changes, update the link in **all** of these places: the buttons in `index.html`, the JSON-LD block near the top of `index.html`, and `llms.txt`.

## Publishing an update

Use this every time you change the site, including `index.html`, `llms.txt`, `robots.txt` or `sitemap.xml`.

1. Open the repository on github.com.
2. Click **Add file → Upload files**.
3. Drag in the changed files (for example `index.html`), or the whole `assets/` folder if you added images.
4. Replace any existing file when asked.
5. Type a short message such as "Fix Amazon product links" and click **Commit changes**.
6. Wait 1–2 minutes, then open https://paramkisan.in/ and press **Ctrl + F5** to clear the cache.

To check the build status, open the **Actions** tab. A green tick means the update is live.

## First-time setup (already done)

The site is already live at https://paramkisan.in/. Keep this section for reference if you ever move hosts.

1. Create a free GitHub account at https://github.com.
2. Create a new **public** repository (for example `paramkisan`).
3. Upload the project files: `index.html`, `robots.txt`, `sitemap.xml`, `llms.txt`, `README.md` and the `assets/` folder.
4. Go to **Settings → Pages**.
5. Set **Source** to *Deploy from a branch*, choose branch `main` and folder `/ (root)`, then click **Save**.
6. Under **Custom domain**, enter `paramkisan.in` and click **Save**. Tick **Enforce HTTPS** when available.
7. At your domain registrar, point DNS to GitHub Pages:
   - `A` records for `@` to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www` to `YOUR-USERNAME.github.io`

## Checking the agent and search files

After each update, confirm these open in the browser:

- https://paramkisan.in/robots.txt
- https://paramkisan.in/sitemap.xml
- https://paramkisan.in/llms.txt

Then do a quick check:

- Open https://search.google.com/test/rich-results and enter `https://paramkisan.in/` to confirm the product data is read.
- Click every "Buy on Amazon" button and confirm the Amazon page shows the matching Param Kisan product.

## After the site is live

1. **Google Search Console** (https://search.google.com/search-console): add `paramkisan.in`, verify ownership, then submit `https://paramkisan.in/sitemap.xml`.
2. **Instagram**: the bio links to https://paramkisan.in/.
3. **Amazon listings**: keep the brand name "Param Kisan" in every title so agents can connect the listings to this site.

## Troubleshooting

| Problem | Fix |
|---|---|
| Images are blank | File name in `assets/` doesn't match the table above, or the file is missing. |
| Old version still shows | Press Ctrl + F5. If it still shows, wait 10 minutes and try again. |
| Custom domain shows a 404 or GitHub error | Check the Custom domain setting, and that the DNS records are correct. |
| Site isn't served over HTTPS | Tick **Enforce HTTPS** in Settings → Pages. |
| Link opens the wrong product | Check the ASIN table above, and update the button, JSON-LD and `llms.txt`. |
