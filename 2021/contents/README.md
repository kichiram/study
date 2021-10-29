# 学習コンテンツ
## 1. AWS EC2インスタンス作成と設定
### 1.1. [EC2インスタンスの作成](https://github.com/kichiram/aws/tree/main/create_ec2_instance/README.md)
Amazon Linuxのインスタンスを作成します。
### 1.2. [EC2インスタンスへの接続方法](https://github.com/kichiram/aws/tree/main/connect_ec2_instance/README.md)
作成したAmazon Linuxのインスタンスに接続します。ブラウザベースでも接続可能なためターミナルなどの準備は不要です。（ただし、エディタなどはすぐバグります）
### 1.3. [外部からssh以外のアクセスを許可する設定](https://github.com/kichiram/aws/tree/main/setup_security/README.md)
動作確認のためブラウザなどから接続するための設定を行ないます。学習環境なので全開にしますが本来は必要最低限にしてください。
## 2. 監視コンポーネントの概要説明
### 2.1. [prometheus](https://prometheus.io/)
* https://qiita.com/MetricFire/items/8a16632590ac558a9a14
### 2.2. [grafana](https://grafana.com/)
* https://qiita.com/Chanmoro/items/a23f0408f0e64658a775
## 3. 監視コンポーネントのインストール
### 3.1. [prometheus](https://github.com/kichiram/prometheus/blob/main/install/README.md)
### 3.2. [prometheus exporter](https://github.com/kichiram/prometheus/tree/main/exporter/README.md)
### 3.3. [alertmanager](https://github.com/kichiram/alertmanager/blob/main/install/README.md)
### 3.4. [grafana](https://github.com/kichiram/grafana/blob/main/install/README.md)
## 4. [golang](https://golang.org/)
### 4.1.概要説明
* https://www.yunabe.jp/docs/why_golang_is_good.html
* https://go-tour-jp.appspot.com/welcome/1
### 4.2. [インストール](https://github.com/kichiram/golang/blob/main/install/README.md)
### 4.3. [検証用HTTP Serverのセットアップ](https://github.com/kichiram/golang/blob/main/http_server/README.md)
## 5. prometheusの設定
### 5.1. [起動オプション](https://prometheus.demo.do.prometheus.io/flags)
### 5.2. [設定ファイルについて](https://github.com/kichiram/prometheus/tree/main/config/README.md)
#### 5.2.1. [監視ターゲット設定](https://github.com/kichiram/prometheus/tree/main/config/scrape_configs)
#### 5.2.2. [アラートルール設定]()
#### 5.2.3. [レコーディングルール設定]()
#### 5.2.4. [アラートルール設定]()
## 6. alertmanagerの設定
### 6.1. [設定ファイルについて]()
#### 6.1.1. [アラート通知設定]()
## 7 .grafana
#### 7.1. [データソース設定]()
#### 7.2. [ダッシュボード作成]()
