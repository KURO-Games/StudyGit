# StudyGit
さて、初心者用にGitの使い方とSourceTreeの使い方を紹介します。
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


## SourceTreeの使い方
まずはソースツリーをダウンロード、インストールします。
インストール作業は省略します。  
[SourceTree](https://www.sourcetreeapp.com)


筆者はMac派なのでMacからご説明します。  
### アカウント認証
まずは、アカウントの認証を行います。  
環境設定>アカウント
![環境設定](https://github.com/KURO-Games/StudyGit/blob/master/pic/Original/00.png)  
アカウントのホストはGitHub  
認証タイプはBasic(パスワード認証)  
ユーザー名とパスワードを記入し保存を押しましょう。
![アカウント](https://github.com/KURO-Games/StudyGit/blob/master/pic/Original/01.png)  

### リポジトリのクローン
まず、GitHubに行って、Clone or Downloadをクリック、画像のオレンジ色のボタンを押して、URLをコピーします。  
![GithubURL](https://github.com/KURO-Games/StudyGit/blob/master/pic/PS/02-01.png)  

今度はSourceTreeに移動して、新規をクリック、ソースURLに先程のURLをペースト、クローンボタンを押します。  
![SourceTreeURL](https://github.com/KURO-Games/StudyGit/blob/master/pic/Original/03.png)
これでクローン作業は終了です。  
![SourceTreeURL](https://github.com/KURO-Games/StudyGit/blob/master/pic/Original/04.png)
### ブランチを切る
筆者、ブランチを切り忘れたので、このタイミングで書きかけ用のブランチを作りたいと思います。  
まず、オレンジ枠のブランチボタンを押します。
![Branch1](https://github.com/KURO-Games/StudyGit/blob/master/pic/PS/04-01.png )  
このような画面が出てきたら、名前を書いて、ブランチを作成のボタンを押して作ります。  
![Branch2](https://github.com/KURO-Games/StudyGit/blob/master/pic/Original/05.png)
下記のように表示されればブランチの作成は終了です。  
![Branch3](https://github.com/KURO-Games/StudyGit/blob/master/pic/PS/06-01.png )  
### コミット、プッシュする
さて、これ、テキストベースで書き込んでいるので、GitHub上でどのように写っている確認したいので、GitHub上に一度上げてみようとおもいます。  
  
  左上にあるコミットボタンを押します  
  ![Commit1](https://github.com/KURO-Games/StudyGit/blob/master/pic/PS/06-02.png )
このような画面が出てきたと思います。  
では、変更を加えるファイル(今回はREADME.md)の横にあるチェックボタンを押します。
 ![Commit2](https://github.com/KURO-Games/StudyGit/blob/master/pic/PS/07-01.png )
 上のステージングに移動したら、コメントをつけて、コミットします。
 ![Commit3](https://github.com/KURO-Games/StudyGit/blob/master/pic/Original/09.png)  
 これにてコミットは終了です。  
 前の画像で、’コミットをただちにプッシュする’にチェックを入れてなかった場合はここの画像でプッシュボタンを押します。
  ![Commit4](https://github.com/KURO-Games/StudyGit/blob/master/pic/Original/10.png)  

### マージする
さて、masterブランチにwritingブランチをマージしていこうと思います。  
実は、左側のブランチ名をクリックするとそのブランチに移動できます。  
  
  では、masterブランチに移動します。
  移動すると下記のようにmasterブランチの横にマークがつきます。  
    移動が完了したら、マージボタンを押します。
 ![Marge1](https://github.com/KURO-Games/StudyGit/blob/master/pic/PS/11-01.png )
 Writingブランチの最新である’SourceTree書きかけ’を選択します。  
 そしてそのままOKを押します。  
  ![Marge2](https://github.com/KURO-Games/StudyGit/blob/master/pic/Original/12.png)  
  SourceTree上では'origin/ブランチ名'がリモートリポジトリ名で’ブランチ名’のみの場合、ローカルリポジトリになります。  
  下記の画像を見ると、’master’ブランチの横に”1コミット先行”と書かれているので、ローカルリポジトリはすでに’SourceTree書きかけ’にいる事がわかります。  
  ではPushを押して、リモートリポジトリも’SourceTree書きかけ’にしようと思います。  
![Marge3](https://github.com/KURO-Games/StudyGit/blob/master/pic/Original/13.png)  
![Marge4](https://github.com/KURO-Games/StudyGit/blob/master/pic/Original/14.png)
下記の画像のように’master’ブランチ'origin/master'ブランチ共に同じ場所にある場合、リモート側と同じ状態になりました。  
![Marge5](https://github.com/KURO-Games/StudyGit/blob/master/pic/Original/15.png)
  
  
*****
20/05/29(fri) 03:08現在  
来週(20/06/05)までにWindows版追加します。

