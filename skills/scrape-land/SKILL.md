---
name: scrape-land
description: Use when the user needs content or data from the web that a plain fetch cannot get, structured fields from pages, web search results, or lists of local businesses. Explains which scrape.land tool to call and how to keep it cheap.
---

# Using scrape.land

scrape.land's tools read the web through a rotating network that gets past most blocks. Every call spends the user's request units; blocked and failed calls are free.

## Pick the tool

- **web_search**: you do not have URLs yet. Returns up to 10 results; read the promising ones with fetch_page.
- **fetch_page**: you have a URL and want its content. Default `format: "markdown"` is the cheapest to read.
- **extract_data**: you want specific fields as JSON. Pass `fields` (CSS selectors) when you can see the markup; pass `prompt` for plain-English extraction (Scale plan and above).
- **find_local_businesses**: lists of businesses by category and place, with website, phone and email filters.

## Keep it cheap and reliable

- Only set `render: true` when the page needs JavaScript (an empty or skeleton result without it). A render costs more units.
- Fetch one page and check it before fetching many.
- If a result says `"blocked": true`, retry once; it was not billed.
- A response over 200 KB is truncated; ask for `markdown` or extract fields instead of whole HTML.
