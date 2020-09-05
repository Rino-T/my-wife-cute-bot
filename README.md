# 今日も妻が可愛い Tweet Bot

「今日も妻が可愛い」と定期的に呟くためだけのものです。

AWS LambdaにAWS SAMを利用してデプロイして利用します。

## Requirements

* Runtime: Python3.8
* [aws-sam-cli](https://docs.aws.amazon.com/ja_jp/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html)
* tweepy3.9.0
* Twitter API用の各種キー（Twitter Developerに登録して取得してください）

Twitter APIの各種キーはAWS Lambdaの環境変数として設定して使います。

## Deploy

AWS CLI用ののクレデンシャルなどは設定されているものとします。

```bash
$ sam build
$ sam deploy --guided
``` 

`sam deploy --guided` をすると、各種パラメータを要求されるので、適切に設定してください。
このタイミングでTwitter API用の環境変数が設定されます。

## Delete AWS Resources

クラウドフォーメーションのスタックを削除してください。