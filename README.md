# 調子ノート — GitHub Pages公開用

お預かりした試作HTMLを、そのまま index.html に配置しています。
スマホ用の画面幅設定があり、CSSとJavaScriptもHTML内に含まれています。
追加ライブラリ・インストール・ビルドは不要です。

## ZIPの中身

- index.html：アプリ本体
- README.md：この説明書
- .nojekyll：静的ファイルをそのまま配信するための設定

## GitHub Pagesで公開する

1. このZIPを展開します。ZIP自体をアップロードするのではありません。
2. GitHubでリポジトリ（例：cho-note）を作ります。無料プランの場合は Public を選びます。
3. ファイルのアップロード画面（Add file → Upload files、空のリポジトリでは uploading an existing file）を開きます。
4. 展開したファイルをアップロードし、Commit changesで保存します。index.html がリポジトリの一番上に来るようにしてください。フォルダごと入れて一段深くしないでください。
5. Settings → Pages を開きます。
6. Build and deployment の Source で Deploy from a branch を選びます。
7. Branch は main（アップロード先のブランチ）、フォルダは /(root) を選んで Save を押します。
8. 公開処理が終わったら、Pages画面に表示されるURLを開きます。

URLの例：https://あなたのユーザー名.github.io/cho-note/

.nojekyll が端末上で隠れて選べない場合も、この構成では index.html と README.md のアップロードで利用できます。
公開後に404になる場合は、公開処理の完了、Pagesのブランチ設定、index.html の配置を確認してください。

公式手順：
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## スマホで使う

公開URLをスマホのブラウザで開いてください。毎回HTMLをダウンロードする必要はありません。
ブックマークしておくと、次から同じURLで開けます。
ブラウザに「ホーム画面に追加」がある場合は、そこからショートカットも作れます。
このパッケージにはオフライン動作を保証する仕組みは含まれていません。

## 記録の保存と試作版の仕様

- 記録は利用した端末・ブラウザの localStorage に保存されます。サーバーへの記録送信や端末間同期はありません。
- ブラウザのデータ消去で記録が消えます。バックアップ・復元機能は未実装です。
- ダウンロードしたHTMLで入力した記録は、公開URLへ自動移行しません。利用するブラウザやURLのドメインが変わっても保存場所が変わります。
- 元の試作版の動作を維持しています。開き直すと項目選択画面から始まります。
- 保存済みの当日入力は入力画面へ復元されません。同じ日に再保存すると、その日の記録は今回の入力内容で上書きされます。
- グラフは直近30日から最大14件・最大5項目、まとめは最大10項目を表示する簡易仕様です。
- アプリ本体は公開されますが、端末内で入力した記録はリポジトリには追加されません。

今回は公開用の梱包のみで、試作版の機能変更は行っていません。
