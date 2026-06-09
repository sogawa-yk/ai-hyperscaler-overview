# 第1章 レビュー結果

## 構成・文体レビュー（chapter-reviewer）

総合評価 4.5/5。固定小節構成・用語統一・章間整合性・図表品質・理解度チェックはすべて準拠。

修正必須:
- （中）1.1の長文（約109字）を2文に分割。
- （中）1.2の長文（約120字）をAzure／AWSで2文に分割。

任意（低）: 1.2・1.3の各社解説をもう一段厚くする余地。

## 技術検証レビュー（tech-verifier）

18項目中17件「正確」、1件「要修正」。

**要修正（重要）**: Microsoft Entra Agent ID は基準日2026-06-09時点で既に **GA済み（2026-05-01 GA）**。Microsoft Agent 365 の一部で、Agent Identity Blueprint／Agent Identity／OBO用 Agent User Account／Entra ID Governance統合を持つ。原稿の「方向を打ち出している」「確立途上」「要確認（提供状態）」は実態より弱い。1.5のカード「他社での実現」、表1.2の注記、表1.3「他社にありOCIにない」の3箇所をGA済み前提に更新する。
出典: https://learn.microsoft.com/en-us/entra/agent-id/what-is-microsoft-entra-agent-id

その他（AWS Trusted Identity Propagation、Cognito CIAM、Entra External ID〔2024-05-15 GA、旧B2C後継〕、OCI Token Exchange+Identity Propagation Trust〔allowImpersonation, source_authn_prinクレーム〕、RFC 8693のgrant_type/トークンタイプURI）はすべて正確と確認。

## 情報ソース検証（citation-verifier）

問題なし。ソース要否対象6件すべてOK。「要確認」マークも適切。
任意（低）: 参考文献URLの粒度。[^2]やOracle/AWS/GoogleのURLをドメイントップから具体ページへ降ろすと検証性が上がる。

## 理解度チェック問題フォーマット検証（quiz-format-checker）

問題なし。4問、3種混在（概念確認×2・判断×1・設計×1）、難易度混在、全要素準拠。

## Mermaid構文検証（mermaid-syntax-checker）

問題なし。4ブロックすべて構文正常・配色準拠。sequence図はthemeVariables、graph/flowchartはclassDef配色準拠。

---

## 対応結果
- **対応日**: 2026-06-09
- **修正内容**:
  - Entra Agent ID を GA済み（2026-05-01）前提に更新（1.5カード、表1.2注記、表1.3）。エージェントID領域はAzureが専用製品GAで先行、OCIは弱みとして明示を強化。
  - 1.1・1.2の長文を各2文に分割（80字以内）。
  - 参考文献のOCI（Token Exchange）・各社URLを具体ページへ更新、[^2]に具体URL付与。
