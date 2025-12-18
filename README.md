# GitHub meta

GitHub Meta Repository for [@ndxbn](https://github.com/ndxbn)

## リポジトリ管理方針
リポジトリのライセンス管理、依存関係、およびスカフォールディングに関する方針です。

リポジトリを作る際は、空のリポジトリを作り、言語ごとの `create` スクリプトで初期化します。（例： `bun create ndxbn/bun`、 `composer create-project `ndxbn/php` など）
もしくは、リポジトリテンプレートとして使っても良いです。

各リポジトリテンプレートには「その言語での初期セットアップに必要なファイル」しか含まれていません。つまり、[Community health file](https://docs.github.com/ja/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)は含まれていません。
それらはリポジトリ作成後に、`ndxbn/.github` リポジトリのオートヒーリングによって補完されます。

## License Policy
原則として、すべての公開リポジトリには MIT License を適用します。

すべてのソースコードは REUSE Software 仕様に準拠し、機械可読な著作権およびライセンス情報を保持する必要があります。
定期的に、各ファイルのヘッダーの有無をチェックするワークフローを流しています。

特定のリポジトリで異なるライセンス（例: Apache 2.0, GPL）を適用する場合、そのリポジトリのルートに手動で `LICENSE` ファイルを変更してください。

依存ライブラリのライセンス互換性は、LicenseFinder を用いて管理します。
私のリポジトリでは基本的に MIT ですが、その前提で使用できるライブラリのライセンスの一覧を `global_decisions.yml` で定義しています。

### Audit Workflow

- Global Policy: デフォルトでは、このリポジトリにある `global_decisions.yml` を使用して依存関係をスキャンします。
- Local Policy: リポジトリ固有の例外（例: 特定のCopyleftライセンスの許可）が必要な場合、各リポジトリ内に `doc/dependency_decisions.yml` を配置することで、グローバル設定を上書きします。

