---
id: c-far
aliases:
  - C-Far
tags: []
created: "2025-05-28"
updated: "2025-05-28"
---

# C-Far
## Far
- 遠い
- 遥か

## C言語におけるfar
16bitOSではメモリ空間が64KBしかない。farポインタを使用することで64KB以上のメモリ空間を扱うことができる。
farポインタは、[[セグメント方式]]でメモリ空間を管理する。

### メモリ配置領域指定
関数、変数の宣言時に、far(またはnear)を指定することで、メモリ配置領域を指定することができる。

| キャスト演算子 | サイズ |
| -------------- | --------------- |
| near | 2バイト |
| far | 4バイト |


## 参考文献
https://tool-support.renesas.com/autoupdate/support/onlinehelp/ja-JP/csp/V8.02.00/CS+.chm/Compiler-CCRL.chm/Output/ccrl04c0101y.html
https://tool-support.renesas.com/autoupdate/support/onlinehelp/ja-JP/csp/V8.02.00/CS+.chm/Compiler-CCRL.chm/Output/ccrl04c0206y0003.html#96683
