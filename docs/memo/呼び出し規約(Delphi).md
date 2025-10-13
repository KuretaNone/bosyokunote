---
id: 呼び出し規約(Delphi)
aliases:
  - 呼び出し規約(Delphi)
  - Delphi-呼び出し規約
tags:
  - Delphi
created: "2025-05-28"
updated: "2025-05-28"
---

# Delphi-呼び出し規約
ProcudureやFunctionを宣言する際に呼び出し規約が指定できる。
呼び出し規約によって、ルーチンに引数が渡される順序が決まる。呼び出し規約は、スタックからのパラメータ削除、レジスタを使用したパラメータの受け渡し
エラーや、例外の処理にも影響を及ぼす。デフォルトは`register`。

## 呼び出し規約の種類

| 指令 | パラメータの順序 | クリーンアップの対象 | レジスタ経由のパラメータ渡し |
| --------------- | --------------- | --------------- | --------------- |
| rgister  | 未定義 | ルーチン     | o |
| pascal   | 未定義 | ルーチン     | x |
| cdecl    | 右から左 | 呼び出し側 | x |
| stdcall  | 右から左 | ルーチン   | x |
| safecall | 右から左 | ルーチン   | x |

## 参考文献
https://docwiki.embarcadero.com/RADStudio/Alexandria/ja/%E6%89%8B%E7%B6%9A%E3%81%8D%E3%81%A8%E9%96%A2%E6%95%B0%EF%BC%88Delphi%EF%BC%89
