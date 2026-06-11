# CLAUDE.md

Guidance for AI coding agents working in this repository.

## What this repo is

The **public metadata repository** for the AdCrunch MCP server, published to the
official [MCP Registry](https://registry.modelcontextprotocol.io) as
`dev.adcrunch/mcp`.

This repo holds **metadata only** — there is no server code here. The actual MCP
server is a remote Cloudflare Worker served at `https://mcp.adcrunch.dev/mcp`
(its source lives in the `adcrunch` monorepo).

| File                 | Purpose                                                        |
| -------------------- | ------------------------------------------------------------- |
| `server.json`        | MCP Registry manifest (`dev.adcrunch/mcp`, remote endpoint)   |
| `mcp.json`           | Client config for Open Plugins / cursor.directory auto-detect |
| `.plugin/plugin.json`| Open Plugins manifest (metadata + logo)                       |
| `README.md`          | Public-facing install/usage docs                              |

## Git conventions

- **Always commit with author `AdCrunch <support@adcrunch.dev>`.** Pass it
  explicitly: `git commit --author="AdCrunch <support@adcrunch.dev>" -m "..."`.
- Use [Conventional Commits](https://www.conventionalcommits.org/) for messages.

## Publishing

Publishing to the MCP Registry uses **DNS authentication** on the
`dev.adcrunch` namespace (apex TXT record on `adcrunch.dev`).

Releases are automated by `.github/workflows/publish-mcp.yml`: pushing a `v*`
tag derives the version from the tag, writes it into `server.json`, and
publishes. To cut a release:

```bash
git tag v1.0.2 && git push origin v1.0.2
```

Requires the `MCP_PRIVATE_KEY` repo secret (the Ed25519 private key matching the
apex TXT record).

## Versioning

The git tag is the single source of truth for the published version — the
workflow overwrites `server.json`'s `version` at publish time. Each version is
immutable in the registry; re-publishing an existing version is rejected, so
every release needs a new tag.
