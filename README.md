# Google Apps Script

## ReceiptMailToPDF

AppleやAirレジなどのメールそのものをPDF化する必要性がある領収書メールを、Googleドライブの指定フォルダにファイル名 yyyyMMdd_HHmmss_Vendor.pdf のルールでPDFとして自動保存するためのスクリプト

### 必要な事前準備

- Gmailでラベル[Receipt]とその直下にサブラベル[Waiting]を作成
- Gmailのフィルタ機能で対象にしたいメールに専用ラベル（Receipt/Waiting）を設定するフィルタを作る
- Googleドライブで、Google Apps Scriptを新規作成してこのスクリプトをコピーし、FOLDER_ID_INVOICEの箇所に保存対象としたいGoogleドライブフォルダのフォルダIDを設定（フォルダIDは、フォルダを開いた時のアドレスの https://drive.google.com/drive/folders/xxxxx のxxxxxx）
- Google Apps Scriptのトリガー設定で、毎日6時など自動稼働するように設定
