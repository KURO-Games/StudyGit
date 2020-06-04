### ソースコードによるコンフリクト
#### 1.コンフリクトを意図的に発生させる
では、まず基準になるソースコードを用意します。  
今回はこのようなソースコードをmasterブランチに用意してみました。  
![コンフリ1](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/Source/01.png)  
今回、このソースコードを操作するのは、'foo'ブランチと、’fugafuga’ブランチです。  
  
では、fooブランチではこのようにソースコードを追加したこととします。
![コンフリ2](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/Source/02.png)  
fooブランチでコミット、プッシュします。  
  
また、同時刻、fugafugaブランチでは、以下のソースコードを追加しました。  
![コンフリ3](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/Source/03.png)  
fugafugaブランチでコミット、プッシュします。
  
この状態で、SourceTreeを見てみると、インデックスはこのようになります。
![コンフリ4](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictSource/01.png)  
では、masterブランチにマージしていきます。最初は、fooブランチをマージします。
こちらは当然、マージは成功します。
![コンフリ5](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictSource/02.png)  
![コンフリ6](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictSource/04.png)  
では今度は、fugafugaブランチをマージします。
![コンフリ7](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictSource/06.png)  
ですが、マージの競合、コンフリクトが発生します。
![コンフリ8](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictSource/07.png)  
![コンフリ9](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictSource/08.png)  

#### 2.コンフリクトが起きた要因
コンフリクトが起きた要因ですが、それは、同じ行を二つのブランチが操作したことによる、データの衝突です。  
![コンフリ10](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictSource/03.png) 
![コンフリ11](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictSource/05.png) 

#### 3.コンフリクトの解消方法
コンフリクトの解消方法ですが、私のやり方をご紹介します。  
まず初めに、競合が発生しているファイルの・・・をクリックし、’競合を解決’の蘭で、あまり変更がないファイルを選択します。  
自身の変更内容で解決...今の作業中のブランチを残す  
相手の変更内容で解決...マージしているブランチのファイルで上書きする  
  
今回は、自身の変更内容で解決します。
解決が終わったら、コミット、プッシュします。
  ![コンフリ12](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictSource/09.png) 
  ![コンフリ13](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictSource/10.png) 
  今のソースコードは、fugafugaブランチのソースコードが追加されていないので、追加します。  
インデックスをダブルクリックすると、その変更点まで戻れます。(チェックアウトできます。)  
  ![コンフリ14](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictSource/11.png) 
  ![コンフリ15](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictSource/12.png) 
  これにて、fugafugaブランチが追加したところまで戻ってきました。
  ではfugafugaが追加したソースコードをコピーします。
  ![コンフリ16](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/Source/04.png) 
そうしたら、任意のブランチ(全て同じ場所にある状態)で、ソースコードにペーストします。
  ![コンフリ17](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/Source/05.png) 
このまま、コミット、プッシュして全てのソースコードの統合が終わりました。
![コンフリ18](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictSource/13.png) 
