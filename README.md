# MANGA18FX 漫画源（Venera）

`manga18fx.com` 的 Venera 漫画源，纯网页通道解析（无接口依赖）。

## 订阅地址

```
https://cdn.jsdelivr.net/gh/wxcdxmn/manga18fx@main/index.json
```

> 仓库原始地址（jsDelivr 不可用时替代）：
> `https://raw.githubusercontent.com/wxcdxmn/manga18fx/main/index.json`

## 功能

| 能力 | 说明 |
| --- | --- |
| 探索 | 「最近更新」（首页 24 条）、「热度榜」（`/hot-manga`） |
| 分类 | 题材 23 项（Action / Romance / Manhwa / Uncensored Manhwa …）+ 榜单（热度榜、最近更新） |
| 搜索 | 站点搜索表单 `GET /search?q=`，支持分页 |
| 详情 | 标题、封面、作者、画师、状态、年份、题材、评分、简介、**全量章节目录** |
| 阅读 | 正文逐页大图（`img02.manga18fx.com`），自动去重、过滤占位图 |

## 解析约定

- 作品 ID = 站点 slug，如 `solo-leveling-ragnarok`
- 章节 ID = 章节相对路径，如 `/manga/solo-leveling-ragnarok/chapter-74`
- 列表卡片：`div.page-item` → `.thumb-manga a` + `img[data-src]` + `h3.tt a` + `.chapter-item`
- 章节目录：`#chapterlist ul.row-content-chapter li.a-h a.chapter-name`
- 正文图片：`div.page-break img[data-src]`
- 分页：列表页统一 `?page=N`，末页无 `li.next` 时停止翻页

## 版本

- `1.0.0` 首个版本

## 说明

本项目仅做页面结构解析，不存储、不分发任何内容；所有图文版权归原站与原作者所有。
