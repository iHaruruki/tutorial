---
layout: default
title: "Config"
lang: "ja"
parent: "Git"
nav_order: 2
permalink: "/git/config/"
---

# ユーザー情報を設定する
Gitのユーザ設定（ユーザー名，メールアドレス）を行います．
ここで設定されたユーザ情報は変更履歴を記録する際に一緒に記録され，誰がその変更履歴を記録したのかを確認する場合に使われます．

## ユーザー名
```bash
git config --global user.name "ユーザー名を書く"
```
設定を確認する
```bash
git config --global user.name
# {ユーザー名として設定した値が表示される}
```
## メールアドレス
```bash
git config --global user.email "メールアドレスを書く"
```
設定を確認する
```bash
git config --global user.email
# {メールアドレスとして設定した値が表示される}
```