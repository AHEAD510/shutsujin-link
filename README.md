# shutsujin-link

Notion → Mac の橋渡し専用ページ。`https://ahead510.github.io/shutsujin-link/?page=<Notion page id>` を開くと、`shutsujin://open?page=<id>` へ転送して Mac 側の「出陣フォーム.app」を起動する。

- 転送のみ。送信・データ保存・外部通信は行わない
- ページIDが32桁の16進数でない場合は何もしない
- 本体（AHEAD SALES ENGINE 出陣フォーム）は非公開リポジトリ側で管理

## 司令室との関係

Notionからの既存HTTPSリンクと自動転送は維持。司令室は同じURLのページIDを
検証してMacのURLスキームを直接開く。両経路とも入力・CAPTCHA・送信の既存確認を省略しない。
ブラウザからMacアプリの起動成功や送信完了を判定したとは表示しない。

武将・家紋・戦場背景は司令室の既存画像を縮小したもの。外部CDN・常時アニメーションなし。
`?page=<32桁ID>&preview=1` は自動転送も起動ボタンも無効化するデザイン確認用。
ローカルプレビューは `http://127.0.0.1:8766/shutsujin-link.html`。
公開サイトへの反映は別途公開操作が必要。HTMLと `assets/` を一緒に更新すること。
