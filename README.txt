ぼかしマスク（PWA 版）

■ 今回の更新（顔を中心にした自動マスク、ぼかし強度の調整）で差し替えるファイル
  - index.html …… 差し替え
  - sw.js ……… 差し替え（キャッシュ番号を v3 に上げてあります）
  mediapipe フォルダ / icons / manifest.webmanifest は変更なし
  （mediapipe フォルダをまだ入れていない場合は追加してください）
  GitHub Desktop でリポジトリのフォルダにコピーして Commit → Push すれば反映されます。

■ 自動検出について
  - 初めて「人を自動検出」を使うときだけ、インターネット接続が必要です。
    人物検出モデル（EfficientDet-Lite、数MB）と顔検出モデル（BlazeFace、約0.2MB）を
    自動でダウンロードして端末に保存します。
    「高精度」を初めて選んだときも、別のモデルを1回だけダウンロードします。
  - 一度使えば、以降はオフラインでも動きます。
  - 料金はかかりません（MediaPipe・モデルとも Apache 2.0 ライセンス、処理はすべて端末内）。

■ 新しく公開するとき（GitHub Pages）
  1. リポジトリにこのフォルダの中身をすべて置く
  2. Settings（リポジトリの設定）→ Pages → Branch を main / (root) にして Save
  3. https://<ユーザー名>.github.io/<リポジトリ名>/ を Android の Chrome で開き、
     「⋮」→「アプリをインストール」

■ 次回以降アプリを更新するとき
  index.html を差し替え、sw.js の CACHE = 'blurmask-v3' の番号を上げてください。
