---
id: Build時の警告を解決する
aliases:
  - Build時の警告を解決する
  - MkDocs Buildのエラーを解決する
tags: []
created: "2025-06-01"
updated: "2025-06-01"
---

# MkDocs Buildのエラーを解決する

[[MkDocs]]で`Build`コマンドを実行したとき、以下のようにログが出力されます。

いくつかWARNIGが出力されているので、これらを極力解決していきます。


<details>
<summary>ログ</summary>

```bash
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\IPアドレス.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\LYT.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.プログラミング言語Bu
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\LaTeX.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find CSS.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find 表のalignを指定する.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find ファイル内リンクを設定する.md in directory D:\KuretaNone\docs
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\Markdown.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
INFO    -  Doc file 'memo/Markdown.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'memo/Markdown.md' contains an unrecognized relative link 'CSS', it was left as is.
INFO    -  Doc file 'memo/Markdown.md' contains an unrecognized relative link
           '%E8%A1%A8%E3%81%AEalign%E3%82%92%E6%8C%87%E5%AE%9A%E3%81%99%E3%82%8B', it was left as is.
INFO    -  Doc file 'memo/Markdown.md' contains an unrecognized relative link
           '%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E5%86%85%E3%83%AA%E3%83%B3%E3%82%AF%E3%82%92%E8%A8%AD%E5%AE%9A%E3%81%99%E3%82%8B',
           it was left as is.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\MarkdownからPDF変換時に改ページを挿入.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\Microsoft.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING -  [ObsidianBridgePlugin] Unable to find Python.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find 静的サイト.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find YAML.md in directory D:\KuretaNone\docs
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\MkDocs.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
INFO    -  Doc file 'memo/MkDocs.md' contains an unrecognized relative link 'Python', it was left as is.
INFO    -  Doc file 'memo/MkDocs.md' contains an unrecognized relative link
           '%E9%9D%99%E7%9A%84%E3%82%B5%E3%82%A4%E3%83%88', it was left as is.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\Neovim.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\Obsidian.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\PDF.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\PKM.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING -  [ObsidianBridgePlugin] Unable to find コマンドラインシェル.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find スクリプト言語.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Linux.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find macOS.md in directory D:\KuretaNone\docs
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\PowerShell.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link
           '%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%83%A9%E3%82%A4%E3%83%B3%E3%82%B7%E3%82%A7%E3%83%AB', it was
           left as is.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link
           '%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%97%E3%83%88%E8%A8%80%E8%AA%9E', it was left as is.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link 'Linux', it was left as is.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link 'macOS', it was left as is.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\TeX.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\WinScp.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\XServer.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\Zettelkasten.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\css.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\fork.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING -  [ObsidianBridgePlugin] Unable to find obsidian.md in directory D:\KuretaNone\docs
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\obsidian.nvim.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
INFO    -  Doc file 'memo/obsidian.nvim.md' contains an unrecognized relative link 'obsidian', it was left as is.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\vim.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING -  [ObsidianBridgePlugin] Unable to find OS.md in directory D:\KuretaNone\docs
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\windows.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
INFO    -  Doc file 'memo/windows.md' contains an unrecognized relative link 'OS', it was left as is.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\アラート記法.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\サイト.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\サーバー.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\ソフトウェア.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\ドメイン.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\ハードウェア.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING -  [ObsidianBridgePlugin] Unable to find html.md in directory D:\KuretaNone\docs
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\マークアップ言語.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
INFO    -  Doc file 'memo/マークアップ言語.md' contains an unrecognized relative link 'html', it was left as is.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\折り畳みを挿入する.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\数式(LaTeX)を表現する.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\暮田のん.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\画像がresフォルダに保存されない.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\組版.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page note\KuretaNoneで解決したい問題.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING -  [ObsidianBridgePlugin] Unable to find Obsidian.nvim.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find neovim.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find git.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Python.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find markdown.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING:root:First revision timestamp is older than last revision timestamp for page note\Mkdocsを使ってサイトを作ろう.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains a link 'Obsidian.nvim', but the target
           'note/Obsidian.nvim' is not found among documentation files.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'neovim', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'git', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'Python', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'markdown', it was left as
           is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'HTML', it was left as is.
WARNING -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains a link 'KuretaNone.net', but the target
           'note/KuretaNone.net' is not found among documentation files.
WARNING -  [ObsidianBridgePlugin] Unable to find Xserver.md in directory D:\KuretaNone\docs
WARNING:root:First revision timestamp is older than last revision timestamp for page note\サーバー管理画面からFTPアカウントの設定をする.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
INFO    -  Doc file 'note/サーバー管理画面からFTPアカウントの設定をする.md' contains an unrecognized relative link 'Xserver', it was
           left as is.
WARNING:root:First revision timestamp is older than last revision timestamp for page note\マカフィーリブセーフを削除したい.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find html.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find javascript.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING:root:First revision timestamp is older than last revision timestamp for page note\生き恥をさらす場所を作ろう.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net'
           is not found among documentation files.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net'
           is not found among documentation files.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net'
           is not found among documentation files.
INFO    -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains an unrecognized relative link 'html', it was left as is.
INFO    -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains an unrecognized relative link 'javascript', it was left as is.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net'
           is not found among documentation files.
```

