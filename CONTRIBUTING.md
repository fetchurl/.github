# Contributing to fetchurl

This is the **organization default** contribution guide for [github.com/fetchurl](https://github.com/fetchurl). It applies to public repositories under the org that do not ship their own `CONTRIBUTING` file.

The project is split across repositories on purpose. File issues and pull requests against the **right** repo so maintainers and CI stay focused.

## Where to contribute

| Kind of change | Repository |
|----------------|------------|
| Protocol behavior, wire format, headers, env vars, versioning | [fetchurl/spec](https://github.com/fetchurl/spec) (`SPEC.md`) |
| Reference server & CLI (Go), container image | [fetchurl/fetchurl](https://github.com/fetchurl/fetchurl) |
| JavaScript / TypeScript client | [fetchurl/sdk-js](https://github.com/fetchurl/sdk-js) |
| Python client | [fetchurl/sdk-python](https://github.com/fetchurl/sdk-python) |
| Rust client | [fetchurl/sdk-rust](https://github.com/fetchurl/sdk-rust) |
| Java client | [fetchurl/sdk-java](https://github.com/fetchurl/sdk-java) |
| Project docs site | [fetchurl/fetchurl.github.io](https://github.com/fetchurl/fetchurl.github.io) |
| Org profile / default community health files | [fetchurl/.github](https://github.com/fetchurl/.github) |

Normative protocol lives only in **spec**. Servers and SDKs implement it; they are not the source of truth for protocol semantics.

## Issues

- **Protocol proposals and clarifications** → [fetchurl/spec](https://github.com/fetchurl/spec)
- **Bugs and feature requests for an implementation** → that server or SDK repo
- **Security-sensitive findings** → do **not** open a public issue; follow the org [security policy](./SECURITY.md) (private vulnerability reporting preferred)

Include enough context to reproduce: version or commit, environment, expected vs actual behavior, and minimal steps or logs.

## Pull requests

1. Open the PR against the repository that owns the change (see the table above).
2. Keep protocol changes in **spec** (with `CHANGELOG.md` updates when behavior changes). Follow that repo’s versioning notes before touching wire/header/env semantics.
3. Keep implementation PRs focused: one concern, tests for the behavior you change, and no unrelated refactors.
4. Prefer small, reviewable diffs. Link related issues.

There is no CLA. Contributions are under the repository’s license (typically MIT — see each repo’s `LICENSE`).

## Development tips

Each implementation repo documents its own toolchain (often `mise.toml`, language-native tests, and a `make_release` helper). From a clone of the repo you are changing:

- Read that repository’s `README.md` first.
- Run the existing test command(s) before opening a PR (`go test`, language package tests, etc.).
- For protocol work, start from [SPEC.md](https://github.com/fetchurl/spec/blob/main/SPEC.md) and the spec changelog.

Clients configure the cache server with `FETCHURL_SERVER` (base URL ready to append `/:algo/:hash`); see the [spec](https://github.com/fetchurl/spec/blob/main/SPEC.md).

## Questions

If you are unsure which repository owns something, open a short issue on [fetchurl/spec](https://github.com/fetchurl/spec) or ask in the discussion on the closest related repo. Prefer the wrong repo with a clear description over staying silent — maintainers can transfer or redirect.
