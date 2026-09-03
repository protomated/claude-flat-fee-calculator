# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

**Flat-Fee Repricing Calculator** — a Claude Desktop plugin for solo and small-firm attorneys. One skill (`/flat-fee-calculator`): Build a revenue-impact model comparing hourly billing to flat-fee pricing for tasks you've sped up with AI tools. Takes your current hourly rate, typical task time before/after using AI, and matter volume, then outputs a CSV with candidate flat-fee price points that preserve margin. Pricing/business modeling only, no legal advice implications. There is no runtime code, no MCP server beyond the declared Filesystem connector, and no backend. The product is entirely content: a markdown skill file and JSON manifests.

This repo is the source of truth for this skill's content. It also ships via the [Protomated plugin marketplace](https://github.com/protomated/protomated-plugins-official) — re-sync that repo's copy manually when this one changes.

## Repo layout

```
plugin/           The installable plugin (packaged into .zip)
  .claude-plugin/plugin.json   Manifest validated by scripts/validate-plugin.mjs
  .mcp.json                    Declares filesystem connector requirement
  manifest.json                Plugin display metadata
  prompts/system-prompt.md     Master system prompt — compliance guardrails live here
  skills/flat-fee-calculator/SKILL.md  The single skill; YAML frontmatter + markdown body
scripts/
  validate-plugin.mjs          Validates plugin/ structure before packing
```

## Commands

```bash
npm run validate   # validate plugin/ structure
npm run build       # validate → pack → checksum
npm run release      # build + gh release create
```

## Compliance constraints — non-negotiable

1. **Confirmation gating**: Claude must show the attorney exactly what it will do and get explicit in-conversation confirmation before writing any file.
2. **Required output wrapper**: every skill output must begin with `AI-ASSISTED DRAFT — ATTORNEY REVIEW REQUIRED` and end with the `Not legal advice` footer.
3. **Plan-tier warning**: consumer-tier Claude (claude.ai Personal / Pro) must not be used with client-privileged content.

Do not weaken these constraints.
