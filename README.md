# Google Apps Script

## GmailToPDF

Gmailに届いたメール本文を、差出人アドレス（ドメインのみでも可）を条件として、Googleドライブの指定フォルダにファイル名 yyyyMMdd_HHmmss_Vendor.pdf のルールでPDFとして自動保存するためのスクリプトです。

電子帳簿保存法に対応するために、AppleやAirレジなどのメールそのものをPDFファイルとして保存する必要性がある領収書メールの自動保存などに活用できます。

### 必要な事前準備

- Gmailでラベル[ToPDF]を作成
- Gmailのフィルタ機能で対象にしたいメールに専用ラベル（ToPDF）を設定するフィルタを作る
- Googleドライブで、Google Apps Scriptを新規作成してこのスクリプトをコピーし、vendorsの配列に["対象メールの差出人アドレス（ドメインのみでも可）","ファイル名に付けたい名前（Appleなど）", "保存対象としたいGoodleドライブのフォルダID", "処理後に追加したいラベル"] を設定（フォルダIDは、フォルダを開いた時のアドレスの https://drive.google.com/drive/folders/xxxxx のxxxxxx）
- Google Apps Scriptのトリガー設定で、毎日6時など自動稼働するように設定

## AttachementToDrive

Gmailに届いたメールの添付ファイルを、差出人アドレスとメールの件名に含まれる文字を条件として、Googleドライブの指定フォルダにファイル名 [元ファイル名or新しいファイル名_yyyyMMdd_HHmmss.元拡張子] のルールで自動保存するためのスクリプトです。 

### 必要な事前準備

- Gmailでラベル[ToDrive]を作成
- Gmailのフィルタ機能で対象にしたいメールに専用ラベル（ToDrive）を設定するフィルタを作る
- Googleドライブで、Google Apps Scriptを新規作成してこのスクリプトをコピーし、targetFoldersの配列に["対象メールの差出人アドレス（ドメインのみでも可）","件名に含まれる文字", "保存対象としたいGoodleドライブのフォルダID", "新しいファイル名(空白なら元のファイル名に)"]を設定（フォルダIDは、フォルダを開いた時のアドレスの https://drive.google.com/drive/folders/xxxxx のxxxxxx）
- Google Apps Scriptのトリガー設定で、毎日6時など自動稼働するように設定
