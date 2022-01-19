# 学習コンテンツ（作成中）
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
lertmanagerのインストールを実施します。
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
### 6.1. [設定ファイルについて]()
alertmanagerの設定ファイルについて概要説明を行ないます。
#### 6.1.1. [アラート通知設定]()
アラート通知を設定してメールで確認できるようにします。
## 7 .grafana
grafanaの設定方法を理解します。
#### 7.1. [データソース設定]()
データソースを設定してprometheusのメトリクスを利用できるようにします。
#### 7.2. [ダッシュボード作成]()
ダッシュボードとグラフを作成してprometheusのメトリクスを可視化します。
