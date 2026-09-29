# gishi

業務の聞き取りから、AIを組み込んだ業務ツールの設計・開発・運用まで担当しています。
どこを自動化すると効果が大きいかの整理から関わります。

- 生成AIを使った業務の自動化（Claude API など）
- Python・PHP（Laravel）での業務システム・Webアプリ開発、API連携
- AWSでのインフラ構築と運用保守

開発では Claude Code と OpenAI Codex を日常的に使い、設計の判断と動作確認は自分で行っています。

## 公開しているデモ

| リポジトリ | 内容 |
|---|---|
| [support-faq-rag](https://github.com/gishi-dev/support-faq-rag) | 製品のマニュアルやFAQをもとに、問い合わせへ根拠付きで答えるAIチャット。資料にないことは推測せず窓口へ案内し、答えられなかった質問をFAQ追加の候補として記録します。 |
| [inquiry-triage](https://github.com/gishi-dev/inquiry-triage) | 問い合わせメールを、AIが分類・緊急度・担当に仕分け、社内の対応方針に沿った返信の下書きまで用意するツール。送信は担当者が確認してから行います。 |
| [rule-evaluation](https://github.com/gishi-dev/rule-evaluation) | 多拠点の実績データを集計し、基準値・例外条件などのルールに沿って評価の算出と対象者の抽出を行う仕組み。ルールは担当者が画面で直せ、すべての評価に算出根拠が残ります。 |
| [ai-dev-workflow](https://github.com/gishi-dev/ai-dev-workflow) | Claude Code・Codex で開発を回す進め方と、AIに渡すルールファイルの見本。IssueからAIが実装し、自己レビューと人の承認を経てマージするまでの仕組みをまとめています。 |

| サポートAIチャット | 問い合わせメールの仕分け |
|---|---|
| ![サポートAIチャット](https://raw.githubusercontent.com/gishi-dev/support-faq-rag/main/images/chat-answer.png) | ![問い合わせメールの仕分け](https://raw.githubusercontent.com/gishi-dev/inquiry-triage/main/images/inbox.png) |

デモに登場する会社・製品・人物・メールは、すべて架空のものです。
