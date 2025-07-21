---
id: 作成したNoteのメタデータに作成日と更新日を付ける
aliases:
  - 作成したNoteのメタデータに作成日と更新日を付ける
tags:
  - Obsidian
created: "2025-05-20"
updated: "2025-05-21"
---

# 作成したNoteのメタデータに作成日と更新日を付ける

[[Obsidian.nvim]]でNoteのメタデータに作成日と更新日を付ける方法を教えてください。

## Obsidianでのメタデータ
Noteの先頭に`---`で囲まれた部分にメタデータを[[yaml]]で記述することができる。

## 作成日と更新日を付ける

[[lazy.nvim]]を使用しているため`lua\plugins\Obsidian.lua`に以下のように記述する。
```bash
cd $env:localappdata\nvim
```

note_frontmatter_funcに
os.time()を使用して作成日と更新日を付けた。
createdとupdatedはyamlのメタデータに記述される。

## 更新日の更新

更新日を更新するには？
*`updated`をメタデータから削除する*

Formatで決まっているメタデータが破損していない限り、一度保存されたメタデータは更新されない。
(`# hgoe`等で新しくTagが生成される、aliasesがなくなる等) 
また、更新されるのは破損しているメタデータ飲みのため、作成日や更新日は更新されない。

メタデータがから更新日を削除すれば、新たに更新日が付与されるのでそれを利用する。
