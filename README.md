# qiita_app_sei

## このプロジェクトを自分のパソコンに入れる方法
1. 緑色のCodeボタンを押す  
![image](https://github.com/user-attachments/assets/b611423e-67c4-4ccb-98ed-b805a5c38fbf)
2. タブバーでHTTPSを選択し、下に表示されているURLの右のコピーアイコンを押す  
![image](https://github.com/user-attachments/assets/fd9c14ad-cef0-42cd-89a0-befe02311ce0)
3. Macに入っているTerminalを開く
4. `git clone https://github.com/find-focus-inc/qiita_app_sei.git` と入力し、Enterボタンを押す  
![image](https://github.com/user-attachments/assets/e82dc394-f289-4822-ae08-a3f4b9f683e8)
5. Macに入っているAndroid Studioを開く
6. 右の方にあるOpenボタンを押す  
![image](https://github.com/user-attachments/assets/fe4ecf70-c1e5-4029-8890-91494f03ac7e)
7. Finderが開くのでqiita_app_seiを選択し、開くボタンを押す
8. Android Studioに以下の画面が表示されたら、OK
![image](https://github.com/user-attachments/assets/a910e74f-5b9b-4eaf-bb0f-e1118e302ff7)

## 基本的なgit操作
今回は個人開発としてアプリ開発をしますが、今後実務としてやるならほとんどの場合がチーム開発になります。チーム開発に必要なのが、git操作です。このgithubを操る上では絶対に必要になるものです。今回は基本的な操作しか載せませんが、もっと知りたい場合は自分で調べてみてください。  

- add
自分のパソコンで編集したファイルをインデックスに上げるためのコマンドです。インデックスとはコミットするファイルを準備するところです。最初はcommitするために実行するコマンドだと覚えておくといいでしょう。  
使用例は`git add main.dart`です。main.dartの部分はcommitしたいファイル名を指定しましょう。次に紹介するstatusコマンドで編集しているファイルを確認して、そこからコピペするのが一番いいでしょう。
- status
ファイルが今どの層にいるのかを確認するためのコマンドです。githubに変更したファイルを送信するためには「ワークツリー -> インデックス -> リポジトリ」の順にファイルを流していく必要があります。先ほど紹介したaddコマンドは「ワークツリー -> インデックス」にファイルを流すためのコマンドです。  
ワークツリーとは自分が作業している場所のことで、リポジトリとは自分がコミットしたファイルが集まる場所のことです。  
使用例は`git status`です。
- commit
「インデックス -> リポジトリ」にファイルを流すためのコマンドです。ここでようやくローカルリポジトリを更新します。  
使用例は`git commit -m "appBarを修正"`です。「appBarを修正」の部分は自分が実装(修正)した内容を書いてください。この部分はPull Requestを作った際に実際に表示される部分なので、しっかりと書きましょう。  
- push
ローカルリポジトリの内容をリモートリポジトリに反映させるためのコマンドです。リモートリポジトリは今回の場合はgithubだと思っておいてください。このコマンドを打ったら、Pull Requestを作ることができます。  
使用例は`git push origin feature/create-album-page`です。feature/create-album-pageの部分は今実際に作業しているブランチ名を書いてください。  
- checkout
自分がいるブランチを他ブランチに移動するためのコマンドです。ブランチとは作業場のことを指します。基本的にはmainブランチでは作業せず、自分専用の作業ブランチを作成してから、作業にとりかかる必要があります。  
使用例は`git checkout main`や`git checkout -b feature/create-album-page`です。前者はmainブランチに移動するコマンドで、後者はfeature/create-album-pageブランチを作成するのと同時に作成したブランチに移動してくれるコマンドです。  
- pull
リモートリポジトリ(github)から情報を取得し、ローカルリポジトリに取得した情報を反映させるためのコマンドです。主にPull Requestがマージされた後に使うことが多いと思います。  
使用例は`git pull origin main`です。これはgithubから取得した情報をmainブランチに反映させますよっというコマンドです。mainの部分は反映させたいブランチ名に適宜変えてください。  
- merge
ローカルリポジトリのあるブランチの情報を自分がいるブランチに反映させるコマンドです。特に自分が今いるブランチを最新にするためにmainブランチから取得する時に使います。  
使用例は`git merge origin/main`です。これはmainブランチの情報を自分が今いるブランチに反映させますよっというコマンドです。mainの部分は情報を取得したいブランチ名に適宜変えてください。  
- fetch
リモートリポジトリ(github)から新たなブランチを取得したり、ブランチの情報を更新するコマンドです。特に自分が今いるブランチを作成したブランチに変更があるかを確かめるのに使います。  
使用例は`git fetch`です。

