---
id: MkDocsを使ってサイトを作る
aliases: []
tags: []
created: "2025-06-02"
updated: "2025-06-02"
---

![こんな感じで単語の補完候補が出てくる](res/1748665975.png)

[[Neovim]]上での単語補完

---

私の勤めているところでは、[[Markdown]]形式のメモがそこまで浸透していないので、[[Markdown]]ファイルをそのまま渡すのも何となく気が引けます。
また、画像を挿入したりしている場合はその画像も一緒に渡す必要があり、単一ファイルで完結しないにも面倒です。

かといって、書いたメモをPDFに変換するにも、[[MarkdownからPDF変換時に改ページを挿入]]しなおしたり、体裁を整える。必要があります。
これも面倒です。

というか、そもそも[[Markdown]]は[[HTML]]に変換することを目的とした[[マークアップ言語]]なので、共有するなら、[[HTML]]にすればええやん。と思いました。

## MarkdownをHTMLに変換しよう。

前述したとおり、[[Markdown]]は、[[HTML]]に変換することを目的とした[[マークアップ言語]]です。

今回は[[MkDocs]]というツールを使います。

どうして[[MkDocs]]を使うのかというと
[Minerva](https://minerva.mamansoft.net/Home)の[MkDocsでObsidianと互換性の高いドキュメントベースを実現する](https://minerva.mamansoft.net/%F0%9F%93%98Articles/%F0%9F%93%98MkDocs%E3%81%A7Obsidian%E3%81%A8%E4%BA%92%E6%8F%9B%E6%80%A7%E3%81%AE%E9%AB%98%E3%81%84%E3%83%89%E3%82%AD%E3%83%A5%E3%83%A1%E3%83%B3%E3%83%88%E3%83%99%E3%83%BC%E3%82%B9%E3%82%92%E5%AE%9F%E7%8F%BE%E3%81%99%E3%82%8B)の記事を拝読したからです。

なのでほぼ100記事の内容を使用しています。

(faviconの設定や簡単な設定は変更しています。)

なので、使用する環境は記事が提供しているものとおなじものとします。

強いていえば、記事内で提供されていた。[一発で環境構築するシェル](https://minerva.mamansoft.net/%F0%9F%93%98Articles/%F0%9F%93%98MkDocs%E3%81%A7Obsidian%E3%81%A8%E4%BA%92%E6%8F%9B%E6%80%A7%E3%81%AE%E9%AB%98%E3%81%84%E3%83%89%E3%82%AD%E3%83%A5%E3%83%A1%E3%83%B3%E3%83%88%E3%83%99%E3%83%BC%E3%82%B9%E3%82%92%E5%AE%9F%E7%8F%BE%E3%81%99%E3%82%8B#%E4%B8%80%E7%99%BA%E3%81%A7%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E3%81%99%E3%82%8B%E3%82%B7%E3%82%A7%E3%83%AB)
を[[PowerShell]]で実行できるように書き換えたくらいです。

## 前提

- [[Git]]
- [[Python]] 

上記がインストールされていること。

## 環境構築

細かい設定を羅列しても[MkDocsでObsidianと互換性の高いドキュメントベースを実現する](https://minerva.mamansoft.net/%F0%9F%93%98Articles/%F0%9F%93%98MkDocs%E3%81%A7Obsidian%E3%81%A8%E4%BA%92%E6%8F%9B%E6%80%A7%E3%81%AE%E9%AB%98%E3%81%84%E3%83%89%E3%82%AD%E3%83%A5%E3%83%A1%E3%83%B3%E3%83%88%E3%83%99%E3%83%BC%E3%82%B9%E3%82%92%E5%AE%9F%E7%8F%BE%E3%81%99%E3%82%8B)の二の舞になるので、詳細はこちらを参考してください。

以下を`.ps1`で保存し[[PowerShell]]から実行をすれば[[Windows]]でも、環境構築ができます。

```powershell
Set-StrictMode -Version Latest
$ErrorActionPreference = 'Stop'

New-Item -ItemType Directory -Path "Mkdocs-Sample" -Force | Out-Null
Set-Location "Mkdocs-Sample"

New-Item -ItemType Directory -Path "docs" -Force | Out-Null

@"
site_name: Mkdocs-Sample
strict: true
use_directory_urls: false
# TODO: site_url: これを設定しないと静的デプロイしたサイトでは有効にならない
theme:
  name: material
  icon:e
    logo: material/file
    repo: material/github
  features:
    - navigation.instant
    - navigation.instant.progress
    - content.code.copy
  palette:
    - media: "(prefers-color-scheme: light)"
      scheme: default
      primary: dark-blue  # ライトテーマ時の色
      toggle:
        icon: material/weather-night
        name: ダークモードに切り替え
    - media: "(prefers-color-scheme: dark)"
      scheme: slate
      primary: dark blue       # ダークテーマ時の色
      toggle:
        icon: material/weather-sunny
        name: ライトモードに切り替え

plugins:
  - obsidian-bridge
  - awesome-nav
  - glightbox
  - search:
      lang: ja
  - backlinks_section:
      title: "🖇️ Backlinks"
      description: ""
      add_to_toc: false
      hide_if_empty: true
  - git-revision-date-localized:
      strict: false
      enable_creation_date: true
      locale: ja
      timezone: Asia/Tokyo

markdown_extensions:
  - footnotes
  - md_in_html
  - obsidian_callouts
  - pymdownx.magiclink
  - pymdownx.snippets:
      check_paths: true
      base_path: docs
  - pymdownx.superfences:
      custom_fences:
        - name: mermaid
          class: mermaid
  - pymdownx.tasklist:
      custom_checkbox: true
  - pymdownx.tabbed:
      alternate_style: true
"@ | Set-Content -Encoding UTF8 "mkdocs.yml"

@"
mkdocs
mkdocs-material
# WARNINGが出なくなったらこちらを使う
# mkdocs-obsidian-bridge
git+https://github.com/tadashi-aikawa/mkdocs-obsidian-bridge
mkdocs-awesome-nav
mkdocs-backlinks-section-plugin
mkdocs-git-revision-date-localized-plugin
mkdocs-git-authors-plugin
mkdocs-glightbox
"@ | Set-Content -Encoding UTF8 "requirements.txt"

@"
nav:
  - index.md
"@ | Set-Content -Encoding UTF8 "docs/.nav.yml"

@"
Hello Mks & Obsidian !!

- [[サンプル]]
"@ | Set-Content -Encoding UTF8 "docs/index.md"

@"
## Callout

> [!info]
> INFOのCallout
"@ | Set-Content -Encoding UTF8 "docs/サンプル.md"

git init && git add . && git commit -m "Initial commit"
python -m venv .venv
. .\.venv\Scripts\Activate.ps1
python.exe -m pip install --upgrade pip
pip install -r requirements.txt
```

## 作成したMarkdownをMkDocsでHTMLに変換する

先ほどのスクリプトを実行すると、`docs`フォルダが作成されます。そこに[[Markdown]]ファイルを配置していきます。

ファイルを配置したら、以下のコマンドを実行します。

> [!NOTE]
> pyrhonの仮想環境を有効にしてから実行してください。

```PowerShell
mkdocs build
```

このコマンドを実行すると、`site`フォルダが作成され、その中にHTMLファイルが生成されます。

## サーバーにアップロードする。

生成された`site`フォルダを[[XServer]]などの[[サーバー]]にアップロードします。
現状は以下の手順で更新をしています。

1. [[サーバー管理画面からFTPアカウントの設定をする]]
2. [[WinScp]]を利用して`site`フォルダを`public_html`フォルダにアップロードする。

![1748679476.png](res/1748679476.png)

もっと効率的な方法があればそっちに移行したい。

## さいごに

[[MkDocs]]を使うことで、[[Markdown]]で書いたメモを簡単に[[HTML]]に変換して、[[サーバー]]にアップロードすることができました。

KuretaNone.netはこのようにして作成をしています。
