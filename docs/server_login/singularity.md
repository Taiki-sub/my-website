---
id: singularity
title: singularity利用方法
sidebar_label: singularity利用方法
sidebar_position: 3
---
 
### jupyter利用方法
 
### 1. singularityの利用方法
 
    - sshを用いてサーバにログイン
        学内から：FromCampus(./FromCampus.md)
        学外から：FromOutside(.server_login/FromOutside.md)
    - 自身のディレクトリに移動
        ```bash
        cd /mnt/data1/[ユーザ名]
        ```
    - エディタ(vi)を開く
        ```bash
        vi [任意のフォルダ名].def
        ```
    - viを開いた状態で「i」を押して編集、以下をエディタに入力
        ```bash
        Bootstrap: library
        From: debian
        ```
    - 「Esc」を押して「wq!」と入力して終了
    - sifファイルの作成
        ```bash
        singularity build --fakeroot [任意のファイル名].sif [上記で作成したファイル(エディタ)名].def
        ```
        - "INFO:    Build complete: aaa.sif"と出れば成功
    - シンギュラリティのコンテナにログイン
        ```bash
        singularity shell [上記で作成したファイル名].sif
        ```
    - exitでログアウト

### 2. singularity利用時の便利なコマンド

    - singularityにログインせずに実行する方法
        ```bash
        singularity exec [上記で作成したファイル名].sif [command]
        ```
            - 例
                ```bash
                singularity exec aaa.sif pwd
                ```
    - ログアウトしても実行し続けさせる方法
        ```bash
        singularity instance start [上記で作成したファイル名].sif [任意のインスタンス名]
        ```
    - インスタンスが立っているかの確認方法
        ```bash
        singularity instance list
        ```
    - インスタンスを止める方法
        ```bash
        singularity instance stop [上記で設定したインスタンス名]
        ```
    - 実行結果を待たずに他のコマンドを入力可能にする方法
        ```bash
        nohup [command] &
        ```
    - シンギュラリティのホームディレクトリを自分の個人ファイルに設定する方法
        - ホームディレクトリに移動
            ```bash
            cd ~
            ```
        - bash_profileエディタ(vi)を開く
            ```bash
            vi .bash_profile
            ```
        - viを開いた状態で「i」を押して編集、最終行に以下をエディタに入力
            ```bash
            export SINGULALITY _HOME=/mnt/data1/[ユーザ名]
            ```
        - 「Esc」を押して「wq!」と入力して終了