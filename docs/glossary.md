# 用語集 (Glossary)

**更新日**: 2026-06-09

本用語集は執筆時の表記統一の基準であり、レビュー時の照合にも使用する。製品名・サービス名は陳腐化しうるため、確認日を意識して扱う（各章で再確認する）。

## 凡例

- **表記**: 本書での統一表記
- **英語**: 英語表記（初出時に併記）
- **定義**: 本書における定義
- **初出**: 最初に登場する章

---

## 本書の方法論用語

### 軸 (Axis / Role)
**定義**: ある領域を見通すための座標。「役割」とも言う。本書は製品ではなく軸を教える。製品は軸上の点（プロット）として扱う。軸は陳腐化しない。
**初出**: 序章

### 原点 (Origin)
**定義**: 本書がすべての軸を相対座標で語る際の基準点。本書ではOCIを原点に置く。
**初出**: 序章

### プロット (Plot)
**定義**: 軸上に配置された各社の具体的な製品・サービス。製品名は更新対象（陳腐化する）。
**初出**: 序章

### 対訳 (Cross-reference)
**定義**: 他社製品が「OCIでは何に相当するか」を示す対応関係。記号 `≒`（ほぼ相当）／`△`（部分的）／`なし`（相当なし）で表す。
**初出**: 序章

### 両方向ギャップ (Bidirectional Gap)
**定義**: 「他社にあってOCIにない」と「OCIにあって他社にない」を双方向で示す差分。
**初出**: 序章

### SWOTスライス (SWOT Slice)
**定義**: 領域ごとに切り出した各社の強み・弱み。OCIの弱みを必ず含める。
**初出**: 序章

### 新顔の分類手順 (Classification Procedure)
**定義**: 各領域章末に置く、未知の新製品を軸上のどこに置くか判断する再現可能な手順。
**初出**: 序章

### スナップショット (Snapshot)
**定義**: 確認日時点での製品・状態の記録。本書は不変の軸と更新対象のスナップショットを分離する。
**初出**: 序章

### ケイパビリティ・カード (Capability Card)
**定義**: 論点が立つ要件を定型（課題／OCIでの実現／他社での実現／差分の見立て／確認日）で記述する反復単位。
**初出**: 第1章

---

## クラウド事業者

### AWS
**英語**: Amazon Web Services
**定義**: Amazon が提供するクラウドプラットフォーム。本書の比較対象4社の一つ。
**初出**: 序章

### Azure
**英語**: Microsoft Azure
**定義**: Microsoft が提供するクラウドプラットフォーム。本書の比較対象4社の一つ。
**初出**: 序章

### Google Cloud
**英語**: Google Cloud Platform（GCP）
**定義**: Google が提供するクラウドプラットフォーム。本書では「Google Cloud」と表記し、GCPと略さない。
**初出**: 序章

### OCI
**英語**: Oracle Cloud Infrastructure
**定義**: Oracle が提供するクラウドプラットフォーム。本書が原点（基準点）に置く事業者。
**初出**: 序章

---

## アイデンティティ／認可（第1章）

### IDaaS (Identity as a Service)
**定義**: アイデンティティ管理をクラウドサービスとして提供する形態。
**初出**: 第1章

### ワークフォースID (Workforce Identity)
**定義**: 従業員・社内ユーザーのアイデンティティ。
**初出**: 第1章

### CIAM (Customer Identity and Access Management)
**定義**: 顧客・外部ユーザー向けのアイデンティティ管理。
**初出**: 第1章

### ワークロードID (Workload Identity)
**定義**: 人間ではなくアプリケーション・サービスに付与されるアイデンティティ。
**初出**: 第1章

### フェデレーション (Federation)
**定義**: 異なるIDドメイン間で認証情報を信頼・連携する仕組み。
**初出**: 第1章

### 委譲 (Delegation)
**定義**: あるエンティティが別のエンティティに代わって権限を行使すること。
**初出**: 第1章

### ID伝播 (Identity Propagation)
**定義**: 呼び出しの連鎖を通じて、元のユーザーのアイデンティティを下流（データ層を含む）まで引き継ぐこと。
**初出**: 第1章

