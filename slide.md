---
marp: true
paginate: true
header: 'マネージャー不在の組織は機能するのか？'
---

<style>
/* 基本スタイル */
section {
  font-family: 'Hiragino Sans', sans-serif;
  padding: 40px;
  font-size: 24px;
}

h1 {
  color: #395ACC;
  font-size: 32px;
  margin-bottom: 1em;
}

h2 {
  font-size: 28px;
}

strong {
  color: #F777A6;
}

/* 共通レイアウト */
.container {
  display: flex;
  gap: 40px;
}

/* テーブル共通スタイル */
table {
  width: 100%;
  border-collapse: collapse;
  margin: 1em 0;
  font-size: 18px;
}

th {
  background: #f5f5f5;
  font-weight: bold;
  padding: 16px;
}

td {
  border: 1px solid #ccc;
  padding: 16px;
  vertical-align: top;
  line-height: 1.8;
}

/* ノート・サマリー共通スタイル */
.note, .summary {
  background: #f5f5f5;
  padding: 20px;
  line-height: 1.6;
}

.note {
  border-left: 4px solid #395ACC;
  font-size: 18px;
  margin-top: 20px;
}

.summary {
  font-size: 22px;
}

/* ユーティリティクラス */
.flex-shrink-0 {
  flex-shrink: 0;
}

.flex-grow-1 {
  flex-grow: 1;
}
</style>

# マネージャー不在の組織は機能するのか？
## 元VPoEから見たUbieの実態

<div style="position: absolute; bottom: 80px;">

### Ubie株式会社
橋山 牧人

</div>

---
# 自己紹介

<style scoped>
.container {
  align-items: flex-start;
}
.profile-image {
  flex-shrink: 0;
}
.profile-text {
  flex-grow: 1;
}
</style>

<div class="container">
<div class="profile-image">

![width:180px](./images/selfee.jpg)

</div>
<div class="profile-text">

### 略歴
- 橋山 牧人 / [@hashiyaman](https://twitter.com/hashiyaman)
- Engineering Organization Lead @Ubie
- これまで: EM/VPoE として10年以上の経験
  - 楽天グループ: お買い物かごシステムの開発・運用
  - OLTA: 開発組織のマネジメント全般、採用・評価制度の設計

### Ubie入社の理由
- ホラクラシーによるマネージャー不在の組織運営、評価と報酬を切り離す仕組みがどのようにワークしているか興味があったため

</div>
</div>

---
# ホラクラシー組織とは

ホラクラシーは、従来の階層型組織構造とは異なる組織運営モデルである。

<style scoped>
.container {
  align-items: center;
}
.structure-image {
  text-align: center;
}
.caption {
  font-size: 14px;
  color: #666;
  margin-top: 8px;
}
</style>

<div class="container">
<div class="structure-image">

![height:300px](./images/holacracy.png)

<div class="caption">ロール・サークルの階層構造を示した図</div>

</div>
<div class="structure-text">

### 重要な特徴
- 意思決定や権限を、個人ではなく役割（ロール）に紐づけ分散させる
- **階層構造を持つ**組織であり、完全なフラットではない

</div>
</div>

---
# ホラクラシー組織における意思決定の仕組み

従来の階層型組織では、多くの承認プロセスが組織のボトルネックとなっていた。
ホラクラシーでは、各ロールが課題解決の責任と権限を持つため迅速な判断が可能。

<style scoped>
.container {
  display: flex;
  align-items: center;
  gap: 40px;
}
.decision-image {
  flex-shrink: 0;
  width: 50%;
  text-align: center;
}
.decision-table {
  flex-grow: 1;
  width: 50%;
}
img {
  max-height: 300px;
  width: auto;
}
table {
  width: 100%;
  font-size: 20px;
  margin: 0 auto;
}
</style>

<div class="container">
<div class="decision-image">

![height:250px](./images/decision-making.png)

</div>
<div class="decision-table">

| 従来の階層型組織 | ホラクラシー組織 |
|:--|:--|
| マネージャーに相談 | 関係者に直接相談 |
| マネージャー経由で調整 | 担当者が優先順位を判断 |
| 承認後に実施 | 特別な承認なく実施 |

</div>
</div>

---
# Ubieにおけるマネジメントのやり方

1. リソースアサインメント

2. 人材開発（目標設定・フィードバック）


---
# リソースアサインメント

四半期ごとのOKRを基準に、各サークル内で優先順位とリソースを決定する。
この時、必要に応じてサークルやロールの組織構造（ガバナンス*1）を再編成する。

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
.note {
  background: #f5f5f5;
  border-left: 4px solid #395ACC;
  padding: 12px 20px;
  margin-top: 20px;
  font-size: 18px;
}
table {
  width: 100%;
  font-size: 22px;
  margin: 0 auto;
}
</style>

<div class="container">

| プロセス | 階層型組織 | ホラクラシー組織（Ubie） |
|:--|:--|:--|
| OKRの決定 | マネージャーが実施 | ・担当サークル、ロールが実施 |
| 組織構造の決定 | マネージャーが実施 | ・サークルリード(*2)、担当ロールが実施 |
| 優先順位の決定 | マネージャー・POが実施 | ・サークルリード、担当ロールが実施 |
| リソースアサイン | ・マネージャー間で相談<br>・上位マネージャーの承認 | ・担当サークル・ロール間で相談<br>・専用サークル・ロールがサポート<br>・既定の周知プロセスで承認 |

<div class="note">

*1 ホラクラシー用語。サークルの責任・権限の範囲、所属するロールや会議体などのコミュニケーション設計などを意味する。
*2 役割の割り当てやリソース管理の責任を持つが、**メンバーへの直接的な命令権はない**ところがマネージャーとの違いである。

</div>

</div>

---
# リソースアサインメントの実例

（例）OKRを推進するための新規開発を行うチームの組成

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  gap: 30px;
}
table {
  width: 100%;
  font-size: 18px;
  margin: 0 auto;
}
th {
  background: #f5f5f5;
  font-weight: bold;
  padding: 16px;
}
td {
  vertical-align: top;
  line-height: 1.8;
  padding: 16px;
}
</style>

