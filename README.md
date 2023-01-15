# GitHub Actionsテスト
- EC2にデプロイ（サンプル）

## デプロイ手順
1. mainブランチにpushする
2. GitHub Actionsが走る
3. sshセキュリティグループで22番ポートを開ける
4. EC2にssh接続する
5. git pullする
6. sshセキュリティグループで22番ポートを閉じる

## sercretsの設定
下記で設定する <br/>
settings > Secrets and variables > New repository secret
<br/>
- AWS_ACCESS_KEY（AWSアクセスキー）
- AWS_SECRET_KEY（AWSシークレットキー）
- EC2_USER_NAME（EC2のユーザー名）
- EC2_HOST_NAME（EC2のホスト名）
- EC2_SECURITY_GROUP_ID（EC2のセキュリティグループID）
- GIT_PRIVATE_KEY（認証鍵）

## 関連記事
- [Github Actions で secret を使う](https://qiita.com/inouet/items/c7d39ac4641c05eec4a0)
- [GitHub ActionでAWS EC2にデプロイを実行する(Amazon Linux)](https://qiita.com/kubota_ndatacom/items/1055df9b1568b86ddb41#4-awscli%E3%81%AE%E5%88%9D%E6%9C%9F%E8%A8%AD%E5%AE%9A)

