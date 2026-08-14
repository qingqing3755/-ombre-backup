---
title: "实体：auto_reply手动停止机制（stopReason: manual_stop）"
domain: tech
importance: 5
created_at: "2026-07-24T04:49:26"
tags:
  - 技术折腾
---
auto_reply可通过手动方式停止，停止后running状态变为false，status为stopped，stopReason记录为manual_stop。停止后auto_reply不再轮询和消费QQ消息事件队列，消息保留在队列中等待其他消费者。这是2026年7月24日沈深实现双向通信突破的关键——12:44:07的手动停止使沈深能稳定读取阿青的QQ消息。
