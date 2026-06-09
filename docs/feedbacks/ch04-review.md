# 第4章 レビュー結果

## 構成・文体レビュー（chapter-reviewer）

総合評価 4/5。4層構成・図表・ケイパビリティカード・章間整合性・図表品質は高水準。

修正必須:
- （高）理解度チェックを5問に（仕様準拠。現状4問）。RAG構成要素分解の利点 or OCI強み弱みを追加。
- （中）「基盤モデル」の初出（L17）を日本語（英語）形式に。
- （中）80字超の3文（L13導入、L89 MCP説明、L130 SageMaker）を分割。
- （低）L17「すぐに陳腐化」を「短期間で陳腐化」に（禁止表現回避）。

## 技術検証レビュー（tech-verifier）

16項目中12正確・3要修正・1要確認。

**要修正（重要）**:
1. Vertex AI は2026-04-22（Cloud Next 26）に **Gemini Enterprise Agent Platform** へ正式改称。基準日2026-06-09時点で旧名。Microsoft Foundryの改称は脚注で扱うのにGoogle側未反映は非対称。表4.1/4.3/4.4/本文/参考文献を更新し改称脚注を付す。
2. MCP対応は4社とも**実装済み**（AWS AgentCore Runtime、Azure Foundry Agent Service、Google ADK、OCI MCP Calling）。「対応の方向（要確認）」は保守的すぎる。「対応済み（成熟度は流動的）」へ。
3. Microsoft Foundryの名称は2026-01 Product Termsで確定。脚注[^1]の「正式名称は要確認」を確定情報に整える。

任意: 各社エージェント基盤の現行固有名（Bedrock AgentCore、Vertex AI Agent Builder/Agent Engine/ADK）併記。SageMaker→Amazon SageMaker AI。OCI Enterprise AI 包括ブランド。

## 情報ソース検証（citation-verifier）

- （中）表4.5の両方向ギャップに出典付与か第5章への前方参照明示。「OCIにあり他社にない:データ近接」の排他性が弱い（他社もDB内ベクトルを持つ）→設計の重心差に緩和。
- （中）「最も激しい/最も速い」最上級・「先行有利」を緩和か出典付与。
- （最優先）表4.3 OCIのMCP「要確認」→出典付き「対応」（MCP Calling, docs.oracle.com/.../generative-ai/mcp.htm）。
- （低）Microsoft参考文献URLを /azure/foundry/ へ。

## 理解度チェック問題フォーマット検証（quiz-format-checker）

フォーマット全準拠（4問、3種混在）。※問題数は仕様5問に対し4問（chapter-reviewer指摘）。

## Mermaid構文検証（mermaid-syntax-checker）

問題なし。4図＋JSON、構文正常・配色準拠。図4.1の連結無向エッジも有効。

---

## 対応結果
- **対応日**: 2026-06-09
- **修正内容**:
  - Vertex AI → 「Gemini Enterprise Agent Platform（旧 Vertex AI）」へ更新（表4.1/4.3/4.4/本文/参考文献）。改称脚注[^3]を追加。現行固有名（Bedrock AgentCore、Vertex AI Agent Builder/ADK）を併記。
  - MCP対応を4社「対応済み（成熟度は流動的）」へ格上げ。脚注[^2]に各社の実装名とOCI MCP CallingのURLを追記。OCI MCPを出典付き「対応」に。
  - 脚注[^1]をMicrosoft Foundry確定（2026-01 Product Terms）に整える。
  - 理解度チェックにQ5（RAG構成要素分解の利点）を追加し5問に。
  - 基盤モデルの初出併記、80字超3文の分割、「すぐに」→「短期間で」。
  - 表4.5のデータ近接の排他性を設計重心の差に緩和し第5章への前方参照を明示、最上級表現を緩和。Microsoft URL更新。
