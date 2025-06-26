---
id: Claude Codeのインストール
aliases:
  - Claude Codeのインストール
tags: []
created: "2025-06-20"
updated: "2025-06-20"
---

# Claude Codeのインストール

https://docs.anthropic.com/ja/docs/claude-code/getting-started
を参考に[[Windows]]環境でのインストール手順をまとめる。
## 環境構築

[[Windows]]で[[Claude Code]]を動かすのに必要な環境は以下の二つ。

1. [[WSL]]([[Ubuntu]]20.04+)
2. [[Node.js]] 18.x以上

## WSLのインストール

[[WSLをインストール]]を参照。

> [!NOTE]
> セットアップが完了したらPCを再起動
> ここからは[[WSL]]上の[[Ubuntu]]環境の作業

## Node.jsのインストール

[[Node.js]]をインストールする。

> [!NOTE]
> [[Windows]]ですでに[[Node.js]]がインストールされている場合は、[[nvm]]経由で[[Node.js]]をインストールする必要がある。

そのため、まずは[[nvm]]をインストールする。

### nvmのインストール

https://github.com/nvm-sh/nvm
を参考に、以下のコマンドを実行する。
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
```
新しいシェルに置き換え
```bash
exec $SHELL
```

### nvmからNode.jsをインストール

```bash
nvm install 22
nvm use 22
nvm alias default 22
```
## Claude Codeのインストール

```bash
npm install -g @anthropic-ai/claude-code
```

## 初期設定
まずは起動

```bash
claude
```

### styleの選択
キモオタクなので、以下からDark modeを選択

1. Dark mode
2. Light mode
3. Dark mode (colorblind-friendly)
4. Light mode (colorblind-friendly)
5. Dark mode (ANSI colors only)
6. Light mode (ANSI colors only)

### アカウント、APIキーの設定
Enterを押してるとURLが表示されるので接続して[[Anthropic]]のアカウントへログイン。
コードが表示されるので、コピペ

### 注意書き    

以下は適当な日本語訳

1. Claudeはミスをします。
2. リスクがあるから信頼できるツールを使用しよう。

## まとめ
[[nvm]]経由でインストールするってわかってたらもっと早く終わってたのに。  
[公式のチュートリアル](https://docs.anthropic.com/ja/docs/claude-code/tutorials)
を参考に始めようかな。
