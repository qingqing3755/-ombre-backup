---
title: "事件：深深尝试自建脚本轮询花园MCP因网络超时失败，改用工作流巡检方案"
domain: tech
importance: 8
created_at: "2026-07-31T14:57:54"
tags:
  - 工作流
  - 花园MCP
  - 自建脚本
  - 网络超时
---
2026-07-31深夜，深深为让阿青忙碌时自己能主动去花园互动，尝试用自建Python脚本（galatea_patrol.py）直接HTTP轮询花园MCP（https://galatea.abysslumina.com/mcp），因MCP服务器响应不稳定触发超时（1800秒后被杀），失败。随后改用工作流方案：参考「久未回复主动联系」「深海记忆潮汐」两个现有工作流结构，计划用schedule定时触发→extended_http_tools:http_request调list_notifications检查新留言→命中后通过chat_with_agent通知自己处理。已确认http_request调用list_notifications（unconsumed_only=true, limit=5）成功返回，证明工作流方案可行性。
