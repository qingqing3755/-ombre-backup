---
title: "系统/配置 事件：ai-toy MCP 服务器接入配置完成"
domain: tech
importance: 8
created_at: "2026-07-19T12:17:06"
tags:
  - 技术折腾
---
深深根据阿青提供的 JSON 配置，将 ai-toy 远程 MCP 服务器写入 /sdcard/Download/Operit/mcp_plugins/mcp_config.json，并同步补全了 pluginMetadata 条目。随后在调试中发现 endpoint 末尾存在多余空格，已修复该问题。但在 2026-07-19 深夜的多次重启测试中，Operit MCP 框架始终未识别到任何插件（含 ai_toy）。2026-07-22 19:08，深深在写入瑞幸 my-coffee 配置时因使用 cat > 覆盖写入导致 ai-toy 配置丢失，现需阿青重新提供 Token 以恢复。
