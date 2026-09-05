# 価値場理論 — モデルノート

## 1. 目的

本ノートは、価値場理論（Value-Field Theory; VFT）の Core を README より形式的に整理する。

VFT は、**実物・物理側の資源状態 K、主体別の簿価資本状態 K_i、主体ごとの主観的評価・期待状態 P_i、actor-side process / event A_i** を同一の因果・会計構造で記述する。

Core は、実物世界と通貨・会計世界を区別する。ただし独立した「二つの宇宙」を置くのではなく、物理・実物側の activity / flow を monetary measurement / bookkeeping によって抽象的な通貨単位へ写像し、P/L と B/S を接続する。

---

## 2. K：実物・物理側の resource state

`K_t` は、時点 `t` に存在する実物・物理側の resource state を表す。

```text
K_t
```

対象 projection に応じて、設備、土地、原材料、製品、時間、身体、技能、知識、労働力、エネルギー等を含みうる。

K は「外部に実在するものすべて」ではない。契約、制度、規範、法的権利関係、金融 claim の法的構造等を、それだけを理由に K へ含めない。

K の利用・変換・消費・生成等は A を通じて起こり、その結果として resource change が実現する。

---

## 3. K_i：B/S 側の actor-indexed book-value capital

`K_i,t` は、主体 `i` に帰属する資本 position を B/S 上の通貨単位で定量表現したものとする。

```text
common physical / economic state
        ↓ ownership / holding / attribution
        ↓ recognition / valuation / bookkeeping
      K_i,t
```

### K と K_i の型

`K_i` は K の subset でも、K の互いに素な partition でもない。

`(K_i)_i` は、common K と economic events に対して ownership / holding / attribution rule と monetary valuation / bookkeeping rule を適用した **actor-indexed representation** である。

したがって、共同所有・重複帰属・連結契約・複雑な資本構成を排除しない。`K_i` の変化は、common K の物理量が同じだけ変化したことを意味しない。

### 金融資産との境界

預金、債券、売掛債権等は、その根拠となる契約・法的権利関係そのものを K とみなすのではなく、会計 projection が financial asset position として認識・評価した **B/S 上の K_i** として表現できる。

---

## 4. 使用価値と交換価値

VFT では、同一の physical resource を少なくとも二つの value representation から扱う。

```text
same resource r
├─ use-value representation
└─ exchange-value representation
```

### 使用価値

使用価値は、resource `r` が主体の A / transformation をどのように可能にし、期間内でどの程度効用を実現するかに関係する。

物理的な保有 stock は時点で数えられるが、その stock 量だけから主体にとっての効用量は一意に決まらない。限界効用の逓減等により、実現効用は期間中の利用・消費・充足に依存する。この意味で使用価値は **flow-oriented** である。

個別用途の代替可能性や効用関数を Core では固定しない。

### 交換価値

交換価値は、異質な resource を他の resource / money との比較関係から共通尺度へ写像した量である。

交換価値は比較可能な尺度へ変換されることで、時点の stock / position として表現・集計できる。この意味で交換価値は **stock-oriented** である。

使用価値を時点 stock として共通尺度化・比較評価した場合、その表現は exchange-value representation へ移ったものとして扱う。

### 複式簿記との関係

使用価値と交換価値の二重表現は、同一対象を二つの側面から保持するという意味で複式簿記を想起させる。

ただしこれは **説明上のアナロジー** であり、VFT は全主体が借方・貸方や会計恒等式を内的に保持すると仮定しない。

個人は利用可能量・交換可能量を感覚的に保持しうる一方、企業は在庫管理・評価・会計原則等によってより形式的に保持しうる。

---

## 5. P：subjective evaluation / expectation state

各 `P_i,t` は、主体 `i` の将来見通し、評価、選好、信用、信念、期待、規範認識等を含む subjective state である。

```text
P_t = (P_i,t)_{i in I}
```

P はどれだけ共有されても主観状態である。shared P は複数主体の P の共通性・整合性・分布として扱い、客観的な社会価値の真値とはみなさない。

