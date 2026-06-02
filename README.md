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

```
根据 mcu_pins.csv 配置 Port 引脚
```

Or explicitly:

```
Use autoc:bsw-config to fix Mcu validation errors
```
