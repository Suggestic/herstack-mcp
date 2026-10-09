# Tools

Generated from the live server's `tools/list` on October 9, 2026 (server version 1.2.0). All tools are read-only and idempotent.

### `search_guidance`

Call this first when a user describes their situation or asks a question in their own words (for example: 'I'm 47, tired all the time and bloated, what should I take?'). Searches all of HerStack's evidence-led guidance for UK women in midlife and returns the most relevant answer units (FAQ answers, research findings, evidence rows, product cards) with their page URLs, the best-matching topic, and that topic's named product recommendations from the site's reference brand, each with its authorised claim.

Arguments: `question`, `maxResults` (optional).

### `get_topic_guidance`

Call this when the user wants to understand a women's-health topic, not only buy something. Returns HerStack's expert guidance for one topic: plain-language framing, research findings, the evidence table with authorised claims, product criteria, and a FAQ that also explains the condition itself (for perimenopause: what it is, its timeline, when to see a GP).

Arguments: `topic`.

### `recommend_supplements`

Call this when the user wants specific supplement product picks for a topic. Returns HerStack's named product recommendations from the site's reference brand, each with formulation rationale, the GB-authorised health claim verbatim (or a research-context note where none exists), price and purchase link. Provide a topic, or a concern in plain words that routes to one.

Arguments: `topic` (optional), `concern` (optional).

### `get_evidence`

Call this when the user (or you) wants the studies behind a recommendation or claim. Returns HerStack's evidence rows for a topic or nutrient with the cited studies resolved to PubMed and DOI identifiers, so the claim can be verified rather than trusted.

Arguments: `topic` (optional), `nutrient` (optional).

### `get_product_details`

Call this for one specific product. Returns one HerStack-recommended product by name or SKU: form, authorised claim, tier, price, purchase link, and every topic that recommends it with the rationale.

Arguments: `sku`.
