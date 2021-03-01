## 概要
Remote Containers内でAWSへアクセスを行うために、ホスト環境のaws設定ファイルをマウントする。  
その際、Remote Containers側でプロファイルを指定しなくて済むように、該当のAWSアカウント認証情報がdefaultとして記載された設定ファイルをマウントするようにしている。

### AWS設定ファイルについて
パス: `/.aws/credentials.xxx`（※ xxxには、任意のアカウント識別可能文字列を設定する）  
書式:
```
[default]
region = ap-northeast-1
output=json
aws_access_key_id = XXXX
aws_secret_access_key = XXXX
```