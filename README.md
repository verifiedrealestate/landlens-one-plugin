# LandLens One for Claude

Ask Claude about any land in Tamil Nadu. This plugin connects Claude Code and Cowork to the LandLens One MCP server, which puts the state's land, registration, planning, court and legal registers behind one set of tools. Claude picks the right check and states the price before it spends a credit.

The plugin holds no code of its own. It points Claude at `https://verified.realestate/mcp`, the same server Claude, ChatGPT and other apps connect to.

## Install

```
/plugin marketplace add verifiedrealestate/landlens-one-plugin
/plugin install landlens-one@landlens-one
```

Then run `/mcp`, choose `plugin:landlens-one:landlens` and sign in with the phone number on your LandLens account. A one-time code arrives on WhatsApp, and a new number gets an account at its first sign-in.

## What you can ask

- "What is the guideline value at 13.0281, 80.2453?"
- "Is survey 163 in Karappakam inside a coastal or flood zone?"
- "Show me the land record for survey 3884/279 in Mylapore, Chennai."
- "Pull the registered transactions for this plot from the encumbrance certificate."
- "How many LandLens credits do I have left?"

It covers land records (patta, chitta, TSLR) and the mapped parcel boundary (FMB), guideline values, encumbrance certificates and registered deeds, zoning, coastal regulation, flood and other restriction layers, planning approvals and RERA projects, stamp duty and registration fees, and court record searches.

## Pricing

About half of the 100+ tools are free. The rest spend credits from your LandLens wallet, charged only when a register answers. An action that needs an explicit yes, such as an encumbrance pull or a certified copy, returns a quote first and runs only after you approve it. Each connected app has a daily credit ceiling. Credits are bought on the LandLens dashboard.

## Without the plugin

Any client that takes a remote MCP server can use the same URL:

```
claude mcp add --transport http landlens https://verified.realestate/mcp
```

Scripts can use the plain HTTP API with an API key from the LandLens dashboard. Both are described at https://verified.realestate/landlens/mcp.

## Links

- Documentation: https://verified.realestate/landlens/mcp
- Privacy policy: https://verified.realestate/privacy-policy
- Terms: https://verified.realestate/terms
- Support: hello@verified.realestate

## Licence

MIT. See [LICENSE](LICENSE).
