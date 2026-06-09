# 第5章 レビュー結果

## 構成・文体レビュー（chapter-reviewer）

総合評価 4.5/5。仕様整合性・章間整合性・図表・カード・クイズ高水準。出典主義（要確認・脚注・確認日）徹底。

修正必須: （中）line 13の100字文を分割。
任意（低）: 脚注line 341分割、リスト番号の出現順（5.2が5.1より先＝仕様準拠だが逆転）、DB内ベクトル/NL→SQL/ハイブリッド検索の初出英語併記タイミング。

## 技術検証レビュー（tech-verifier）

7項目すべて「正確」。重点項目の結論:
- **Deep Data Security は実在**（正式名 Oracle Deep Data Security）。行/列/セル単位の宣言的SQL認可をDB層で強制、Oracle AI Database 26aiに組込み。位置づけは「agentic AI向けのidentity-aware data access control」で本章の論旨と一致。
- **Oracle Database 現行正式呼称は Oracle AI Database 26ai**（2025-10改称、23ai系継続、版番号23.26.x、23.26.2が2026-04）。
- Oracle AI Vector Search、Select AI（SELECT AI <action> 構文、chat等）も確認。AWS/Azure/Google CloudのDB内ベクトル・認可も全て正確。

**改善**: 脚注の「要確認」は基準日時点で確定情報として扱える。断定形へ更新し公式URLを付すと精度向上。図5.2/表5.3の「Token Exchangeで運ばれた身元を評価」はその具体機構名でDDSが評価する一次ソース未確認のため、「DBが受け取ったユーザー身元」と一般化が安全。Select AIのchat例は公式は引用符なし。

## 情報ソース検証（citation-verifier）

誇張・排他性の過剰主張なし。OCIの強みは設計上の特徴に限定、弱みも明示、最上級・マーケ語なし。
- （中）表5.5「OCIにあり他社にない」は設計思想に限定され許容範囲（個別機能の排他性は主張せず）。Deep Data Security公式URLを脚注に。
- （中）Deep Data Securityの「要確認」は保守的すぎ（26aiでGA済み）。URL追加し提供状態を事実化。
- （中/軽）他社認可記述・表5.5の弱み断定に出典or「本書の見立て」明示。参考文献を具体ページへ。

## 理解度チェック問題フォーマット検証（quiz-format-checker）

問題なし。5問、3種混在（概念×3・判断×1・設計×1）。任意: 難易度が応用に4問偏り。

## Mermaid構文検証（mermaid-syntax-checker）

問題なし。4ブロック構文正常・配色準拠。図5.1の2 subgraphも有効。

---

## 対応結果
- **対応日**: 2026-06-09
- **修正内容**:
  - line 13の長文を2文に分割。
  - Deep Data Security を確定情報に格上げ（Oracle AI Database 26aiで2026-04 GA）。脚注[^3]に公式URL付与、参考文献に追加。
  - Oracle Database 現行呼称を「Oracle AI Database 26ai（2025-10、23.26.x）」として脚注[^1]を確定形に。Select AI脚注[^2]も確定形＋chat例の引用符を除去。
  - 図5.2/表5.3の「Token Exchangeで運ばれた身元」を「DBが受け取ったユーザー身元」に一般化。
  - 表5.5の弱み欄に「本書の見立て」を明示。参考文献を各機能の具体ページへ更新。
  - DB内ベクトル/NL→SQL/ハイブリッド検索の初出に英語併記を整理。
