# 学習コンテンツ
## 1. AWS EC2インスタンス作成と設定
Amazon Linuxのインスタンスを作成して利用する方法を理解します。
### 1.1. [EC2インスタンスの作成](https://github.com/kichiram/aws/tree/main/create_ec2_instance/README.md)
Amazon Linuxのインスタンスを作成します。
### 1.2. [EC2インスタンスへの接続方法](https://github.com/kichiram/aws/tree/main/connect_ec2_instance/README.md)
作成したAmazon Linuxのインスタンスに接続します。ブラウザベースでも接続可能なためターミナルなどの準備は不要です。（ただし、エディタなどはすぐバグります）
### 1.3. [外部からssh以外のアクセスを許可する設定](https://github.com/kichiram/aws/tree/main/setup_security/README.md)
動作確認のためブラウザなどから接続するための設定を行ないます。学習環境なので全開にしますが本来は必要最低限にしてください。
## 2. 監視コンポーネントの概要説明
監視コンポーネントの概要を理解します。
### 2.0 サーバ監視入門の入門
その前に。。。
* https://simple-it-life.com/2016/11/06/monit/
### 2.1. [prometheus](https://prometheus.io/)
下記ページをもとにprometheusの概要説明を行ないます。
* https://qiita.com/MetricFire/items/8a16632590ac558a9a14
### 2.2. [grafana](https://grafana.com/)
下記ページをもとにgrafanaの概要説明を行ないます。
* https://qiita.com/Chanmoro/items/a23f0408f0e64658a775
## 3. 監視コンポーネントのインストール
監視コンポーネントのインストール方法を理解します。
### 3.0. システム構成図（実際は1台のサーバに詰め込みますが。。。）
![image](https://user-images.githubusercontent.com/91726058/150090117-165166b7-0eb0-47dd-aaef-00cd0e50daec.png)
### 3.1. [prometheus](https://github.com/kichiram/prometheus/blob/main/install/README.md)
prometheusのインストールを実施します。
### 3.2. [prometheus exporter](https://github.com/kichiram/prometheus/tree/main/exporter/README.md)
prometheusの複数のexporterをインストールを実施します。
### 3.3. [alertmanager](https://github.com/kichiram/alertmanager/blob/main/install/README.md)
alertmanagerのインストールを実施します。
### 3.4. [grafana](https://github.com/kichiram/grafana/blob/main/install/README.md)
grafanaのインストールを実施します。
## 4. [golang](https://golang.org/)
golangについて概要を理解します。
### 4.1.概要説明
下記ページをもとにgolangの概要説明を行ないます。
* https://www.yunabe.jp/docs/why_golang_is_good.html
* https://go-tour-jp.appspot.com/welcome/1
### 4.2. [インストール](https://github.com/kichiram/golang/blob/main/install/README.md)
golangのインストールを実施します。
### 4.3. [検証用HTTP Serverのセットアップ](https://github.com/kichiram/golang/blob/main/http_server/README.md)
golangで作成された検証用のHTTP Serverをセットアップします。
## 5. prometheusの設定
prometheusの設定方法を理解します。
### 5.0. [prometheusのdaemonの設定ファイル修正](https://github.com/kichiram/prometheus/tree/main/change_setting)
### 5.1. [起動オプション](https://prometheus.demo.do.prometheus.io/flags)
prometheusの起動オプションについて重要なものを説明します。
### 5.2. [設定ファイルについて](https://github.com/kichiram/prometheus/tree/main/config/README.md)
prometheusの設定ファイルについて概要説明を行ないます。
#### 5.2.1. [監視ターゲット設定](https://github.com/kichiram/prometheus/tree/main/config/scrape_configs)
監視ターゲットを設定してprometheusで確認できるようにします。
#### 5.2.2. [grok exporter設定](https://github.com/kichiram/prometheus/tree/main/exporter/grok_exporter/config)
prometheusのgrok_exporterの設定を変更してログのメトリクスを出力します。
#### 5.2.3. [アラートルール設定](https://github.com/kichiram/prometheus/tree/main/config/alerting_rules)
アラートを設定してprometheusで確認できるようにします。
#### 5.2.4. [レコーディングルール設定](https://github.com/kichiram/prometheus/tree/main/config/recording_rules)
レコーディングルールを設定してprometheusで確認できるようにします。
## 6. alertmanagerの設定
alertmanagerの設定方法を理解します。
### 6.1. [設定ファイルについて](https://github.com/kichiram/alertmanager/blob/main/config/README.md)
alertmanagerの設定ファイルについて概要説明を行ないます。
#### 6.1.1. [アラート通知設定](https://github.com/kichiram/alertmanager/tree/main/config/alertmanager)
アラート通知を設定してメールで確認できるようにします。
### 6.2. [サイレンス](https://github.com/kichiram/alertmanager/blob/main/silence/README.md)
アラート通知を停止する方法を理解します。
## 7 .grafanaの設定
grafanaの設定方法を理解します。
#### 7.1. [データソース設定](https://github.com/kichiram/grafana/blob/main/datasource/README.md)
データソースを設定してprometheusのメトリクスを利用できるようにします。
#### 7.2. [ダッシュボード作成](https://github.com/kichiram/grafana/blob/main/dashboards/README.md)
ダッシュボードとグラフを作成してprometheusのメトリクスを可視化します。
## 8 .まとめと補足
#### 8.1. まとめ
[今回の勉強会で利用した環境、技術](https://github.com/kichiram/study/tree/main/2021#%E5%88%A9%E7%94%A8%E7%92%B0%E5%A2%83%E6%8A%80%E8%A1%93)
- [prometheus](https://github.com/kichiram/prometheus)は私が利用した中で重要だと思われる設定やexporterについて説明しましたが、他にも有用なものがありますので補足で追加説明します。
- [alertmanager](https://github.com/kichiram/alertmanager)はメール通知のみでしたが、slackに通知する場合は[こちら](https://zenn.dev/empenguin/articles/721ba3164a2196)のページが参考になります。
- [golang](https://github.com/kichiram/golang)は軽く触れただけですが、興味があれば[A Tour of Go](https://go-tour-jp.appspot.com/welcome/1)などで学習頂ければと思います。
#### 8.2. 補足
- バッチの監視
  - prometheusはsnode（監視サーバ）から監視に必要な情報（メトリクス）を収集するため拡張性などに優れていますが、mnode(監視対象サーバ)側で常にメトリクスを公開している必要があるためバッチ処理の監視には向いていません。バッチ処理の監視は下記のいずれかで実施すると良いです。
    - [pushgateway](https://qiita.com/MetricFire/items/c4753396259923a0c9e2)というメトリクス送信型のものを利用する
    - node_exporterの[Textfile Collector](https://qiita.com/sugitak/items/25007e6bbb18ead107af)というのを利用してnode_exporterにメトリクスを送る
    - ログを適切に出力して[grok_exporter](https://github.com/kichiram/prometheus/tree/main/exporter/grok_exporter)で状況がわかるようメトリクスを出力する
- [prometheusの関数](https://prometheus.io/docs/prometheus/latest/querying/functions/)
  - 監視で便利な関数
    - [changes](https://prometheus.io/docs/prometheus/latest/querying/functions/#changes)：メトリクスの値が変更されたかを確認したい場合
    - [delta](https://prometheus.io/docs/prometheus/latest/querying/functions/#delta)：期間の最初から最後までで増加した値を知りたい場合。ただし、カウンタのリセットには対応していない
    - [increase](https://prometheus.io/docs/prometheus/latest/querying/functions/#increase)：上記同様でカウンタのリセットにも対応しているが、値が減るようなメトリクスだと誤作動する。
    - [label_replace](https://prometheus.io/docs/prometheus/latest/querying/functions/#label_replace)：ラベルの値を正規表現で置換したい場合
- [prometheusの演算子](https://prometheus.io/docs/prometheus/latest/querying/operators/)
  - sum by：指定したラベル単位に値を集計したい場合
  - sum without：指定したラベル以外で値を集計したい場合
- メトリクスの長期保存
  - 監視サーバには様々なメトリクスが必要なため容量の観点などからメトリクスの長期保存には不向きです。メトリクスの長期保存は下記のいずれかで実施すると良いです。
    - 別途メトリクス長期保存用のprometheusを用意し、メトリクスを厳選して保存する
    - [remote storage](https://prometheus.io/docs/prometheus/latest/storage/#remote-storage-integrations)を用意して、メトリクスを厳選して保存する。利用できる[storage](https://prometheus.io/docs/operating/integrations/#remote-endpoints-and-storage)