</details>

## 問題の分類

ログをソートして、問題を分類します。

1. 複数行にわたる警告統合する
2. ソートする

<details>
<summary>整理ソートしたログ</summary>

```bash
INFO    -  Doc file 'memo/Markdown.md' contains an unrecognized relative link '%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E5%86%85%E3%83%AA%E3%83%B3%E3%82%AF%E3%82%92%E8%A8%AD%E5%AE%9A%E3%81%99%E3%82%8B', it was left as is.
INFO    -  Doc file 'memo/Markdown.md' contains an unrecognized relative link '%E8%A1%A8%E3%81%AEalign%E3%82%92%E6%8C%87%E5%AE%9A%E3%81%99%E3%82%8B', it was left as is.
INFO    -  Doc file 'memo/Markdown.md' contains an unrecognized relative link 'CSS', it was left as is.
INFO    -  Doc file 'memo/Markdown.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'memo/MkDocs.md' contains an unrecognized relative link '%E9%9D%99%E7%9A%84%E3%82%B5%E3%82%A4%E3%83%88', it was left as is.
INFO    -  Doc file 'memo/MkDocs.md' contains an unrecognized relative link 'Python', it was left as is.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link '%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%83%A9%E3%82%A4%E3%83%B3%E3%82%B7%E3%82%A7%E3%83%AB', it was left as is.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link '%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%97%E3%83%88%E8%A8%80%E8%AA%9E', it was left as is.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link 'Linux', it was left as is.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link 'macOS', it was left as is.
INFO    -  Doc file 'memo/obsidian.nvim.md' contains an unrecognized relative link 'obsidian', it was left as is.
INFO    -  Doc file 'memo/windows.md' contains an unrecognized relative link 'OS', it was left as is.
INFO    -  Doc file 'memo/マークアップ言語.md' contains an unrecognized relative link 'html', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'Python', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'git', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'markdown', it was left as is.
INFO    -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains an unrecognized relative link 'neovim', it was left as is.
INFO    -  Doc file 'note/サーバー管理画面からFTPアカウントの設定をする.md' contains an unrecognized relative link 'Xserver', it was left as is.
INFO    -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains an unrecognized relative link 'html', it was left as is.
INFO    -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains an unrecognized relative link 'javascript', it was left as is.
WARNING -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains a link 'Obsidian.nvim', but the target 'note/Obsidian.nvim' is not found among documentation files.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  [ObsidianBridgePlugin] Unable to find CSS.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Linux.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find OS.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Obsidian.nvim.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Python.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Python.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Xserver.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find YAML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find git.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find html.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find html.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find javascript.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find macOS.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find markdown.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find neovim.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find obsidian.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find コマンドラインシェル.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find スクリプト言語.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find ファイル内リンクを設定する.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find 表のalignを指定する.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find 静的サイト.md in directory D:\KuretaNone\docs
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\IPアドレス.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\LYT.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\LaTeX.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\Markdown.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\MarkdownからPDF変換時に改ページを挿入.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\Microsoft.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\MkDocs.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\Neovim.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\Obsidian.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\PDF.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\PKM.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\PowerShell.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\TeX.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\WinScp.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\XServer.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\Zettelkasten.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\css.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\fork.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\obsidian.nvim.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\vim.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\windows.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\アラート記法.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\サイト.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\サーバー.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\ソフトウェア.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\ドメイン.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\ハードウェア.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\マークアップ言語.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\折り畳みを挿入する.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\数式(LaTeX)を表現する.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\暮田のん.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\画像がresフォルダに保存されない.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\組版.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page note\KuretaNoneで解決したい問題.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page note\Mkdocsを使ってサイトを作ろう.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page note\サーバー管理画面からFTPアカウントの設定をする.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page note\マカフィーリブセーフを削除したい.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
WARNING:root:First revision timestamp is older than last revision timestamp for page note\生き恥をさらす場所を作ろう.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
```

