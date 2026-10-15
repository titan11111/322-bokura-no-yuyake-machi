# 322-bokura-no-yuyake-machi 「ぼくらの夕やけ町」

旧フォルダ名は `322-day094`。番号は変更しない。公開前にタイトルへ合わせて改名した。

## 操作/設定UI

| 項目 | 決定 |
|---|---|
| 入力 | Pointer Events + `setPointerCapture`。十字キー／Bダッシュ／Aしらべる。PCは WASD・矢印・X/Shift・Z/E/Space |
| カメラ | 画面ドラッグで見回す。SELECTで後方。STARTでポーズ |
| ポーズ | START / Esc。ポーズ中は住人の動きも止まる |
| ミュート | 未実装。WebAudioは開始タップで unlock |
| 保存 | 未使用（毎回最初から） |
| iOS | viewport-fit / maximum-scale=1 / user-scalable=no / safe-area / body `touch-action:none` / Three.js 同梱 |

## ゲーム概要

昭和43年10月の放課後。じゃんけんに負けた主人公が鬼になり、目をつぶって10数えたあと、町に隠れた友だち5人を探す。駄菓子屋・土管・銭湯・神社などを回り、お宝8つも集め、夕やけチャイムまでに公園へ帰る。

- 対象端末: iPhone Safari / GitHub Pages。外部CDNなし
- コアループ: 歩く → 店や人と話す（ヒント） → 友だちを見つける → お宝を拾う → チャイムまでに集合
- 勝敗: 友だち5人の発見数とお宝8つの収集数でエンディング文が変わる。時間切れでも終了する
- 音声: WebAudio合成。ファイルなし
- ファイル: `index.html` + `three.min.js`（r128 同梱）

## 未確定・既知の不足

- ミュートトグルなし
- `localStorage` 未使用
- iPhone実機の通しプレイは未検証
- ヘッドレス描画は遅い環境で RAF が落ちることがある（Metal付き確認では60 RAF/秒の実績あり）
