# リポジトリ構造 (Repository Structure)

本書プロジェクトのディレクトリ構成を定義する。本書はハンズオン書ではなく横断リファレンスのため、サンプルコードのソースツリーは持たない（コード例は原稿内に最小限のSQL／設定断片として埋め込む）。

## 全体構成

```
ai-hyperscaler-overview/
├── CLAUDE.md                      # プロジェクトメモリ（執筆ルール）
├── docs/                          # 永続ドキュメント（何を・どう書くか）
│   ├── ideas/
│   │   └── concept.md             # 書籍コンセプト案（執筆スペック・入力）
│   ├── book-plan.md               # 書籍企画書
│   ├── book-architecture.md       # 章構成・章間依存関係
│   ├── writing-guidelines.md      # 執筆ガイドライン（文体・表記・図表・引用）
│   ├── glossary.md                # 用語集（表記統一基準）
│   ├── repository-structure.md    # 本ファイル
│   ├── figure-list.md             # 図表一覧（全章横断）
│   ├── chapter-specs/             # 各章の仕様書
│   │   ├── ch00-spec.md           # 序章
│   │   ├── ch01-spec.md 〜 ch06-spec.md
│   │   ├── ch90-spec.md           # 統合章
│   │   └── ch99-spec.md           # 終章
│   ├── sources.md                 # 章横断の出典・確認日ログ（任意）
│   └── feedbacks/                 # 読了後フィードバック（随時）
├── manuscript/                    # 原稿本文
│   ├── ch00/
│   │   ├── ch00.md
│   │   └── figures/               # 章内の図表ソース（Mermaid等）
│   ├── ch01/ 〜 ch06/
│   ├── ch90/                      # 統合章
│   └── ch99/                      # 終章
└── .steering/                     # 作業単位のドキュメント（作業ごとに作成）
    └── YYYYMMDD-chNN-section/
        ├── requirements.md
        ├── design.md
        └── tasklist.md
```

## 章とディレクトリの対応

本書の章は序章・第1〜6章・統合章・終章で構成される。ファイル名のゼロ埋め番号と章の対応は以下のとおり。

| 章 | 仕様書 | 原稿ディレクトリ |
|----|-------|----------------|
| 序章 | `chapter-specs/ch00-spec.md` | `manuscript/ch00/` |
| 第1章 アイデンティティ／認可 | `chapter-specs/ch01-spec.md` | `manuscript/ch01/` |
| 第2章 実行基盤 | `chapter-specs/ch02-spec.md` | `manuscript/ch02/` |
| 第3章 オブジェクトストレージ | `chapter-specs/ch03-spec.md` | `manuscript/ch03/` |
| 第4章 マネージドAI | `chapter-specs/ch04-spec.md` | `manuscript/ch04/` |
| 第5章 データ側AI | `chapter-specs/ch05-spec.md` | `manuscript/ch05/` |
| 第6章 観測性／ガバナンス | `chapter-specs/ch06-spec.md` | `manuscript/ch06/` |
| 統合章 地図の全体像 | `chapter-specs/ch90-spec.md` | `manuscript/ch90/` |
| 終章 公式RA読み比べ | `chapter-specs/ch99-spec.md` | `manuscript/ch99/` |

## 命名規則

- **章番号**: ゼロ埋め2桁（`ch00`〜`ch06`）。統合章は `ch90`、終章は `ch99`（concept §12 の提案に準拠）
- **原稿本文**: `manuscript/chNN/chNN.md`
- **図表ソース**: `manuscript/chNN/figures/` 配下に Mermaid ファイル等を配置
- **ステアリングディレクトリ**: `.steering/YYYYMMDD-chNN-セクション名/`

## 出典・確認日の管理

本書は出典主義・スナップショット明示を重視するため、出典と確認日を二重に管理する。

- 各章の本文末尾に「参考文献」と「確認日」を置く（一次情報源・確認日付き）
- 章横断の出典・確認日ログを `docs/sources.md` に集約する（任意・推奨）。陳腐化しやすい事実（モデル数・GA/プレビュー・リージョン・ブランド改称）の再確認時にここを更新する

## 本プロジェクトに存在しないもの

ハンズオン非スコープのため、以下は持たない:

- アプリケーションのソースツリー（`src/` 等）
- Kubernetesマニフェスト／Terraform／Dockerfile のサンプル
- `docs/sample-code-spec/`（サンプルコード仕様）
- 検証環境・デプロイスクリプト

コード例は原稿内に SQL／設定断片／プロトコル例として最小限埋め込む（`docs/writing-guidelines.md` のコード例ルールを参照）。
