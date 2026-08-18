# Affiliaters extension config

Configuration data for the **Affiliaters Deal Converter** browser extension.

Online stores change their page markup regularly. The files here tell the extension where to
find a product's title, price and image on each supported store, so a change can be corrected
without asking anyone to update or reinstall anything.

## What this is

- **Data, not code.** A list of CSS selectors and text patterns. Nothing served from this
  repo is executed by the extension — it is parsed as JSON and used to look up elements on
  the page you are already viewing.
- **Applied on top of the configuration already inside the extension.** If these files are
  unreachable, unparseable or empty, the extension keeps working exactly as shipped.
- **No personal data**, no tracking, no analytics. Nothing here is user-specific; every
  install reads the same file.

## Files

| Path | Purpose |
|---|---|
| [`v1/selectors.json`](v1/selectors.json) | where to find product details on each supported store |
| `v1/selectors.empty.json` | a known-good empty configuration, used to roll back |
| `v1/version.json` | mirror of the extension's update manifest |

`revision` increases on every change; the extension ignores a file whose revision is lower
than the one it already has.

## Not the extension source

This repo contains configuration only. It is not the extension's source code and installing
it does nothing.

---

Not affiliated with, endorsed by, or connected to any of the stores referenced in these
files. Selector strings describe publicly visible page structure.
