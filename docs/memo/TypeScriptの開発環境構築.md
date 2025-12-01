---
id: TypeScriptの開発環境構築
aliases:
  - TypeScriptの開発環境構築
tags: []
created: 2025-11-09
updated: 2025-11-09
---

# TypeScriptの開発環境構築

## はじめに

エンジニアのはしくれとして、そろそろ[[TypeScript]]を勉強しようとおもいました。
[[Deno]]で[[TypeScript]]の開発環境を構築します。

## Denoのインストール

[[Denoのインストール]]をします。

[[Deno]]は[[TypeScript]]のランタイム環境を提供しているため、これをインストールすれば、[[TypeScript]]を実行できるようになります。

## nvimからTypeSciptのlspを使用する

機能自体はビルトインの[[LSP]]を利用するので
https://github.com/neovim/nvim-lspconfig から設定例を拝借する

### typescript-language-serverのインストール

```bash
npm install -g typescript-language-server typescript
```
### nvim の設定ファイルの変更

1. `lsp.lua`に以下を追加
    ```diff
    + vim.lsp.enable('ts_ls')
    ```
2. nvim-lspconconfigの'ts_ls.lua'の設定ファイルをlspディレクトリに追加

## プロジェクトの初期化

```bash
deno init my_project
```

## プロジェクトの実行

```bash
cd my_project && deno main.ts
```


## テストの実行

```bash
deno test
```

## 参考
- https://docs.deno.com/runtime/
- https://zenn.dev/uki00a/books/effective-deno/viewer/about
