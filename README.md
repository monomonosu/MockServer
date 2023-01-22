# MockServer
APIモックサーバーprism使用テスト。
- とりあえずyaml作成

Dockerを使用する場合
- docker run --init --rm -v $(pwd):/tmp -p 4010:4010 stoplight/prism:4 mock -h 0.0.0.0 "/tmp/swagger.yaml"

``` 
[5:42:35 PM] › [CLI] …  awaiting  Starting Prism…
[5:42:43 PM] › [CLI] ℹ  info      GET        http://0.0.0.0:4010/users
[5:42:43 PM] › [CLI] ℹ  info      POST       http://0.0.0.0:4010/users
[5:42:43 PM] › [CLI] ℹ  info      GET        http://0.0.0.0:4010/users/848
[5:42:43 PM] › [CLI] ▶  start     Prism is listening on http://0.0.0.0:4010 
```

APIを叩く事ができる。


ローカルで実行環境を構築する場合。  
環境によって違いはあるかもだが、Docker起動後に下記コマンドでローカルで立ち上げる事ができるようになった。
- npm install --save-dev @stoplight/prism-cli
- prism mock swagger.yaml
![hoge](images/2023-01-22%2016.55.32.png)

