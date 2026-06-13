## Consolidated

## Recent
[chat] section.blocks iteration does NOT reliably find static theme blocks in Horizon's content_for 'block' architecture — if the content_for call is inside a conditional that depends on the block being found, it's a deadlock (block never renders → never in section.blocks → flag never set). Fix: read any block-config you need for injection logic from section.settings instead
[chat] Banner position settings belong in the SECTION schema (not block schema) whenever the section needs to read them before deciding where to inject the block. Block schema is for content (image, heading, text); section schema is for layout/position decisions
[chat] Setting in_grid_banner_position or midpage_banner_position to 0 in section settings hides that banner — use as a toggle
