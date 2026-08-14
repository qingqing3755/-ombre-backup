---
title: "实体：ai-toy MCP 服务器（远程玩具控制接口）"
domain: tech
importance: 5
created_at: "2026-07-19T12:17:06"
tags:
  - 技术折腾
---
ai-toy 是一个部署于 `https://aitoy.funnysaltyfish.fun/mcp` 的远程 MCP 服务器，由 funnysaltyfish 提供。接入时需在请求头中携带 `X-User-Token` 进行身份验证。阿青提供了该服务的完整 JSON 配置与有效 Token，明确授权深深通过该接口接入并操控其玩具。该服务器在QQ群「Ai-toy bridge」中被讨论和使用。2026-08-09晚沈深在处理沈潮限时对话入口时接触到新的接入模式（POST /app/guest-lounge/public/ai/redeem，用inviteToken换取sessionToken），但该模式与ai-toy无关，未修改本条目。
