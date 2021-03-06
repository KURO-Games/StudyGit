## GitとGitHubの違い
さて、まずは勘違いしやすい所からご説明します。  
**GitとGithubは全くの別物です。**  
  
**Git**とは、**分散型バージョン管理システム**の事です。
>Gitでは、各ユーザのワーキングディレクトリに、全履歴を含んだリポジトリの完全な複製が作られる。したがって、ネットワークにアクセスできないなどの理由で中心リポジトリにアクセスできない環境でも、履歴の調査や変更の記録といったほとんどの作業を行うことができる。これが「分散型」と呼ばれる理由である。  
**GitHub**とは、**Gitの仕組みを使って動いているサービス名**の事です。
  
GitHubでは色々な企業が使用しています。  
例）Unity, EpicGames(Unreal Engine, 他), Colopl, 他...

Gitの仕組みを使っているサービスはGitHubの他にもあります。(BitBucket, GitBucket, GitLab, 他)

***
Gitは基本的にコマンド(CLI)を用いて使用しますが、コマンドを使用しなくても使えるツール**SourceTree**(GUI)を使用する事ができます。
## バージョン管理の用語
さてまずは使い方をご説明する前に用語についてご説明します。  
下記文中に"例)"と書かれたものは、わかりやすい**例**として、**セーブデータ**を例にご説明します。
### リポジトリ(Repository)
まず、リポジトリはリモートリポジトリとローカルリポジトリの2種類に分ける事ができます。  
・リモートリポジトリ  
　専用のサーバ(今回はGitHub)に配置して複数人で共有するためのリポジトリです。  
　例)サーバーに置いてある共通のセーブデータ  
・ローカルリポジトリ  
　ユーザ一人ひとりが利用するために、自分の手元のマシン上に配置するリポジトリです。  
　例)自分のセーブデータ
　

### クローン(Clone)
リモートリポジトリを、ローカルリポジトリとして保存します。  
例)サーバーから自分用のセーブデータをダウンロードする。    
### インデックス(Index)
以前に変更をしたファイルの変更点を記録しているもののリスト。  
例)セーブデータ変更記録リスト。  
### ブランチ(Branch)
ブランチを作ることをよく、’ブランチを切る’と言います。  
インデックスからブランチを切ることによって同じフォルダの作業環境を作る事ができます。  
良く、個人の作業環境を作る事が多いです。  
GitHubにリポジトリを作った時から存在している’master’ブランチは動くもの(完成版)を保存している場合が多いです。  
例)セーブデータ変更記録リストからセーブデータの複製を作る  
### マージ(Marge)
変更を加えたファイルのあるブランチ同士を結合します。  
### フェッチ(fetch)
リモートリポジトリに変更が加わっていないか確認をします。  
### プル(Pull)
リモートリポジトリの変更が加わったファイルを保存します。
### コミット(Commit)
ローカルリポジトリーに変更記録を加える。  
コミットしたからと言って痩せるわけではありません。  
例)自分のセーブデータにセーブする。  
### プッシュ(Push)
ローカルリポジトリの変更点をリモートリポジトリに送信します。  
例) セーブデータをサーバーにアップロードする。  
### コンフリクト(Conflict)
変更内容をマージにより統合する際、同じファイルの重複する部分が変更されていると、変更同士が衝突を起こす事をコンフリクト(競合)と言います。  
この状態が起きた時はマージが中断されるので、自分の方のブランチで変更をする、いったんマージを中止し元に戻す方法のどちらかを選択し、実行する必要があります。  
それ以外の操作は、解決するまで使えません。  
よく、’コンフリ’と呼ばれています。

