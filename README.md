# Merlion Fertility Centre — Website

A single-page, static website for Merlion Fertility Centre (Singapore Centre for Reproductive & Oncofertility Medicine). No build step, no backend — pure HTML/CSS/JS.

## Structure

```
index.html          # the whole site
assets/logo.png      # clinic logo
```

## Running locally

Just open `index.html` in a browser, or serve it with any static server, e.g.:

```
python3 -m http.server
```

## Deploying on GitHub Pages

1. Push this folder to a GitHub repo.
2. Go to **Settings → Pages**.
3. Set the source branch to `main` (or `master`) and folder to `/ (root)`.
4. Your site will be live at `https://<username>.github.io/<repo-name>/`.

## Editing content

Everything lives in `index.html`:
- **Hero** — top of the file, inside `<section class="hero">`
- **About** — `<section class="about" id="about">`
- **Services** — `<section id="services">`, each service is a `.service-row`
- **Doctors / team** — `<section class="doctors" id="doctors">`, each person is a `.doctor` block
- **Patient stories** — `<section class="testimonials" id="stories">`, each quote is a `.testimonial-slide`
- **Contact & location** — `<section id="contact">`

The contact form currently has no backend — it just shows a confirmation message client-side. To make it actually send messages, connect it to a form service (e.g. Formspree, Getform) or your own backend, and point the `<form>`'s submit handler at it.
