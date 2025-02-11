# DevContainer 環境セットアップ

このプロジェクトは、ローカル環境を汚さずに開発を行うために VSCode の DevContainer を活用し、Docker を用いた実行環境を構築します。

---

## 📂 フォルダ構成
```
pg/
 ├── python/        # Python プロジェクト用ディレクトリ
 │    ├── <project_name>/  # 各 Python プロジェクトのディレクトリ
 │    │    ├── .devcontainer/  # DevContainer の設定ファイル
 │    │    │    ├── devcontainer.json  # VSCode DevContainer 設定
 │    │    │    ├── Dockerfile  # Docker の設定
 │    │    ├── src/  # ソースコード
 │    │    ├── requirements.txt  # 必要な Python ライブラリ
 │
 ├── node/          # Node.js プロジェクト用ディレクトリ
 │    ├── <project_name>/
 │    │    ├── .devcontainer/
 │    │    │    ├── devcontainer.json
 │    │    │    ├── Dockerfile
 │    │    ├── src/
 │    │    ├── package.json  # 必要な Node.js ライブラリ
 │
 ├── java/          # Java プロジェクト用ディレクトリ
 │    ├── <project_name>/
 │    │    ├── .devcontainer/
 │    │    │    ├── devcontainer.json
 │    │    │    ├── Dockerfile
 │    │    ├── src/
 │    │    ├── pom.xml  # Maven プロジェクトの場合
 │    │    ├── build.gradle  # Gradle プロジェクトの場合
 │
 ├── cpp/           # C++ プロジェクト用ディレクトリ
 │    ├── <project_name>/
 │    │    ├── .devcontainer/
 │    │    │    ├── devcontainer.json
 │    │    │    ├── Dockerfile
 │    │    ├── src/
 │    │    ├── CMakeLists.txt  # CMake プロジェクトの場合
 │
 ├── php/           # PHP プロジェクト用ディレクトリ
 │    ├── <project_name>/
 │    │    ├── .devcontainer/
 │    │    │    ├── devcontainer.json
 │    │    │    ├── Dockerfile
 │    │    ├── src/
 │    │    ├── composer.json  # Composer パッケージ管理ファイル
 │
 ├── go/            # Go プロジェクト用ディレクトリ
      ├── <project_name>/
           ├── .devcontainer/
           │    ├── devcontainer.json
           │    ├── Dockerfile
           ├── src/
           ├── go.mod         # Go モジュール定義ファイル
           ├── go.sum         # Go モジュールのチェックサム
```

---

## 🚀 使い方

### **1. VSCode で DevContainer を開く**
1. `pg/<環境>/<プロジェクト名>` を VSCode で開く。
2. `Ctrl + Shift + P` → `Dev Containers: Reopen in Container` を実行。
3. コンテナが起動し、指定の環境がセットアップされる。

### **2. CLI から起動する場合**
```sh
cd pg/<環境>/<プロジェクト名>
docker build -t <project_name> .
docker run --rm -it -v "$(pwd)":/workspace <project_name> /bin/bash
```

---

## 🔧 事前準備（必要要件）
- **Docker**（バージョン 20 以上推奨）
- **VSCode**（最新版推奨）
- **VSCode の DevContainer 拡張機能**（次のセクションで説明）

### **Docker のインストール**
- [公式サイト](https://www.docker.com/) からインストールしてください。
- `docker -v` でインストール確認。

### **VSCode のインストール**
- [公式サイト](https://code.visualstudio.com/) からインストールしてください。

---

## 🖥️ Hello, World の実行方法

### **Python の場合**
```sh
python src/main.py
```

### **Node.js の場合**
```sh
node src/index.js
```

### **Java の場合**
```sh
javac src/Main.java
java -cp src Main
```

### **C++ の場合**
```sh
g++ src/main.cpp -o src/main
./src/main
```

### **PHP の場合**
```sh
php src/index.php
```

### **Go の場合**
```sh
go run src/main.go
```

---

この設定を活用すれば、言語ごとに最適な環境を簡単に構築できます！ 🎯

