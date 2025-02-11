FROM golang:latest

# システムの更新とGitのインストール
RUN apt-get update && \
    apt-get install -y git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# 作業ディレクトリの設定
WORKDIR /workspace

# Go toolsのインストール
RUN go install golang.org/x/tools/gopls@latest && \
    go install github.com/go-delve/delve/cmd/dlv@latest && \
    go install honnef.co/go/tools/cmd/staticcheck@latest

# ... 既存のGo関連の設定 ...