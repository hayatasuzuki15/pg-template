FROM node:18

WORKDIR /workspace


COPY package.json package-lock.json* ./
# システムの更新とGitのインストール
RUN apt-get update && \
    apt-get install -y git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    npm install

CMD [ "/bin/bash" ]
