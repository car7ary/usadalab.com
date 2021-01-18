---
layout: default
title: docker
---

# Docker

## docker.credentials.errors.InitializationError

### エラーログ

```bash
$ docker-compose up
docker.credentials.errors.InitializationError: docker-credential-desktop.exe not installed or not available in PATH
```

### 原因

docker-credential-desktop.exe に Path が通っていないため。

### 解決方法

`.profile`に Path を追加

```bash
$ echo "/mnt/c/Program Files/Docker/Docker/resources/bin" >> ~/.profile
$ exec $SHELL -l
$ echo $PATH | grep Docker
```