</details>

ソートするとわかりやすいですね。
大きく分けて以下の4種類の情報があります。

```bash
INFO    -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains an unrecognized relative link 'javascript', it was left as is.
WARNING -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  [ObsidianBridgePlugin] Unable to find CSS.md in directory D:\KuretaNone\docs
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\IPアドレス.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
```

私は英語が読めないので、AIに聞きましょう。

以下、AIによる解答

---

### ✅ `INFO` メッセージ

```
INFO    -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains an unrecognized relative link 'javascript', it was left as is.
```

- **意味**：`生き恥をさらす場所を作ろう.md` という Markdown ファイル内に、`[リンク名](javascript)` のようなリンクがありました。
- **問題点**：`javascript` は相対リンクとしては認識されないため、そのままにされています。
- **対応策**：
  - 明示的に JavaScript を使いたいリンクであれば問題ありません。
  - もし意図しない文字列なら、リンク先を修正しましょう。

### ⚠️ `WARNING` メッセージ（リンク切れ）

```
WARNING -  Doc file 'note/Mkdocsを使ってサイトを作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
```

* **意味**：Markdown ファイル内に `[リンク名](note/KuretaNone.net)` のようなリンクがありますが、対象ファイルが見つかりません。
* **対応策**：
  * 実際に `note/KuretaNone.net.md` など該当ファイルが存在するか確認。
  * 拡張子のミスやファイルの削除、名前の変更の可能性があります。

### ⚠️ `WARNING` メッセージ（CSSファイルが見つからない）

```
WARNING -  [ObsidianBridgePlugin] Unable to find CSS.md in directory D:\KuretaNone\docs
```

* **意味**：`CSS.md` というファイルを `D:\KuretaNone\docs` フォルダ内に探しましたが見つかりませんでした。
* **原因**：ObsidianBridgePlugin などのプラグインがリンクされたファイルを探す際に発生することがあります。
* **対応策**：
  * `CSS.md` が実際に存在するか、パスが正しいか確認してください。

### ⚠️ `WARNING:root:` メッセージ（Gitのタイムスタンプ矛盾）

```
WARNING:root:First revision timestamp is older than last revision timestamp for page memo\IPアドレス.md. This can be due to a quirk in `git` follow behaviour. You can try to set `enable_git_follow: false` in the plugin configuration.
```

* **意味**：Git プラグインが `memo\IPアドレス.md` の変更履歴をたどる際、最初のリビジョンのタイムスタンプが最後のリビジョンよりも新しくなってしまったという矛盾を検出しました。
* **原因**：`git log --follow` の仕様により、ファイルのリネームや移動を追跡する際にこうした矛盾が起こることがあります。
* **対応策**：
  * `mkdocs.yml` のプラグイン設定で `enable_git_follow: false` を指定して `--follow` の使用を無効にすることで解消できる場合があります。

## AIの解説を受けて

infoは僕の怠慢による[[デッドリンク]]なのでその単語の自分の理解をするmemoを作成すればいいのですね。
これは[[KuretaNoneで解決したい問題]]にも書いてある問題です。

ほかの二つもリンク切れ関連っぽいですね

最後だけ、Gitプラグインが関連してるみたいです。

こういう時に自分にある程度最初に環境が出来上がっているものを使用するとなんのためのプラグインかわからなくなりますよね。

まぁ、今回の場合は作成日と変更日を表示してるのでその関連だと思います。

## 対策

[[デッドリンク]]は気合でどうにかします…なんか説明しようとすると壮大なコンテンツだと大変だよね。

