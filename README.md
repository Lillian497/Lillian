# Jekyll Pretty Blog (Project Page)
自動列出文章 + 分類頁 + 歸檔時間軸 + 美化樣式（assets/main.scss）。

## 部署
1) 把整個資料夾上傳到你的 repo（例如 Lillian）。
2) 編輯 `_config.yml`：
   - `baseurl: "/Lillian"` 改成你的 repo 名稱；如果 repo 叫 `lillian497.github.io`，請改成 `""`。
   - `url: "https://你的使用者名.github.io"` 改成你的使用者頁。
3) Settings → Pages：Branch = main，Folder = /(root)。
4) 開 `https://你的使用者名.github.io/你的repo/`。

## 新增文章
在 `_posts/` 建 `YYYY-MM-DD-my-post.md`：
```markdown
---
layout: post
title: 我的新文章
date: 2025-09-01
categories: [景點]   # 可多個
---

內文...
```
