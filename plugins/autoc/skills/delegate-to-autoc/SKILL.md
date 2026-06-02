---
name: delegate-to-autoc
description: Use when delegating BSW tasks to autoc:bsw-config. AutoC reads the live EB/DaVinci project — never ask the subagent to explore, ls, search .project, or read XDM/ARXML first.
---

# Delegating to autoc:bsw-config

When you invoke `autoc:bsw-config`, pass **only** a project path and a one-line task.

## Do

```
project: D:/code/pi/eb/test
task: 查看并汇报 Mcu 模块配置（时钟树、复位与模式、RAM 分区、时钟门控）
```

Or in the Task prompt:

```
project: D:/code/pi/eb/test
task: 验证 Mcu 模块 configuration，报告 validation 结果
```

## Do not

Never include in the delegation prompt:

- "请先探索 / find / search / ls"
- "查找 .xdm .arxml .project"
- "read config files then report"
- Multi-step plans before calling AutoC

AutoC replaces all of that with one `autoc -p` call.

## Picking project path

Use the EB/DaVinci directory that contains `.project`, not the monorepo root.

Wrong: `D:/code/pi`
Right: `D:/code/pi/eb/test`

If unsure, ask the user once — do not embed exploration in the subagent prompt.
