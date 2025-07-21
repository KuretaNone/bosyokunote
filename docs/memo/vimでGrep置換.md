---
id: vimでGrep置換
aliases:
  - 一括置換
tags:
  - vim
created: "2025-05-28"
updated: "2025-05-28"
---

## VimでGrep置換

~~~vim
:%s/longint/Integer
u
:args **/*.pas
:set hidden
:argdo %s
G
:argdo w
G
~~~

1. longintをIntegerに変換
2. 戻す
3. バッファに.pasを読み込む
4. バッググラウンドで行うように設定
5. バッファに読み込んだファイルに対して、直線の置換処理を実行(longint→Integer)
6. 一時停止したのを最後まで実行
7. バッファに読み込んだファイルに対して、保存
8. 一時停止したのを最後まで実行

参考
https://qiita.com/noc06140728/items/61380bb0c3cc42d7db3c
