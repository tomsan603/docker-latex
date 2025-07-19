## 仕組み
このレポジトリではDockerを用いてtex執筆環境を構築したコンテナーを作成しました。  
これにより環境構築の手間が省け、ローカルPCも汚れません。

![構造1](./images/architecture.png)  

コンテナーは新たなパソコンを作るというイメージです。コンテナーはすぐに作ったり消したりすることが可能なので気軽にtexなどを導入できます（ミスしたら消してまた作成するだけです）しかしコンテナーを作るにはDocker Engine、Docker Engineを動かすにはLinux(WSL)が必要です。よってDocker Desktopをダウンロードする必要があります。Docker DesktopはDocker EngineやLinux(WSL)、Docker Composeなどをまとめてインストールしてくれます。なおVS Codeはエディターでファイルの中身を書き換えやすくします（誤字チェックや文法チェックなどさまざまな機能を追加できるのでメモ帳の完全上位互換です）

![構造2](./images/architecture2.png)

VS Codeの機能の1つであるRemote Developmentは.devcontainerフォルダーをもとにDocker Composeに指示を出します。そうするとDocker Composeがdocker-compose.ymlファイルを読み込んでDocker Engineに指示を出します。Docker EngineはDockerfileをビルドしてイメージをつくってイメージからコンテナーを作成します。また、ホストPCのファイルをマウントします。Dockerfileはどのような環境を作るかをテキスト形式で書けます。これによりだれでも同じコンテナーが作れるというわけです。また、Dockerfileを書き換えるだけでいろいろな環境も作れてしまいます。（Dockerfileなどのファイルの説明は省略します。興味がある人はDockerを学ぶといいと思います）

Remote Developmentはコンテナーを作成させる際、VS Code(Server)をコンテナー内に置きます。これによりホストPCのVS Code(UI)で画面を操作するとその動作がサーバーに送られて、実際の処理がコンテナー内のサーバーで行われて処理結果がホストPCのVS Code(UI)に送られます。（通信はDocker Engineを介しています）これはPCでブラウザを見るときと同じ仕組みです。
