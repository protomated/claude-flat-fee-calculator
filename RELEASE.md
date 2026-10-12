# Flat-Fee Repricing Calculator

Fixed the skill calling other installed plugins' tools unprompted — it was observed reaching into Legal Billing Tracker's time-entry lookup during a routine run, because connected tools are account-wide, not scoped to the invoked skill, and the grounding-data instructions were ambiguous enough to read as license to use any available source. Added an explicit scope boundary: Filesystem only, and only if already connected — nothing else.

## What's included

### `/flat-fee-calculator` — Flat-Fee Repricing Calculator

Build a revenue-impact model comparing hourly billing to flat-fee pricing for tasks you've sped up with AI tools. Takes your current hourly rate, typical task time before/after using AI, and matter volume, then outputs a CSV with candidate flat-fee price points that preserve margin. Pricing/business modeling only, no legal advice implications.

## Setup

Install time: approximately 5 minutes. Connect Filesystem once in Claude Desktop → Settings → Connectors. See `plugin/CONNECTORS.md` for step-by-step instructions.

## Compliance

Requires Claude for Work, Claude Team, or Claude Enterprise. Do not use a consumer Claude plan (Claude Pro or Personal) with confidential matter information. Every output carries the `AI-ASSISTED DRAFT — ATTORNEY REVIEW REQUIRED` header and `Not legal advice` footer. The skill never writes a file without your explicit in-conversation confirmation.
