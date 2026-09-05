# 価値場理論 — 計測

## 1. 目的

本書は、価値場理論の Core を実証・観測・会計へ落とす際の境界を整理する。

Core では、K は資源・資本、`K_i` は主体 `i` に所有・保有・帰属する資源・資本、`P_i` は主体ごとの subjective evaluation / expectation state、A は actor-side process / event として扱う。

VFT は K / K_i / P / ΔK の完全観測を前提としない。計測上の中心は、**何を直接観測し、何を記帳し、何を proxy から推定するかを区別すること**にある。

---

## 2. K と K_i の計測

K は対象経済・社会に存在する resource / capital state を参照する。

`K_i` は、そのうち主体 `i` に所有・保有・帰属すると扱う部分である。`K_i` は主体の主観的な「利用可能感」ではない。その認識は P に属する。

K / K_i の真値を主体本人や観測者が完全に把握しているとは仮定しない。未把握資産・債務、評価差、共有資産、複雑な帰属関係等により、実際の状態と認識・記帳値はずれうる。

候補 observable / records には、

- 資産台帳・在庫台帳
- 現金・金融資産残高
- 設備・土地・原材料・製品
- 労働時間・人的資本・技能
- 物量・稼働・消耗記録

等がある。

所有・帰属をどう扱うかは法域・会計境界・対象 projection に依存する。Core は普遍的な所有判定関数を固定しない。

---

## 3. P の計測

`P_i` は、主体 `i` が持つ将来見通し、評価、選好、信用、信念、規範認識等を含む主観状態である。

P は多数主体に共有されても主観状態であり、客観的な P の真値へ変わるわけではない。

必要な projection では、主体集合 `G` の P の共通性・整合度・分布を shared P として扱える。ただし shared P も直接観測される単一客観量ではなく、複数主体の proxy から推定する。

候補 proxy には、

- 期待・信念・選好・評価の調査
- 発話・文章・選択履歴
- 信用・信頼に関する調査値
- 契約・制度への履行期待・執行期待
- 市場 outcome から間接推定される期待

等がある。

価格、金利、スプレッド、支持率、rating 等は P そのものではなく、P と K / A / market process の相互作用から生じる observable でありうる。

### proxy admissibility

P proxy を使う場合は少なくとも、

1. target A / ΔK より前に観測されたか
2. 同時決定なら joint model を明示しているか
3. target outcome を使って P を事後構成していないか
4. proxy validity を別データ・制約で検証できるか

を確認する。

---

## 4. 契約・制度の観測

契約・制度を、そのまま K の resource / capital として扱わない。

- 契約締結・政策変更・判決・制度変更 → observable event / A
- 契約書・法令・判決文等 → record / information source
- 主体が履行・執行・継続をどう期待するか → P
- 執行・履行によって実際に生じた資源・資本移転 → ΔK

契約には法的効力がありうるが、その効力を資源量と同一視しない。VFT 上では、法的・制度的事実と、主体がそれをどう認識・期待するか、そして最終的にどの resource / capital change が実現したかを分けて追う。

---

## 5. A の観測可能性と時間型

A は各主体側で生じる process / event を表す。

外部 action event は直接観測できる場合がある。取引、移動、発話、投資、労働、生産、契約締結、政策実施等が該当する。

内部 decision / observation / interpretation は直接観測できない場合があり、proxy を要する。

時間型は、普遍的な状態遷移式を固定せず、

```text
(K_t0, P_t0)
      ↓ conditions
A_(t0,t1]
      ↓ realized processes / resource use
(K_t1, P_t1)
```

とする。

---

## 6. ΔK / ΔP の観測と記帳

### ΔK

`ΔK` は K の利用・移転・変換・消費・生成等の結果として実現した resource / capital change を表す。

実証では主に、

1. 会計・台帳・取引記録等による記帳
2. 活動後の resource / capital state の観測

から ΔK をトレースする。

一つの A が複数の ΔK を生む場合は、それぞれを別 record として保持する。

```text
A
├─ material       -10
├─ labor input     -5
├─ equipment wear  -2
└─ product         +20
```

区間活動量を表す独立変数 `H` は置かない。gross production / consumption / transaction 等を分析したい場合は、A と ΔK records の event history を用いる。

### net change と gross activity

同じ区間で生産100・消費100が起こり最終在庫が変わらない場合、net state change は0になりうる。しかし生産・消費の各 record は残る。

