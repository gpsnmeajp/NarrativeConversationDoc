# 応用的なインストール方法

このページでは、上級者向けのインストール方法を説明します。

!!! info "初心者の方は"
    基本的なインストールは [インストール](../setup/installation.md) ページをご覧ください。

## ソースコードから実行（Windows）

プログラミングに慣れている方や、最新の開発版を使いたい方向けです。

### 必要なもの

- Python 3.11以降
- Git（任意）

### 手順

**1. リポジトリをダウンロード**

Gitを使う場合：

```powershell
git clone https://github.com/gpsnmeajp/NarrativeConversation.git
cd NarrativeConversation
```

Gitを使わない場合：

- [GitHubページ](https://github.com/gpsnmeajp/NarrativeConversation)の「Code」→「Download ZIP」からダウンロード
- ZIPを解凍してフォルダを開く

**2. 仮想環境を作成**

PowerShellまたはコマンドプロンプトで、以下を実行：

```powershell
cd backend
python -m venv venv
venv\Scripts\Activate.ps1
```

!!! warning "実行ポリシーエラーが出た場合"
    PowerShellで「実行ポリシー」のエラーが出たら、管理者権限でPowerShellを開いて以下を実行：
    ```powershell
    Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
    ```

**3. 必要なパッケージをインストール**

```powershell
pip install -r requirements.txt
```

**4. サーバーを起動**

```powershell
python run_server.py
```

**5. ブラウザで開く**

`http://127.0.0.1:8000` にアクセスしてください。

---

## Linuxでのインストール

Linux（Ubuntu）ユーザー向けの手順です。

### 動作確認環境

- Ubuntu 24.04 LTS（動作確認済み）
- その他のディストリビューションでも動作する可能性があります

### 必要なもの

- Python 3.11以降
- Git

### 手順

**1. 必要なパッケージをインストール**

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.11 python3.11-venv python3.11-dev git
```

**2. リポジトリをクローン**

```bash
git clone https://github.com/gpsnmeajp/NarrativeConversation.git
cd NarrativeConversation/backend
```

**3. 仮想環境を作成**

```bash
python3.11 -m venv venv
source venv/bin/activate
```

**4. 必要なパッケージをインストール**

```bash
pip install -r requirements.txt
```

**5. サーバーを起動**

```bash
python run_server.py
```

**6. ブラウザで開く**

`http://127.0.0.1:8000` にアクセスしてください。

---

## macOSでのインストール

macOSでも動作すると思われますが、正式には確認されていません。

---

## 開発者向け情報

### 開発モードで起動

```bash
python run_server.py --reload
```

ファイルの変更を検知して、自動的に再起動します。

### 別のポートで起動

```bash
python run_server.py --port 8080
```

デフォルトの8000番ポートが使用中の場合に使用します。

### ログレベルの変更

```bash
python run_server.py --log-level debug
```

デバッグ情報を表示します。

---

## トラブルシューティング

### Python 3.11が見つからない

**Ubuntu/Debian:**
```bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.11
```

**その他のLinux:**
- ディストリビューションのパッケージマネージャーで確認
- [公式サイト](https://www.python.org/downloads/)からビルド

### 仮想環境の有効化がうまくいかない

**Linux/macOS:**
```bash
source venv/bin/activate
```

**Windows (PowerShell):**
```powershell
venv\Scripts\Activate.ps1
```

**Windows (cmd):**
```cmd
venv\Scripts\activate.bat
```

### パッケージのインストールが失敗する

```bash
# pipをアップグレード
pip install --upgrade pip

# 再度インストール
pip install -r requirements.txt
```

---

## 次のステップ

インストールが完了したら、[初期設定](../setup/initial-setup.md)に進んでください。

困ったときは：

- [トラブルシューティング](../troubleshooting/faq.md)

