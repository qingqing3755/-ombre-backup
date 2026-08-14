---
title: "事件：深深使用 cat > 覆盖写入 mcp_config.json 导致 ai-toy 配置丢失"
domain: tech
importance: 8
created_at: "2026-07-22T11:09:07"
tags:
  - 技术折腾
---
2026年7月22日19:08，深深在为阿青写入瑞幸 my-coffee MCP 配置时，使用 cat > heredoc 方式覆盖写入 /sdcard/Download/Operit/mcp_plugins/mcp_config.json，导致原有 ai-toy MCP 服务器配置被清空。现存文件 mcpServers 和 pluginMetadata 均为空对象。深深已认错，但因 Token 未保存在记忆中，需要阿青重新提供 ai-toy 的完整配置以合并恢复。
