FROM python:3.11

# 作業ディレクトリを設定
WORKDIR /workspace

# 必要なツールをインストール
RUN apt-get update && apt-get install -y \
    git \
    && rm -rf /var/lib/apt/lists/*

# 依存関係をインストール
COPY requirements.txt /workspace/
RUN pip install --no-cache-dir -r requirements.txt

# デフォルトのシェルを bash に
CMD [ "/bin/bash" ]
