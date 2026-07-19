# Support

This is the **organization default** support guide for [github.com/fetchurl](https://github.com/fetchurl). It applies to public repositories under the org that do not ship their own `SUPPORT` file.

fetchurl is a multi-repo project. Pick the channel that matches the kind of help you need so maintainers can respond in the right place.

## Documentation

- Live docs site: [fetchurl.github.io](https://fetchurl.github.io)
- Normative protocol: [fetchurl/spec](https://github.com/fetchurl/spec) (`SPEC.md`)
- Org overview: [github.com/fetchurl](https://github.com/fetchurl)

## Usage and protocol questions

| Topic | Where |
|-------|--------|
| Protocol behavior, wire format, headers, env vars (`FETCHURL_SERVER`, etc.) | Issues on [fetchurl/spec](https://github.com/fetchurl/spec) |
| Running the reference server or CLI | Issues on [fetchurl/fetchurl](https://github.com/fetchurl/fetchurl) |
| Client / SDK integration | The relevant SDK: [sdk-js](https://github.com/fetchurl/sdk-js), [sdk-python](https://github.com/fetchurl/sdk-python), [sdk-rust](https://github.com/fetchurl/sdk-rust), [sdk-java](https://github.com/fetchurl/sdk-java) |
| Docs site content | [fetchurl/fetchurl.github.io](https://github.com/fetchurl/fetchurl.github.io) |

Include version or commit, environment, expected vs actual behavior, and minimal steps or logs when filing an issue.

## Security-sensitive reports

**Do not** open a public issue for vulnerabilities. Prefer private vulnerability reporting on the affected repository, or follow the org [security policy](./SECURITY.md).

## Contributing code or docs

How to choose a repository, open issues, and submit pull requests is covered in [CONTRIBUTING.md](./CONTRIBUTING.md).

## Unsure where to start?

Open a short issue on [fetchurl/spec](https://github.com/fetchurl/spec) with what you are trying to do. Maintainers can redirect or transfer if another repo owns it.
