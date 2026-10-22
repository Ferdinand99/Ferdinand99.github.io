<p align="center">
  <img src="site/favicon.svg" alt="" width="96" height="96">
</p>

<h1 align="center">Hedgerow</h1>

<p align="center"><strong>Small, self-hosted apps that live together.</strong></p>

<p align="center"><a href="https://hedgerow.tools/">hedgerow.tools</a></p>

Hedgerow is the family name of a few small apps you run on your own machines: self-hosted services
for your server and fast native tools for your desktop. A hedgerow is the habitat these animals
share: the vole lives at its foot, the kestrel hunts along it and the newt hides in its damp
corners. Each app is one of them, named *Adjective + Animal*.

| App | What it does | Status | Links |
|---|---|---|---|
| **Vigilant Vole** | Self-hosted uptime monitoring, an Uptime Kuma alternative | Released | [Website](https://hedgerow.tools/Vigilant-Vole/) · [GitHub](https://github.com/Ferdinand99/Vigilant-Vole) |
| **Nimble Newt** | Fast, modern text editor for Windows and macOS | Released | [Website](https://hedgerow.tools/Nimble-Newt/) · [GitHub](https://github.com/Ferdinand99/Nimble-Newt) |
| **Keen Kestrel** | Self-hosted, Sentry-compatible error tracking and cookieless analytics | In development | [Website](https://hedgerow.tools/Keen-Kestrel/) · [GitHub](https://github.com/Ferdinand99/Keen-Kestrel) |

What they share: built in Rust, SQLite for the services, privacy first with no trackers, one
Apple-inspired design system, 26 interface languages, easy installs on Docker, Unraid, Proxmox and
Linux (or Windows and macOS for the editor), and the MIT license. Vigilant Vole and Keen Kestrel
are moving onto a shared foundation crate, `vole-kit`.

## This repository

This is the GitHub user site for [@Ferdinand99](https://github.com/Ferdinand99), served at the root
of `https://hedgerow.tools/`. The apps' own sites live in their repositories and are served
under their paths (`/Vigilant-Vole/`, `/Nimble-Newt/`, `/Keen-Kestrel/`).

- `site/` is the whole website: plain HTML, CSS and a small script, no build step. It uses the same
  design tokens and components as the app sites, a self-hosted Inter font, a strict Content
  Security Policy, and makes no requests to other sites.
- `.github/workflows/pages.yml` publishes `site/` on every push to `main` that touches it, or by
  hand from the Actions tab. One-time setup: **Settings → Pages → Build and deployment → Source:
  GitHub Actions**.

To preview locally, serve the folder with any static server, for example
`python -m http.server -d site 8000`, and open <http://localhost:8000/>.

## License

[MIT](LICENSE). Inter is licensed under the SIL Open Font License ([`site/fonts/Inter-LICENSE.txt`](site/fonts/Inter-LICENSE.txt)).
The Sylo and Subtrack icons on the site belong to their projects; Subtrack is source-available,
not open source.
