# Subspace Public Pages

This folder contains the lightweight public pages needed for App Store Connect:

- `support/` - support page for users and App Review
- `privacy/` - privacy policy for Subspace Subscription Tracker
- `index.html` - small link hub until the full landing page is built

The pages are plain static HTML and CSS. They intentionally include no analytics, no tracking scripts,
no JavaScript, and no third-party dependencies.

## Production URLs

The main Subspace app repository stays private. Public App Store support pages are deployed
from a separate public GitHub repository:

- Website repository: `https://github.com/Shairy111/SubspaceSite`

Use these stable public URLs in App Store Connect:

- Support URL: `https://shairy111.github.io/SubspaceSite/support/`
- Privacy Policy URL: `https://shairy111.github.io/SubspaceSite/privacy/`

The root link hub is available at:

- Website hub: `https://shairy111.github.io/SubspaceSite/`

If the final domain changes later, update App Store Connect to point at the deployed equivalents.

## Deployment

Deploy only the contents of this `website/` folder to the root of the public `SubspaceSite`
repository. Do not copy the Swift app source, Xcode project, local app data, or private docs.

GitHub Pages for `SubspaceSite` is configured to publish from:

- branch: `main`
- folder: repository root (`/`)

No build step is required. The site is plain HTML and CSS.

## Local Preview

From the repo root:

```sh
python3 -m http.server 8080 --directory website
```

Then open:

- `http://localhost:8080/support/`
- `http://localhost:8080/privacy/`

## Launch Notes

- The support page currently uses GitHub issues as the public support channel.
- Add a dedicated support email later if desired.
- Keep the privacy policy updated if Subspace adds analytics, account systems, external services,
  or any behavior that changes how user data is handled.
