<p align="center"> <img src="https://user-images.githubusercontent.com/91356865/144049159-1ebbd095-87d2-4a3c-81cb-277cc1d4c7b7.png" width="300"> </p> <p align="center"> Starting Up the API Environment on a "Full-of-Beans" SandBox </p>

***

# sap-sandbox-rmq-c4hana
sap-sandbox-rmq-c4hana は、[sap-sandbox-c4hana](https://github.com/latonaio/sap-sandbox-c4hana) における API READS の内、RabbitMQ からのメッセージを受けてイベントドリブンでランタイムを実行し、アウトプットとしてRabbitMQへメッセージを出力するよう対応されたリソースをまとめたリポジトリです。  
sap-sandbox の 「sandbox」は、Netflix 韓国ドラマ 「START-UP」 より、すべての開発者のための 地ならし になればという想いから命名されました。  
なお、各リポジトリのリソースは、そのままクラウド環境におけるアプリケーションにも適用可能です。  

## 前提条件  
sap-sandbox-rmq-c4hana は、オンプレミス版である（＝クラウド版ではない）SAPC4HANA API の利用を前提としています。  
クラウド版APIを利用する場合は、ご注意ください。

## Latona における SAP 領域・機能ごと の リソース整備状況    
下の図において、チェックマークが付いているリソースが、Latonaにおいて(少なくとも1次の)整備が行われたものであり、github上に公開されています。  

![リソース整備状況](documents/sap-sandbox-c4hana.png)

## sap-sandbox-rmq-c4hana における SAP領域・機能 の選択基準
sap-sandbox-rmq-c4hana におけるSAP領域・機能は、SAP C4HANA のあらゆる領域・機能のうち、世界中の企業で繰り返し利用される、利用頻度の高いものと判断されるものが、選択されています。

## Port 番号 の 適用方針 
| type      | Area         | ポート番号    |
| :-------- | :----------------------------- | :---------------------------------------- |
| NodePort  | Central Functions              | 30591-30600 |
|           | Touch Points             |    30601-30610    |
|           | Operations |          30611-30620                                 |
|           | Employee |30621-30625|
|           | Authentication           |             30626-30630                              |