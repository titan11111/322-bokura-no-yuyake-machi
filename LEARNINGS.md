# 322-bokura-no-yuyake-machi LEARNINGS

## 2026-10-15 フォルダ改名・公開前整備

- 画面タイトルは当初から「ぼくらの夕やけ町」。フォルダだけ `322-day094` のままだった。
- 番号は変えず `322-bokura-no-yuyake-machi` へ改名。公開URLが旧名に依存しないことを、改名前に Pages 404 で確認した。
- `<title>` が `<body>` 側にあり、viewport に `maximum-scale` / `user-scalable=no` が無かったので head へ移した。
- `playtest/` は公開実体から除外（`.gitignore`）。
