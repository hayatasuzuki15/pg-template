FROM node:latest

# システムの更新とGitのインストール
RUN apt-get update && \
    apt-get install -y git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# ... 既存のNode.js関連の設定 ... 