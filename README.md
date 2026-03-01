# Amazon Returns & Orders — Claude Cowork Skill

A Claude Cowork skill plugin that makes Amazon returns and order troubleshooting fast and hands-off. Tell Claude what you need, it handles the rest.

## What it does

- **Returns with QR codes** — navigates Amazon, clicks through every screen, and gets you a no-box, no-label QR code for drop-off at Whole Foods, UPS, Kohl's, Staples, or Amazon Fresh
- **Order troubleshooting** — handles missing packages, stolen packages, wrong items, items missing from packages, tracking issues, wrong charges, cancellations, and replacements
- **Minimal input** — tells you upfront exactly what info it needs so you give it once and walk away
- **Never gets stuck** — uses smart defaults for every intermediate Amazon screen so the flow runs end-to-end without blocking on confirmations

## Install

Add this plugin directory to Claude Cowork:

```
claude plugins add /path/to/amazon-returns-plugin
```

Or clone this repo and point Claude Cowork to it.

## Usage

Just talk naturally. The skill auto-activates when you mention Amazon returns or order issues.

**Returns:**
```
"Return my AirPods, drop off at Whole Foods"
"I want to return the keyboard I bought last week, UPS"
```

**Order issues:**
```
"My Amazon package says delivered but I never got it"
"Amazon sent me the wrong item"
"My package was stolen"
"Cancel my most recent Amazon order"
```

Claude navigates Amazon, finds the order, clicks through the return/issue flow, and stops only at the final submit button for your approval.

## How it works

1. You describe the problem
2. Claude asks for any missing info (drop-off location is required for returns)
3. Claude navigates to your Amazon orders, finds the item, and runs through the entire flow
4. Claude stops at the final confirmation with a one-liner summary
5. You say yes, done

## Requirements

- Claude Cowork with browser access
- Signed into Amazon in the browser

## Plugin structure

```
.claude-plugin/
  plugin.json          # Plugin manifest
skills/
  amazon-returns/
    SKILL.md           # The skill — all logic in one file
```

## License

MIT
