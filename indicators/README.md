# indicators

TradingView Pine Script（v6）のインジケーター置き場。

| ファイル | 内容 |
|---|---|
| `finreit_diagnostic_v1_0.pine` | 金融・REIT 財務診断 v1.0（オリジナル・参照用） |
| `finreit_diagnostic_v1_1.pine` | 金融・REIT 財務診断 v1.1（改良版） |

## 方針

- **TradingView 内蔵データのみで完結**する。使用する外部取得関数は `request.financial` / `request.splits` / `request.security` のみ。外部 API・手入力・持ち越し補完は行わない。
- 現在値ベースの診断であり、ポイントインタイムのバックテスト用データではない。
- 規制上の健全性判定や売買推奨ではない。

## 使い方

1. TradingView の Pine エディタに `.pine` の内容を貼り付けて「チャートに追加」。
2. **標準ローソク足の日足**で使用する（それ以外はエラー停止）。
3. 業種が自動判定されない銘柄は「採点モード」を手動選択する。モーゲージ REIT は「判定停止」を ON にする。

## v1.1 の変更点

`finreit_diagnostic_v1_1.pine` 冒頭のコメントを参照。
