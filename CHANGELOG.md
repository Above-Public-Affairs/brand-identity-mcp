# Changelog

## [2026-06-08]

### Fixed
- Semantic colors (success / warning / error / info) in the `design-language.md` now match the PDF — both are pulled from the same emotion-based palette, instead of the markdown using a fixed default set that disagreed with the document for every brand
- Brand documents now safely handle client names and other inputs containing `<`, `>`, `&`, or quotes — these are HTML-escaped so unusual names (e.g. "Smith & Sons") can't break the generated markup

## [2026-04-03]

### Fixed
- Fixed 500 error on MCP connection by switching to per-session transport pattern with Express (matches working Advocacy Content MCP server)

### Changed
- Converted from Claude skill (SKILL.md) to MCP server with TypeScript
- Now uses `generate_brand_identity` tool via MCP protocol instead of skill invocation

### Added
- MCP server with `generate_brand_identity` tool and `brand-identity-guide` prompt
- 13 section generators: strategy, voice/tone, messaging, colors, typography, imagery, applications, do's/don'ts, foundations, components, patterns, tokens, implementation guide
- Emotion-based color palette system (trust, excitement, calm, urgency, empowerment, hope)
- Emotion-based font pairing system (6 curated Google Font pairings)
- WCAG contrast ratio calculations and accessibility ratings on all color swatches
- 30+ UI component specs with states, accessibility, and code-ready dimensions
- Design tokens as JSON with CSS custom property generation
- Political-specific content: yard signs, palm cards, bumper stickers, fundraising appeals, voter outreach
- Full HTML-to-PDF pipeline via Chrome headless
- design-language.md companion file for developer quick-reference
- GitHub repo: thecantercompany/brand-identity-mcp
