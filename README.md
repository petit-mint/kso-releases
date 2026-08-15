# KSO Releases

KSOパイロット版のWindows向け公開配布リポジトリです。

## ダウンロード

[Releases](https://github.com/petit-mint/kso-releases/releases)から最新バージョンをダウンロードしてください。

- `KSO_Pilot_<version>_Distribution.zip`: インストーラーと手順書をまとめた配布パッケージ
- `KSO_Pilot_<version>_x64-setup.exe`: Windows 64ビット版インストーラー
- `KSO_Pilot_<version>_x64-setup.exe.sha256`: インストーラーのSHA-256
- `KSO_Operation_Guide_Pilot_<version>.zip`: 操作ガイド

## SHA-256の確認

PowerShellで次のコマンドを実行し、同梱の`.sha256`ファイルに記載された値と一致することを確認してください。

```powershell
Get-FileHash -Algorithm SHA256 .\KSO_Pilot_<version>_x64-setup.exe
```

## ソースコードについて

このリポジトリは配布ファイル専用です。KSOの開発ソースコードは含まれていません。