### OBO (On-Behalf-Of)
**定義**: Azure（Entra）における委譲フロー。アプリがユーザーに代わって下流APIを呼ぶ際のトークン取得方式。
**初出**: 第1章

### Token Exchange
**英語**: OAuth 2.0 Token Exchange (RFC 8693)
**定義**: あるトークンを別のトークンに交換する標準フロー。OCIのID伝播の基盤。
**初出**: 第1章

### Identity Propagation Trust
**定義**: OCIで外部IdPからのID伝播を信頼するための設定。impersonationで代理元を保持する。
**初出**: 第1章

### エージェントID (Agent Identity)
**定義**: AIエージェントに付与されるアイデンティティ。Entra Agent ID 等。
**初出**: 第1章

---

## 実行基盤（第2章）

### マネージドKubernetes (Managed Kubernetes)
**定義**: クラウド事業者が管理するKubernetesサービス。EKS / AKS / GKE / OKE。
**初出**: 第2章

### OKE
**英語**: Oracle Container Engine for Kubernetes
**定義**: OCIのマネージドKubernetes。公式名称は「Container Engine for Kubernetes」、略称OKE。
**初出**: 第2章

### サーバーレスコンテナ (Serverless Container)
**定義**: インフラ管理なしにコンテナを実行する形態。Fargate / Container Apps / Cloud Run / Container Instances。
**初出**: 第2章

### レジストリ (Container Registry)
**定義**: コンテナイメージを保管する場所。
**初出**: 第2章

---

## オブジェクトストレージ（第3章）

### オブジェクトストレージ (Object Storage)
**定義**: 非構造化データをオブジェクト単位で格納するストレージ。S3 / Blob / GCS / OCI Object Storage。
**初出**: 第3章

### レイクハウス (Lakehouse)
**定義**: データレイクとデータウェアハウスの特性を統合したアーキテクチャ。
**初出**: 第3章

### テーブルフォーマット (Table Format)
**定義**: オブジェクトストレージ上の表形式データを管理する形式（Iceberg / Delta Lake 等）。
**初出**: 第3章

---

## マネージドAI（第4章）

### 基盤モデル (Foundation Model)
**定義**: 大規模に事前学習され、多様なタスクに適用できるAIモデル。
**初出**: 第4章

### マネージドRAG (Managed RAG)
**定義**: 検索拡張生成の構成要素を事業者が統合提供する形態。
**初出**: 第4章

### RAG (Retrieval-Augmented Generation)
**定義**: 検索拡張生成。外部データを検索して生成に与える手法。
**初出**: 第3章

### エージェント基盤 (Agent Platform)
**定義**: AIエージェントの構築・実行を支える事業者のサービス群。
**初出**: 第4章

### ガードレール (Guardrails)
**定義**: 生成AIの入出力を制御・制限する安全機構。
**初出**: 第4章

### MLプラットフォーム (ML Platform)
**定義**: 機械学習モデルの開発・運用を支える基盤。SageMaker / Azure ML / Vertex AI / OCI Data Science。
**初出**: 第4章

### MCP (Model Context Protocol)
**定義**: モデルと外部ツール・データを接続する標準プロトコル。
**初出**: 第4章

### Amazon Bedrock
**定義**: AWSのマネージド基盤モデルサービス。
**初出**: 第4章

### Microsoft Foundry
**定義**: Azureの基盤モデル／AIアプリ基盤（旧 Azure AI Studio → AI Foundry → Microsoft Foundry。確認日付きで扱う）。
**初出**: 第4章

### Vertex AI
**定義**: Google CloudのML／生成AI統合プラットフォーム。
**初出**: 第4章

### OCI Generative AI
**定義**: OCIのマネージド生成AIサービス。
**初出**: 第4章

---

## データ側AI（第5章）

### DB組み込みAI (In-Database AI)
**定義**: データベース内でAI機能（ベクトル検索・LLM呼び出し等）を実行する方式。
**初出**: 第5章

### DB内ベクトル (In-Database Vector)
**定義**: データベース内に埋め込みベクトルを格納し検索する機能。
**初出**: 第5章

