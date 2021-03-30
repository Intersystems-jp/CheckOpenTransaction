# ジャーナルファイルにオープンされたままのトランザクションが残っていないかを確認するサンプル

**【注意】**

確認対象のジャーナルファイルサイズが大きい場合、ジャーナルファイルが多数ある場合は、**実行に時間がかかるため**、弊社サポートセンターまでご連絡ください。


サンプルコードでは、オープンされたままのトランザクションが存在しているかどうかの確認と、存在する場合は対象ファイル名とジャーナルレコード情報が出力されます。

実行例は以下の通りです。

IRIS／Caché のターミナルを開く、またはログインして、以下実行します。

```
USER>do ##class(ISJ.JournalUtility).GetOpenTransaction()

現在のジャーナルファイル名：/usr/irissys/mgr/journal/20210330.002

〇〇　オープン中の対象ジャーナルレコード一覧　〇〇

=== File Name : /usr/irissys/mgr/journal/20210330.001 ===
Address : TimeStamp : ProcessID : RemoteSystemID : TypeName : Transaction
1834156 : 2021-03-30 13:19:00 : 5194 : 1073741824 : BeginTrans : 1
```
