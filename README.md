# Boilerplate

This repository is the ever-changing boilerplate of my preferred development
stack and workflow for simple web projects. Components include:

- [`Hugo`](https://gohugo.io/) for content management.
- ['UIKit`](https://getuikit.com/) for web components.
- [`TypeScript`](https://www.typescriptlang.org/) for dynamic behavior on pages.
- [`SCSS`](https://sass-lang.com/documentation/syntax) for web styles and
  customizing the UIKit theme.
- [`Cloudflare Pages`](https://pages.cloudflare.com/) for serving content.
- [`Cloudflare Workers`](https://workers.cloudflare.com/) for customizing how
  web pages are served, including putting pages behind a login.

## Setup

No setup is needed to modify content of existing pages. Just modify the Markdown
files for the page under `content/` directly in Github or locally with your
preferred editor. To preview changes before they are deployed, open a pull
request and a preview site will be deployed for your branch.

To test changes locally or create new pages:

1. [Install Node.js](https://nodejs.dev/learn/how-to-install-nodejs)
2. Clone this repository.
3. Run `npm install` in the root directory of your clone.

## Developing

To test the site locally, run `npm start`, then navigate to the prompted web
page in your browser (usually `http://localhost:1313/`). It should automatically
refresh whenever you make a change.

To create a new page, run `npm run new path/to/new/page.md` where
`path/to/new/page.md` is the location of the page on the site (aka. relative to
`content/`).

To deploy the site manually, run `npm run build` and copy `public/` to your
server's web root. This should not normally be necessary since the site is
automatically deployed whenever the `main` branch is updated.

## Organization

This site uses
[Hugo's default directory structure](https://gohugo.io/getting-started/directory-structure/).

- `archetypes/` contains templates to simplify creating new pages.
  [See docs](https://gohugo.io/getting-started/directory-structure/).
- `assets/` contains non-HTML files which are preprocessed with
  [Hugo Pipes](https://gohugo.io/hugo-pipes/introduction/) like images, SCSS,
  and TypeScript.
- `content/` contains Markdown files to define the site's page content.
  [See docs](https://gohugo.io/content-management/organization/#organization-of-content-source).
- `layouts/` contains HTML templates which define the site's structure.
  [See docs](https://gohugo.io/templates/introduction/)
- `laouts/partials/` contains partial pages which are used in other templates.
- `layouts/shortcodes/` contains shortcode definitions which can be used from
  Markdown content [See docs](https://gohugo.io/content-management/shortcodes/).
- `static/` contains additional files which do not need preprocessing and are
  made available on the site as-is.
- `package.json` contains versions for the site's dependencies. While these are
  typically used from TypeScript, some like Font Awesome and UIKit also have
  content referenced from SCSS or directly mounted into `static/` via
  `config.toml`.
  [See docs](https://docs.npmjs.com/cli/v7/configuring-npm/package-json)
- `config.toml` is the Hugo configuration file.
  [See docs](https://gohugo.io/getting-started/configuration/).
