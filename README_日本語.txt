# STUDY LEAGUE — iPhone / Safari版

## iPhoneへの追加方法
1. このフォルダ一式を、HTTPS対応のWebホスティングにアップロードします（例：GitHub Pages / Netlify）。
2. 公開された `https://...` のURLを、iPhoneのSafariで開きます。
3. Safari下部（または上部）の共有ボタン「□↑」をタップします。
4. 「ホーム画面に追加」→ 表示名を確認 →「追加」。
5. ホーム画面の STUDY LEAGUE アイコンから起動します。

## 注意
- `index.html` だけでなく、`manifest.webmanifest`、`sw.js`、`icons/` も同じ階層のまま公開してください。
- ホーム画面追加とオフラインキャッシュにはHTTPS配信が必要です。ファイルアプリからHTMLを直接開く方法ではPWAとして動作しません。
- 記録はそのiPhoneのSafari内（localStorage）に保存されます。別端末とは同期されません。SafariのWebサイトデータ削除で消える場合があるため、成績タブから定期的にJSONを書き出してください。
- AIライバルは元のHTML版と同じくアプリ内シミュレーションです。
- YPTとの自動同期はまだ接続していません。APIキーをHTMLに直接埋め込まない設計にしています。
- iOSではバックグラウンド中に画面更新が止まる場合がありますが、タイマーは開始時刻を保存しているため、戻った時に経過時間を再計算します。
