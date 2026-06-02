# autoc-plugin-cc

Claude Code plugin for [AutoC](https://www.autoc-tool.com/) — BSW configuration subagent for EB tresos and DaVinci Configurator.

Subagent: **`autoc:bsw-config`**

## Install

```bash
/plugin marketplace add autoc-tool/autoc-plugin-cc
/plugin install autoc@autoc-tool
/reload-plugins
```

Or session-only:

```bash
claude --plugin-dir ./plugins/autoc
```

## Prerequisites

- [AutoC CLI](https://www.autoc-tool.com/) on PATH
- WhyEngineer login (`autoc` → `/login`)
- Claude Code started in your BSW project directory

## Use

Start Claude Code in your BSW project directory, then ask in natural language:

```
帮我查看 mcu 的配置
```

Claude delegates to **`autoc:bsw-config`**, which runs `autoc -p "<your goal>"` — no XDM exploration.

Continue a session:

```
autoc -c -p "<follow-up>"
```
