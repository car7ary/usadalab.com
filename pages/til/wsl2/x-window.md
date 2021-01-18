---
layout: default
title: x-window
---

# X Window System

## Server Application

VcXsrv Windows X Server

## 初期セットアップ

1. `xlaunch.exe`を実行して設定ファイル`config.xlaunch`を作成
1. Startup フォルダに`config.xlaunch`を配置。これによって Windows 起動時に自動でサーバが実行される。
1. WSL から Display を認識できるように設定を追加する
   ```bash
   # .profile
   export DISPLAY=$(cat /etc/resolv.conf | grep nameserver | awk '{print $2}'):0
   ```
   ```bash
   $ exec $SHELL -l
   ```
