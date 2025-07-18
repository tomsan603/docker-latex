## docker-latex
このレポジトリではDocker、Git、VS Codeのみを使いTexで執筆できる環境を提供します。  
数式や画像だけでなく理系で使うような記法（ブラケット記法）やパイソンコード埋め込みなども使えます。  
環境はWindowsを主に想定しています。

## 前提条件
1. Docker Desktop、Git、VS Codeをインストールしてください。  
2. 以下のVS Code拡張機能をインストールしてください。  
（VS Code内でCtrl＋Shift＋Xをした後、以下のを入力＆インストールボタン押すだけです。）
- [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)  
- [Latex Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)  

## 手順
1. 任意のディレクトリで以下のコードを実行します
    ```Power Shell
    git clone https://github.com/tomsan603/docker-latex.git　
    ```
2. VS Codeでdocker-latexフォルダーを開きます
3. devContainerを起動します
   - 左下の`><`アイコンを選択したのち、`コンテナーで再度開く`を選択します
   - 初回起動時はビルドに20分ほどかかります（2回目以降はすぐ起動します）
4. texフォルダーなどを作ってそこにtexファイルを格納し、ビルドボタン＆PDF表示ボタンを押すとtexフォルダーと同階層にoutフォルダーが作られ、そこに出力結果が格納されます