# 第3章 レビュー結果

## 構成・文体レビュー（chapter-reviewer）

総合評価 4/5。仕様整合性・用語統一・章間整合性・図表品質は高水準。

修正必須:
- （中）line 35の長文（85字）を分割。
- （中）line 115の長文（93字）を分割。

修正推奨: 理解度チェックの種類偏り（概念確認×2・設計×1、判断問題欠落）。判断問題を追加。

## 技術検証レビュー（tech-verifier）

17項目中16件「正確」、1件「要修正」。

**要修正**: Google の Dataplex は 2026-04-10 に改称（Dataplex Universal Catalog→Knowledge Catalog、Dataplex Catalog→BigQuery universal catalog）。基準日2026-06-09時点では旧称。表3.1と確認日セクションを「Knowledge Catalog（旧 Dataplex）」へ更新。
出典: https://docs.cloud.google.com/dataplex/docs/release-notes

正確確認: 各社ストレージ階層名、OCI PAR（S3署名付きURL相当）、OCI S3互換API、各社イベント連携、Iceberg/Delta Lake。
注記: S3の「Glacier 等」は総称表現で許容。Azure Fabric（Synapse後継）方向は整合。Oracleは"Autonomous AI Database"へのブランド更新進行中（次回確認）。

## 情報ソース検証（citation-verifier）

**重要（高）**: 本書の核である出典主義に対し、ギャップ断定・「デファクト」一般化に脚注紐付けが不足。
- 表3.3「他社にありOCIにない: S3エコシステム」に出典なし。「広大/厚み」の定量含意を緩めるか出典付与。
- 表3.3「OCIにあり他社にない: Autonomous Database近接」の排他性が不成立（他社も自社DB/DWHとストレージ近接を持つ）。固有性を「自律運用DBとの統合」に限定し前提併記。
- 「S3のデファクト地位/突出」に出典なし。各社がS3互換APIを提供している事実が中立的証左。
- 表3.1の分析サービス名の参考文献追加。GCS URLを docs.cloud.google.com へ。

## 理解度チェック問題フォーマット検証（quiz-format-checker）

必須要素は全準拠（3問）。任意改善: 判断問題が欠落、Q追加でバランス向上。

## Mermaid構文検証（mermaid-syntax-checker）

問題なし。4ブロック構文正常・配色準拠。

---

## 対応結果
- **対応日**: 2026-06-09
- **修正内容**:
  - line 35・115の長文を分割。
  - Dataplex→「Knowledge Catalog（旧 Dataplex）」に更新（表3.1・確認日）。脚注で改称を明記。
  - 表3.3のギャップを出典主義に整合: S3デファクトに脚注[^1]（各社S3互換API提供を証左）、Autonomous Database近接の固有性を「自律運用DBとの統合」に限定し他社も近接を持つ前提を併記[^3]、S3エコシステムの「広大/厚み」を緩和。
  - 参考文献に各社分析サービスdocを追加、GCS URLを更新。
  - 理解度チェックに判断問題Q4を追加（S3互換APIに基づく選択）。