したがって、gross activity と net state change の違いは、独立変数を追加するのではなく、**記帳粒度・event history・aggregation rule** で扱う。

### ΔP

`ΔP_i` は主体 `i` の P に実現した変化を表す。

```text
P_i,t0 -> P_i,t1
```

P は一般に非加法的であり、普遍的な算術差は定義しない。

---

## 7. 会計評価と surplus

異質な ΔK は物理単位のまま直接加算できない場合がある。

指定した valuation / bookkeeping rule により共通尺度へ写像し、同じ accounting boundary で差し引く。

```text
realized ΔK records
        ↓ valuation / bookkeeping
accounting entries
        ↓ aggregation
surplus / deficit
```

surplus は直接観測される物理量ではなく、**実現した ΔK records を特定の会計・評価体系で集約した派生量**である。

したがって surplus を測る場合は、少なくとも次を明示する。

1. 対象 ΔK records
2. accounting boundary
3. valuation / unit-of-account
4. recognition timing
5. aggregation / offset rule
6. ownership / attribution rule

貨幣は、保有される資産として K に現れる場合と、unit of account / valuation scale として使われる場合を区別する。

---

## 8. E[ΔK] の位置づけ

`E_i[ΔK]` は、主体 `i` が形成する expected realized resource / capital change である。

`E_i[ΔK]` は desire / preference / plan ではない。望ましさ・選好は P に属する。

ΔK が多次元で expectation を直接定義できない場合は、projection 側で必要な quantitative representation を定める。

candidate action ごとの forecast が必要なら、

```text
E_i[ΔK(S, τ) | a, I_i]
```

のように表せる。

---

## 9. 集約とミクロ／マクロ

ミクロとマクロは別の K ではない。同じ K と同じ ΔK records を、異なる ownership / accounting / aggregation boundary から観測する。

micro observable から macro observable を再構成する場合にだけ、projection-local な aggregation / coarsening rule を追加する。

集約では少なくとも、

- actor set
- ownership / attribution boundary
- accounting boundary
- ΔK record の対応
- P proxy の集約方法
- shared P の推定方法
- surplus / deficit の帰属・分配
- 情報損失

を明示する。

---

## 10. 3つの管理合理性を扱う計測

resource-realization / activity-flow / P-downside の3則は、意思決定合理性の公理系として扱う。

計測では「3則が存在するか」を毎回再証明するのではなく、actor / context / institution / role / time horizon によって、3則の比重・優先順位・分担がどう変わり、どの A / ΔK / ΔP が生じるかを扱う。

P-downside を扱う際は、対象主体集合、P 次元、shared P proxy、downside / threshold / viability criterion を事前に定める。客観的な P 真値の存在は仮定しない。

---

## 11. 経済射影での計測

### plan / choice と budget

必要な economic projection では planned / chosen resource change を `x_i` と書ける。

```text
x_i          = planned / chosen resource change
E_i[ΔK(...)] = expected realized resource change
```

予算制約は `x_i` 側へ置き、forecast と混同しない。

### 使用価値・労働価値・交換価値

- 使用価値：K が特定目的の A / transformation を可能にする機能を観測・評価
- 労働価値：投入 labor activity / labor time を計測尺度として採用
- 交換価値・価格：market / accounting valuation
- surplus：ΔK records を共通尺度化して得る accounting residual

これらを同一の「価値」変数へ潰さない。

---

## 12. 実証上の原則

少なくとも以下を明示する。

1. 観測スケール
2. K の対象範囲
3. K_i の ownership / attribution rule
4. K / K_i の observable / records
5. P の採用次元・proxy
6. shared P の対象 actor set と推定法
7. A の観測単位・event ordering
8. ΔK records の認識・記帳方法
9. ΔP の proxy / mapping
10. expectation operator / `E[ΔK]` の推定方法
11. valuation / bookkeeping / accounting boundary
12. surplus / deficit の集約規則
13. planned / expected / realized change の分離
14. 3則の priority / constraint / horizon
15. compatibility / market equilibrium を扱う場合の追加条件
16. 欠測・測定誤差・情報損失

目的は、**資源・資本そのもの、主体の主観、行為、実現変化、会計評価、余剰を同一視しないこと**にある。

---

© T. Nuno  
Licensed under CC BY 4.0