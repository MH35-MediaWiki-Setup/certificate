# Certificate
ACMでのSSL証明書発行用

## 使い方

1. `aws cloudformation deploy --template-file formation.yml --stack-name [stack name] --parameter-overrides DomainName=[certificate domain name]`する
2. しばらく待つと、Certificate ManagerのサービスコンソールにDNSレコードの設定内容が出てくるので設定する
3. しばらく待つ

なお、このテンプレートはサーバを設置するリージョンとus-east-1リージョンの2回、デプロイが必要なので、デフォルトでないリージョンでは`--region`オプションを指定してリージョン指定すること
