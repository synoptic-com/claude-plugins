# Synoptic plugins

Claude plugins for [Synoptic](https://www.synoptic.com/) news feeds and source monitoring.

| Plugin | Description |
| --- | --- |
| [synoptic](plugins/synoptic) | Follow live feeds from Twitter/X, Telegram and GitHub to press releases, SEC filings, IPOs, court dockets and economic releases, and publish your own feeds with Synoptic. |

## Install

In Claude Code:

```bash
claude plugin marketplace add synoptic-com/claude-plugins
claude plugin install synoptic@synoptic
```

Then run `/mcp`, select `synoptic` and sign in. See the [plugin README](plugins/synoptic/README.md) for permissions, data handling and troubleshooting.

## License

[Apache License 2.0](LICENSE). The license doesn't grant rights to the Synoptic name or logo.
