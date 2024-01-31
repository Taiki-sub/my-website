---
id: docker_download
title: dockerのダウンロードとチュートリアル
sidebar_label: dockerのダウンロードとチュートリアル
sidebar_position: 1
---

### Dockerのダウンロードとチュートリアル

### 1. Dockerとは

  - Dockerとは、コンテナ型仮想化技術を用いることで，再現可能な仮想環境を構築するためのソフトウェアです
  <img src={require('./img/docker_kiso.png').default} width="100%"/>
  - Dockerを使うことで、簡単に，誰でも，同じ環境を構築できます

### 2. Docker Desktopのインストール

  - 以下のリンクより自身のMacチップに応じたバージョンをダウンロード
    https://matsuand.github.io/docs.docker.jp.onthefly/desktop/mac/install/
  - ダウンロードファイルを実行し、インストールを完了させる
  - この画面が出れば成功
  <img src={require('./img/docker_toppage.png').default} width="100%"/>

### 2. Dockerを動かしてみる
  - Dockerの利用は以下のような手順で行います
  <img src={require('./img/docker_container.png').default} width="100%"/>
  - 今回は“Hello world”と出力するだけの実行ファイルをDockerコンテナ上で動かします
  
  #### 1. 実行ファイルの作成
  - 作業用ディレクトリを作成し、以下の内容をファイル名「helloworld」で保存する
  ```
  #!/bin/sh
  echo "Hello, World"
  ```
  
  #### 2. DockerFileの作成
  - 以下の内容をファイル名「dockerfile」で保存する
  ```
  FROM ubuntu:16.04
  COPY helloworld /usr/local/bin
  RUN chmod +x /usr/local/bin/helloworld
  CMD ["helloworld"]
  ```
  #### 3. Dockerイメージの作成
  - `cd`コマンドで作業用ディレクトリに移動し、以下のコマンドを実行する
  ```
  docker image build -t helloworld:latest .
  ```
  - 以下のように表示されればビルド成功
  <img src={require('./img/docker_image.png').default} width="100%"/>

  #### 4. Dockerコンテナの作成
  - 以下のコマンドを実行する
  ```
  docker container run helloworld:latest
  ```
  - "helloworld"と表示されれば成功
