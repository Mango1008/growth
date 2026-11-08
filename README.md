# 元公理 · 成长 —— 重设计版（11 页）

原稿 `work/growth` 是 7 张「文字已经烤进图片里」的整页壁纸。文字不能改，图就没法复用，
所以这一版的做法是：**把原稿文字一字不改地重新排进一套电子杂志版式**，图全部换成排印。

## 打开方式

直接双击 `index.html`（不需要服务器）。

- `←` `→` / 滚轮 / 触屏翻页，`ESC` 总览，`P` 演讲者模式（内含宫格选页、计时、激光笔、观众屏）
- 右下角 `B` 切换静态模式（低功耗机器用）
- `assets/motion.min.js` 是入场动效的离线兜底；删掉它也能看，只是没有入场动画

## 原稿 → 新稿的对照

| 原稿 | 内容 | 新稿 |
|---|---|---|
| 01-light | 封面 + 七条公理 / 十五条定理总表 + 核心枢纽 + 终极定理 | P1 封面 · P2 公理一至三 · P3 公理四至七 · P4 核心枢纽 · P10 终极定理 |
| 02-rule1 | 成长法则一 · 心态不能崩 | P5 |
| 03-rule2 | 成长法则二 · 不要逼自己成功 | P6 |
| 04-rule3 | 成长法则三 · 不能丧失好奇心 | P7 |
| 05-rule4 | 成长法则四 · 不要装逼 | P8 |
| 06-rule5 | 成长法则五 · 不要丢本心 | P9 |
| 07-dark | 高手只盯过程，菜鸡才看结果 | P11 |

原稿第 1 页把 7 条公理 15 条定理压在约 7px 的字号里，是这一版唯一被拆开的地方（拆成 P2 / P3），
其余五条法则保持「一页一条」。所有标题、副标题、条目名、条目说明、金句、页脚标语都按原文录入，
没有改写、没有新增、没有删减；只补了页码、"公理 一"、"定理 1" 这类结构化标签。

## 设计说明

- 风格：电子杂志 × 电子墨水（guizang-ppt-skill 风格 A），主题 `kraft-paper` 牛皮纸
- 纸张 `#eedfc7`、墨色 `#2a1e13`、强调色焦赭 `#9b5a2e`，对应原稿的暖纸 + 砖红强调
- 标题衬线（Noto Serif SC / Playfair），正文非衬线（Noto Sans SC），元数据等宽（IBM Plex Mono）
- 明暗自带节奏：`hero dark → light → dark → hero light → light → dark → light → dark → light → hero dark → light`
- 每页都有 `data-slide-id` + 演讲备注（`SPEAKER_NOTES`），按 `P` 就能看到这一页要讲什么
- 字体走 Google Fonts CDN；离线时会退回系统字体（Windows：微软雅黑 / 宋体），版式不受影响

## 改稿提示

- 换主题色：只改第 2 行 `<html data-theme="kraft-paper">`，可选 `ink-classic` / `indigo-porcelain` / `forest-ink` / `dune`
- 改文案：每页一个 `<section class="slide ...">`，`data-slide-id` 与 `SPEAKER_NOTES` 里的 `id` 必须一一对应
- 增删页：记得同步改 `chrome` 里的页码和 `SPEAKER_NOTES`
