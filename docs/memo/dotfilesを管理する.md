---
id: dotfilesを管理する
aliases:
  - dotfilesを管理する
tags: []
created: 2025-10-25
updated: 2025-10-25
---
# dotfilesを管理する

例に漏れず、なんちゃってエンジニアなので、[[dotfiles]]を管理します。

設定ファイルは全てテキストファイルで行われるべきだと思います。

 ## 管理する物

 - Windows
    - Windows terminalのsettings.json
    - windows terminalのprofile
    - nvim
    - yazi
- Linux
    - bash
    - vim
    - nvim
    - yazi
    - tmux

この辺は管理したいですね。

## 運用方法

### リポジトリの作成

1. [[GitHub]]に`dotfiles`という[[リポジトリ]]を作成する
2. 設定ファイルを追加していく

### リポジトリからCloneして実際に使おう

1. [[リポジトリ]]からCloneする
2. 元のファイルを退避させる
    ```bash
    mkdir backup && mv ~/.bashrc backup
    ```
3. [[シンボリックリンク]]を貼る