<div class="container">

| プロセス | 階層型組織（前職まで） | ホラクラシー組織（Ubie） |
|:--|:--|:--|
| チーム組成 | - 自分が必要なスキル・チーム構成を検討する<br>- 各チームと調整しながらメンバーをアサインする | - 適任者が自主的にロール・サークルを作りリードになる<br>- 必要なメンバーを他サークル・ロールと調整して集める |
| リソース調整 | - 必要に応じ他チームからの異動や新規採用を検討する<br>- **最終決定権はマネージャー（自分）が保持** | - 自分は候補提案や交渉をサポートする<br>- **最終判断はロール同士・サークル同士で決定** |

</div>

---
# 人材開発（目標設定・フィードバック）

評価を報酬と切り離しつつ、**Self-Development Policy** に基づき、社員自身が能力開発の主体となる目標設定とフィードバックの仕組みを導入している。

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
.note {
  background: #f5f5f5;
  border-left: 4px solid #395ACC;
  padding: 12px 20px;
  margin-top: 20px;
  font-size: 18px;
}
table {
  width: 100%;
  font-size: 22px;
  margin: 0 auto;
}
</style>

<div class="container">

| プロセス | 階層型組織 | ホラクラシー組織（Ubie） |
|:--|:--|:--|
| 目標設定 | マネージャーが主導 | ・メンバーが事業戦略やOKRをもとに自ら決定<br>・U-map(*1)を参考に伸ばすべき能力を設定 |
| 評価・フィードバック | マネージャーが一元的に実施 | ・伴走ペア(*2)による定期的なフィードバック |
| 能力開発支援 | マネージャーとHRが担当 | ・専門のロール、サークルを各部署に設置<br>・サポート機能を伴奏ペア、担当ロールで分散 |

<div class="note">

*1 個人の役割と進化の方向性を明確化するスキルマップ。事業のフェーズや役割に応じて複数の分類が定められている。
*2 人材開発のロールを担い、同じサークルに所属する経験者。U-mapにおいて「戦略策定・操舵力」に強みを持つ。

</div>

</div>

---
# 人材開発の実例

