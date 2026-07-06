# Mound City Fund — Website

Static website for Mound City Fund, a Missouri nonprofit making charitable redevelopment grants in North St. Louis. Built as plain HTML and CSS with no build step, so it deploys directly to GitHub Pages.

## Structure

- `index.html` — Home: mission, the vacancy problem, how the grant works, ecosystem framing, and a document index
- `the-case.html` — Economic Rationale and Market Landscape & Positioning (the two-part donor case)
- `grants.html` — Grant Program Guidelines and Application Procedures
- `grant-agreement.html` — Grant Agreement overview (plain-language summary of key terms) and grant application download
- `donors.html` — Gift Acceptance Policy and Donor Privacy Policy
- `governance.html` — Governance and Transparency (Whistleblower, Document Retention, Public Disclosure)
- `faq.html` — Frequently Asked Questions
- `target-area.html` — Published Target Area (schematic map and governing definition)
- `contact.html` — Contact page (grant, donor, partner, and governance inquiries)
- `assets/styles.css` — Shared stylesheet (design set palette: navy #003049, red #C12126, cream #FFF7EA; Georgia house type)
- `assets/mcf-wordmark-cream.png`, `assets/mcf-badge-cream.png` — Transparent logo assets for dark backgrounds (used in the header and footer)
- `assets/mcf-wordmark-blue.png`, `assets/mcf-badge-blue.png`, `assets/favicon.png` — Transparent navy logo assets for light backgrounds

## Deploying to GitHub Pages

1. Create a new repository on GitHub (for example, `mound-city-fund` under your account, or `YOURUSERNAME.github.io` for a root user site).
2. Upload all of these files preserving the folder structure (the `assets` folder must sit next to the HTML files). You can drag and drop them in the GitHub web interface via "Add file > Upload files," or push with git:
   ```
   git init
   git add .
   git commit -m "Mound City Fund website"
   git branch -M main
   git remote add origin https://github.com/YOURUSERNAME/mound-city-fund.git
   git push -u origin main
   ```
3. In the repository, go to Settings > Pages. Under "Build and deployment," set Source to "Deploy from a branch," choose the `main` branch and the `/ (root)` folder, and save.
4. The site will be live within a minute or two at `https://YOURUSERNAME.github.io/mound-city-fund/` (or at `https://YOURUSERNAME.github.io/` if you used the special root repository name).

## Custom domain (optional)

If you have a domain like moundcityfund.org, add it under Settings > Pages > Custom domain, then create the DNS records your registrar requires (a CNAME pointing to `YOURUSERNAME.github.io` for a subdomain like www, or GitHub's four A records for the apex). Enable "Enforce HTTPS" once the certificate is issued.

## Placeholders to update before launch

- Ensure the four moundcityfund.org mailboxes referenced on `contact.html` and `donors.html` (grants@, give@, partners@, info@) are set up and monitored (the mailing address, 9909 Manchester Road, Unit 109, Saint Louis, MO 63122, is already in place)
- Add the fillable grant application PDF at `assets/MCF-Grant-Application.pdf` (the Grant Agreement page links to this path)
- The donation platform embed on `donors.html` (a commented slot marks exactly where to paste Zeffy, Givebutter, Stripe, or PayPal embed code; delete the "coming soon" notice when live)
- The target area on `target-area.html` is marked as a draft pending Board adoption; remove the draft notice once adopted by resolution, and refine the schematic boundary if desired
- The per-project grant cap once set annually by the Board
- The 501(c)(3) disclosure language site-wide upon receipt of the IRS determination letter
