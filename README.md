# Voca CIC Docs

Knowledge base for the **Voca CIC Administrator's Guide, Version 12.2.1**, published with [Fern](https://buildwithfern.com).

## Structure

- `fern/fern.config.json` – Fern organization (`voca-cic`) and CLI version
- `fern/docs.yml` – site settings and navigation
- `fern/pages/*.mdx` – one page per guide section (URL set by the `slug` in each page's front matter)
- `fern/assets/images/` – screenshots and icons

## Publishing

- **Pull request** → `.github/workflows/preview-docs.yml` builds a preview link (staging).
- **Push to `main`** → `.github/workflows/publish-docs.yml` publishes the live site.
- Both need the repository secret `FERN_TOKEN` (created with `fern token`).

## Local check

```bash
npm install -g fern-api
fern check
fern docs broken-links
fern docs dev
```
