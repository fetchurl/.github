# fetchurl

Content-addressable URL caching for CI and package managers.

Clients ask a cache server for `algo/hash` and pass source URLs; the server fetches, verifies, and stores. Servers are **untrusted** — clients always verify hashes. Designed for repeated dependency downloads without MITM proxies or fragile workflow-cache keys.

Normative behavior lives in the **[protocol spec](https://github.com/fetchurl/spec)**; everything else implements it.

## Repositories

| Repository | What it is |
|------------|------------|
| **[spec](https://github.com/fetchurl/spec)** | Normative protocol (`SPEC.md`), versioned independently |
| **[fetchurl](https://github.com/fetchurl/fetchurl)** | Reference **server & CLI** (Go), container image |
| **[sdk-js](https://github.com/fetchurl/sdk-js)** | JavaScript / TypeScript client (`fetchurl-sdk`) |
| **[sdk-python](https://github.com/fetchurl/sdk-python)** | Python client (`fetchurl-sdk`) |
| **[sdk-rust](https://github.com/fetchurl/sdk-rust)** | Rust client (`fetchurl-sdk`) |

## Quick orientation

```text
                    ┌─────────────┐
                    │    spec     │  protocol only
                    └──────┬──────┘
           implements / speaks protocol
     ┌─────────────────┼─────────────────┐
     ▼                 ▼                 ▼
┌──────────┐    ┌────────────┐    ┌────────────┐
│ fetchurl │    │  sdk-js    │    │ sdk-python │  …
│ (server) │    │  (npm)     │    │  (PyPI)    │
└──────────┘    └────────────┘    └────────────┘
```

- **Run a cache:** [fetchurl/fetchurl](https://github.com/fetchurl/fetchurl) — image `ghcr.io/fetchurl/fetchurl`
- **Wire a client:** set `FETCHURL_SERVER` to the server base URL (ready to append `/:algo/:hash`); see [spec](https://github.com/fetchurl/spec/blob/main/SPEC.md)
- **Propose protocol changes:** issues/PRs on [spec](https://github.com/fetchurl/spec)
- **Implementation bugs:** the relevant server or SDK repo

## Links

- Protocol: [fetchurl/spec](https://github.com/fetchurl/spec)
- Org: [github.com/fetchurl](https://github.com/fetchurl)
