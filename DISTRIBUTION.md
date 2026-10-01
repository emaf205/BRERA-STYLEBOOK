# StyleBook distribution map

The site is the conversion hub. Distribution should send qualified visitors to either the long-form guide or the product page, then to Gumroad.

## Core flow

Search / GitHub / social → Netlify site → product proof or guide → Gumroad

## Channels worth using

### GitHub
Use the repository README as a commercial discovery page. Keep the paid application out of the public repo.

### Google and Bing
Submit the live `sitemap.xml` through Google Search Console and Bing Webmaster Tools. The guide is the main organic content asset.

### LinkedIn
Publish a short native post around one workflow problem, then link to the relevant guide section or live demo. Do not repost the full sales copy.

### Pinterest
Use the real StyleBook screenshots as pins linked to the guide or live product page. This channel matches the product's visual-reference use case better than generic text-first promotion.

### X
Use one concise problem/solution observation plus a screenshot or short demo clip and a tracked link.

### Newsletter
Send release notes or a practical reference-management tip. Link to the guide first when the audience is not already product-aware.

### Reddit / communities
Manual and context-specific only. Share the workflow or guide when it directly answers a discussion. Do not automate promotional posting.

## Deploy-trigger automation

Netlify deploy notifications can trigger an HTTP webhook. Connect that webhook to n8n or Zapier when you want a successful production deploy to create distribution tasks or drafts.

Recommended automation:

1. Netlify production deploy succeeds.
2. Webhook sends page URL + release label to n8n/Zapier.
3. Workflow creates channel-specific drafts/tasks.
4. Human reviews them before public posting.

Avoid auto-posting identical text to every channel.

## Tracking

Use different `utm_source` values per channel and keep `utm_campaign=stylebook-v120` for this release. The site preserves incoming UTM parameters when it generates Gumroad links.
