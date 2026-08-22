# KSO Releases

KSOパイロット版のWindows向け公開配布リポジトリです。

## 最新版

**KSO Pilot 0.3.0**をプレリリースとして公開しています。

[KSO Pilot 0.3.0のダウンロードと変更履歴](https://github.com/petit-mint/kso-releases/releases/tag/v0.3.0)

パイロット版は正式版に向けた検証中のリリースです。配信本番で使用する前に、使用するPC、OBS設定、セットリストで動作を確認してください。

## 0.3.0の主な機能

- 現在曲と歌唱済み履歴を表示するOBSブラウザソース
- 曲情報の配置、背景、文字、アニメーションを調整できるスタイルエディタ
- KSO内でのYouTube検索、動画選択、セットリストへのURL取り込み
- KSOが背面にある場合も使える8種類のグローバルショートカット
- 二重起動の防止と、終了時のYouTube音声、オーバーレイサーバー、OBS処理の停止
- 既存の0.2.0以前のOBSプロファイル、LRC、セットリストとの互換性維持

## ダウンロード

初めて利用する場合は、インストーラーと操作ガイドをまとめた`KSO_Pilot_0.3.0_Distribution.zip`を推奨します。

[Releases](https://github.com/petit-mint/kso-releases/releases)では、次のファイルを公開しています。

- `KSO_Pilot_<version>_Distribution.zip`: インストーラーと手順書をまとめた配布パッケージ
- `KSO_Pilot_<version>_x64-setup.exe`: Windows 64ビット版インストーラー
- `KSO_Pilot_<version>_x64-setup.exe.sha256`: インストーラーのSHA-256
- `KSO_Operation_Guide_Pilot_<version>.zip`: 操作ガイド

## SHA-256の確認

PowerShellで次のコマンドを実行し、同梱の`.sha256`ファイルに記載された値と一致することを確認してください。

```powershell
Get-FileHash -Algorithm SHA256 .\KSO_Pilot_<version>_x64-setup.exe
```

0.3.0インストーラーの正しいSHA-256は次の値です。

```text
f1b78d6958a84d7c6eb0706c2755b210581ac85d7d6e82baf7e9130b96b74dca
```

`Get-FileHash`を利用できない環境では、Windows標準の次のコマンドでも確認できます。

```powershell
certutil -hashfile .\KSO_Pilot_<version>_x64-setup.exe SHA256
```

## ソースコードについて

このリポジトリは配布ファイル専用です。KSOの開発ソースコードは含まれていません。
