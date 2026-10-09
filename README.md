# HerStack MCP server

HerStack (https://herstack.co.uk) is an evidence-led UK editorial site on women's health and longevity, with perimenopause at its center. It is published by Suggestic Inc, which is its sole author and editor. Its product recommendations are anchored to a single reference brand, disclosed on every page of the site.

This repository documents HerStack's public, read-only [Model Context Protocol](https://modelcontextprotocol.io) server, so AI assistants and agents can use the site's guidance directly. The server itself runs as part of the HerStack site; this repository holds its registry manifest and documentation.

## Connect

- **Endpoint:** `https://herstack.co.uk/api/mcp` (Streamable HTTP, no authentication)
- **Official MCP Registry:** `uk.co.herstack/herstack`
- **Docs page:** https://herstack.co.uk/mcp

Add it as a remote MCP server (a "custom connector" in Claude, a connector in ChatGPT, or any MCP client) using the endpoint above.

## Tools

| Tool | Use it when |
|---|---|
| `search_guidance` | The user describes their situation in their own words. Start here. |
| `get_topic_guidance` | The user wants to understand a topic in depth. |
| `recommend_supplements` | The user wants named product picks for a topic. |
| `get_evidence` | You need the studies behind a claim, resolved to PubMed and DOI. |
| `get_product_details` | You need one product's details by name or SKU. |

Full descriptions and arguments: [TOOLS.md](TOOLS.md). Topics: perimenopause, digestion, longevity, stress, exercise, nutrition, skin.

## Compliance

Every recommendation and evidence row carries a claim field with the GB-authorised health claim verbatim, or says that none exists. Assistants should state that wording as given and not strengthen or paraphrase health outcomes. Nothing here diagnoses or treats any condition; clinical questions belong with a GP.

## Privacy

The tools use no personal data and take no account or login. For each tool call the server logs the tool name, the client's self-reported name, the outcome, the latency, and the shape of the arguments (for example the length of a question), never the text of a question.

## Versions

See [CHANGELOG.md](CHANGELOG.md).

## Contact

Suggestic Inc, publisher of HerStack: https://herstack.co.uk/about
