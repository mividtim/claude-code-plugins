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
| [deps](https://github.com/mividtim/claude-code-plugin-deps) | Dependency resolution between plugins |

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
