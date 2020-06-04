### Unityのシーンによるコンフリクト前編
P.S. Unity 2019.3 から、UIが少しだけ変わりました。  筆者は 2 by 3 の画面で行っています。  
また、長いので、前編と後編に分けています。  
#### 1.コンフリクトを意図的に発生させる
masterブランチにはこんなシーンを用意しています。  
![Unity1](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/01.png)  
ソースコード編で登場したfooブランチと、fugafuga (以下fuga) ブランチで行います。  
では、まず先にfugaブランチでシーンを編集します。  
fugaブランチでは、真ん中にButtonを設置しました。
![Unity2](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/02.png)  
次に、fooブランチでは真ん中にCubeを設置します。(名前は Tohu)
![Unity3](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/03.png)  
各ブランチでコミット、プッシュします。
![Unity4](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/04.png)  
  
では、masterブランチにマージしていきます。まず初めはfugaブランチをマージします。
![Unity5](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/05.png)  
![Unity6](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/06.png)  
  
次に、fooブランチをマージしようとしますが、コンフリクトが発生します。  
![Unity7](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/07.png)  
![Unity8](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/08.png)  
  
  #### 2.コンフリクトが起きた要因
  こちらも、ソースコードと同じように、二つのブランチでデータ衝突が起きたことが原因です。  
  また、SerializeFieldなどのエディタ拡張をしている場合のInspectorの値を変更した場合なども起こりやすいので注意しましょう。  
  [後編 コンフリクトの解消方法](https://github.com/KURO-Games/StudyGit/blob/master/md/Conflict/conflict-unity-scene2.md)
