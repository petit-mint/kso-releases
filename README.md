# KSO Releases

KSOパイロット版のWindows向け公開配布リポジトリです。

## 最新版

**KSO Pilot 0.4.0**をプレリリースとして公開しています。

[KSO Pilot 0.4.0のダウンロードと変更履歴](https://github.com/petit-mint/kso-releases/releases/tag/v0.4.0)

パイロット版は正式版に向けた検証中のリリースです。配信本番で使用する前に、使用するPC、OBS設定、セットリストで動作を確認してください。

## 0.4.0の主な変更

- セットリスト作成をメインタブへ独立
- 設定を「基本設定」「配信操作」「OBS接続」「表示デザイン」の4カテゴリーへ再編
- 広い画面と狭い画面に対応した設定カテゴリーナビゲーション
- OBS接続と表示デザイン間の相互導線
- 既存のテーマ、ショートカット、OBSプロファイル、LRC、セットリストとの互換性維持

## ダウンロード

初めて利用する場合は、インストーラーと操作ガイドをまとめた`KSO_Pilot_0.4.0_Distribution.zip`を推奨します。

[Releases](https://github.com/petit-mint/kso-releases/releases)では、次のファイルを公開しています。

| ファイル | 内容 |
| --- | --- |
| `KSO_Pilot_<version>_Distribution.zip` | 推奨。インストーラー、インストール手順書、操作ガイド、変更履歴をまとめた配布パッケージです。 |
| `KSO_Pilot_<version>_x64-setup.exe` | Windows 64ビット版のインストーラー単体です。手順書をすでにお持ちの方向けです。 |
| `KSO_Pilot_<version>_x64-setup.exe.sha256` | インストーラーが正しくダウンロードされたか確認するためのSHA-256値です。 |
| `KSO_Operation_Guide_Pilot_<version>.zip` | 操作ガイドのみをまとめたファイルです。 |

## SHA-256の確認

PowerShellで次のコマンドを実行し、同梱の`.sha256`ファイルに記載された値と一致することを確認してください。

```powershell
Get-FileHash -Algorithm SHA256 .\KSO_Pilot_<version>_x64-setup.exe
```

0.4.0インストーラーの正しいSHA-256は次の値です。

```text
69951ed3e7c38cea009cbf39843e3f379d37817fc67b13eed58d77b1df28b343
```

`Get-FileHash`を利用できない環境では、Windows標準の次のコマンドでも確認できます。

```powershell
certutil -hashfile .\KSO_Pilot_<version>_x64-setup.exe SHA256
```

## ソースコードについて

このリポジトリは配布ファイル専用です。KSOの開発ソースコードは含まれていません。
