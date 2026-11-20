# WSA v1.4.4 正式公開・検証情報

## リリース情報

- 製品名：Web Security Assessment Platform (WSA)
- バージョン：1.4.4
- リリース種別：Local Test
- 公開日：2026-11-19

## 署名鍵情報

- 署名方式：Ed25519
- Key ID：`9f23e3adf9f7f2c9`
- 公開鍵指紋（SHA-256）：

`9f23e3adf9f7f2c96ff45814baa318eedf95eccfe794537cba914d3b1846f10c`

## 配布ファイル

- ZIP：`WSA_v1.4.4_Web_FileScanner_Local_Test.zip`
- ZIP SHA-256：

`feb4d9d6528c7ea02f3c9c96cc4389e21e7ea25837f8bb020cdf9756bbc40d6f`

- Bootstrap：`WSA_BOOTSTRAP.mjs`
- Bootstrap SHA-256：

`f6b69d96795c2dfcf5db94d84a3a9cf65c6111a99413534cf814e8a8cf4512d9`

## 公式配布先

https://wsa-release-api.youtube-marketingdx-trainingworkers.workers.dev/api/releases/latest

## 検証結果

- ブートストラップSHA-256照合：PASS
- ZIP SHA-256照合：PASS
- Ed25519署名検証：PASS
- ファイルインベントリ検証：PASS
- ディスク再ハッシュ：PASS
- 本番公開後の配布API確認：PASS

## 利用上の注意

本リリースはLocal Test版です。

Web診断は試験用URLのみ対応し、任意の実サイト診断には未対応です。

Windows実機でのインストール、Defender連携、実環境でのスキャン動作は別途検証が必要です。

本製品は既存のウイルス対策ソフトを代替するものではありません。

## 検証方針

配布ファイルのSHA-256、公開鍵指紋、Ed25519署名検証結果を照合してから実行してください。

いずれかが一致しない場合は実行を中止してください。
