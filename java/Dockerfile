FROM openjdk:17

# システムの更新とGitのインストール
RUN apt-get update && \
    apt-get install -y git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# ... 既存のJava関連の設定 ... 