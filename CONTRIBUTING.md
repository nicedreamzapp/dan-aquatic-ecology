# Contributing

Thanks for taking a look. This is Dan Close's thesis portfolio, so fixes to the science, typos and
anything that breaks on a phone are all welcome.

## Reporting a problem

Open an [issue](https://github.com/nicedreamzapp/dan-aquatic-ecology/issues/new/choose). The things
that make it quick to fix:

- which page (for example `dan-aquatic-ecology.html`) and which section or slide
- your browser and device, and whether you opened the file directly or through the live site
- a screenshot, and any errors from the browser console
- for a science correction, a source we can check

## Running it locally

There is no build step and nothing to install.

```bash
git clone https://github.com/nicedreamzapp/dan-aquatic-ecology
cd dan-aquatic-ecology
open index.html
```

If a `file://` quirk shows up, serve the folder instead:

```bash
python3 -m http.server 8088
```

Each page is a single HTML file with inline CSS and JavaScript. Please keep it that way, so the
pages still work when emailed or AirDropped. No npm, bundlers or CDN dependencies.

## Tests

There are no automated tests. Before sending a change, open the page you touched in a desktop
browser and at phone width, click through the modals or slides, and check the console for errors.

## Pull requests

Small and focused is easiest to review. For big changes, open an issue first so we can talk it
through. Keep the existing file names, since other sites link to them.

Please follow the [code of conduct](CODE_OF_CONDUCT.md).
