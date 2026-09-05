# 価値場理論 — 既存概念・応用への射影ノート

> この文書は Core 定義ではなく、既存概念・応用領域への projection candidate を保存する。

## 1. 基本構造

VFT の経済射影では、

- `K`：実物・物理側の resource state
- `K_i`：B/S 上の actor-indexed book-value capital position
- `P_i`：subjective evaluation / expectation state
- `A_i`：actor-side process / event
- `ΔK`：K に実現した resource change

を区別する。

```text
physical K
   ↓ A_i
physical / use-value flow
   ↓ exchange / monetary measurement
P/L_i
   ↓ closing / attribution / distribution
B/S_i = K_i
```

`K_i` は K の subset / partition ではない。

---

## 2. 使用価値 / 交換価値

同一 resource は use-value side と exchange-value side の二重表現を持ちうる。

### use-value

resource が主体の A / transformation をどのように可能にし、期間内でどの程度効用を実現するかという側。

物理的 stock は時点で数えられるが、主体にとっての効用量は stock だけから一意に決まらず、限界効用の逓減等により期間中の利用・消費・充足との関係で評価される。

### exchange-value

resource を他の resource / money と比較可能な共通尺度へ写像した側。

時点 stock を共通尺度化して比較・集計する場合、その表現は exchange-value 側とみなす。

```text
use-value      ≈ flow-oriented / P/L-like
exchange-value ≈ stock-oriented / B/S-like
```

この対応は複式簿記を想起させるが、あくまで説明上のアナロジーであり、借方・貸方等を VFT Core の普遍構造とはしない。

---

## 3. 契約・制度・金融資産

契約・制度・法的権利関係それ自体は K の resource quantity としない。

一方、預金、債券、売掛債権等が会計上 financial asset position として認識・評価される場合、その monetary position は B/S 上の `K_i` に含められる。

主体が契約・制度の履行・執行・継続をどう期待するかは P に属する。

---

## 4. P/L / B/S / surplus

P/L は期間中の physical / economic flow を monetary unit で表現する。B/S は actor-specific capital stock / position を monetary unit で表現する。

帳簿そのものは actor-specific であり、主体ごとに recognition / valuation / bookkeeping が異なりうる。財務報告・統計はその外部 representation である。

```text
physical / use-value flow
   ↓ exchange-value measurement
P/L monetary amounts
   ↓ comparison / aggregation
surplus / deficit
   ↓ attribution / retention / distribution
B/S K_i
```

surplus は physical primitive ではなく、exchange-value の共通尺度へ写像した input / output 等の差分として成立する accounting-derived period increment / residual である。

---

## 5. P 更新

加工・変換によって同一由来の resource でも利用可能性が変わり、使用価値が変わる。

```text
K_t
 ↓ A
K_t1
 ↓ changed use possibilities / realized use-value
P_i update
```

主体は、A が K をどのような利用可能状態へ変えるかについて期待を持ち、実現した結果を受けて P_i を更新する。

---

## 6. 3つの管理合理性公理

1. resource-realization
2. activity-flow
3. P-downside

3則は経験的普遍法則ではなく VFT の constitutive rationality assumptions である。

経験的仮説は projection ごとに objective / priority / weight / constraint / threshold / horizon を具体化して形成する。

---

## 7. plan / forecast / equilibrium

必要な economic projection では planned / chosen resource change を `x_i` と書く。

```text
x_i          = planned / chosen resource change
E_i[ΔK(...)] = expected realized resource change
```

`E_i[ΔK(S,τ) | a,I_i]` の `|a` は observational conditioning ではなく action-contingent forecast の略記である。

compatibility / market equilibrium / accounting consistency / steady state は別概念とする。

---

## 8. Marxian categories

VFT は Marxian economics が区別した use-value / labor / exchange-value / surplus / accumulation を一般化された構造上で表現できる。

ただし、Marx 固有の value theory は projection-specific specialization である。

### labor

labor activity / labor time は physical / productive flow の一部として記述できる。

Marxian labor-value を構成する場合は socially necessary labor time 等の追加条件を導入する。

### surplus

generic surplus は exchange-value に写像された input / output 等の差分を、指定 accounting boundary で計量した monetary increment / residual とする。

Marxian surplus value と同一視するには Marx 固有の追加条件が必要である。

### accumulation / distribution

surplus の attribution / retention / distribution が次期 B/S 上の `K_i` を変える過程として記述する。

---

## 9. ミクロ／マクロ

```text
micro
K, K_i, P_i -> A_i -> physical/use-value flow -> P/L_i -> K_i(t+1)

                         ↓ external reporting / aggregation

macro
physical production / consumption
aggregate exchange-value increment / surplus
capital-stock distribution
capital accumulation
shared P
```

主体ごとの帳簿自体が共通化されることは仮定しない。外部 reporting / statistical transformation を介して macro representation を構成する。

---

## 10. 射影時に明示するもの

1. K の resource coordinates
2. actor set
3. A の event unit
4. ΔK の観測単位
5. use-value の期間・効用 proxy
6. exchange-value / monetary measurement rule
7. P/L recognition / classification
8. B/S ownership / attribution / recognition
9. K_i の book-value rule
10. P / shared P の proxy
11. E[ΔK] の推定法
12. accounting boundary
13. surplus の算出・帰属・分配
14. Marxian specialization を使う場合の追加条件
15. micro / macro reporting / aggregation rule

---

© T. Nuno  
Licensed under CC BY 4.0