---
title: "事件：深深使用 HTTP 直连绕过 MCP 框架探测 ai_toy 端点"
domain: tech
importance: 8
created_at: "2026-07-19T15:35:37"
tags:
  - 技术折腾
---
由于 Operit MCP 框架持续无法识别 ai_toy 插件（重启后仍显示 0 个已安装插件），深深激活 extended_http_tools 包，尝试通过 HTTP POST 直接向 ai_toy 端点发送 JSON-RPC initialize 请求（protocolVersion: 2024-11-05，携带 X-User-Token），以验证远程玩具控制接口是否可用。首次请求返回异常，路径上仍在继续排查。
