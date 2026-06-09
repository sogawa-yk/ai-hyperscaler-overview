# 第6章 レビュー結果

## 構成・文体レビュー（chapter-reviewer）

総合評価 4.5/5。仕様・用語・章間整合・図表・カード定型はほぼ完璧。

修正必須: （高）6.5の「監査 log」を「監査ログ」に（日英混在タイポ）。
推奨: （中）理解度チェックに判断問題を追加（現状 概念×3・設計×1）。
任意（低）: 6.2のOTel定義を脚注へ寄せ本文短縮、6.5にカードへの導線参照。

## 技術検証レビュー（tech-verifier）

7項目中5正確・1要修正・1要確認。
**要修正**: OTel GenAI semconv の `gen_ai.system` は非推奨（→ `gen_ai.provider.name`）。他3属性（gen_ai.request.model, gen_ai.usage.input_tokens/output_tokens）は現行で正確。リスト6.1を更新。
**確認**: Microsoft Agent 365 は2026-05-01 GA（エージェント統制のcontrol plane、Entra/Purview連携、監査証跡）。Langfuse、各社o11y・監査・AIゲートウェイ（Azure API Management の AI gateway、Apigee）も正確。Purviewはデータガバナンス寄りでAPI操作監査はAzure Monitor/Activity Logが主役の点に留意。

## 情報ソース検証（citation-verifier）

誇張・無根拠断定なし、参考文献URL6件すべて有効、「要確認」運用適切。
- （中）gen_ai.system更新（同上）。
- （低）表6.3のOCI弱みセルに「（要確認）」を追加し章内の不確実性表記を統一。

## 理解度チェック問題フォーマット検証（quiz-format-checker）

フォーマット全準拠（4問）。任意: 判断問題追加でバランス向上。

## Mermaid構文検証（mermaid-syntax-checker）

問題なし。4ブロック構文正常・配色準拠。

---

## 対応結果
- **対応日**: 2026-06-09
- **修正内容**:
  - 6.5「監査 log」→「監査ログ」。
  - リスト6.1の `gen_ai.system` を `gen_ai.provider.name` に更新（旧名をコメント併記）。
  - 理解度チェックにQ5（判断問題：共通層中心か各社LLM特化o11y中心かの選択）を追加し5問に。
  - 表6.3のOCI弱みセルに「（要確認）」を追加。
  - Agent 365 のGA（2026-05-01）を本文・カードに事実として明記。
