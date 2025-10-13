---
id: markitdownを使ってみる
aliases:
  - markitdownを使ってみる
tags: []
created: "2025-06-03"
updated: "2025-06-03"
---

# markitdownを使ってみる

https://Github.com/microsoft/markitdown

社内資料が大体Office製品を使用してるので、資料を[[Markdown]]で管理するために[[markitdown]]を使ってみる。

## インストール

[[Python]]の仮想環境を作成

```powershell
python -m venv venv
```

仮想環境を有効化
```powershell
venv\Scripts\Activate.ps1
```

MarkItDownをインストール
```powershell
pip install "markitdown[all]"
```

