---
id: Neovimの環境構築
aliases: []
tags: []
created: "2025-05-28"
updated: "2025-05-28"
---

## neovimのダウンロード
wingetからダウンロード
~~~
winget install Neovim.Neovim
~~~

## lazy.vimのダウンロード
Lazy.nvimを導入する前に事前準備が必要になる。

### luarockのダウンロード

### NeedFontのダウンロード
本家NerdFontは日本語に弱いから
HackGenをインストールする。
https://Github.com/yuru7/HackGen

https://lazy.folke.io/
元々あるファイルを移動させる
~~~
Move-Item $env:LOCALAPPDATA\nvim $env:LOCALAPPDATA\nvim.bak  
~~~
~~~
Move-Item $env:LOCALAPPDATA\nvim-data $env:LOCALAPPDATA\nvim-data.bak
~~~

導入方法は本家を見た方が早い。

## other
viで起動したい!
~~~
mkdir %homepath%\bin
~~~
~~~
$ENV:Path+=";%homepath%\binにPath"
~~~
vi.bat
~~~
@echo off
nvim %*
~~~

を設置する。

## ターミナルからWTで起動するときにカレントディレクトリにしたい
Terminalの左下の⚙からSettingJsonに下記を追加
~~~json
{
    "profiles": {
        "defaults": {
            "startingDirectory": "."
        }
    }
}
~~~
