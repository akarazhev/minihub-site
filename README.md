# minihub-site

The page served at [minihub.app](https://minihub.app).

Hand-written static HTML. No build step, no dependencies: an edit is a
commit is a deploy.

## Deployment

Cloudflare Pages, connected to this repository.

- Build command: none
- Output directory: repository root
- Custom domain: `minihub.app` (apex), `www` redirects to it

## The one rule

**Only list what works right now.**

The `Live` section contains running products. It does not contain plans,
roadmaps, or anything labelled "coming soon". If a product is not
reachable at a URL today, it does not appear on this page.

## Adding a project

Copy the existing block inside the `Live` section of `index.html`:

```html
<a class="project" href="https://example.minihub.app">
  <h3>Product Name</h3>
  <p>One sentence, taken from the product's own meta description.</p>
  <span class="project-url">example.minihub.app</span>
</a>
```

Take the description from the product's own `meta description` rather than
writing a new one, so there is a single source of truth.

## Design notes

The page is read by people who spend their day reading dense financial
documents. It is set as a document, not as a startup landing page: system
fonts, one accent colour, no animation, no hero image, no calls to action.

Content must be present in the server response. No client-side rendering.
