---
id: git_clone
title: git cloneの用意と実行
sidebar_label: git cloneの用意と実行
sidebar_position: 1
---
**このページでは、トークンの作成方法とgit cloneの実行方法を説明する**
### １. トークンの作成
    - **トークン作成済みの方は，２に進んでください**
    - **GitHubのホーム([https://github.com/](https://github.com/))へ移動してログイン**

    - **右上の自分のアイコンをクリック**

    - **歯車マークの「setting」をクリック**

    - **左のサイドバーの下の方にあるDeveloper Settingsをクリック**

    - **Personal access tokens Token (classic)をクリック**

    - **General new token (classic)をクリック**

    - **自分のパスワードを入力を入力**

    - **Noteに目的（目的以外でも良いから何か）を入力し，Select scopesのrepoをクリックしてチェック**

    - **サイトの下の方にあるGenerate tokenをクリックすれば，tokenの作成完了（メモ必須）**


### ２. git cloneの実行方法
    - **ターミナルを開く**

    - **git cloneの実行**
        ```
        git clone https://github.com/Wakayama-SocSEL/socusaurus.git
        ```
    - **git cloneでユーザ名とパスフレーズの入力を求められた方は，ユーザ名とトークン（パスワードフレーズ）を入力**  
  