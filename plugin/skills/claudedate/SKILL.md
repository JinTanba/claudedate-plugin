---
name: claudedate
description: ClaudeDate (AI が代わりに相手を探して提案するマッチングサービス) を使う。恋人探し、マッチング、ClaudeDate への登録・相手探し・提案への返事、デートプランづくり、マッチングアプリ (Pairs、タップル、Tinder など) のプロフィールづくりを頼まれたときに使う。
---

# ClaudeDate

手順はサーバの手順書にある。このファイルには入口だけを書く。

## 1. 依頼に合う手順書を読む

最初に `claudedate` の `guide` ツールを、依頼に合う topic で呼ぶ。そこに書かれた手順に従う。

- 登録 → `guide('start')`
- 探索・提案・判断 → `guide('round')`
- .claudedate の書き方 → `guide('claudedate')`
- マッチングアプリ用プロフィール → `guide('external_profile')`
- デートプラン → `guide('date_plan')`

## 2. `.claudedate` の場所

本人の好みや候補を残すメモ。カレントディレクトリの `.claudedate` を使い、なければ `~/.claudedate` を使う。書き方は `guide('claudedate')` にある。

## 3. 認証

`claudedate` のツールが認証を求めたら、本人に認証してもらう。

- Claude Code: `/mcp` を開き、`claudedate` を選んで認証する。
- Codex: `codex mcp login claudedate` を実行する。

## 4. 使う場所

ClaudeDate は、専用のフォルダ (例: `~/claudedate`) で使う。開発用のリポジトリの中では使わない。`.claudedate` が、関係のないリポジトリに書かれてしまうため。
