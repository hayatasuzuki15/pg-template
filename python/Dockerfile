FROM python:3.11

# システムの更新とGitのインストール
RUN apt-get update && \
    apt-get install -y git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# ... 既存のPython関連の設定 ... 