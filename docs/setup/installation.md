# インストール

このページでは、Narrative Conversationをパソコンにインストールする方法を説明します。

!!! info "初心者の方へ"
    このページでは、**Windows向けの実行ファイル版**（最も簡単な方法）を説明します。
    
    Linux、macOS、ソースコードから実行したい方は、[応用的なインストール方法](../advanced/advanced-installation.md)をご覧ください。

## 動作環境

### 対応OS

このページで説明する実行ファイル版は、**Windows 11**（または Windows 10）で動作します。

### 必要なスペック

- **OS**: Windows 11 / Windows 10
- **インターネット接続**: 必須（AIサービスとの通信に必要）

!!! info "他のOSをお使いの方"
    - **Linux（Ubuntu等）**をお使いの方 → [応用的なインストール方法](../advanced/advanced-installation.md)
    - **macOS**をお使いの方 → [応用的なインストール方法](../advanced/advanced-installation.md)
    - **ローカルLLM**を使いたい方 → [ローカルLLMを使う](../advanced/local-llm.md)

## インストール方法（Windows向け）

!!! info "推奨：実行ファイル版"
    初心者の方は、以下の実行ファイル版が最も簡単です。プログラミングの知識は不要です。

### 1. ダウンロード

1. [GitHubのリリースページ](https://github.com/gpsnmeajp/NarrativeConversation/releases/)を開きます
2. `narrative_conversation_vXXX.zip`（Xはバージョン番号）をクリックしてダウンロードします

![ダウンロードページ](placeholder-download-page.png)

### 2. 解凍

1. ダウンロードしたZIPファイルを右クリック
2. 「すべて展開」を選択
3. 展開先を選んで「展開」をクリック（デスクトップや「ドキュメント」フォルダなど、好きな場所でOK）

!!! warning "重要"
    「ダウンロード」フォルダのまま使うと、後で自動削除される可能性があります。必ず別の場所に移動してください。  
    なお、Program FilesやAppDataなどのシステムフォルダでは正常に動作しないため、避けてください。


### 3. 起動

1. 解凍したフォルダを開く
2. `narrative_conversation.exe`をダブルクリック
3. 初回起動時、Windowsから「WindowsによってPCが保護されました」という警告が出る場合があります
   - 「詳細情報」をクリック
   - 「実行」ボタンをクリック
   ファイアーウォール警告が出た場合は、許可してください。(拒否でも動きますが、後々スマホからアクセスできなくなる可能性があります)
4. 以下の表示が出れば正常にサーバーが起動しています。この画面は閉じずに放置してください。

```
INFO:     Application startup complete.
INFO:     Uvicorn running on http://0.0.0.0:8000 (Press CTRL+C to quit)
```

!!! info "セキュリティ警告について"
    このアプリは個人開発者が公開しているため、Windowsの警告が出ることがあります。ウィルス検査済みです。
    が、もし心配な場合は[応用的なインストール方法](../advanced/advanced-installation.md)のソースコード版を試してください。(高難易度)

### 4. ブラウザで開く

以下のどちらかの方法で、画面を起動してください。

+ フォルダに同梱されている「開く」ショートカットを開く
+ ブラウザを開いて手動で `http://127.0.0.1:8000` にアクセスする

![起動画面](placeholder-first-launch.png)

!!! tip "うまく起動しないときは"
    [よくある質問](../troubleshooting/faq.md)ページを参照してください。

---

## アンインストール

Narrative Conversationは、同じフォルダにあるファイルをすべて削除するだけで安全にアンインストールできます。  
物語データなどは同じフォルダの `data` フォルダに保存されているので、必要に応じてバックアップしてください。

## 次のステップ

インストールが完了したら、[初期設定](initial-setup.md)に進んで、AIサービスとの接続設定を行いましょう。
