ぼかしマスク（PWA 版）の公開手順 — GitHub Pages の場合

1. github.com で新しいリポジトリを作る（Public、名前は何でも可。例: blur-mask）
2. 「Add file」→「Upload files」で、この zip の中身（index.html / manifest.webmanifest /
   sw.js / icons フォルダ）をすべてドラッグして Commit する
   ※ zip ごとではなく、展開した中身をアップロードしてください
3. Settings → Pages → Branch を「main」「/(root)」にして Save
4. 1〜2分後に https://<ユーザー名>.github.io/blur-mask/ で開ける
5. Android の Chrome でそのURLを開き、メニュー「⋮」→「アプリをインストール」

一度インストールして起動すれば、以降は機内モードでも使えます。

アプリを更新したとき：index.html を差し替え、sw.js の CACHE = 'blurmask-v1' を
'blurmask-v2' のように番号を上げてください（端末側のキャッシュが入れ替わります）。

Cloudflare Pages / Netlify の場合は、このフォルダをそのままドラッグ＆ドロップで公開できます。
