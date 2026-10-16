# Synoptic

Follow live feeds from Twitter/X, Telegram and GitHub to press releases, SEC filings, IPOs, court dockets and economic releases, and publish your own feeds with [Synoptic](https://www.synoptic.com/), from Claude.

Synoptic is a marketplace of feeds from Synoptic and independent providers. With this plugin, Claude can find feeds for news, press releases, SEC filings, IPOs, court updates, economic releases and government announcements, read their updates, set up supported source monitors, organize your Synoptic workspace, publish your own feeds, and explain how an application can receive a feed over Synoptic's REST and WebSocket APIs. Ongoing collection runs in Synoptic; coverage, update speed, filters and API access depend on the feed and your account.

## Skills

- **read-streams**: find source-specific feeds and read accessible updates.
- **configure-source-monitoring**: set up supported tracking and change target selections without dropping existing ones.
- **connect-feed-to-app**: prepare REST, WebSocket and structured publishing integrations.
- **publish-content**: create your own feeds and publish content you approve.
- **manage-workspace**: organize dashboards, collections, and keyword, regex or AI filters.
- **manage-account**: read or edit your profile, author follows, notification preferences and notifications.
- **request-stream-or-feature**: send a stream or feature request to the Synoptic team.

The skills change only what you ask for and keep settings you didn't ask to change.

## Get started

1. Add the plugin, then connect the Synoptic connector: in Claude, open the plugin's **Connectors** tab and select **Connect**; in Claude Code, run `/mcp`, select `synoptic` and authenticate.
2. Sign in to Synoptic and choose permissions. **Research** (read streams, posts, authors and follows) is selected by default; **Read only**, **Organize workspace**, **Publish content** and **Full** are also available, or set each category yourself.
3. Ask Claude, for example: "Find a feed for new SEC filings and show me the latest updates."

In Claude Code you can also install the plugin with `/plugin install synoptic --marketplace synoptic-com/claude-plugins`.

Public stream discovery (`search`, `streams_all`, `get_stream`, `fetch`) doesn't need a Synoptic account; every other tool does. The [MCP documentation](https://docs.synoptic.com/s/mcp/mcp) lists every tool and the permission it needs.

## Data and privacy

The plugin contains skills and one remote connector. It runs nothing on your computer: no hooks, scripts or local servers.

Tool calls go to Synoptic's MCP server at `https://mcp.api.synoptic.com/mcp`, operated by Synoptic. Depending on what you ask, Claude sends:

- search terms and stream, post and user IDs, to find feeds and read posts;
- stream names, descriptions and post text you ask Claude to publish;
- changes to your follows, target selections, workspace, profile and notification settings;
- stream and feature requests, each of which opens a support ticket with the Synoptic team.

Synoptic receives these tool inputs, not the rest of your conversation. Permissions never go beyond what your Synoptic account can already do. Posts and notifications can contain text written by other people, so review changes Claude proposes after reading them. See the [privacy policy](https://synoptic.com/policy) and [terms](https://synoptic.com/terms).

The connector doesn't offer administrator actions, billing or checkout, API-key or exchange-credential management, or live trading.

## Troubleshooting

- **Tools are missing or Claude asks you to sign in**: connect the Synoptic connector as in Get started.
- **A tool says a permission is missing**: reconnect and grant that category. Added permissions apply after you reconnect; removed ones apply right away.
- **A rate-limit error (HTTP 429)**: following a stream or author, posting, profile and username changes, and requests each allow 120 calls per hour; other changes share a limit of 30 calls per minute. Wait and retry.
- **Disconnect**: in Synoptic, open **Settings → Connected Accounts** and select **Disconnect** next to **AI apps (MCP)**.

For help, email [info@synoptic.com](mailto:info@synoptic.com).

## License

[Apache License 2.0](LICENSE). The license doesn't grant rights to the Synoptic name or logo.