### Select AI
**定義**: OracleのSQLからLLMを呼び出す／自然言語をSQLに変換する機能。
**初出**: 第5章

### NL→SQL (Natural Language to SQL)
**定義**: 自然言語の問いをSQLクエリに変換する機能。
**初出**: 第5章

### ハイブリッド検索 (Hybrid Search)
**定義**: ベクトル検索とキーワード検索を組み合わせた検索方式。
**初出**: 第5章

### Deep Data Security
**定義**: OracleのDB内で行/列/セル単位の認可を宣言的に行い、SQL生成元を問わず一貫適用する仕組み。
**初出**: 第5章

### Trusted Identity Propagation
**定義**: AWS等で、ユーザーIDをデータサービスまで伝播させる仕組み。RLS/CLSと組み合わせる。
**初出**: 第5章

### RLS / CLS (Row-Level Security / Column-Level Security)
**定義**: 行単位／列単位のアクセス制御。
**初出**: 第5章

---

## 観測性／ガバナンス（第6章）

### 観測性 (Observability、o11y)
**定義**: システムの内部状態を外部出力（メトリクス・ログ・トレース）から把握する能力。
**初出**: 第6章

### LLM特化o11y (LLM Observability)
**定義**: LLM／エージェントの挙動（トークン・コスト・品質・トレース）に特化した観測性。
**初出**: 第6章

### OTel GenAI semconv
**英語**: OpenTelemetry GenAI Semantic Conventions
**定義**: 生成AIの観測データに関するOpenTelemetryの意味規約。クラウド非依存の共通層。
**初出**: 第6章

### Langfuse
**定義**: LLMアプリの観測・評価のためのオープンソースツール。クラウド非依存。
**初出**: 第6章

### AIゲートウェイ (AI Gateway)
**定義**: AIモデルへのアクセスを集約・制御・監査する中間層。
**初出**: 第6章

### 行動監査 (Action Audit)
**定義**: ユーザー・エージェントの操作を記録・追跡すること。Agent 365 / Deep Data Securityの監査等。
**初出**: 第6章

---

## 統合・実践（統合章・終章）

### 対訳辞書 (Cross-reference Dictionary)
**定義**: 全領域を横断した「他社→OCI」対応を集約した辞書。統合章で構成する。
**初出**: 統合章

### リファレンスアーキテクチャ (Reference Architecture、RA)
**定義**: 事業者が公式に提示する典型的なアーキテクチャ設計。AWS SRA / Azure AI Landing Zones / Google Cloud Architecture Center / OCI Architecture Center。
**初出**: 終章

---

## 索引（五十音順）

### あ行
ID伝播、IDaaS、AIゲートウェイ、軸、エージェントID、エージェント基盤、OBO、オブジェクトストレージ、観測性、原点

### か行
ガードレール、確認日、基盤モデル、ケイパビリティ・カード、行動監査

### さ行
作業（→軸）、SWOTスライス、新顔の分類手順、スナップショット、Select AI

### た行
対訳、対訳辞書、テーブルフォーマット、DB組み込みAI、DB内ベクトル、Deep Data Security、Token Exchange

### な行
NL→SQL、新顔の分類手順

### は行
ハイブリッド検索、フェデレーション、プロット、Vertex AI、ワークフォースID（→わ行）

### ま行
マネージドAI、マネージドKubernetes、マネージドRAG、MCP、MLプラットフォーム、Microsoft Foundry

### や行
（なし）

### ら行
ラングフューズ（Langfuse）、リファレンスアーキテクチャ、両方向ギャップ、レイクハウス、レジストリ、RLS / CLS、RAG

### わ行
ワークフォースID、ワークロードID

### A-Z
AWS、Azure、CIAM、Deep Data Security、Google Cloud、Identity Propagation Trust、Langfuse、MCP、NL→SQL、OCI、OCI Generative AI、OKE、OTel GenAI semconv、RAG、RLS / CLS、Select AI、SWOTスライス、Token Exchange、Trusted Identity Propagation、Vertex AI
