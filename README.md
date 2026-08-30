# KSO Releases

KSOパイロット版のWindows向け公開配布リポジトリです。

## 最新版

**KSO Pilot 0.5.0**をプレリリースとして公開しています。

[KSO Pilot 0.5.0のダウンロードと変更履歴](https://github.com/petit-mint/kso-releases/releases/tag/v0.5.0)

パイロット版は正式版に向けた検証中のリリースです。配信本番で使用する前に、使用するPC、OBS設定、セットリストで動作を確認してください。

## 0.5.0の主な変更

- 利用者が保存先を選べるマイソング／レパートリー管理
- マイソングとセットリストの双方向連携、アーティスト情報、曲順ドラッグ、複製
- 実際の歌唱履歴、歌唱回数・最終歌唱日の自動更新と取り消し
- Markdown／CSV／YouTubeチャプター用の配信後出力
- セットリストv1と既存のテーマ、ショートカット、OBS設定との互換性維持

## ダウンロード

初めて利用する場合は、インストーラーと操作ガイドをまとめた`KSO_Pilot_0.5.0_Distribution.zip`を推奨します。

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

0.5.0インストーラーの正しいSHA-256は次の値です。

```text
dded0f28fb4ad9f952b2861de5264106d8f0ee366d186d0613e0b33f9cd2df16
```

`Get-FileHash`を利用できない環境では、Windows標準の次のコマンドでも確認できます。

```powershell
certutil -hashfile .\KSO_Pilot_<version>_x64-setup.exe SHA256
```

## Microsoft Defender SmartScreenが表示された場合

KSOパイロット版は現在コード署名されていないため、正しい配布ファイルでもWindowsの「このアプリは認識されませんでした」という警告が表示されることがあります。この警告が表示されてもインストールは可能です。

このGitHub Releasesから入手したファイルであり、ファイル名とSHA-256が上記の値または同梱の`.sha256`ファイルと一致することを確認した後、SmartScreen画面の「詳細情報」を選択し、続いて「実行」を選択してください。配布元を確認できない場合やSHA-256が一致しない場合は実行しないでください。

## ソースコードについて

このリポジトリは配布ファイル専用です。KSOの開発ソースコードは含まれていません。
