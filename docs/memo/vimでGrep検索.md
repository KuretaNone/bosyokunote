---
id: vimでGrep検索
aliases: []
tags:
  - vim
created: "2025-05-28"
updated: "2025-05-28"
---
標準のvimの環境で、サクラエディタのようなGrep検索機能がないか確かめる。
:grep {パターン} {ファイル}
は検索結果の使い勝手が悪い

:vimgrepはサブフォルダまで検索してくれない。
Telescope.nvimが提供してくれている。
<Leader>+g で検索できる。

さくらエディタはまだ使い勝手がいい。

