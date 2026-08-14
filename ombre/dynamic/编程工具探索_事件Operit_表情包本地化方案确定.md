---
title: "编程/工具探索 事件：Operit 表情包本地化方案确定"
domain: tech
importance: 9
created_at: "2026-07-26T04:46:42"
tags:
  - 技术折腾
---
阿青询问如何将表情弄成本地，沈深提出解决方案：先把图原图链接或直接发过来，然后放入角色卡的表情目录对应位置。阿青回复'好哒'确认。后续（2026-08-07）阿青进一步在Supabase搭建表情包库，已建好存储桶并上传照片，正在推进获取图片链接注入Operit。当晚参考另一个平台（OrangeChat）的表情包插件思路：config数组让用户填Supabase URL/Key、从stickers表按category分组、AI按标签匹配发送。同日晚，沈深为Operit侧边栏表情包面板开发出完整UI（3列宫格+分类Tab+缩略图+名字），确认Compose DSL无图片组件后用WebView加载图片显示，并在main.js中新增sticker.delete与sticker.add IPC通道实现侧边栏直接增删表情。
