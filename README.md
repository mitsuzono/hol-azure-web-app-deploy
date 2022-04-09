# hol-azure-web-app-deploy
## ハンズオンの目標
CI/CDを理解し、パイプラインを組めるようになる

## 事前準備が必要なもの
- GitHubアカウント
    - https://github.co.jp/
- Microsoftアカウント
    - https://account.microsoft.com/account?lang=ja-jp

## 手順
- GitHubでサンプルリポジトリを自分のアカウントにフォークする
    - C#: https://github.com/mitsuzono/azure-web-app-csharp
    - JavaScript: https://github.com/mitsuzono/azure-web-app-js
    - Python: https://github.com/mitsuzono/azure-web-app-python
- GitHub Actionsのワークフロー定義ファイル（YAML）を作る
    - https://docs.microsoft.com/ja-jp/azure/app-service/deploy-github-actions
        - パターン1：「デプロイ センターを使用する」を実施（Web Appの作り方は別途案内）
        - パターン2（自信がある人）：「ワークフローを手動で設定する」以降を実施
- ワークフロー実行結果を確認
- 変更を加えて再度プッシュ、Web Appsに変更が反映されるか確認

## 早く終わった人用
- マルチステージビルド
    - Web Appsのプランを上げ、スロットを増やす
    - ワークフローの変更（トリガーの追加、デプロイ先を別スロット指定）
    - ブランチでCI/CDを手動実行 (workflow_dispatch)
        - https://docs.github.com/ja/actions/managing-workflow-runs/manually-running-a-workflow
    - ワークフローにPRトリガーを追加
        - https://docs.github.com/ja/actions/using-workflows/events-that-trigger-workflows#pull_request
    - PR作成して、CI/CD結果を確認
    - PRマージして、CI/CD結果を確認

## その他参考
- GitHub Actions Documentation
    - https://docs.github.com/en/actions
- GitHub Learning Lab
    - https://lab.github.com/
- Web アプリを作成する（App Service）
    - https://azure.microsoft.com/ja-jp/get-started/web-app/
