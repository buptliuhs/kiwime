+++ 
draft = false
date = 2020-03-17T21:33:18+13:00
title = "Redis"
slug = "" 
tags = []
categories = []
thumbnail = "images/tn.png"
description = ""
+++

## Run Redis in a Docker Container
```
$ docker run --name some-redis -d redis
```

## Connect to Redis from another Docker Container
```
$ docker run --name some-redis-application --link some-redis:redis -d debian
```

```
$ docker run -it --name some-redis-cli --link some-redis:redis --rm redis redis-cli -h redis -p 6379
redis:6379>
redis:6379> set a 1
OK
redis:6379> get a
"1"
redis:6379>
```

## Run Redis with Port-Forwarding
```
$ docker run --name some-redis -p 7001:6379 -d redis
```

## Install redis-cli
```
$ npm install -g redis-cli
```

```
$ rdcli -h localhost -p 7001
localhost:7001> set a 1
OK
localhost:7001> get a
1
localhost:7001>
```