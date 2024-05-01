# docker_kakuninkun_server

## 概要

[Golangプロジェクト](https://github.com/unSerori/kakuninkun_server)のDocker開発環境。

### 開発環境

Windows 11 Pro : 10.0.22631.3447  
Visual Studio Code: 1.88.1  
Docker Desktop: 4.29.0: Engine: 26.0.0  
image: golang:1.22.2-bullseye  
image: mysql:latest

## 環境構築

Windowsを対象としている

1. Docker Desktopをインストール  [Docker Hub windows-install download](https://docs.docker.com/desktop/install/windows-install/)
2. このリポジトリをクローン
3. .envファイルをもらうか作成。

    ```env:.env
    MYSQL_ROOT_PASSWORD: ルートユーザのパスワード
    MYSQL_USER: ユーザ名
    MYSQL_PASSWORD: ユーザのパスワード
    MYSQL_DATABASE: 使用するdatabase名
    ```

4. VScodeでフォルダーを開き以下のコマンド。Docker拡張機能（[ms-azuretools.vscode-docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)）も入れておく。

    ```cmd
    docker compose up -d --build
    ```

5. Dockerタブからgo_serverをアタッチ
6. 新しいウィンドウでGolangプロジェクトの環境構築  
[Golangプロジェクト](https://github.com/unSerori/kakuninkun_server)  
SSH URL:  

    ```SSH:SSH URL
    git@github.com:unSerori/kakuninkun_server.git
    ```
