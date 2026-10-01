# Deployment

## Primary target

Existing Netlify project:

`https://brera-stylebook.netlify.app/`

This is a static site. No build command is required. `netlify.toml` publishes the repository root.

## Netlify Drop — first deployment

Netlify Drop currently accepts a project folder **or ZIP file**. This package is built with `index.html` at the ZIP root, so you can drag the ZIP directly into Netlify Drop / the manual deploy area for the existing project. If your browser or project UI refuses the ZIP, extract it and drag the extracted folder instead.

1. Drag `StyleBook-v1.2.0-Netlify-GitHub-Public.zip` into the existing Netlify project deploy area.
2. Confirm the homepage, `/guide/`, `/contact/` and `/privacy/` load.
3. Confirm the 21-second demo video plays.
4. Submit the contact form once and check the submission under Netlify Forms.

## Connect GitHub after the Drop deploy

Follow `NETLIFY-TO-GITHUB.md`. Once GitHub is connected, use GitHub as the source of truth and let Netlify deploy commits automatically.

## Forms

The contact form contains Netlify Forms markup, a honeypot and client-side states for sending, success and error. Netlify must detect the form after deployment.

`process_form.php` is kept only as a fallback for normal PHP hosting. It is not used by Netlify.

## FTP / PHP fallback

Upload the same site files to a PHP-capable host. Configure the destination address in `process_form.php` as documented inside that file. Do not commit real credentials or secret values to a public repository.

## Domain / SEO

Canonical, Open Graph, sitemap and robots currently use the existing Netlify production domain. If you later move to a custom domain, replace the absolute domain in:

- `index.html`
- `guide/index.html`
- `contact/index.html`
- `privacy/index.html`
- `sitemap.xml`
- `robots.txt`
- `llms.txt`
- `README.md`
