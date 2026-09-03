# Personal academic site

A simple, dependency-free personal site (plain HTML/CSS/JS — no Jekyll, no build step) built for free hosting on GitHub Pages.

## Editing your content

Everything is in `index.html`. Search for these and replace with your own info:

- Your name and tagline (appears in the sidebar and hero)
- The "About" paragraphs
- Timeline entries under "Education & Experience"
- Entries under "Publications", "Talks", "Projects & Research", "Outside the Lab"
- Email and social links under "Contact"

Colors, fonts, and spacing all live in `styles.css` if you want to tweak the look — the main color variables are at the top of the file under `:root`.

## Adding your CV or other PDFs

Drop files into the `files/` folder, e.g. `files/cv.pdf`. Then link to them from `index.html` like:

```html
<a href="files/cv.pdf">Download CV</a>
```

## Deploying on GitHub Pages (free)

1. Create a new repository on GitHub named exactly `<your-username>.github.io` (this exact name is what makes it a user site).
2. Upload these files to the repository (or `git push` them — see below).
3. Go to the repo's **Settings → Pages**, and under "Build and deployment" set the source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Wait a minute or two, then visit `https://<your-username>.github.io`.

### Using git from the command line

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
git push -u origin main
```

## Using a custom domain (optional)

If you buy a domain later, add a `CNAME` file to the repo root containing just your domain (e.g. `yourname.com`), then point your domain's DNS at GitHub Pages following [GitHub's custom domain guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
