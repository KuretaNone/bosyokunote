---
id: 画像がresフォルダに保存されない
aliases:
  - 画像がresフォルダに保存されない
tags: []
created: "2025-05-30"
updated: "2025-05-30"
---

# 画像がresフォルダに保存されない

[[obsidian.nvim]]で画像を挿入する際に`:ObsidianPasteImg`を実行しても画像が`res`フォルダに保存されない。

## 原因

これは勘違い。`site`フォルダ内の`res`フォルダを参照していた。

実際は`docs`フォルダ内の`res`フォルダに保存されている。
