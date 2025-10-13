---
id: yazi
aliases:
  - yazi
tags: []
created: 2025-07-17
updated: 2025-07-17
---

# yazi
[[Rust]]製の[[CLI]]ファイルマネージャ[[Vim]]ライクなキーバインドで操作できるのが利点。

## 操作について
基本動作は省略

| キー | 操作 |
| -------------- | --------------- |
| <space>g | cd |
| y | cd pwd で起動 |
| q | cd pwd で終了 |

### 下の二つはPowerShellの設定プロファイルに以下を追加する必要がある。
[[PowerShellの設定プロファイル]]に以下を追加

```ps1
function y {
    $tmp = (New-TemporaryFile).FullName
    yazi $args --cwd-file="$tmp"
    $cwd = Get-Content -Path $tmp -Encoding UTF8
    if (-not [String]::IsNullOrEmpty($cwd) -and $cwd -ne $PWD.Path) {
        Set-Location -LiteralPath (Resolve-Path -LiteralPath $cwd).Path
    }
    Remove-Item -Path $tmp
}

```

## yaziの設定ディレクトリ
```
cd $env:AddData\yazi
```