P の完全観測は前提とせず、projection ごとに proxy を用いる。

契約・制度は、それ自体を K の resource quantity へ押し込まず、法的・制度的 event / record、主体の履行・執行期待 P、実際に生じた resource / accounting effect を分けて扱う。

### 加工・変換と P 更新

同一由来の資源でも、A による加工・変換後には利用可能性が変わり、使用価値も変化する。

```text
K_t
 ↓ A
K_t1
 ↓ changed use possibilities / realized use-value
P_i,t -> P_i,t1
```

主体は、どの A が K をどのような利用可能状態へ変えるかについて期待を持つ。実現した加工結果・使用価値は、その期待を更新し、次の A を条件づける。

---

## 6. A：actor-side process / event

A は各主体側で生じる process / event を表す。

```text
A_τ = (A_i,τ)_{i in I}
```

生産、消費、交換、投資、労働、移転、契約締結、政策、情報伝達等を必要な粒度で A として記述する。

---

## 7. ΔK：物理・実物側の realized resource change

`ΔK` は、A 等により K に実現した resource change を表す。

重要なのは、**ΔK は会計仕訳ではない**という点である。会計仕訳は、物理・実物側で起きた activity / change を monetary measurement と recognition rule によって帳簿へ写像した表現である。

また `ΔK` は必ずしも単一の

```text
K_t1 - K_t0
```

を意味しない。異質な resource coordinates では、それぞれの resource change を記述し、endpoint net difference が必要な場合だけ対象 projection で集約する。

---

## 8. P/L と B/S

VFT では、P/L と B/S を同じ会計帳簿として一括りにせず、表現対象を分ける。

### P/L 側

P/L が表現する対象は、期間中に物理・実物世界で起きた activity / flow である。

```text
K_t0
 ↓ A
production / consumption / labor / depreciation / exchange / transfer
 ↓ monetary measurement μ
P/L entries
```

P/L statement 自体は通貨単位で記帳されるが、その対象は期間中の physical / economic flow である。

この意味で、使用価値の実現を期間フローからみる構造は **P/L-like** である。

### B/S 側

B/S は、主体別の資本 stock / position を抽象的な通貨単位で表現する。

```text
B/S_i(t) ≡ K_i,t
```

この意味で、交換価値を比較可能な時点 stock として表現する構造は **B/S-like** である。

### 主体別帳簿

帳簿そのものは actor-specific であり、主体ごとに recognition / valuation / bookkeeping が異なりうる。

財務報告や統計は、その個別帳簿から外部向けに構成される別 representation であり、帳簿そのものが共通化されることを意味しない。

### P/L と B/S の接続

P/L と B/S は、同じ抽象的通貨単位量によって接続する。

```text
physical flows
    ↓ monetary / exchange-value measurement
P/L monetary amounts
    ↓ period aggregation / closing / attribution / distribution
B/S monetary positions K_i
```

期間損益は B/S 上の資本増減へ寄与するが、増資、配当、資本取引、評価差等があるため、P/L の期間損益と B/S の `ΔK_i` を普遍的に同一視しない。

---

## 9. surplus

surplus は K の physical primitive ではない。

余剰は、physical / use-value flow の input / output 等を **exchange-value の共通尺度へ写像して比較したときに成立する差分**である。

```text
physical / use-value flow
      ↓ exchange-value measurement
input / output monetary amounts
      ↓ comparison / accounting
surplus / deficit
      ↓ attribution / retention / distribution
B/S positions K_i(t+1)
```

したがって surplus は単なる物理量の増加ではない。同じ physical K でも、主体・知識・交換体系・valuation rule が異なれば exchange-value と surplus は異なりうる。

機械が、その利用法を知らない主体には単なる物体としてしか認識されないように、resource の物理的存在だけでは use-value / exchange-value / surplus は一意に決まらない。

---

## 10. 時間型と因果経路

VFT の主要経路は概念的に、

