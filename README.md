# OKLCH ピッカー PWA — GitHub Pages 公開手順

1. GitHubで新規リポジトリを作成(公開名がURLになる。例: `oklch-picker`)
2. このフォルダの中身(`index.html`, `manifest.webmanifest`, `sw.js`, `icon-180.png`, `icon-512.png`)をリポジトリのルートに置いて push
3. リポジトリの Settings → Pages → Source を「Deploy from a branch」、Branch を `main` / `(root)` にして保存
4. 数分後 `https://<ユーザー名>.github.io/oklch-picker/` で公開される
5. iPhoneのSafariで開き、共有 → **ホーム画面に追加**

## メモ

- Service Worker がキャッシュするので、2回目以降はオフラインで起動する
- 更新を配信したいときは `sw.js` の `CACHE` のバージョン(`oklch-picker-v1`)を上げて push
- クリップボード読み取り(タップでペースト)はHTTPS必須 → GitHub Pagesは対応済み
- リポジトリをprivateにしたままPagesを使うには有料プランが必要。中身は単なるピッカーなのでpublicで問題ないはず