gitの方は最初に[[MkDocsを使ってサイトを作る]]時に最初にコミットしていこう一度も差分を取ってない私の怠慢が原因ですね。

[[lazygit]]を使用しているのでこちらでコミットしていきましょう

![1748870040.png](res/1748870040.png)

本当は[[GitHub]]のプライベートリポジトリとかにプッシュしておく方がいいですね。

これはまたいつの日か…

## 実践

さっきの画像でわかる通り、いったんGitに差分をコミットしてみました。

<details>
<summary>整理ソートしたログ</summary>

```bash
INFO    -  Doc file 'index.md' contains an unrecognized relative link 'Mkdocs%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%A6%E3%82%B5%E3%82%A4%E3%83%88%E3%82%92%E4%BD%9C%E3%82%8D%E3%81%86', it was left as is.
INFO    -  Doc file 'memo/Build時の警告を解決する.md' contains an unrecognized relative link 'Kure%5B%5BKuretaNone%E3%81%A7%E8%A7%A3%E6%B1%BA%E3%81%97%E3%81%9F%E3%81%84%E5%95%8F%E9%A1%8C', it was left as is.
INFO    -  Doc file 'memo/Build時の警告を解決する.md' contains an unrecognized relative link 'Mkdocs%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%A6%E3%82%B5%E3%82%A4%E3%83%88%E3%82%92%E4%BD%9C%E3%82%8B', it was left as is.
INFO    -  Doc file 'memo/Build時の警告を解決する.md' contains an unrecognized relative link 'lazygit', it was left as is.
INFO    -  Doc file 'memo/Markdown.md' contains an unrecognized relative link '%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E5%86%85%E3%83%AA%E3%83%B3%E3%82%AF%E3%82%92%E8%A8%AD%E5%AE%9A%E3%81%99%E3%82%8B', it was left as is.
INFO    -  Doc file 'memo/Markdown.md' contains an unrecognized relative link '%E8%A1%A8%E3%81%AEalign%E3%82%92%E6%8C%87%E5%AE%9A%E3%81%99%E3%82%8B', it was left as is.
INFO    -  Doc file 'memo/Markdown.md' contains an unrecognized relative link 'CSS', it was left as is.
INFO    -  Doc file 'memo/Markdown.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'memo/MkDocs.md' contains an unrecognized relative link '%E9%9D%99%E7%9A%84%E3%82%B5%E3%82%A4%E3%83%88', it was left as is. WARNING -  [ObsidianBridgePlugin] Unable to find コマンドラインシェル.md in directory D:\KuretaNone\docs WARNING -  [ObsidianBridgePlugin] Unable to find スクリプト言語.md in directory D:\KuretaNone\docs
INFO    -  Doc file 'memo/MkDocs.md' contains an unrecognized relative link 'Python', it was left as is.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link '%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%83%A9%E3%82%A4%E3%83%B3%E3%82%B7%E3%82%A7%E3%83%AB', it was left as is.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link '%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%97%E3%83%88%E8%A8%80%E8%AA%9E', it was left as is.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link 'Linux', it was left as is.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link 'macOS', it was left as is.
INFO    -  Doc file 'memo/obsidian.nvim.md' contains an unrecognized relative link 'obsidian', it was left as is.
INFO    -  Doc file 'memo/windows.md' contains an unrecognized relative link 'OS', it was left as is.
INFO    -  Doc file 'memo/マークアップ言語.md' contains an unrecognized relative link 'html', it was left as is.
INFO    -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains an unrecognized relative link 'HTML', it was left as is.
INFO    -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains an unrecognized relative link 'Python', it was left as is.
INFO    -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains an unrecognized relative link 'git', it was left as is.
INFO    -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains an unrecognized relative link 'markdown', it was left as is.
INFO    -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains an unrecognized relative link 'neovim', it was left as is.
INFO    -  Doc file 'note/サーバー管理画面からFTPアカウントの設定をする.md' contains an unrecognized relative link 'Xserver', it was left as is.
INFO    -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains an unrecognized relative link 'html', it was left as is.
INFO    -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains an unrecognized relative link 'javascript', it was left as is.
WARNING -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains a link 'Obsidian.nvim', but the target 'note/Obsidian.nvim' is not found among documentation files.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  [ObsidianBridgePlugin] Unable to find CSS.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find HTML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Kure[[KuretaNoneで解決したい問題.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Linux.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Mkdocsを使ってサイトを作る.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Mkdocsを使ってサイトを作ろう.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find OS.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Obsidian.nvim.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Python.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Python.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Xserver.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find YAML.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find git.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find html.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find html.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find javascript.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find lazygit.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find macOS.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find markdown.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find neovim.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find obsidian.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find ファイル内リンクを設定する.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find 表のalignを指定する.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find 静的サイト.md in directory D:\KuretaNone\docs
```

