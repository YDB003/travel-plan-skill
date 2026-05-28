# Travel Plan Skill V2

Codex skill for China domestic travel planning.

## What It Does

- Plans domestic trips in China, including Hong Kong, Macau, and Taiwan.
- Supports quick and deep planning modes.
- Uses staged decisions: basic info, destination, points of interest, lodging, transport, itinerary, and optional visual output.
- Marks dynamic data such as hotel prices, availability, tickets, and reservations with confidence levels.
- Supports visual travel guide output as local HTML, PNG, or PDF.

## Structure

```text
.
├── SKILL.md
└── references
    ├── output_templates.md
    ├── source_strategy.md
    └── visual_output.md
```

## Notes

- Xiaohongshu is preferred for point-of-interest discovery, but the default output links to search result pages instead of scraping individual posts.
- Hotel recommendations use one stable primary source link plus a recommendation reason.
- For visual output, AI-generated images must be clearly labeled and must not be presented as real photos or real navigation maps.
