 <p align="center">
  <img src="site/favicon.svg" alt="" width="96" height="96">
</p>

<h1 align="center">Hedgerow</h1>

<p align="center"><strong>Small, self-hosted apps that live together.</strong></p>

<p align="center"><a href="https://hedgerow.tools/">hedgerow.tools</a></p>

Hedgerow is a family of small apps you run on your own machines: self-hosted services for your server and fast native tools for your desktop. A hedgerow is the habitat these animals share: the vole lives at its foot, the kestrel hunts along it, the newt hides in its damp corners and the wren nests in its tangles. Each app is named *Adjective + Animal*.

| App | What it does | Status | License | Links |
|---|---|---|---|---|
| **Vigilant Vole** | Self-hosted uptime monitoring, an Uptime Kuma alternative | Released | AGPL-3.0-only (proposed; PR pending) | [Website](https://hedgerow.tools/Vigilant-Vole/) · [GitHub](https://github.com/Ferdinand99/Vigilant-Vole) · [License PR](https://github.com/Ferdinand99/Vigilant-Vole/pull/61) |
| **Nimble Newt** | Fast, modern text editor for Windows and macOS | Released | AGPL-3.0-only (proposed; PR pending) | [Website](https://hedgerow.tools/Nimble-Newt/) · [GitHub](https://github.com/Ferdinand99/Nimble-Newt) · [License PR](https://github.com/Ferdinand99/Nimble-Newt/pull/25) |
| **Keen Kestrel** | Self-hosted, Sentry-compatible error tracking and cookieless analytics | Early release (v0.1) | AGPL-3.0-only (proposed; PR pending) | [Website](https://hedgerow.tools/Keen-Kestrel/) · [GitHub](https://github.com/Ferdinand99/Keen-Kestrel) · [License PR](https://github.com/Ferdinand99/Keen-Kestrel/pull/40) |
| **Wise Wren** | Keeps Docker containers up to date without surprises: approve, snapshot, health check, rollback | In design | AGPL-3.0-only (proposed; PR pending) | [Website](https://hedgerow.tools/Wise-Wren/) · [GitHub](https://github.com/Ferdinand99/Wise-Wren) · [License PR](https://github.com/Ferdinand99/Wise-Wren/pull/32) |

The apps share a privacy-first approach, a common design system and, increasingly, a shared Rust foundation. `vole-kit`, the shared foundation crate in Vigilant Vole, is included in that project's proposed AGPL-3.0-only relicensing. KestrelKit is also proposed to move to AGPL-3.0-only: [KestrelKit license PR](https://github.com/Ferdinand99/KestrelKit/pull/8).

The license changes above are proposed in draft pull requests and are not effective until the relevant changes are merged. Check each project's repository for its current license.

## This repository

This is the GitHub user site for [@Ferdinand99](https://github.com/Ferdinand99), served at the root of `https://hedgerow.tools/`. The apps' own sites live in their repositories and are served under their paths (`/Vigilant-Vole/`, `/Nimble-Newt/`, `/Keen-Kestrel/`, `/Wise-Wren/`).

- `site/` is the whole website: plain HTML, CSS and a small script, with no build step. It uses the same design tokens and components as the app sites, a self-hosted Inter font and a strict Content Security Policy.
- `.github/workflows/pages.yml` publishes `site/` on every push to `main` that touches it, or manually from the Actions tab. One-time setup: **Settings → Pages → Build and deployment → Source: GitHub Actions**.

To preview locally, serve the folder with any static server, for example:

```sh
python -m http.server -d site 8000
```

Then open <http://localhost:8000/>.

## License

The website source code in this repository is licensed under the [MIT License](LICENSE). This license applies to the website code in this repository, not automatically to the separate Hedgerow app repositories.

Third-party assets retain their own licenses:

- Inter is licensed under the SIL Open Font License; see [`site/fonts/Inter-LICENSE.txt`](site/fonts/Inter-LICENSE.txt).
- The Sylo and Subtrack icons belong to their respective projects. Subtrack is source-available, not open source.
