# hello-world

A minimal example plugin for Claude Code. It exists to show the full plugin
lifecycle: write the files, validate them, install the plugin, and see each
component run. It contains one skill, one agent, and one hook, and none of them
touch your files or run anything beyond a greeting.

## Components

| Component | Name | What it does |
|-----------|------|--------------|
| Skill | `hello` | Greets the user and confirms the plugin is loaded |
| Agent | `greeter` | A subagent that greets and identifies itself |
| Hook | `SessionStart` | Prints `hello-world plugin loaded` when a session starts |

## Install

From a marketplace that lists this plugin:

```
/plugin install hello-world --marketplace lointfujinet/demo_marketplace
```

To try it locally without a marketplace:

```
claude --plugin-dir D:\ASTEC_Plugin\hello-world
```

## Usage

- Run `/hello-world:hello`, or say "hello plugin", to trigger the skill.
- Ask Claude to "run the greeter agent" to trigger the agent.
- Start a new session to see the hook message.

## Requirements

No setup is needed. The hook uses `echo`, which works on Windows, macOS, and Linux.

## License

MIT
