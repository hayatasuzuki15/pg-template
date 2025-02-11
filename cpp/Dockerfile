FROM gcc:latest

# システムの更新とGitのインストール
RUN apt-get update && \
    apt-get install -y git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# ... 既存のC++関連の設定 ... 