```text
K_t, (K_i,t)_i, (P_i,t)_i
          ↓ conditions
        (A_i,τ)_i
          ↓
physical activity / ΔK
          ↓ changed use-value / realized outcome
       P_i update
          ↓ exchange / monetary measurement
       P/L_i(τ)
          ↓ closing / attribution / distribution
       (K_i,t1)_i
```

と置く。

---

## 11. E[ΔK]

`E_i[ΔK(S,τ)]` は、主体 `i` が将来の realized resource change について形成する forecast を表す。

`E_i[ΔK]` は desire / preference / plan ではない。望ましさや選好は P_i に属する。

candidate action ごとの forecast は必要に応じて、

```text
E_i[ΔK(S,τ) | a, I_i]
```

と書ける。ここで `| a` は observational conditioning を意味せず、candidate action `a` を採った場合についての **action-contingent forecast** の略記である。

---

## 12. 3つの管理合理性公理

VFT の decision model は次の3則を constitutive rationality assumptions として置く。

1. **resource-realization**：望ましい resource / capital outcome の実現へ向けて A を動かす
2. **activity-flow**：必要な activity / process の流れを維持・拡張できるよう K / P / A を調整する
3. **P-downside**：P 側の大幅な毀損により主体・組織・系の A が成立しなくなることを防ぐ

3則は経験的普遍法則ではない。経験的に検証可能な仮説は、projection 側で objective / priority / weight / constraint / threshold / horizon 等を具体化して形成する。

---

## 13. 経済学への射影

### plan / choice と forecast

必要な economic projection では、planned / chosen resource change を `x_i` と書ける。

```text
x_i          = planned / chosen resource change
E_i[ΔK(...)] = expected realized resource change
```

budget feasibility は plan / choice 側へ置き、forecast と区別する。

### compatibility / equilibrium / accounting

- compatibility / feasibility：主体間 plan が相互に実行可能であること
- market equilibrium：compatibility に射影先理論の choice / optimality / clearing 等を加えたもの
- accounting consistency：指定 accounting rule による記帳・連結が整合すること
- steady state：対象状態について別途定める動学条件

これらは別概念である。

### Marxian categories

VFT は、Marxian economics が区別した use-value / labor / exchange-value / surplus / accumulation を一般化された構造上で表現できる。

ただし Marx 固有の value theory は、socially necessary labor time 等の追加条件を置く **projection-specific specialization** として扱う。

- use-value：K が特定 A / transformation を可能にし、期間内で実現される利用・効用側の価値
- labor measure：physical / productive flow としての labor activity / labor time
- Marxian labor-value：SNLT 等を追加した specialized projection
- exchange-value / price：異質な resource を比較可能にする market / monetary valuation
- surplus：exchange-value へ写像された input / output 等の差分として成立する accounting increment
- Marxian surplus value：Marx 固有の追加条件を満たす specialized interpretation
- accumulation：surplus の帰属・留保・分配による B/S 上の K_i の変化

---

## 14. ミクロ／マクロ接続

ミクロとマクロは、同じ physical K と、そこから形成される主体別 monetary representations を異なる scope で観測・集約することで接続する。

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

主体ごとの帳簿自体が共通化されることは仮定しない。macro measure は reporting / statistical transformation を介した別 representation である。

---

## 15. Core で固定しないもの

- K の標準 resource coordinates
- use-value の具体的効用関数・代替可能性
- exchange-value の monetary measurement / valuation function
- ownership / attribution / recognition rule
- 具体的 accounting standard
- P/L と B/S の closing rule
- surplus の普遍的算出式
- P の普遍的更新式
- A の deterministic choice function
- E[ΔK] の確率測度・期待形成式
- 3則の具体的 objective / weight / priority / threshold
- market equilibrium の普遍的条件
- micro-to-macro reporting / aggregation rule

---

## 16. 関連ノート

- [計測](02_measurement.md)
- [既存概念・応用への射影](../notes/projections.md)
- [拡張・再検討ノート](../notes/future_topics.md)

---

© T. Nuno  
Licensed under CC BY 4.0