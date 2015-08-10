# create-ff-csr

SSLサーバー証明書の申請に必要な署名要求(CSR)を作成するスクリプトです。

## Usage

### Generate a new KEY

    rake "gen_key[domainname]"

### Generate a new CSR

    rake "gen_csr[domainname]"
