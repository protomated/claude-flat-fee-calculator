# Flat-Fee Repricing Calculator — Claude Desktop Plugin

A Claude Desktop plugin for solo and small-firm attorneys. One skill (`/flat-fee-calculator`): Build a revenue-impact model comparing hourly billing to flat-fee pricing for tasks you've sped up with AI tools. Takes your current hourly rate, typical task time before/after using AI, and matter volume, then outputs a CSV with candidate flat-fee price points that preserve margin. Pricing/business modeling only, no legal advice implications.

Distributed free by [Protomated](https://protomated.com).

---

## Repo layout

```text
plugin/           Installable plugin (packaged into .zip)
  .claude-plugin/plugin.json   Identity manifest
  .mcp.json                    Declares filesystem connector requirement
  manifest.json                Display metadata
  prompts/system-prompt.md     Master system prompt — compliance guardrails live here
  skills/flat-fee-calculator/
    SKILL.md                   The single skill

scripts/
  validate-plugin.mjs          Validates plugin/ structure before packing

.github/workflows/
  validate.yml     Runs on every push/PR — validates plugin structure
  release.yml      Runs on vX.Y.Z tags — builds, checksums, and publishes a GitHub Release
```

---

## Skill

| Skill | What it does |
|---|---|
| `/flat-fee-calculator` | Build a revenue-impact model comparing hourly billing to flat-fee pricing for tasks you've sped up with AI tools. Takes your current hourly rate, typical task time before/after using AI, and matter volume, then outputs a CSV with candidate flat-fee price points that preserve margin. Pricing/business modeling only, no legal advice implications. |

---

## Development

```bash
npm run validate   # validate plugin/ structure
npm run build      # validate → pack → checksum
npm run release    # build + gh release create (requires gh CLI + repo write access)
```

---

## Part of the Protomated Plugin Marketplace

This plugin also ships via the [Protomated plugin marketplace](https://github.com/protomated/protomated-plugins-official) (git-native install, no zip needed) — install this repo's zip release if you want a pinned version instead.

## License

Apache 2.0. See [LICENSE](LICENSE).
