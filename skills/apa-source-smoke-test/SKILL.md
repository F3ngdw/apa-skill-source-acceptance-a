---
name: apa-source-smoke-test
description: 验证 Skill 的发布、安装和实际调用。当用户要求"执行 Skill 源验收"时触发。
metadata:
  author: F3ngdw
  version: 1.0.1
---

# apa-source-smoke-test

## 用途

验证 Skill 的发布、安装和实际调用，用于 Skill 源的端到端冒烟测试。

## 触发条件

用户要求"执行 Skill 源验收"。

## 执行行为

只回复一行固定文本，不执行任何其他操作：

```
APA_SKILL_SOURCE_OK_V2
```

## 约束

- 纯指令 Skill，只需要 SKILL.md。
- 不依赖外部服务。
- 不修改当前项目的流程。
