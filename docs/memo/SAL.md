---
id: SAL
aliases:
  - SAL
tags:
  - winapi
created: "2025-05-28"
source: https://learn.microsoft.com/ja-jp/cpp/code-quality/understanding-sal?view=msvc-170
updated: "2025-05-28"
---

# SAL
[[Microsoft]]が考案した、[[ソースコード]]上に記述する注釈のこと。
コンパイル時には無視されるため、他のプラットフォームに移植する際は削除しても問題ない。

例：
```cpp
wchar_t * wmemcpy(
   _Out_writes_all_(count) wchar_t *dest,
   _In_reads_(count) const wchar_t *src,
   size_t count)
{
   size_t i;
   for (i = 0; i <= count; i++) { // BUG: off-by-one error
      dest[i] = src[i];
   }
   return dest;
}
```

`_Out_writes_all_(count)`や、`_In_reads_(count)`が[[SAL]]の注釈である。

