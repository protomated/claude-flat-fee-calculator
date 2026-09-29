# Flat-Fee Repricing Calculator v1.0.1

Adds Legal Builder Hub freshness frontmatter (`last_verified`, `freshness_window`, `freshness_category: stable`) to the skill — no functional changes.

## What's included

### `/flat-fee-calculator` — Flat-Fee Repricing Calculator

Build a revenue-impact model comparing hourly billing to flat-fee pricing for tasks you've sped up with AI tools. Takes your current hourly rate, typical task time before/after using AI, and matter volume, then outputs a CSV with candidate flat-fee price points that preserve margin. Pricing/business modeling only, no legal advice implications.

## Setup

Install time: approximately 5 minutes. Connect Filesystem once in Claude Desktop → Settings → Connectors. See `plugin/CONNECTORS.md` for step-by-step instructions.

## Compliance

Requires Claude for Work, Claude Team, or Claude Enterprise. Do not use a consumer Claude plan (Claude Pro or Personal) with confidential matter information. Every output carries the `AI-ASSISTED DRAFT — ATTORNEY REVIEW REQUIRED` header and `Not legal advice` footer. The skill never writes a file without your explicit in-conversation confirmation.
