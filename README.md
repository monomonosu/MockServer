# MockServer
APIモックサーバーprism使用テスト。
- とりあえずyaml作成

Dockerを使用する場合
- yamlファイル作成
- docker run --init --rm -v $(pwd):/tmp -p 4010:4010 stoplight/prism:4 mock -h 0.0.0.0 "/tmp/swagger.yaml"

``` 
[5:42:35 PM] › [CLI] …  awaiting  Starting Prism…
[5:42:43 PM] › [CLI] ℹ  info      GET        http://0.0.0.0:4010/users
[5:42:43 PM] › [CLI] ℹ  info      POST       http://0.0.0.0:4010/users
[5:42:43 PM] › [CLI] ℹ  info      GET        http://0.0.0.0:4010/users/848
[5:42:43 PM] › [CLI] ▶  start     Prism is listening on http://0.0.0.0:4010 
```

APIを叩く事ができる。


