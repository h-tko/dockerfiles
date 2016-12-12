# 今あるもの

・centos7 + golang
・centos7 + redis

# centos7 + golang


# centos7 + redis

redisサーバとして運用される想定の設定
以下の内容でrun

```
$ docker run --name redis -d centos7_redis
```

redisデフォルトポートでポートフォワード（6379）

webアプリ側のコンテナからは以下の手順で参照する

```
$ docker run --link redis:<好きなalias名（cacheなど）> -i -t cent7_go
```
