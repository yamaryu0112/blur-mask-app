ぼかしマスク（PWA 版）

■ 今回の更新（人の自動検出を追加）で差し替える／追加するファイル
  - index.html …… 差し替え
  - sw.js ……… 差し替え（キャッシュ番号を v2 に上げてあります）
  - mediapipe フォルダ …… 新規追加（人物検出エンジン、約10MB）
  icons / manifest.webmanifest は変更なし
  GitHub Desktop でリポジトリのフォルダにコピーして Commit → Push すれば反映されます。

■ 自動検出について
  - 初めて「人を自動検出」を使うときだけ、インターネット接続が必要です。
    検出モデル（Google の EfficientDet-Lite、数MB）を自動でダウンロードして端末に保存します。
    「高精度」を初めて選んだときも、別のモデルを1回だけダウンロードします。
  - 一度使えば、以降はオフラインでも動きます。
  - 料金はかかりません（MediaPipe・モデルとも Apache 2.0 ライセンス、処理はすべて端末内）。

■ 新しく公開するとき（GitHub Pages）
  1. リポジトリにこのフォルダの中身をすべて置く
  2. Settings（リポジトリの設定）→ Pages → Branch を main / (root) にして Save
  3. https://<ユーザー名>.github.io/<リポジトリ名>/ を Android の Chrome で開き、
     「⋮」→「アプリをインストール」

■ 次回以降アプリを更新するとき
  index.html を差し替え、sw.js の CACHE = 'blurmask-v2' の番号を上げてください。