（例）エンジニアの能力開発プロセス

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  gap: 30px;
}
table {
  width: 100%;
  font-size: 18px;
  margin: 0 auto;
}
th {
  background: #f5f5f5;
  font-weight: bold;
  padding: 16px;
}
td {
  vertical-align: top;
  line-height: 1.8;
  padding: 16px;
}
</style>

<div class="container">

| プロセス | 階層型組織（前職まで） | ホラクラシー組織（Ubie） |
|:--|:--|:--|
| 目標設定・評価 | - 私やマネージャーが毎週1on1でフィードバック<br>- 目標設定や評価は私が最終決定権を保持 | - エンジニアがU-mapを参考に自身で目標設定<br>- 伴走ペアが定期的にフィードバックを実施 |
| 能力開発の方向性 | - **マネージャーがWill/Canを考慮して決定** | - エンジニア自身が主体的に決定する<br>- **組織はサポートと仕組みづくりに徹する** |

</div>

---
# マネージャー不在の組織の良い点・課題点

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  gap: 30px;
}
table {
  width: 100%;
  font-size: 18px;
  margin: 0 auto;
}
th {
  background: #f5f5f5;
  font-weight: bold;
  padding: 16px;
}
td {
  vertical-align: top;
  line-height: 1.8;
  padding: 16px;
}
.note {
  background: #f5f5f5;
  border-left: 4px solid #395ACC;
  padding: 12px 20px;
  margin-top: 20px;
  font-size: 18px;
}
</style>

<div class="container">

| 観点 | 良い点 | 課題点 |
|:--|:--|:--|
| リソースアサインメント | 担当者間で優先順位やリソースの調整が可能で、マネージャーがボトルネックにならず意思決定が迅速 | トピックごとに適切な担当者とのコミュニケーションが必要で、組織規模に比例して調整コストが増加 |
| 人材開発 | キャリアの自己決定を本人の責任とすることで、納得感が高い目標設定とフィードバックを実現 | キャリアの一貫性・連続性を担保する難易度が高く、ライフステージの変化への対応が課題 |

<div class="note">

### キーポイント
- ホラクラシーは、**リソース調整のリードタイムや機会損失コストがコミュニケーションコストを上回る場合**に効果的
- 人材開発の主体は本人に置きつつ、サポート制度（フィードバックトレーニング、コーチング等）を拡充
- トレードオフとなる課題の解決には、**階層型組織と同様に**様々な仕組みや改善が必要

</div>

</div>

---
# まとめ

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  gap: 30px;
}
.summary {
  background: #f5f5f5;
  padding: 20px;
  line-height: 1.6;
  font-size: 22px;
}
</style>

<div class="container">

<div class="summary">

### ホラクラシー組織の特徴
- 意思決定や権限を、**役割（ロール）に紐づけ分散**
- **各ロールが課題解決の責任と権限を持ち**、迅速な判断が可能

### Ubieにおけるマネジメント機能の実現
- リソースアサインメント: サークル間の自律的な調整と意思決定により実現
- 人材開発: Self-Development Policy に基づく目標設定とフィードバックの仕組みを導入

### マネージャー不在組織の要点
- 意思決定の迅速化とコミュニケーションコストのトレードオフ
- キャリアの自己決定によるマネジメントコストの低減とキャリアの一貫性担保のトレードオフ

</div>

</div>

---
# 興味を持っていただいた方へ

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  gap: 30px;
}
.content {
  background: #f5f5f5;
  border-left: 4px solid #395ACC;
  padding: 20px;
  line-height: 1.6;
}
.links {
  display: flex;
  gap: 20px;
  margin: 20px 0;
}
.button {
  background: #395ACC;
  color: white;
  padding: 12px 24px;
  border-radius: 4px;
  text-decoration: none;
  font-weight: bold;
}
</style>

<div class="container">

### 採用情報
- 総合採用サイト：https://recruit.ubie.life/#jobdescription
- カジュアル面談：https://recruit.ubie.life/casual-meeting

### 発表者へのお問い合わせ
- X: [@capyogu](https://twitter.com/capyogu)
- Note: [note.com/hashiyaman](https://note.com/hashiyaman)

</div>