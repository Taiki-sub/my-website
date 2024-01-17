---
id: FromCampus
title: 学内からサーバにログインする方法
sidebar_label: 学内からSocSELサーバ
sidebar_position: 1
---

### 学内からsshを用いることでSocSELサーバにログインする方法

### 1. サーバに接続

  - ターミナルに以下を入力
    ```bash
      ssh ユーザー名@133.42.160.101
    ```
    - ユーザ名を確認したい場合は以下を入力
      ```bash
      whoami
      ```
    - サーバ2にログインしたい場合は以下を入力
      ```bash
      ssh ユーザー名@133.42.160.102
      ```
    - 初めてログインの場合には
      ```bash
      Are you sure you want to continue connecting (yes/no/[fingerprint])? 
      ```
      と表示されることがあるので、
      ```bash
      yes
      ```
      を入力してEnter(return)を押す

### 2. パスワードの設定

  - 「1. サーバに接続」を完了すると
    ```bash
    ユーザ名@133.42.160.101's password:
    ```
    と表示されるので自身の設定したいパスワード入力
  - ターミナルの表示が
    ```bash
    [ユーザ名@socsel-brain-001 ~]$
    ```
    に左側の表示が変わればログイン完了

### 3. 接続の解除

  - sshの接続解除
    ```bash
    exit
    ```
    を入力するとログアウト