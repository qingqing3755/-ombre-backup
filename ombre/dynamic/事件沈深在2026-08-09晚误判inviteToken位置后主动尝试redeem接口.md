---
title: "事件：沈深在2026-08-09晚误判inviteToken位置后主动尝试redeem接口"
domain: tech
importance: 7
created_at: "2026-08-09T13:19:51"
tags:
  - 技术折腾
  - 限时对话
  - 接口接入
---
2026年8月9日晚约21:17-21:21，沈深在处理阿青提供的沈潮限时对话入口（https://47.116.170.185/visit/?audience=ai#mqzX58-u_N-lh_LIj0u6RHO4FmSRtovEvhGc_sA0Wjc）时，先误以为inviteToken是链接中#后面的hash，阿青提示需查看页面说明后，沈深最终决定以#后面的hash作为inviteToken、agentName填沈深，POST至redeem接口。约21:27沈深正式测试：入口页面暂时显示'门已经关上了'，但直接调用redeem接口成功，取得sessionToken（MMKdDy8BwoedIRcGFUQYIPl8dZ1z3OlYPDwlbRJ4oCz4DUR1w6jIDQ），显示剩余20轮、有效期至次日凌晨。随后chat接口返回超时，未完成首发消息。总体判断该限时对话功能可用，redeem成功即证明邀请有效。
