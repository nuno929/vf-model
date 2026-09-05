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
physical flows / ΔK
   ↓ monetary measurement
P/L_i
   ↓ closing / attribution / distribution
B/S_i = K_i
```

`K_i` は K の subset / partition ではない。

---

## 2. 契約・制度・金融資産

契約・制度・法的権利関係それ自体は K の resource quantity としない。

一方、預金、債券、売掛債権等が会計上 financial asset position として認識・評価される場合、その monetary position は B/S 上の `K_i` に含められる。

主体が契約・制度の履行・執行・継続をどう期待するかは P に属する。

---

## 3. P/L / B/S / surplus

P/L は期間中の physical / economic flow を monetary unit で表現する。B/S は actor-specific capital stock / position を monetary unit で表現する。

```text
physical flow
   ↓ μ
P/L monetary amounts
   ↓ aggregation / consolidation
surplus / deficit
   ↓ attribution / retention / distribution
B/S K_i
```

surplus は physical primitive ではなく accounting-derived period increment / residual である。

---

## 4. 3つの管理合理性公理

1. resource-realization
2. activity-flow
3. P-downside

3則は経験的普遍法則ではなく VFT の constitutive rationality assumptions である。

経験的仮説は projection ごとに objective / priority / weight / constraint / threshold / horizon を具体化して形成する。

---

## 5. plan / forecast / equilibrium

必要な economic projection では planned / chosen resource change を `x_i` と書く。

```text
x_i          = planned / chosen resource change
E_i[ΔK(...)] = expected realized resource change
```

`E_i[ΔK(S,τ) | a,I_i]` の `|a` は observational conditioning ではなく action-contingent forecast の略記である。

compatibility / market equilibrium / accounting consistency / steady state は別概念とする。

---

## 6. Marxian categories

VFT は Marxian economics が区別した use-value / labor / exchange-value / surplus / accumulation を一般化された構造上で表現できる。

ただし、Marx 固有の value theory は projection-specific specialization である。

### use-value

K が特定の A / transformation を可能にする機能・有用性として扱う。

```text
use-value ≠ subjective utility ≠ price
```

### labor

labor activity / labor time は physical / productive flow の一部として記述できる。

Marxian labor-value を構成する場合は socially necessary labor time 等の追加条件を導入する。

### exchange-value / price

market / monetary valuation として扱う。

### surplus

generic surplus は指定 P/L accounting boundary における monetary increment / residual とする。

Marxian surplus value と同一視するには Marx 固有の追加条件が必要である。

### accumulation / distribution

surplus の attribution / retention / distribution が次期 B/S 上の `K_i` を変える過程として記述する。

---

## 7. ミクロ／マクロ

```text
micro
K, K_i, P_i -> A_i -> physical flow -> P/L_i -> K_i(t+1)

                         ↓ aggregation / consolidation

macro
physical production / consumption
aggregate P/L increment / surplus
capital-stock distribution
capital accumulation
shared P
```

同じ physical K と monetary representations を異なる scope で観測・集約することで接続する。

---

## 8. 射影時に明示するもの

1. K の resource coordinates
2. actor set
3. A の event unit
4. ΔK の観測単位
5. monetary measurement / valuation rule
6. P/L recognition / classification
7. B/S ownership / attribution / recognition
8. K_i の book-value rule
9. P / shared P の proxy
10. E[ΔK] の推定法
11. accounting boundary / consolidation rule
12. surplus の算出・帰属・分配
13. Marxian specialization を使う場合の追加条件
14. micro / macro aggregation rule

---

© T. Nuno  
Licensed under CC BY 4.0