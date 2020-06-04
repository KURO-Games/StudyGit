### Unityのシーンによるコンフリクト後編
#### 3.コンフリクトの解消方法
今回は相手の変更内容で解決(fooブランチのCubeがあるシーンで上書き)します。 
![Unity1](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/09.png)  
![Unity2](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/10.png)  
![Unity3](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/11.png)  
![Unity4](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/12.png)  ![Unity5](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/13.png)  
![Unity6](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/14.png)  
コンフリクトが解消されて、Cubeのみが残りました。  
![Unity7](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/15.png)  
では、fugaブランチのButtonを実装します。まずは、fugaがコミットしたインデックスを選択、ダブルクリックします。  
![Unity8](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/16.png)  
![Unity9](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/17.png)  
外部で変更されたので、再読み込みするか聞いてきました。  
Reloadボタンを押しましょう。
![Unity10](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/18.png)  
今回はボタン単体なので、CanvasごとPrefab化します。
![Unity11](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/19.png)  
![Unity12](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/20.png)  
シーンは保存せずに破棄します。  
そのままPrefabをコミット、プッシュします。
![Unity13](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/21.png)  ![Unity14](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/22.png)  
マージします。  
マージが終わったら、シーンにPrefabを追加します。
![Unity9](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/23.png)  
これで、統合は終了です。(見えやすいように、Buttonのアルファ値を下げています。)
![Unity9](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/ConflictUnity/24.png)  

#### 4.別の方法で持ってくる
前の章ではコミット方式で持ってきましたが、別の方法を使うこともできます。  
Prefab化した後に、UnityPackageとしてExportする方法も使うことができます。
![EX1](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/EX/01.png)  
![EX2](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/EX/02.png)  
![EX3](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/EX/03.png)  
![EX4](https://github.com/KURO-Games/StudyGit/blob/master/pic/StudyConflict/EX/04.png)  
