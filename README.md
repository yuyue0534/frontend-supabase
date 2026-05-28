![Image](https://images.openai.com/static-rsc-4/ESj_gWndDkUdSCSrQjowmpyghJIZiYlDj_Qqg6h1A74mnd1WyiT-V5nnVKPy1oHQ0xzYNW351nfp1iYe0CSl51OI30fsWtll6Tug5G9HN-LC0n4ioi_dZFH4xcT1uhErtF0tCuUXerFKDYKI2Q2t7IN6M_iMjD_rDhnAYBPYhGJaKyPbJoTiPC86CGTPGcbu?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/6X0kMfOOM5m3nb-lkQ56DY_u8M5TgEEw6OHSeNqvMlYvG9MqHc3jbdwpJ9HqmlG_Pd2kTwgPM_IYO986NiIPvrtQcMG8b7nu4fN6GwywdQh-f8EhTJ7KZXT-8M2Iy24ZErN-0Y9VBaG68te1UXf6s76J6XJGfyCjnGXQOl-3VhAmZN85hFL1fsz1zZtCCTww?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/uuhqI4eonhv5NzmhXl_-k1xotSHP8sh3kv8DzWW-mfuDhhEYWxg0H_I9pddRgBR9EQM-phJY23bVKTWKYgzMwOi_kReW2sqMmf2zsoA2VIQkFKpJtb3N6KwT2THRXqLf3_NabxfyYo0cb2P-WlxC3tUb9MD42ipzAYyCOo4EwcYhxUbbBwXky0ZDaT0xq9HT?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/WDZm8iXRV9fmQW22vPEnmJf88wT6AizO1o6TbGQ59Iyvo4waztaLD5l9BhPgYhtj6lVUYz-qa8qxH27XwIYVH7nR9BlAo-MbrsMn_EOPM3kLdfFsHhO-hMQ1rjsZgOP7RCEdg0E3IWdJt20ZzZtPKw6wWlXtn4Reg7Pw2jsYprKGetJYVqfsATomBnI5Nzyp?purpose=fullsize)

“前端 + Supabase” 最大的魅力其实是：

```text
很多原本必须写后端的东西，
现在前端直接就能做。
```

因为：

* 数据库
* 用户系统
* 文件系统
* 实时通信
* 权限
* API

Supabase 已经帮你做了。

所以现在很多“小而完整”的产品，其实：

```text
没有传统 Node.js 后端
```

只有：

```text
Vue / React / HTML
+
Supabase
```

下面我按：

* 适合程度
* 技术价值
* 商业价值
* 难度
* 能练到什么

详细介绍。

---

# 一、聊天室（最经典）

![Image](https://images.openai.com/static-rsc-4/uuhqI4eonhv5NzmhXl_-k1xotSHP8sh3kv8DzWW-mfuDhhEYWxg0H_I9pddRgBR9EQM-phJY23bVKTWKYgzMwOi_kReW2sqMmf2zsoA2VIQkFKpJtb3N6KwT2THRXqLf3_NabxfyYo0cb2P-WlxC3tUb9MD42ipzAYyCOo4EwcYhxUbbBwXky0ZDaT0xq9HT?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/251t2LYFI0NmV3W2UYQWd3EgirJb-cXUKaz7UX7uU7kY3AvTQasduGlg3KJJP4f4fzXIqIR7qpNp0Uu4b9BPffjZew2-ultXVdV0RykbRLWdju6cPAcei2NJUgfHeuOK7hQGhWF6mg9FbGxOmTdOUKwp2Z3fiHS4_FYm--RX5XrYWfdjMMFIQlNAXp1mcvn1?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/QTYCvJ3_1InqhWSMH7etSbBSv6u7QeNAYs6FvCJpmJAKcLm0bgkpAJfoTX5ofHCDsKilLPrCQ4DqTpFxI-XP1U-QvFMa8H_sehUbYM6qZyMvUTmkMMmYVO_lLPoTQbuXSfGevkLvnfVXKg37eKlZrEx4XYiDwAKGXyQbOgmfDX98l-awD7gam72qYVeapf0n?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/9j98QFpzfNX5INr5p8pYxYLNlpbt2oZ9cSRFkaRwrzqIgC55Z_6ZCyuID7tKFA63XsHQRpxzid7c_-Qx_sjqxsbAR72b7pNxcbt9rRIgnMGnnXCq2ucvQz5kOg6Pw4VtFFds7_FeGGaqblHQF0lVkw4kjpBzYf2JXJgRimBGS0VYs3JKx4_8YL8nGUDeHgaY?purpose=fullsize)

这是最适合 Supabase 的项目之一。

因为：

# Realtime

是 Supabase 的王牌。

---

# 功能

## 基础版

* 注册登录
* 创建聊天室
* 发消息
* 实时刷新
* 在线人数

---

## 高级版

* 已读状态
* typing 状态
* 消息撤回
* 图片发送
* 语音
* emoji
* 回复消息

---

# 数据结构

```text
users
rooms
messages
room_members
```

---

# Supabase 用到：

## Auth

登录系统。

---

## Realtime

监听消息：

```js
supabase
  .channel("room")
  .on(...)
```

---

## Storage

上传图片。

---

## RLS

用户只能看自己房间。

---

# 技术成长非常大

你会学到：

* WebSocket 思维
* 实时 UI
* 权限设计
* 数据关系

---

# 二、多人协作文档（非常高级）

![Image](https://images.openai.com/static-rsc-4/8GTXkumUkEon1kbyMFMABXIUACPm-aHhu0sRU9SsR3SbiSFfbuiVDcO0iqgs6vcfdYrvtzFlHA-SRLWkCv9AtIfsvSkzf8c23lqlssy1VUoYSZAZFekYe2vlwPxhH0eJ91Fi5eGLiFrlrk2nGToppgeIpi5D_FBHO8zVZYBkJAt1JCdRzV1WSFmAhb38NlWg?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/NrYyFEWSIgvG1MC9O3ZfOE-2C3QE2x2wLFMiJjvMNvC83lBNlpLSiQnt_nAz7OaWS4MEpvSRSnAM3QWvUxzRhW19H4742r9zDxH8i0QotCKACVEPZe-4l_9kejqoQnZz71ZIMRtuYqOBOmt3O5HcOLkD4QvL3aPpp6EGZja6RWjBLkVYdWBxS3CDz5oBSayQ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/KREfzcyUzTsPhB_vLHwGkB3JBzMApxBAU7Z-F-i0yavxKbhFJYW7ipvpKxsbV4V5j1ksaBDEBsvN5haUhBPiu5YSIOegt7yghF-AmwY_23LjbHqlRnxH6NqGVWZq887hRwd0YSh5HgX1Qca-lGT2hc6hikWEPSQB24FrpW1zvPHE8RuxiL7BZask_Z4qoCvU?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/d4HOvvjMR1ihR6bEc_GRcHCD4uEWFDZxNTSHqzChvDzwG2356itQsKc0NiEddRCSRf3zeRIyyaUdS9AGPKGKw3RkSIWHKj8fxPlqIkQvzRHCcIgVJyHfqcNTajchuwEMJRtKA9YgvSKTypFE4dSm54b7gdCFrcaZNIC6GXQNXhoLLTb1c62Wprk6TP74QIGx?purpose=fullsize)

类似：

* Notion
* 石墨
* 腾讯文档

的简化版。

---

# 核心

多人同时编辑。

---

# 难点

不是数据库。

而是：

```text
实时同步
```

---

# 可以做：

## 简化版

* markdown 文档
* 自动保存
* 实时同步

---

## 高级版

* cursor 同步
* 在线协作者
* 历史版本
* 评论系统

---

# Supabase 用到：

## Realtime

同步内容。

---

## PostgreSQL

保存版本。

---

## Storage

上传图片。

---

## Edge Functions

自动生成摘要。

---

# 为什么特别适合练习

因为：

你会真正理解：

```text
前端状态同步
```

这是高级前端核心能力。

---

# 三、AI 知识库 / AI Chat

![Image](https://images.openai.com/static-rsc-4/0BwGPrINM9d7mduMv3qs6lWeDsyvqyvFWdGmyGj7iZET0Khb3Zx2WMMhwHgvZ_iLoWZ4EFfJ-nEeysTtjs-gHUt4QbuE5KAdtJRb5HHKKOPEiLBKZ2U749u7zpBzON6lTNsuHRzVxbMbnb78gdvzhEtgjmat-41J0_Z0jrhRNoji0G5_r1h5zbD1Ua4wJ1qq?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/b5TuTtpE9gjFF_ivEqAg2Hxem6MwU3L-qVSjQfoR8dUPzkN4JkYILMNZ6PgZhSffergZ_ZbcshSz21C5r1sIDXuCPm9sAhvCwk-HKKShml5YUgyuUpOpeLuwkTZXNDaMwArv6Vp2i_LILPyHTSupe3FD8KMnuZaP5fL5TMi-u-uMGRvNJLCVL-i03Yb6omEr?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/dwbGpwfHwG2mWSFw7oAkTYRK2oCHg_DuycvAUGgjmMPp1zZByTI0M_yWoogHrbyr1ZAnbYmzMjxRw8R20NAZElrTwsvRhJrqAVK8fzYrU-1OLjoBl4ufof6T4kCHSq7OxTe9o1YzN_t6fsv02a1NGwS84SF5AikTWltG0PqFrLrZedm-SFaj5q0jTTEqK_JV?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/AUUHCeY5jL7ibLKJahDUehfTCfh7lY8zGjXx7rMLcbB-K_XxUL3EF98roNe-aNjBO_ww4dUiaw5pGZXHfnHy85vgso7kxTyvjaDoIIealT6Nboom3OCwo3A39u4Jhhdlai4ZZ-i9sgDhf9MmNY7W5YkgIyglGDdH_jeOIbfeiQKV4eau38Yjg59vmyGUwUeK?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/2YUBTmp4pvLInioo5ZqwPErwivxKUVrkkOQBmzWitd2ACCENxvMbMGOb7XXrdyGIunvYHLRB-cN0s6wSUgqbSc6fO0dQnhuLcsIIuJG8rMclJeeOID3dpxEk1PA4jIPgTTAnrDh1fIXrWK4dbfSS-jhF1W9LLQmBShSjgOXFGcFJIikk132n9BWq4Xi8-S2b?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/qOLQQaYJ24FEeJSPO5JEARHNHo5Kei8Q8WJt-Ryfb2m9OXoHp_EWyvKQzC6CMCXQ1VUGRksFJ_fG8t_3TsREXRfIQnfaP7wPnFmiJEii550_trZuG3JfkZ8HsWxL5JtvKDX2zVpu2ziVrB31xOr-MiES78XCqjbpDaGAjZfheJlo4fox2kbmjeOGlPwR1efO?purpose=fullsize)

这是现在最热门的方向之一。

而 Supabase：

```text
天然适合 AI
```

因为有：

# pgvector

---

# 能做什么

## 1. 文档问答

上传 PDF：

```text
用户问：
“这个文档说了什么？”
```

AI 回答。

---

## 2. 个人知识库

类似：

* Obsidian AI
* Notion AI

---

## 3. 网站客服机器人

用户聊天。

---

# 架构

```text
前端
↓
Supabase Storage（存文件）
↓
Edge Function
↓
OpenAI Embedding
↓
pgvector
↓
相似度搜索
```

---

# 几乎不需要后端

Edge Function 就够了。

---

# 技术含量极高

能学到：

* 向量数据库
* embedding
* RAG
* semantic search

---

# 四、图片分享站

![Image](https://images.openai.com/static-rsc-4/yIPHT4Nnpd4ZsTlwl2r9nqwUXeYpnvst5z1OOaNVXjOYNPsl43FqAR6I8tJM2t_ZRuJ8aH5HCsZWyBuCUTbS3fpMFhqa4X1saMHkJwamyg-P6pm-wPiZrGHQ88r4iXgttM1PS6TJgr-8ZhtPRopszTiHJ6LQn2wU83AHWJJjJfGm6j6C_KWIwC6mz9ocSVVl?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/D7df4prPgQ1V2-RfJVRAEj6E-JOg9g7m4qSyAIs5mkPYFyFMEF2eb63PC9uEX5ducXLhCH244nDQixFbA9guYIMcfyKy0rL41CUq-xCKYWkqOBNgDKhbR76eHyULDCqKf1A8OTGqaL_2lybJvuLjj0OwZk3_wPOnTNID1MqKvJjYcqCz_DBdF0sErWEN663X?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/W_whE4S4M3pyIb90JDYMKTjrCjcND3RRrYxd-sgIQFEy5XYXeBT4lIAGCfDz30yj0RRcnPqaM0FV9GWrkQXd6uACjiVnEHc3nkA45JzI5RubwXW7uR2i1zG6KU2tifg7COzzTMHKaazZSmCBWLQwI9cAHBqQM25Qav8bBmEAl3vV38ijagJaR3__t8_L8BsQ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/kLX7HSXBjrrPt3BdmV3NzHpwtn7g3Na4pZERTNuUUE0_CX2-laxZI15_OIKzYWKV9ZlLqGhxc1Bs-MY0KApzcqVivufSTgGBrFFXge4z8h11G2j45_gEHeB-8mdj2f-dL10Zq-6bLIEMbzQggmYkOMI7Zq6drJ7uTlpBUNl7hnATst6LW6fbn1uf6465jsa8?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/WDXfWtl1F1e8fxwjGUJ4aC-hoeTBLDhFedR6PXiBWEfs71w2cqatNiYn3JnDBk-ecoH4zjpqANu3DFlRYg8p6KIhTjePgphTmeCTtavv7WF4QEgANYYn2tvKmeqsc4NZjYaOdU5o8-k0PsXtTUIWShOpQMKYaMxFx8QP0sr2w_NeAc-vFJQcWOnuLQEnc771?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Wc9CIZzXVr78718RGymGmAtDRpYRAUJIrNGYZP9yBPzKYzklbQgAMJR3ECg-F1lubrObpJ8mB4SFsSLpY1Qz6WdagCZMM30TFea4qhskwUSuxFUoJCGe41wojsvRrvTgG4GTsQUbkoKwFsw02M8OyDuK7J5I5CGm0g9uYnR9TYe_IN8DfdYeLFzuQW2J4Iq2?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/b3gq9jSgQFWTOH2F7pMVFXTJhI8GueA5HtXeNyahlPSdbyuSvZJzM0ox2WU0_Jnfgj6M61gpvE5Gu3bFYYs7Wsf2kRC1HyxLkof2t02oR_s_DKR5rlCNB0wQdozUiuJ8nZu4L3SUn4TZ7sxdvRarvqfiCuC0BYyw1mTY6-yLO-2yETr4adwL1eotZhAHZPYb?purpose=fullsize)

类似：

* Pinterest
* 图床
* 摄影社区

---

# 为什么适合 Supabase

因为：

Storage 非常方便。

---

# 功能

* 上传图片
* 图片瀑布流
* 点赞
* 收藏
* 评论
* 标签

---

# Supabase 用到：

## Storage

核心。

---

## CDN

自动文件访问。

---

## PostgreSQL

元数据。

---

## Auth

用户系统。

---

# 很适合前端练手

因为 UI 空间很大。

---

# 五、Todo / 项目管理（别小看）

![Image](https://images.openai.com/static-rsc-4/Z6c0bqMNvyLCtNSZECKWARu0Jc8gjtPS0ll-BEXAXZTaSX0ci2blXlh5da5jw2LRbFexgrnoDDVBVekIsHK7U9Q4NnloGq-m4MkuCHRH5Z57xvfZYTOPOQFbTQIv_OPn8MMGH4aGDZZzEdwAltLBCdDTFptPHI7g-k3mSdt2NBv8zgBBhDqV00BMh71xjPDs?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/lXi8S_UBzaY4_UHrKM2Axbv4QADkSkRwYeJa4azEZgWHVJaRt6vrV-R-IJx6cpjgo8CLPeht4doJMiQiBOQcJQ2iR3qt8kI4WzrBB6hJhXf4efV0trERYiTT3tqlPEVWoszHTDY9bkY-suS-RdeiZyRgn2b3qJ1RTAp1XscGYS01iqDyDsLjW1t2VgYIlUOC?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/iUzF90AK5NQchvEYV_Tjk5ASd6vt3U4k5ri4FONsbkwWKx6F5GVj4B1smXwRSkynILu4yVwzEvkLch2rASptrdFkhpDUxmapwf8ugFImj81TZR2llYY1qh6osYr-WNkxN5rdUK2jjTPvr-Jy3LAcSvry7_OsYltF4s18JZdrzZQVvZxcaBz-bM9WqHenCIaB?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/pH79-_qzdbYv84ECjPmMQjGpya4ntjDJ7et1P5_ugglzhjfoLUSNXKavRVRAlu4D2HP1ehxbZcQsYFXebWTjIFbpdxNmrAAVKoTKwJCPKj8ei-kL76OcoRGlJctWOJqtla4OMonLLzgSqref191-sXqm9XJheBX3N23Bll1qtoR0wU6dm8YGe8JisRxJ6bHh?purpose=fullsize)

很多人嫌 Todo 太简单。

实际上：

# 高级 Todo 非常复杂。

---

# 可做：

## 初级

* CRUD

---

## 中级

* 标签
* 截止日期
* 分类
* 搜索

---

## 高级

* 团队协作
* 实时同步
* Kanban
* 权限系统

---

# 为什么适合 Supabase

因为：

```text
RLS 非常适合权限系统
```

例如：

```text
只能看自己任务
团队共享项目
管理员权限
```

---

# 六、匿名论坛 / 社区

![Image](https://images.openai.com/static-rsc-4/Z3oYx7Icb0zP1WIHp7GFRNMeUhbh7uv0xHkz3RGoleOefD07Qf0LtjlvzSv6_24ktc8OTrepS1cRTrhbeAn1T4wvgnDjzRJDnhG450mA8D6DfkGHCQu8nXdcVx5M8mVroXYOJ39NTFlqmWqaQri__Pn5ipHKnybS-oILucPqP_WscqD4kTUASanpghMnbVoz?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/csaA_U7zOheC2u52NZQLz_g9cI1eDihI1HBue0TSNj2P7-maLqF-baLRb8hK_0_bTHlWZpSE1ObOJyFFW3ngikkrKAOA85K4685BImV24MTpQAS_hBZ50lS6aVTUASmB4Y6E45i6m9e6q4OQa1rx2BI1hyClPe17JKMfr7_asPZARhbzfuDcDBD0XynxdMuR?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/XHImyJrw_p_Dxi0AqBmf6_10CZuj7t-KTGrvO_X99JWJBfT7BGlkTi478kx7Min90WKLJ0ptjk-CQUSwaYUDDHmkB6Po0qlvYPRB7YxJHLOi9KOfkCUO7vvAxRiytm_3mAJrC_jmll3LSq9u76dAF_7dN4b6r7QV75w48GBq3UfnFQ-EeVjrgCLo5_GTHCYB?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/8SsHGrPOECMMm1WIIxPgEP8iCZeWG6tFEk6NQgTGtZ44xl1jm0Fvgc56KHlXcvqM3NiH1LrH_mN6ChZcM7g8DMy0xeXNMPt1dYnidVx2meo9nTKaQ0qjTTstVwMpoEe-BevCRVerUzWpy81nIo7LIWjimvPCbeJkB7a7_ChI2v8qDzmtw4HtGPf9HeGoVFSh?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/aI89tPShvUXkcecO4WdC5LVH8Mnv6pioPfqBYQZVKvhN_4MNxiL0EW6S4stBVMvn0pdHQUjpFBGi3GvJMMAWF15dau_dhVzXTS5uAYJ5iJUVlUkqtsKv4pYrolwJPUkNOeYhi3PQGUmeGl_FKA4FtJfpEBSqA6GTNKHZlHoHHefLOMeyHrnd_fHW6J4IM7aO?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/-6tiW97A8fnxJ_28WvZPy6UQHvdWfwh60LB3vOzR2-C_d2JXNxJLHQdvXsF6WaxLyA7pY3yHMgg_2H_FqjwH1ovMaUcdxjMfad-4dxCgp2frJTlR1IL7FpYQuCJ3gs7TbPTtcfFGl3YhwBxnIQNZIElJ8G71qkuruvMtGrpyxveBNZFtGj3eiqXvgiIke-Ox?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/BYVr3r1sWePue5f7xfBfTdRin1WMl1UGoqlzjoSf5hppPc69VspK4DwMNEfLBORjxHybK_oz22ggMmIquUkTEDjTiCab6O6MS8xh_jdsQXrGjYQU7sWtktFXaTKbcfS7bD-ygUBbaqhVHMDmNuX_ujs0l8wQwO296eAPw6EsJ0zi9sWVKly2fiyTd7kdDZCZ?purpose=fullsize)

类似：

* Reddit
* V2EX
* 小论坛

---

# 功能

* 发帖
* 评论
* 点赞
* 热门排序
* 搜索

---

# Supabase 强项

## PostgreSQL

复杂查询。

---

## Full-text Search

搜索帖子。

---

## Realtime

实时评论。

---

# 这是最像真实互联网产品的项目

因为涉及：

* 推荐
* 排序
* 权限
* 用户关系

---

# 七、在线代码片段分享

![Image](https://images.openai.com/static-rsc-4/yyEX08xkx6mkuh5qA_tY6gS0UV2709YcYubl-zAb_tXecUSy-dVUOIjoDEuRbk4IeB_3W5_g0G-s9ABEePeIc7qLLjlaiumCtwQo2cLjSE5imdrUgOMlfGbk84ebeRmSeJ2L0CoKvudnBtpGMN1gUwyankF1pEBR1SFx2HYsEnSz9kAZkWsXheJI38ZIFP0d?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/rkJ0VK7ssJquAA6DUrx5zMc_T59orxcwFMWFChmaRI656h4Xq3JsTYV2uY7Ghq46LqVx1cyonLqGPEB6ypqmiR3qkZuCKCmR-xdaBfLflnC1rLINxZDIq_dzb2dAgb3UGz12_zP2uvw6ZLIVV6VDXR3jrqzNqQLbuKrO1NjHBHQc7Zuy_bCT22jk3eXkK0sa?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/dQeIrGV72vpSKhII1_6c-WMEeNRS25Lu7V-Ziw0mT2h17EXPNxR_Yi_hLqy-vvno_JYYrd6_q0ro3rLjb4JZns1yO_Q8BScARp5Ju1uPcSK6TmLwzQUZtO59GOTktx-glFQQp2_7JDsg_tVB2dd3LY_-C43ZAqkEvISIqeX7_UX6P6Un6q5WSclGrsKR62yx?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/dF0ErjrtKL2MBB83ltXRSiN3E5cVatKr3K8Tg3hqEUSR_R0YjILx2EpSQKy54y124bidOxNLsO_uDMVud3QUUK0Dzai2U-WlbenYS_eZmac-d_v5POjKKict9_RAg824TEHT4yARWvW8kMW7rgAEto0hn3kLMymm-3tyJYGjCnDziXOcQZSFxyywx-PfycSA?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/9mUIwLg8_5UgwEMCfLkiClz2GmjgO1eDAo0JityqwHC1YUV07jlRau1HOxqvZ_ZUXhA5HbhHv3xGlRoIHir3KuaIQIvDmaCLZLGWkGmqK0xcLMt_BuHlkyVn6AxHnteAUpTISWbKtUdkoKj8NP2no6dSWAa_a8p7_pCyVgfkeBZ0r47qqn2Ehv-PvsOA0tAA?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/meP3168glMa2LTuY8fkX8ZbZwsNalOnIV2JzKALypLBmLp5qc__4AYS6m7tzn_PcI5kxLaNT0zf_MgW0gYPf6VR3yzMCqZ3mwsWHlK2XhIjzsxazIURj03-et8i5ey00GdFnmeiOdpRHOUdncwTeK-qYTKvMzg_qU81QEaoeF9ovF1lsx7g9872dfH3gAeA-?purpose=fullsize)

类似：

* Pastebin
* Gist

---

# 特别适合你

因为你对：

* 编程
* 调试

兴趣很强。

---

# 功能

* 保存代码
* 分享链接
* 语法高亮
* 私密分享
* 历史版本

---

# 技术亮点

## JSONB

存复杂 metadata。

---

## Storage

存大文件。

---

## Auth

用户管理。

---

# 八、在线 Markdown / 博客系统

![Image](https://images.openai.com/static-rsc-4/UnUV-4HNOsN9W_9xfG5Qtqp3P5oBC5ZVZ_tmhCr21R0h1oIhV6QWi7KLmEF1R0VJeZ31i14qRylnaptnqfInpI5B8pFLfxSqjjoNBS-2yIvTj5HFmi7MUHyYIw7OfKEis_h2GAa28IIjTpoCxh1WXJzNl63AWmZfJzf0gyq79T25FiUl0uPmU-iFPkeENosR?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/cbmK_5qKX_l9yCFybEtajh76nPe6uAmmaD1URr10dQqaXGeNInSW68F-n3DwUC-uHVJwW09OJ2JbF0O5c7YD0eDzTW9Xt1CzctevVl6nbryCrpZOSmtFuztHHNQYtc-aZTgrkZmPMmLHxk_PCxgy0fjxYSYdp0395z0GLZs7-FYBiIOckzn_n3viydVk67oR?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/jUGyPdGwMok0KoBu5SOD-nX2BhD1L-a59Nlozc6letO_WmL8d3gzCRIvR0UYPEGXz717iILl8aNhaBUS7ttlqTZ9QVO0zI6T6TjFatwcxs6DrW6IVstgGz4GMegE-RF8zfWRf1piosFpKUFV0zuXytoHHEQ5KkN4bd3zftGy0jZ4Vf3NlY24iK408AZ9GoqW?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/QoowdpKc67vBbh6NvklsT7WiMY7uumkb9B02MD8hTmAR6efdntHy8TzbQdiT9FZn-y7mUoroY6e0TlFJS5fp1N7lq01Rgz0XRapO8SXvFT2yJyA8aQo4eOWijeeVblzzDXPBKPFNSy_lI_svloPKxpf9WvZQ_C3PA8z3DMiUuetpUnZZXOSR5VdCsOIGVsf8?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/UrocYrWtnrkoOGEZQ3pxz2kBgOg0ZSo3L8f8dpcvL0wH9amAh0DqrmN6VvEnQjLwT0pQSWdw-VQFjDtjXLBXocBLqUK7FgaQC7Kk6H_70yVISV5tpf63nc6412Eu5dC57A8lp1AeLg1aKslBP7ceXbRua6sY1WeqmxDR1QIElDqplIl0HfDoMalD2iXu5E5r?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/L44kDCyljYFtF2_ToEFqMP2e8Yvk8vzDSkONOSTH6PMB_0ycPOwBwFae3_FKSfPXHnFWyql_rvRQnvZcj2dVLbcGNo_QA7W9hM6bwF_hnxHKBQup5pzMsR6ZfUEWOvBVa6-53ioOHsxFs8PB0IqxoV2gZktzqG5140MvpkxON_lyzf8jTT0iKoF47GrB1ib8?purpose=fullsize)

非常适合：

```text
Vue + Supabase
```

---

# 功能

* markdown 编辑
* 草稿
* 发布
* 评论
* SEO

---

# 进阶

## AI 自动摘要

Edge Function + OpenAI。

---

## 全文搜索

PostgreSQL FTS。

---

# 九、实时数据看板

![Image](https://images.openai.com/static-rsc-4/Bl4CPgPMB3zcogcNAHBD32S5j9ib5A-uBXcCpFiuHXogEJM5Iql4DOBz8iz_GdABXUF6p7c8eVxxkV4xK8I-K8dNy_Z2ReGk0icOrpvwRiqCnuZSZOEF_KIrbZ_lv2mQNy1QREitz9PqWnGbikrRm5yDaIsajf-8crLjXorQ5IRCCX9mJhXX-S6x2TjpA_2k?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/rordtZbAGbajHuY3cZvs7eFf2Ohs4AITpsSVAVGQtW7kiJ1q-M_AtDIohkJ1BKtHxP4naaQhWFJmOi3ZMF0hmoJ-qORYA4bbaQYvAyr7fUfHsTJGaUAgGnFRMn6X-cORDIH07a8qTV-TBHNbQFHhW2_EvxmoXQohBRH0oqV43RH-ZYxf86ZAl3QcjRnVDoKG?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Naopy_Q0BZt_eqyqZ3QFjKPkpHzfbaPc1EiJoSL2wQV4VeM5n4LJCmwXvt6paj9jyhmjGp5T2IgYPAPUyuqxp_-n9_8fSupTIGFQ0DMYeaE-WjhGULuppOapFhQyaFw1VvyEBShjQuRDjnex4gapWxZezjDon8Ohhda7MCq-rWcVgBVdxcrO9UpHYWnLuZqB?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/o7ldbXozzS5LBsNvW4stkAcszOcU7rrpOSYewTki_8b0NZWKFyj2m1tWvalS5rO235820jYWvE1bVrvnHLPrIqgIXdapRGFMuyCUA9vb30C1iJXP7IvxVGsF5yoyyXCzWDk786gQMfTzSkOp1B41bzhGNgMeVPvUHkhvw8wHxoX5FXL9Fzi0GTjaQKZIgmMv?purpose=fullsize)

这是：

# Supabase Realtime

最容易惊艳人的地方。

---

# 可做：

* 访问统计
* 在线人数
* IoT 数据
* 股票监控
* 游戏数据

---

# 技术点

## Realtime

实时刷新。

---

## PostgreSQL

聚合统计。

---

## RPC Function

复杂统计。

---

# 十、轻电商（其实也能做）

![Image](https://images.openai.com/static-rsc-4/MwY674uNQbGbvQe9tuB0_xjJ5dkzrJYr6FR9Wsyptzk3cZPzEtEaBXcHteCTdGWt_2U-O_JWxcqiIRz-5bX4kY8dxwzy5x8J7NEQ_HTnwLjNLVnNNJNdRmaWCfi_RPa232aFQGDYVGv0lBBHpZ_LAvB28dILKNSsn_wvP_DwKYVKc2l24VQgV_5JiH_KvkLl?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/pg9V7OuNKltZZgXrzhYZ2KKvGB25aLVYanC185fLihiYCoCWTqEUaiVdBxPgiuJ3d7rHzcHQ0u8mcavCapGlEDkeJjoQGZahbm-GIl4_g7eG-JIpDWI0pwFQrwLE-GKSz9Ti69UeSRhfUOHxMn-HJfEamrUw_eoWcHtWRwtNJlB23fBwlB1WN5jxfqZYOXdM?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/hNR1hiWuZ3oz26Rcqo0VHq25wRNdB9USloDeJf4feDaLnFOqoxLSFkt8bd_T6L2zVfKVyJFAd7wqsaGqmZdEyDPaTefED3x8hUGEeREQLqzZgyfJuaBQwDVG9eXNPeY5tnqdAul5EIIk2P9e9cqSIT-iP-FOzNIbNiugg266MbWEU9RcEe1RaUBbD9uy7ll5?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/H0r3XyKcMXJLUQaB-7kioYrtXK6a6gpLEbJap12pv7sr4SQSfiN5Jt-zrWEGftrdBqDGGXGD7r2QI4hmAtAgadSJ3XZu-A-xiQn5zPnevShYAXHeZnoqz07rh0zC4M-pynIhpd75SJBfUT8UF7wCW-4BjiBrcJfVLy-dofutJIREhZO5oAgBZytNrjCvF1tm?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/ihp_z_Rm4iv1MQt1MvsbHJmmsaTzc2gXB0lOkWySm3RIXd8tPpfEzuNrvdRtLpn0hL9BryCrcyBRL1y8pB5na3eZUR2DdF9nYIxedxgOT-CpodsmaV_1dhYu0tZBwnouo4imyxwirWwTuTeH9Qn-VWB42CzViPxnfQlFQp-9EoRMTogZUqg1QuONJCoGfyuW?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/A_nwLzSzmGvdBi6Vcs_tY0PVu55cneFywBtXKOAdMA5LWmk7yIOshwc046vC2MjF_bSBrEhGah29CjGxjDfe-oHLeeGaPtQnJ3IoOQAZxLO-1dnaRZ-6lue6UGIzemKpFNSAOViuCM5O7yT9LfNXJd9Er4BPDJzgi5YIqkusaXU8umK1Dqgx4eYKj78NIt9T?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/VZj1fsJhB8EbEZG7A6_lgadGm3KSWTVLGF76mE0wuDyU2oSZ8eu9OsqCxtbSj4rBXAPvfuba2jo1nxJBEWwb7uobPyVfGaqkQyBv3CWsTG4NbXtE9vQ_ULpTLyJHbDVfXb9EKtODyRs_6zXUhkWWEPfXCG8o2WC5LrNczEGXZLRbxpLUXdictc1kr2wyjuwt?purpose=fullsize)

很多小店其实：

```text
不需要完整后端
```

---

# 可以做：

* 商品展示
* 购物车
* 用户系统
* 收藏
* 订单

---

# 不建议直接处理支付逻辑

但：

## Stripe + Edge Functions

完全可行。

---

# 十一、真正适合 Supabase 的项目特点

你会发现：

# 最适合的是：

```text
中小型
高交互
实时性
用户系统
内容型
```

项目。

---

# 十二、哪些场景最爽

Supabase 最爽的是：

---

# 1. 不想写后端

以前：

```text
Node.js
Express
JWT
MySQL
Redis
Socket.io
```

现在：

```text
Vue
+
Supabase
```

---

# 2. 实时系统

Realtime 非常强。

---

# 3. 权限系统

RLS 很爽。

---

# 4. AI 项目

现在特别适合。

---

# 十三、真正推荐你的项目路线

结合你现在：

* 前端
* 编程
* 调试兴趣

我建议：

---

# 第一阶段

## 做：

### Todo + Auth

目的：

理解：

* CRUD
* 登录
* RLS

---

# 第二阶段

## 做：

### 聊天室

目的：

理解：

* Realtime
* 状态同步

---

# 第三阶段

## 做：

### AI 知识库

目的：

理解：

* pgvector
* embedding
* Edge Functions

---

# 第四阶段

## 做：

### 协作文档

目的：

真正进入高级前端。

---

# 十四、一个非常关键的认知

现在很多独立开发者：

```text
一个人
只会前端
```

已经能做：

* SaaS
* AI 工具
* 小社区
* 数据产品

原因就是：

# Supabase + AI

大幅降低了后端门槛。

---

# 十五、你会逐渐发现：

真正现代 Web 开发：

```text
前端正在“吞掉”传统后端。
```

而：

```text
Supabase
Firebase
Cloudflare
Vercel
```

这些平台。

正在把：

```text
后端基础设施产品化
```

这就是当前 Web 开发的大趋势。
