# Jeff & Deb — Newlywed Landing Page

A celebratory single-page site built with [Astro](https://astro.build) to share Jeff & Deb's wedding joy and tease their upcoming music releases. The layout includes a hero moment, a wedding day photo gallery, timeline for forthcoming songs, and an email capture block wired for Netlify forms (swap for your preferred email tool when ready).

## Local Development

```bash
npm install
npm run dev
```

- Develops at `http://localhost:4321/` with hot reloading.
- Run `npm run build` anytime to confirm the production output in `dist/`.

## Project Structure

```
/
├── public/
│   └── images/           # Logo + wedding images (replace placeholders)
├── src/
│   └── pages/
│       └── index.astro   # Landing page markup + styling
├── astro.config.mjs
├── package.json
└── tsconfig.json
```

### Replacing the placeholders

1. Drop the real logo in `public/images/logo.svg` (any image format works—update the filename in `index.astro` if you change it).
2. Add wedding photos to `public/images/` and update the `gallery` array at the top of `src/pages/index.astro` with the new filenames and alt text.
3. Adjust copy, timeline dates, and email address in `index.astro` to reflect the latest plans.

The temporary SVGs currently in `public/images/` simply hold layout space and can be deleted once real assets are in place.

## Deploying to Vercel

1. Push this repo to GitHub (or your Git provider of choice).
2. In Vercel, click **New Project** and import the repository.
3. Use the defaults that Vercel detects for Astro:
   - Build Command: `npm run build`
   - Output Directory: `dist`
4. Trigger a deploy. Future pushes to the default branch will auto-deploy.

_Optional_: Add `NETLIFY=true` (or remove the `netlify` attribute) in the newsletter form if you host the form elsewhere. Swap in integrations such as Mailchimp, ConvertKit, or Formspree to collect sign-ups.

## Next Ideas

- Embed an audio player once the first demo is ready.
- Add a stories/blog section by creating Markdown files under `src/pages/`.
- Hook the newsletter form to your email platform for automated welcome notes.
