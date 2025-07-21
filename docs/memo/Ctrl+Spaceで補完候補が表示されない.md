---
id: Ctrl+Spaceで補完候補が表示されない
aliases:
  - Ctrl+Spaceで補完候補が表示されない
tags: []
created: 2025-07-21
updated: 2025-07-21
---

# Ctrl+Spaceで補完候補が表示されない
設定には下記を追加している。
```lua
return {
    'saghen/blink.cmp',
    opts = {
        -- https://cmp.saghen.dev/configuration/keymap.html
        keymap = {
            preset = "enter",
            ['<C-space>'] = { 'show', 'show_documentation', 'hide_documentation' },
        },
    },
},
```

## 解決策
調べたけどよくわからない。
