---
id: ローカルのGitリポジトリにリモートリポジトリを追加
aliases:
  - ローカルのGitリポジトリにリモートリポジトリを追加
tags: []
created: "2025-06-17"
updated: "2025-06-17"
---


# ローカルのGitリポジトリにリモートリポジトリを追加
KuretaNone.netはローカルの[[リポジトリ]]を使って管理しています。
[[GitHub]]に挙げるべく、リモートリポジトリを作成し、ローカルのGitリポジトリをそこにプッシュできるようにします。

## GitHubにリモートリポジトリを作成する。

https://github.com/new

上記アクセスして、リポジトリを作成します。

- Repository name
    リポジトリ名。今回はKuretaNone.netにします。
- Description (optional)
    リポジトリの説明。今回は「KuretaNone.netのソースコードを管理するリポジトリ」ということで、
- 公開範囲の設定
    今回は公開するのでPublicを選択します。

ライセンスや、readme, .gitignoreの設定は今回は行いません。

> [!NOTE]
> ライセンスについての知見がないから、今度調べて設定します。

readmeは別に要らないかなと思います。  
.gitignoreはローカルにすでにあるので、今回は設定しません。  
リポジトリを作成したら、以下のような画面が表示されます。  

![1750176629.png](res/1750176629.png)

今回は下の`..or push an existing repository from the command line`  
和訳すると「既存のリポジトリをコマンドラインからプッシュする」が該当します。

## ..orpush an existing repository from the command line

ローカルにすでにあるリポジトリをGitHubにプッシュするためのコマンドが表示されます。
ローカルのリポジトリに移動して以下のコマンドを実行します。
```bash
cd d:
cd KuretaNone
```
```bash
git remote add origin https://github.com/KuretaNone/KuretaNone.net.git
```
```bash
git branch -M main
```
```bash
git push -u origin main
```

## 追加後
最後のコマンドを実行後しばらくすると先ほど作成したリポジトリにプッシュされます。
```
PS D:\KuretaNone> git push -u origin main
Enumerating objects: 640, done.
Counting objects: 100% (640/640), done.
Delta compression using up to 16 threads
Compressing objects: 100% (342/342), done.
Writing objects: 100% (640/640), 224.94 MiB | 4.66 MiB/s, done.
Total 640 (delta 348), reused 570 (delta 278), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (348/348), done.
To https://github.com/KuretaNone/KuretaNone.net.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```
ローカルでコミットした内容がGitHubに反映されるようですね。

## 終わり

とりあえずリポジトリに作るか～と思いリポジトリを作成したら既存リポジトリをプッシュする方法があったので、ありがたかったです。
これでKuretaNone.netのソースコードをGitHubで管理できるようになりました。
今度はプッシュをしたときにGitHub Actionsで自動的にサイトをビルドして、公開できるようにしたいです。
