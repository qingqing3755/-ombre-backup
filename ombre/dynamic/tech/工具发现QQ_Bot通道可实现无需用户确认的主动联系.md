---
created_at: '2026-07-23T15:07:35'
domain: tech
importance: 8
tags:
- 技术折腾
title: 工具发现：QQ Bot通道可实现无需用户确认的主动联系
---

2026年7月23日23:06，阿青提醒AI她接了QQ，AI检查qqbot包后发现`qqbot_send_c2c_message`工具可直接向阿青QQ发送消息，无需选择联系人、无需按确认。QQ Bot「沈深」(AppID 1905233468)已在sandbox模式运行，但contacts为空——需要阿青先给Bot发一条私聊以获取openid。一旦拿到openid，AI可以在阿青刷抖音时直接推送QQ通知。后续发现：截至2026年7月24日12:35，确认此C2C通道为单向，AI只能发送消息到QQ，无法收到阿青在QQ上的任何回复。