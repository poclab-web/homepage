# Academic Pages
**Academic Pagesは、個人および研究者向けポートフォリオWebサイトのためのGitHub Pagesテンプレートです。**
詳細は https://academicpages.github.io/ をご覧ください。このホームページは、academicpagesで公開されているものをフォークして作成しております。

![Academic Pages template example](images/homepage.png "Academic Pages template example")

# 公開先のホームページのURL

[https://poclab-web.github.io/homepage.github.io/](https://poclab-web.github.io/poclab-website/)

# はじめに

1. GitHubアカウントを作成し（まだ持っていない場合）、メールアドレスを確認してください（必須！）
2. 右上の「Use this template」ボタンをクリックします
3. 「New repository」ページで、リポジトリ名を「[あなたのGitHubユーザー名].github.io」として入力します。これがWebサイトのURLにもなります
4. サイト全体の設定を行い、コンテンツを追加します
5. ファイル（PDF、.zipファイルなど）を`files/`ディレクトリにアップロードします。これらは https://[あなたのGitHubユーザー名].github.io/files/example.pdf でアクセスできます
6. リポジトリの設定の「GitHub pages」セクションでステータスを確認します
7. （オプション）`markdown_generator`フォルダー内のJupyter notebookやPythonスクリプトを使用して、TSVファイルから論文や講演のMarkdownファイルを生成できます

詳細は https://academicpages.github.io/ をご覧ください。

## ローカル環境での実行

リポジトリをクローンした後、ローカルでWebサイトをプレビューするには以下の手順に従ってください。

### macOSユーザー向け

#### 1. 必要なツールの確認・インストール

まず、以下のコマンドでHomebrewがインストールされているか確認してください：
```bash
brew --version
```
Homebrewがインストールされていない場合は、[公式サイト](https://brew.sh/ja/)からインストールしてください。

#### 2. Rubyの管理ツール（rbenv）をインストール
```bash
# rbenvのインストール
brew install rbenv ruby-build

# シェル設定の追加
echo 'eval "$(rbenv init -)"' >> ~/.zshrc
source ~/.zshrc
```

#### 3. 新しいRubyバージョンのインストール
```bash
# 最新の安定版Rubyをインストール
rbenv install 3.3.9

# デフォルトバージョンに設定
rbenv global 3.3.9

# 設定を確認
ruby -v
```

#### 4. bundlerのインストール
```bash
gem install bundler
```

#### 5. プロジェクトの依存関係をインストール
```bash

# ローカルパスを設定（権限エラーを避けるため）
bundle config set --local path 'vendor/bundle'

# 依存関係をインストール
bundle install
```

#### 6. ローカルサーバーの起動
```bash
bundle exec jekyll serve -l -H localhost
```

成功すると、`http://localhost:4000` でサイトを確認できます。

### Windowsユーザー向け

#### 1. Windows Subsystem for Linux (WSL) のインストール

PowerShellを管理者権限で開き、以下を実行：
```powershell
wsl --install
```
再起動後、Ubuntu（または好みのLinuxディストリビューション）を設定してください。

#### 2. WSL内で必要なパッケージをインストール
```bash
# システムをアップデート
sudo apt update && sudo apt upgrade -y

# 必要なパッケージをインストール
sudo apt install ruby-dev ruby-bundler nodejs build-essential gcc make git
```

#### 3. bundlerの確認・インストール
```bash
# bundlerがインストールされているか確認
bundle --version

# もしインストールされていない場合
gem install bundler
```

#### 4. プロジェクトの依存関係をインストール
```bash
# プロジェクトディレクトリに移動
cd /mnt/c/path/to/your/poclab.github.io

# または、WSL内にクローンした場合
cd ~/poclab.github.io

# 権限エラーを避けるためローカルパスを設定
bundle config set --local path 'vendor/bundle'

# 依存関係をインストール
bundle install
```

#### 5. ローカルサーバーの起動
```bash
bundle exec jekyll serve -l -H localhost
```

成功すると、`http://localhost:4000` でサイトを確認できます。

### トラブルシューティング

#### よくある問題と解決方法

**権限エラーが発生する場合：**
```bash
bundle config set --local path 'vendor/bundle'
rm -f Gemfile.lock
bundle install
```

**nokogiriのインストールエラー（macOS）：**
```bash
brew install libxml2 libxslt
gem install nokogiri -- --use-system-libraries
```

**サーバーが起動しない場合：**
```bash
# Gemfile.lockを削除して再インストール
rm Gemfile.lock
bundle install

# デフォルトポートで起動
bundle exec jekyll serve -l -H localhost

# ポートが使用中の場合は別のポートを使用
bundle exec jekyll serve --port 4002 --host localhost
```

### 動作確認

サーバーが正常に起動すると、以下のようなメッセージが表示されます：
```
Server address: http://localhost:4000
Server running... press ctrl-c to stop.
```

ブラウザで `http://localhost:4000` にアクセスして、サイトが表示されることを確認してください。

### 開発時のワークフロー

1. ファイルを編集
2. ブラウザで変更を確認（自動的に更新されます）
3. 満足したらGitHubにプッシュ
4. GitHub Pagesで自動的にサイトが更新されます

## Using Docker

Working from a different OS, or just want to avoid installing dependencies? You can use the provided `Dockerfile` to build a container that will run the site for you if you have [Docker](https://www.docker.com/) installed.

You can build and execute the container by running the following command in the repository:

```bash
chmod -R 777 .
docker compose up
```

You should now be able to access the website from `localhost:4000`.

### Using the DevContainer in VS Code

If you are using [Visual Studio Code](https://code.visualstudio.com/) you can use the [Dev Container](https://code.visualstudio.com/docs/devcontainers/containers) that comes with this Repository. Normally VS Code detects that a development coontainer configuration is available and asks you if you want to use the container. If this doesn't happen you can manually start the container by **F1->DevContainer: Reopen in Container**. This restarts your VS Code in the container and automatically hosts your academic page locally on http://localhost:4000. All changes will be updated live to that page after a few seconds.

## メンテナンス

テンプレートのバグレポートや機能リクエストは[GitHub経由で提出](https://github.com/academicpages/academicpages.github.io/issues/new/choose)してください。テンプレートのスタイルに関する質問については、[GitHubで新しいディスカッションを開始](https://github.com/academicpages/academicpages.github.io/discussions)してお気軽にお尋ねください。

このリポジトリは[Stuart Geiger](https://github.com/staeiou)によって[Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/)からフォーク（その後分離）されました。Minimal Mistakes Jekyll Themeは© 2016 Michael Rose、MIT Licenseで公開されています（LICENSE.mdを参照）。現在は[Robert Zupko](https://github.com/rjzupkoii)によってメンテナンスされており、追加のメンテナーを歓迎しています。

## バグ修正と機能強化

バグ修正や機能強化をプルリクエストとして提出したい場合は、このリポジトリをテンプレートとして使用するのではなく、[フォーク](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)する必要があります。これにより、テンプレートのコピーをフォークに[同期](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork)することも可能になります。

残念ながら、Academic Pagesのようなテンプレートテーマでは、コアテーマのバグ修正や更新を取得するのが少し複雑になる1つの論理的な問題があります。このテンプレートを使用してカスタマイズした場合、同期を試みるとマージコンフリクトが発生する可能性があります。さまざまな.yml設定ファイルやMarkdownファイルを保存したい場合は、リポジトリを削除して再度フォークできます。または、手動でパッチを適用することもできます。

---
<div align="center">
    
![pages-build-deployment](https://github.com/academicpages/academicpages.github.io/actions/workflows/pages/pages-build-deployment/badge.svg)
[![GitHub contributors](https://img.shields.io/github/contributors/academicpages/academicpages.github.io.svg)](https://github.com/academicpages/academicpages.github.io/graphs/contributors)
[![GitHub release](https://img.shields.io/github/v/release/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io/releases/latest)
[![GitHub license](https://img.shields.io/github/license/academicpages/academicpages.github.io?color=blue)](https://github.com/academicpages/academicpages.github.io/blob/master/LICENSE)

[![GitHub stars](https://img.shields.io/github/stars/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io)
[![GitHub forks](https://img.shields.io/github/forks/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io/fork)
</div>
