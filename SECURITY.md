# Security policy

This policy is the **organization default** for [github.com/fetchurl](https://github.com/fetchurl). It applies to every public repository under the org that does not ship its own `SECURITY.md`.

## Scope

In scope: the protocol, reference server/CLI, client SDKs, docs site, and related infrastructure owned by the **fetchurl** organization — for example:

- [fetchurl/spec](https://github.com/fetchurl/spec)
- [fetchurl/fetchurl](https://github.com/fetchurl/fetchurl)
- [fetchurl/sdk-js](https://github.com/fetchurl/sdk-js), [sdk-python](https://github.com/fetchurl/sdk-python), [sdk-rust](https://github.com/fetchurl/sdk-rust), [sdk-java](https://github.com/fetchurl/sdk-java)
- [fetchurl/fetchurl.github.io](https://github.com/fetchurl/fetchurl.github.io)

Out of scope: third-party deployments of the server or forks you do not control; report those to the deployer.

## Supported versions

Security fixes are applied to **current** published lines, not historical tags by default:

| Surface | What we treat as supported |
|---------|----------------------------|
| [spec](https://github.com/fetchurl/spec) | The protocol as described on the default branch (`SPEC.md`); versioning notes live in that repo’s changelog |
| [fetchurl](https://github.com/fetchurl/fetchurl) (server/CLI) | Latest release tag and the default branch; container tags matching those releases on `ghcr.io/fetchurl/fetchurl` |
| Client SDKs (`sdk-js`, `sdk-python`, `sdk-rust`, `sdk-java`) | Latest release of each package on the default publish channel, plus the default branch |
| [docs site](https://github.com/fetchurl/fetchurl.github.io) | Content published at [fetchurl.github.io](https://fetchurl.github.io) |

Older releases may not receive backports unless a fix is critical and practical. Say which version/commit you used when reporting.

## Reporting a vulnerability

**Do not** open a public issue or pull request for security-sensitive findings.

Prefer **GitHub private vulnerability reporting** on the **repository that is most affected** (that repo’s Security tab → Report a vulnerability), when that feature is enabled. Private reports are per repository — do not file an SDK or protocol issue against the server repo (or the reverse) just because one form is easier to find.

If private reporting is unavailable, or you need a direct contact:

- Email: [lucas@lew.tec.br](mailto:lucas@lew.tec.br)
- Subject line: include `[fetchurl security]` and the affected repo name

Include as much of the following as you can:

- Affected repository and version/commit (or container tag)
- Description of the issue and impact
- Steps to reproduce or a proof of concept
- Whether you plan a public write-up, and any preferred timeline

## What to expect

We will acknowledge reports when we can and keep the discussion private until a fix is available or we agree the issue is not security-sensitive. There is no fixed SLA; severity and complexity affect timing.

Please give us a reasonable window to ship a fix before public disclosure.

## Safe harbor

We welcome good-faith research. Avoid testing against production systems you do not own, and do not access or modify data that is not yours.

## Non-security bugs

Protocol questions and ordinary bugs belong in the relevant repository’s public issue tracker (or the [spec](https://github.com/fetchurl/spec) for protocol behavior).
