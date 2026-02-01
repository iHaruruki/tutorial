---
layout: default
title: "setup"
lang: "ja"
parent: "Docker"
nav_order: 1
permalink: "/docker/setup/"
---


# Install WSL(Windows Subsystem for Linux)
1. `PwerShll`を管理者モードで開く（右クリックして，「管理者で開く」）
2. コマンドを入力
```shell
wsl --install
```
3. コンピュータを再起動する

# Install Docker Desktop
1. [Get Started with Docker](https://www.docker.com/get-started/)をブラウザで開く
2. [For Windows user]`Download for Windows-AMD64`をダウンロード

<img src="../../assets/images/docker/download.png" alt="Download" width="80%">

3. ダウンロードした`Docker Desktop Installer.exe`をダブルクリックして，インストール開始
4. `Allow Windows Container to be used with this installation`以外にチェック

<img src="../../assets/images/docker/configration.png" alt="Download" width="80%">

5. `Close and restart`をクリックして，パソコンを再起動する

<img src="../../assets/images/docker/restart.png" alt="Download" width="80%">

# Docker run
1. `Docker Desktop`を起動
2. `Accept`をクリック

<img src="../../assets/images/docker/accept.png" alt="Download" width="80%">

3. `Skip`をクリックして，アカウント登録は行わない（今後，`Docker Hub`を使う予定がある場合は行った方がよい）
4. Window右下の`>_`をクリックし，ターミナル(PowerShell)を開く

<img src="../../assets/images/docker/opening.png" alt="Download" width="80%">

5. `Enable`をクリックする

<img src="../../assets/images/docker/open_terminal.png" alt="Download" width="80%">
<img src="../../assets/images/docker/start_terminal.png" alt="Download" width="80%">

6. ターミナルに以下のコマンドを入力し，Docker imageのpullとコンテナの起動を行う  
（Docker image(size: 12GB)をダウンロードするので10分ほど待つ）
```shell
# docker run --name [CONTAINER NAME] -p <ホスト側のポート>:<コンテナ側のポート> --security-out [seccomp=unconfined] --shm-size=[MEMORY SIZE] [DOCKER IMAGE NAME]
docker container run --name ubuntu2404-ros2 -p 6080:80 --security-opt seccomp=unconfined --shm-size=512m iharuruki/ubuntu2404-ros2-jazzy
```
<img src="../../assets/images/docker/docker_run.png" alt="Download" width="80%">

7. `docker run`実行中に`Do you want to allow public and private networks to access this app?`と聞かれた場合は`Allow`する

8. 以下のメッセージが表示されたら，コンテナの起動が成功した
```shell
2026-02-01 19:45:46,745 INFO success: novnc entered RUNNING state, process has stayed up for > than 1 seconds (startsecs)
2026-02-01 19:45:46,745 INFO success: vnc entered RUNNING state, process has stayed up for > than 1 seconds (startsecs)
```

9. ブラウザを開き，以下のポートにアクセスする  
[http://127.0.0.1:6080](http://127.0.0.1:6080)

10. `noVNE`と表示されたら，`Connect`をクリック

<img src="../../assets/images/docker/vnc.png" alt="Download" width="80%">
<img src="../../assets/images/docker/desktop.png" alt="Download" width="80%">