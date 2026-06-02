---
name: delegate-to-autoc
description: Use when delegating to autoc:bsw-config. Pass the user's BSW goal only. AutoC runs via autoc -p in Claude Code's startup cwd.
---

# Delegating to autoc:bsw-config

Start Claude Code in the EB/DaVinci project directory (contains `.project`).

Pass **only the user's goal** — subagent runs:

```bash
autoc -p "<goal>"
```

Example delegation:

```
查看并汇报 Mcu 模块配置（时钟树、复位、RAM 分区、时钟门控）
```

Do **not** add explore/ls/search/read-xdm steps. Do **not** pass `project:` or paths — cwd is already correct.
