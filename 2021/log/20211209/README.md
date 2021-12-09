# 第1回監視勉強会（2021/12/09）の記録
## アジェンダ
```
第1回監視勉強会アジェンダ
■ 監視勉強会の目的やゴールの説明
https://github.com/kichiram/study/tree/main/2021
■ 学習コンテンツの下記を実施
https://github.com/kichiram/study/blob/main/2021/contents
1. AWS EC2インスタンス作成と設定
2. 監視コンポーネントの概要説明
```
## 学習ログ
アジェンダ通りに進行しました。
## 質疑応答
### EC2のキーペアはインスタンス作成後でも作成できるか？
可能です。[こちら](https://ap-northeast-1.console.aws.amazon.com/ec2/v2/home?region=ap-northeast-1#KeyPairs)から作成できるようです。
### grafanaはグラフを表示する以外の用途はあるか？
基本的には可視化するために利用するのでそれ以外はありません。アラート機能もありますが、prometheusと併用するのであればprometheusの方が優れているためあまり利用しません。
### prometheusのクエリとはどういうものか？
promSQLという独自のものです。データベースで利用するSQLとは別物です。promSQLについては今後説明予定です。
## その他
特になし
