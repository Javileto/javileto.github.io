# Javier Lera — academic website

A Quarto website with a petrol blue and coral identity, D2 JL monogram and a classical homepage with space for a professional photograph.

## No-programming setup using GitHub's website

1. In GitHub, create a new **public** repository named `javierlera.github.io` if your GitHub username is `javierlera`. Otherwise use `<your-username>.github.io`. Do not initialise with a README.
2. Extract this ZIP. Upload **the contents** of the `javierlera-quarto` folder (not the outer folder) to the repository using **Add file → Upload files** and commit to `main`. GitHub's upload interface may not preserve hidden `.github/workflows/publish.yml` depending on how you upload. Verify that the file appears after committing; if it is missing, add it via GitHub's "Create new file", using the exact path `.github/workflows/publish.yml`, and paste its contents.
3. Go to **Settings → Pages** and select **GitHub Actions** as the build/deployment source.
4. Open **Actions**, and run **Publish Quarto website** (or make another commit). Wait for a successful green check.
5. Open `https://<your-username>.github.io` and review the site before connecting your paid domain.
6. Once approved, add the domain `www.javierlera.com` under **Settings → Pages → Custom domain**, and configure DNS records at your domain registrar as indicated by GitHub. Do not point your live domain until the site works.

## Add your portrait later

In `index.qmd`, replace the entire `<div class="portrait-placeholder">...</div>` with:

```html
<img class="portrait-photo" src="assets/portrait.jpg" alt="Portrait of Javier Lera">
```

Upload your image as `assets/portrait.jpg`. Keep it compressed for the web.

## Edit your content

- Homepage: `index.qmd`
- Publications: `publications.qmd`
- Research: `research.qmd`
- Projects: `projects.qmd`
- Teaching: `teaching.qmd`
- Conferences: `conferences.qmd`
- Styles/colors: `styles.css`
- Menu, footer, site configuration: `_quarto.yml`
- JL icon: `assets/jl-monogram.svg`

To change any text on GitHub, open the relevant `.qmd` file, click the pencil icon, make changes and commit. The website publishes automatically after the workflow runs.

## Editorial notes

- The included CV is the PDF provided by the user, whose first page says September 2026. Replace it as needed.
- Some long author lists in the publications page are intentionally abbreviated in this initial draft. Validate against CV before launch.
- Conferences page is a placeholder because the uploaded CV does not give conference details.
- This is a source project: Quarto must render it. The `.github/workflows/publish.yml` file configures GitHub Actions to do this automatically.
