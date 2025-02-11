FROM gcc:latest

WORKDIR /workspace

# 必要なツールをインストール
RUN apt-get update && apt-get install -y \
    cmake \
    gdb \
    make \
    ninja-build \
    && rm -rf /var/lib/apt/lists/*

# デフォルトのシェルを bash に
CMD [ "/bin/bash" ]