</details>

timestampに関する警告は出てこなくなりましたね☻

次に、リンク先が見つからないのを必死に解決します。

今度は全文見ていきましょう。
<details>
<summary>全文</summary>

```bash
INFO    -  [22:52:00] Detected file changes
INFO    -  Building documentation...
INFO    -  The following pages exist in the docs directory, but are not included in the "nav" configuration:
             - memo\Build時の警告を解決する.md
             - memo\Git.md
             - memo\HTML.md
             - memo\IPアドレス.md
             - memo\JavaScript.md
             - memo\LYT.md
             - memo\LaTeX.md
             - memo\Markdown.md
             - memo\MarkdownからPDF変換時に改ページを挿入.md
             - memo\Microsoft.md
             - memo\MkDocs.md
             - memo\Neovim.md
             - memo\Obsidian.md
             - memo\PDF.md
             - memo\PKM.md
             - memo\PowerShell.md
             - memo\Python.md
             - memo\TeX.md
             - memo\Unix.md
             - memo\WinScp.md
             - memo\XServer.md
             - memo\YAML.md
             - memo\Zettelkasten.md
             - memo\css.md
             - memo\fork.md
             - memo\lazygit.md
             - memo\macOS.md
             - memo\obsidian.nvim.md
             - memo\os.md
             - memo\vim.md
             - memo\windows.md
             - memo\アラート記法.md
             - memo\サイト.md
             - memo\サーバー.md
             - memo\ソフトウェア.md
             - memo\デッドリンク.md
             - memo\ドメイン.md
             - memo\ハードウェア.md
             - memo\ファイル内リンクを設定する.md
             - memo\マークアップ言語.md
             - memo\折り畳みを挿入する.md
             - memo\数式(LaTeX)を表現する.md
             - memo\暮田のん.md
             - memo\画像がresフォルダに保存されない.md
             - memo\組版.md
             - memo\表のalignを指定する.md
WARNING -  [ObsidianBridgePlugin] Unable to find Mkdocsを使ってサイトを作ろう.md in directory D:\KuretaNone\docs
INFO    -  Doc file 'index.md' contains an unrecognized relative link 'Mkdocs%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%A6%E3%82%B5%E3%82%A4%E3%83%88%E3%82%92%E4%BD%9C%E3%82%8D%E3%81%86', it was left as is.
WARNING -  [ObsidianBridgePlugin] Unable to find Kure[[KuretaNoneで解決したい問題.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Mkdocsを使ってサイトを作る.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find GitHub.md in directory D:\KuretaNone\docs
INFO    -  Doc file 'memo/Build時の警告を解決する.md' contains an unrecognized relative link 'Kure%5B%5BKuretaNone%E3%81%A7%E8%A7%A3%E6%B1%BA%E3%81%97%E3%81%9F%E3%81%84%E5%95%8F%E9%A1%8C', it was left as is.
INFO    -  Doc file 'memo/Build時の警告を解決する.md' contains an unrecognized relative link 'Mkdocs%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%A6%E3%82%B5%E3%82%A4%E3%83%88%E3%82%92%E4%BD%9C%E3%82%8B', it was left as is.
INFO    -  Doc file 'memo/Build時の警告を解決する.md' contains an unrecognized relative link 'GitHub', it was left as is.
WARNING -  [ObsidianBridgePlugin] Unable to find プログラミング言語.md in directory D:\KuretaNone\docs
INFO    -  Doc file 'memo/JavaScript.md' contains an unrecognized relative link '%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9F%E3%83%B3%E3%82%B0%E8%A8%80%E8%AA%9E', it was left as is.
WARNING -  [ObsidianBridgePlugin] Unable to find CSS.md in directory D:\KuretaNone\docs
INFO    -  Doc file 'memo/Markdown.md' contains an unrecognized relative link 'CSS', it was left as is.
WARNING -  [ObsidianBridgePlugin] Unable to find 静的サイト.md in directory D:\KuretaNone\docs
INFO    -  Doc file 'memo/MkDocs.md' contains an unrecognized relative link '%E9%9D%99%E7%9A%84%E3%82%B5%E3%82%A4%E3%83%88', it was left as is.
WARNING -  [ObsidianBridgePlugin] Unable to find コマンドラインシェル.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find スクリプト言語.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find Linux.md in directory D:\KuretaNone\docs
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link '%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%83%A9%E3%82%A4%E3%83%B3%E3%82%B7%E3%82%A7%E3%83%AB', it was left as is.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link '%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%97%E3%83%88%E8%A8%80%E8%AA%9E', it was left as is.
INFO    -  Doc file 'memo/PowerShell.md' contains an unrecognized relative link 'Linux', it was left as is.
WARNING -  [ObsidianBridgePlugin] Unable to find TUI.md in directory D:\KuretaNone\docs
INFO    -  Doc file 'memo/lazygit.md' contains an unrecognized relative link 'TUI', it was left as is.
WARNING -  [ObsidianBridgePlugin] Unable to find OS.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find OS.md in directory D:\KuretaNone\docs
INFO    -  Doc file 'memo/macOS.md' contains an unrecognized relative link 'OS', it was left as is.
INFO    -  Doc file 'memo/macOS.md' contains an unrecognized relative link 'OS', it was left as is.
WARNING -  [ObsidianBridgePlugin] Unable to find obsidian.md in directory D:\KuretaNone\docs
INFO    -  Doc file 'memo/obsidian.nvim.md' contains an unrecognized relative link 'obsidian', it was left as is.
WARNING -  [ObsidianBridgePlugin] Unable to find html.md in directory D:\KuretaNone\docs
INFO    -  Doc file 'memo/マークアップ言語.md' contains an unrecognized relative link 'html', it was left as is.
WARNING -  [ObsidianBridgePlugin] Unable to find Obsidian.nvim.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find neovim.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find git.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find markdown.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains a link 'Obsidian.nvim', but the target 'note/Obsidian.nvim' is not found among documentation files.
INFO    -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains an unrecognized relative link 'neovim', it was left as is.
INFO    -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains an unrecognized relative link 'git', it was left as is.
INFO    -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains an unrecognized relative link 'markdown', it was left as is.
WARNING -  Doc file 'note/MkDocsを使ってサイトを作る.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  [ObsidianBridgePlugin] Unable to find Xserver.md in directory D:\KuretaNone\docs
INFO    -  Doc file 'note/サーバー管理画面からFTPアカウントの設定をする.md' contains an unrecognized relative link 'Xserver', it was left as is.
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find html.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find javascript.md in directory D:\KuretaNone\docs
WARNING -  [ObsidianBridgePlugin] Unable to find KuretaNone.net.md in directory D:\KuretaNone\docs
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
INFO    -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains an unrecognized relative link 'html', it was left as is.
INFO    -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains an unrecognized relative link 'javascript', it was left as is.
WARNING -  Doc file 'note/生き恥をさらす場所を作ろう.md' contains a link 'KuretaNone.net', but the target 'note/KuretaNone.net' is not found among documentation files.
INFO    -  Documentation built in 6.78 seconds
INFO    -  [22:52:07] Reloading browsers
```

う～～～～これは、リンク切れ、というより大文字小文字の違いっぽいですね。厳密に書いていきましょうか。
あとはnavにメモフォルダを指定してないので、追加しておきます(単語の羅列は正直邪魔かなって思うので、含めていませんでした。)
`.`が含まれるファイルに関しては現在もどうやって解決すればいいのかわからないので、いったん保留

## まとめ

文章を書くときの僕のいい加減さがわかるいい例でしたね。

ちなみに、`mkdocs.yml`の設定で`strict: true`にしておくと`mkdocs build`の時にリンク切れを検出してくれるので、そちらを有効にしておくといいでしょう。

> [!NOTE]
> 最初'mkdocs serve'実行時にエラーで止まってばかりで、[[MkDocs]]を使用したときの雰囲気がわからなったでfalseにしてた。

```yaml
strict: true
```
