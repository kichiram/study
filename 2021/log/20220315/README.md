# 第5回監視勉強会（2022/03/15）の記録
## アジェンダ
```
第4回監視勉強会アジェンダ
■ 学習コンテンツの下記を実施
https://github.com/kichiram/study/blob/main/2021/contents
5. prometheusの設定
5.0. prometheusのdaemonの設定ファイル修正
5.1. 起動オプション
5.2. 設定ファイルについて
5.2.1. 監視ターゲット設定
```
## 学習ログ
アジェンダ通りに進行しました。
### 主な起動オプション
* config.file：設定ファイルのパス
* storage.tsdb.path：メトリクスの保存先
* storage.tsdb.retention.time：メトリクスの保存期間
## 質疑応答
### prometheusをreloadできるようにするのはなぜか
再起動だと一時的にメトリクスの収集が停止し、停止すると一時的にメトリクスが途切れアラートなどを検知出来ない可能性があるため。
### prometheusの起動オプションの設定はどのようにやるのか
実行時に指定します。今回の場合はprometheus.serviceのファイルにオプションを追記して再起動します。
## その他
