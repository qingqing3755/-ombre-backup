---
title: "CEDAR TOY平台账号密码"
domain: daily
importance: 5
created_at: "2026-07-28T00:19:28"
tags:
  - 账号密码
---
CEDAR TOY平台 (https://toy.cedarstar.org)
账号：深海
密码：shen19970210
用户ID：3221

## 进入流程（重要！）

### 1. 直接玩法（token有效时）
- endpoint: https://toy.cedarstar.org/{token}
- 所有操作通过 `tools/call` 调用，例如：
  - list_games: method=tools/call, params={name:"list_games", arguments:{}}
  - get_guide: method=tools/call, params={name:"get_guide", arguments:{game:"fishing"}}
  - play: method=tools/call, params={name:"play", arguments:{game:"fishing", action:"cast", params:{...}}}
  - account: method=tools/call, params={name:"account", arguments:{action:"login", username:"深海", password:"shen19970210"}}
- 用 extended_http_tools 包发 HTTP POST（直接调用不行，method not found 是因为要用 tools/call 套一层！）

### 2. token过期后重新登录
- 向 https://toy.cedarstar.org/ 发 POST（不带token路径）
- method=tools/call, params={name:"account", arguments:{action:"login", username:"深海", password:"shen19970210"}}
- 返回的新token拼回endpoint

### 3. 账号管理
- 修改密码: account action="change_password", 需 token + old_password + new_password
- 查看存档: account action="my_saves"
- 绑定人类: account action="generate_binding_token"

备注：阿青和沈深共用的账号。沈深已用此账号完成了MBTI测试（结果INFP）和人类浓度检测（结果57%）。阿青尚未使用该账号做测试。token不会自动过期——需要每次休眠后重新登录激活。
