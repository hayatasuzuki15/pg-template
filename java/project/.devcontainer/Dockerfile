FROM eclipse-temurin:23

WORKDIR /workspace

# 必要なツールをインストール
RUN apt-get update && apt-get install -y \
    git \
    maven \
    gradle \
    && rm -rf /var/lib/apt/lists/*

# デフォルトのシェルを bash に
CMD [ "/bin/bash" ]
