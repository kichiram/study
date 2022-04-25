# 第6回監視勉強会（2022/04/25）の記録
## アジェンダ
```
第6回監視勉強会アジェンダ
■ 学習コンテンツの下記を実施
https://github.com/kichiram/study/blob/main/2021/contents
5.2.2. grok exporter設定
5.2.3. アラートルール設定
5.2.4. レコーディングルール設定
```
## 学習ログ
5.2.3. [アラートルール設定](https://github.com/kichiram/prometheus/tree/main/config/alerting_rules)のprometheus.ymlの入れ替え方法の4. リロードまで実施
### grok exporter
prometheusでログ監視を実現するexporterの1つ。ログフォーマットを正規表現で定義し、マッチしたログからメトリクスを作ってくれます
### アラートルールファイル
labelのservirityで重要度を設定します。この設定はalertmanagerで通知先をコントロールするなどに使えます
forでアラートまでの待機時間を設定します。再起動直後など一時的な高負荷などはアラートを出したく無い場合に便利です
## 質疑応答
### grok_exporterの[パターンファイル](https://github.com/kichiram/prometheus/blob/main/exporter/grok_exporter/config/patterns/test_httpserver)にある「HTTPSERVER_HELLO_NAME」というのは何か？
「HTTPSERVER_HELLO_LOG」がログ全体のフォーマットを定義したもので、その最後に出力される任意の文字列です
### test_httpseverでnameパラメータを読んでいるのはどこか？
リクエストから[FormValue](https://github.com/kichiram/golang/blob/main/testgo/test_httpserver.go#L34)を使って取得しています
### prometheus.ymlの設定ファイルをチェックした結果がドキュメントと異なるが問題無いか？
アラートルール設定などを追加した場合、複数のファイルがチェックされますが全て「SUCCESS」であれば問題ありません
## その他
時間が想定より掛かってしまい予定通り進捗せずすみませんでした。。。
後日時間が取れたらアラートルール設定などでよく使う[function](https://prometheus.io/docs/prometheus/latest/querying/functions/)の説明もしたいと思います
