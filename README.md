# python-project-template

## Codex の auto mode

`.codex/config.toml` に、Claude Code の auto mode に相当する設定を用意しています。
dev container 内でリポジトリのルートから `codex` を起動し、初回の確認でこのプロジェクトを信頼すると適用されます。
プロジェクトを信頼するまでは、この設定は読み込まれません。

- `workspace-write`: ワークスペース内のファイル編集やコマンド実行をサンドボックス内で行います。
- `on-request` + `auto_review`: サンドボックス外への書き込みやネットワーク利用など、対象となる承認要求をレビューエージェントが判定します。
- `network_access = false`: サンドボックス内からのネットワーク利用を制限します。

自動レビューはサンドボックスの境界を変更しません。レビューで拒否された操作は実行されません。
モデルの選択などは個人の `~/.codex/config.toml` で設定できます。

詳細は公式の [Auto-review](https://learn.chatgpt.com/docs/sandboxing/auto-review) と
[Configuration reference](https://learn.chatgpt.com/docs/config-file/config-reference) を参照してください。
