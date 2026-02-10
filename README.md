# claude-code-plugins

Marketplace for [Tim Garthwaite's](https://github.com/mividtim) Claude Code plugins.

## Install

Add this marketplace to Claude Code:

```shell
/plugin marketplace add mividtim/claude-code-plugins
```

Then browse available plugins:

```shell
/plugin
```

Go to the **Discover** tab to see and install plugins.

## Available Plugins

| Plugin | Description |
|--------|-------------|
| [el](https://github.com/mividtim/claude-code-event-listeners) | Event-driven background task listeners — webhooks, CI, file changes, logs |
| [deps](https://github.com/mividtim/claude-code-plugin-deps) | Dependency resolution between plugins with semver constraints |
| [agency](https://github.com/mividtim/claude-code-agency) | Persistent agent patterns — boot sequence, memory architecture, identity management |
| [el-slack](https://github.com/mividtim/claude-code-el-slack) | Slack event source for el — message listening with bot filtering and dedup |
| [el-sendgrid](https://github.com/mividtim/claude-code-el-sendgrid) | SendGrid inbound email event source for el |
| [el-coderabbit](https://github.com/mividtim/claude-code-el-coderabbit) | CodeRabbit event source for el — PR reviews, comments, thread replies |
| [el-http-poll](https://github.com/mividtim/claude-code-el-http-poll) | HTTP polling event source for el — health checks, deploy waits |
| [recoup](https://github.com/mividtim/claude-code-recoup) | Sell idle capacity on agent marketplaces via x402 micropayments |

## For Projects

To declare these plugins as dependencies for your project, add to `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "mividtim": {
      "source": {
        "source": "github",
        "repo": "mividtim/claude-code-plugins"
      }
    }
  },
  "enabledPlugins": {
    "el@mividtim": true
  }
}
```

Team members will be prompted to install the marketplace and plugins when they open the project.
