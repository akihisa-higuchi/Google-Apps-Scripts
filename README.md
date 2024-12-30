# Google Apps Script

## GmailToPDF

Gmailに届いたメール本文を、Googleドライブの指定フォルダにファイル名 yyyyMMdd_HHmmss_Vendor.pdf のルールでPDFとして自動保存するためのスクリプトです。
メールの差出人ドメインに応じて、ファイル名に設定する名前を決めることができます。

電子帳簿保存法に対応するために、AppleやAirレジなどのメールそのものをPDFファイルとして保存する必要性がある領収書メールの自動保存などに活用できます。

### 必要な事前準備

- Gmailでラベル[Receipt]とその直下にサブラベル[Waiting]を作成
- Gmailのフィルタ機能で対象にしたいメールに専用ラベル（Receipt/Waiting）を設定するフィルタを作る
- Googleドライブで、Google Apps Scriptを新規作成してこのスクリプトをコピーし、FOLDER_ID_INVOICEの箇所に保存対象としたいGoogleドライブフォルダのフォルダIDを設定（フォルダIDは、フォルダを開いた時のアドレスの https://drive.google.com/drive/folders/xxxxx のxxxxxx）
- Google Apps Scriptのトリガー設定で、毎日6時など自動稼働するように設定

## AttachementToDrive

Gmailに届いたメールの添付ファイルを、Googleドライブの指定フォルダにファイル名 元ファイル名_yyyyMMdd_HHmmss.元拡張子 のルールで自動保存するためのスクリプトです。 

### 必要な事前準備

- Gmailでラベル[ToDrive]を作成
- Gmailのフィルタ機能で対象にしたいメールに専用ラベル（ToDrive）を設定するフィルタを作る
- Googleドライブで、Google Apps Scriptを新規作成してこのスクリプトをコピーし、FOLDER_ID_INVOICEの箇所に保存対象としたいGoogleドライブフォルダのフォルダIDを設定（フォルダIDは、フォルダを開いた時のアドレスの https://drive.google.com/drive/folders/xxxxx のxxxxxx）
- Google Apps Scriptのトリガー設定で、毎日6時など自動稼働するように設定
