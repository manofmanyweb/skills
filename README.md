# Man of Many Skills

Agent skills that turn the Man of Many MCP server into a shopping and style adviser. Ask for a gift, a watch, an outfit, a grooming routine or a Black Friday deal, and your AI assistant answers with editor-picked products from Man of Many's published articles: the price as published, why it was picked, and a link to the retailer.

Everything is sourced from the Man of Many MCP server. The skills are written so the assistant never invents products, prices or links, and always finishes with a "Read more on Man of Many" list of the articles it used.

## Install

### Skills CLI

```
npx skills add manofmanyweb/skills
```

### Claude Code plugin marketplace

```
/plugin install manofmany --marketplace manofmanyweb/skills
/plugin install manofmany-skills@manofmany-skills
```

## Connect the Man of Many MCP

The skills need the Man of Many MCP server. In Claude Code:

```
claude mcp add --transport http man-of-many https://mcp.manofmany.com/mcp
```

That is the staging endpoint. The production endpoint will be https://manofmany.com/mcp, and this README will be updated when it is live. If the tools are not connected, each skill tells you and gives you this command.

The server provides these tools: `search_articles`, `get_article`, `latest`, `get_buyers_guide`, `product_picks` and `gift_finder`.

## Skills

| Skill | What it does |
| --- | --- |
| gift-finder | Gift ideas for anyone and any occasion, by recipient, interests and budget |
| watch-advisor | Choose or compare watches, with the verdict from Man of Many's reviews |
| style-me | Outfits and wardrobe picks for an occasion, season and budget |
| grooming-routine | Skincare, shaving, beard, hair and fragrance routines with tested picks |
| black-friday-deals | Worthwhile Black Friday coverage and product picks, without the noise |
| christmas-gifts | Christmas gift ideas by recipient and budget, including stocking fillers |

## Example prompts

- "I need a birthday gift for my sister, she loves coffee, budget $150."
- "What is a good first automatic watch under $1000?"
- "What should I wear to a summer wedding? Budget around $600."
- "Build me a simple skincare routine for dry, sensitive skin."
- "Any Black Friday deals worth buying on headphones?"
- "Christmas gifts for my dad and my partner, $100 each."

## How the answers are shaped

- Picks include the product name and price as published, a short reason, and the retailer link exactly as published.
- Prices change. The skills say so and suggest checking the retailer before buying.
- The assistant only recommends what the tools return. If nothing fits, it says so.
- Every answer ends with a "Read more on Man of Many" list of the cited articles.

## Terms

- Free to use. The skills and the MCP server cost nothing.
- Attribution required. Keep the "via Man of Many" attribution and the article links in answers. Links carry tracking parameters; pass them through unchanged.
- No training. Man of Many content returned by the MCP server must not be used to train or fine-tune AI models.
- Content remains the property of Man of Many. The skill files in this repository are MIT licensed (see LICENSE).

## Contributing

Issues and suggestions are welcome. Each skill lives in `skills/<name>/SKILL.md`, and the folder name must match the `name` in its frontmatter.

## About

Man of Many is an Australian independent publisher covering style, tech, travel, drinks and gear. https://manofmany.com
