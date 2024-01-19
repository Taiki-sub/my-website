---
id: FromCampus
title: 学内からサーバにログインする方法
sidebar_label: 学内からSocSELサーバ
sidebar_position: 1
---

### 学内からsshを用いてSocSELサーバにログイン

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
    - 初めてログインの場合は"Are you sure you want to continue connecting (yes/no/[fingerprint])?" と表示されるので、"yes"を入力

### 2. パスワードの設定

  - 「1. サーバに接続」を完了すると以下が表示されるので自身の設定したいパスワード入力
    ```bash
    ユーザ名@133.42.160.101's password:
    ```
  - ターミナルの左側の表示が以下の様に変わればログイン完了
    ```bash
    [ユーザ名@socsel-brain-001 ~]$
    ```

### 3. 接続の解除

  - sshの接続解除をしたい場合は以下を入力
    ```bash
    exit
    ```