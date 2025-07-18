## docker-latex
このレポジトリではDocker、Git、VS Codeのみを使いTexで執筆できる環境を提供します。  
数式や画像だけでなく理系で使うような記法（ブラケット記法）やパイソンコード埋め込みなども使えます。  
環境はWindowsを主に想定しています。

## 前提条件
1. Docker Desktop、Git、VS Codeをインストールしてください。  
2. VS Codeで以下の拡張機能をインストールしてください。  
（VS Code内でCtrl＋Shift＋Xをした後、以下のを入力＆インストールボタン押すだけです）
- [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)  
- [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)  

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
5. VS Codeを閉じると終了します（また始めるときは手順2に戻る）

## 補足
1. 参考リンク
- [Docker Desktopインストール方法](https://qiita.com/zembutsu/items/a98f6f25ef47c04893b3)  
- [Gitインストール方法](https://qiita.com/takeru-hirai/items/4fbe6593d42f9a844b1c)  
- [VS Codeインストール方法](https://qiita.com/furu38/items/6776acba6621012ee475) 
2. [仕組み](./docs/README.md)