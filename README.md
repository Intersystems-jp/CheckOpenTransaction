# ジャーナルファイルにオープンされたままのトランザクションが残っていないかを確認するサンプル

[サンプルコード](./JournalUtility.cls)を使用して、ジャーナルファイルにオープンされたままのトランザクションが残っていないか確認することができます。

残っている場合は、ジャーナルファイル名とジャーナルレコード詳細が表示されます。

**【注意】**
確認対象のジャーナルファイルサイズが大きい場合、ジャーナルファイルが多数ある場合は、**実行に時間がかかるため**、弊社サポートセンターまでご連絡ください。

## 使用方法

お好みのネームスペースにソースコードをインポートしてご利用ください。

管理ポータル／スタジオを使用している場合は、インポートメニューで[サンプルコード（JounalUtility.cls）](./JournalUtility.cls) を指定してインポートを行います。


VSCode を使用している場合は、[settings.json](./.vscode/settings.json) に接続先情報を指定し、接続を確認した後、[サンプルコード（JounalUtility.cls）](./JournalUtility.cls) を保存することでインポートできます。

接続先指定方法について詳しくは、[VSCode を使ってみよう！](https://jp.community.intersystems.com/node/482976)をご参照ください。 


メソッド実行例は以下の通りです。

IRIS／Caché のターミナルを開く、またはログインして、以下実行します。

```
USER>do ##class(ISJ.JournalUtility).GetOpenTransaction()

現在のジャーナルファイル名：/usr/irissys/mgr/journal/20210330.002

〇〇　オープン中の対象ジャーナルレコード一覧　〇〇

=== File Name : /usr/irissys/mgr/journal/20210330.001 ===
Address : TimeStamp : ProcessID : RemoteSystemID : TypeName : Transaction
1834156 : 2021-03-30 13:19:00 : 5194 : 1073741824 : BeginTrans : 1
```
