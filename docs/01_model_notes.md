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

つまり、

```text
contract / legal relation
        ↓ recognition / enforceability / expectation
financial asset position
        ↓ valuation / bookkeeping
K_i on B/S
```

と分ける。

---

## 4. P：subjective evaluation / expectation state

各 `P_i,t` は、主体 `i` の将来見通し、評価、選好、信用、信念、期待、規範認識等を含む subjective state である。

```text
P_t = (P_i,t)_{i in I}
```

P はどれだけ共有されても主観状態である。shared P は複数主体の P の共通性・整合性・分布として扱い、客観的な社会価値の真値とはみなさない。

P の完全観測は前提とせず、projection ごとに proxy を用いる。

契約・制度は、それ自体を K の resource quantity へ押し込まず、法的・制度的 event / record、主体の履行・執行期待 P、実際に生じた resource / accounting effect を分けて扱う。

---

## 5. A：actor-side process / event

A は各主体側で生じる process / event を表す。

```text
A_τ = (A_i,τ)_{i in I}
```

生産、消費、交換、投資、労働、移転、契約締結、政策、情報伝達等を必要な粒度で A として記述する。

外部 action と内部 decision / observation / interpretation は、必要な projection で区別する。

---

## 6. ΔK：物理・実物側の realized resource change

`ΔK` は、A 等により K に実現した resource change を表す。

重要なのは、**ΔK は会計仕訳ではない**という点である。会計仕訳は、物理・実物側で起きた activity / change を monetary measurement と recognition rule によって帳簿へ写像した表現である。

また `ΔK` は必ずしも単一の

```text
K_t1 - K_t0
```

を意味しない。異質な resource coordinates では、それぞれの resource change を記述し、endpoint net difference が必要な場合だけ対象 projection で集約する。

例えば同じ区間に生産と消費があり、最終在庫が同じでも、期間中の physical flow は存在する。gross flow と endpoint net change を同一視しない。

---

## 7. P/L と B/S：物理世界と通貨世界の接続

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

### B/S 側

B/S は、主体別の資本 stock / position を抽象的な通貨単位で表現する。

```text
B/S_i(t) ≡ K_i,t
```

### P/L と B/S の接続

P/L と B/S は、同じ抽象的通貨単位量によって接続する。

```text
physical flows
    ↓ μ
P/L monetary amounts
    ↓ period aggregation / closing / attribution / distribution
B/S monetary positions K_i
```

期間損益は B/S 上の資本増減へ寄与するが、増資、配当、資本取引、評価差等があるため、P/L の期間損益と B/S の `ΔK_i` を普遍的に同一視しない。

---

## 8. surplus

surplus は K の primitive ではない。

指定した accounting boundary で、P/L 上に monetary measurement された期間中の増減を aggregation / consolidation / offset rule に従って合算し、最終的に残る increment / residual を surplus / deficit として扱う。

```text
physical activity / flow
      ↓ monetary measurement
P/L books
      ↓ aggregation / consolidation
surplus / deficit
      ↓ attribution / retention / distribution
B/S positions K_i(t+1)
```

したがって surplus は、物理世界の独立物体ではなく、期間 activity を抽象的通貨単位で計量・集約した accounting-derived quantity である。

---

## 9. 時間型と因果経路

VFT の主要経路は概念的に、

```text
K_t, (K_i,t)_i, (P_i,t)_i
          ↓ conditions
        (A_i,τ)_i
          ↓
physical activity / ΔK
          ↓ monetary measurement / bookkeeping
       P/L_i(τ)
          ↓ closing / attribution / distribution
       (K_i,t1)_i
```

と置く。

同時に、実現結果・他主体の action・制度変化等は P_i を更新し、次の A_i にフィードバックする。

```text
realized outcome
      ↓ perception / interpretation
P_i,t -> P_i,t1
      ↓
next A_i
```

---

## 10. E[ΔK]

`E_i[ΔK(S,τ)]` は、主体 `i` が将来の realized resource change について形成する forecast を表す。

`E_i[ΔK]` は desire / preference / plan ではない。望ましさや選好は P_i に属する。

candidate action ごとの forecast は必要に応じて、

```text
E_i[ΔK(S,τ) | a, I_i]
```

と書ける。ここで `| a` は observational conditioning を意味せず、candidate action `a` を採った場合についての **action-contingent forecast** の略記である。

---

## 11. 3つの管理合理性公理

VFT の decision model は次の3則を constitutive rationality assumptions として置く。

1. **resource-realization**：望ましい resource / capital outcome の実現へ向けて A を動かす
2. **activity-flow**：必要な activity / process の流れを維持・拡張できるよう K / P / A を調整する
3. **P-downside**：P 側の大幅な毀損により主体・組織・系の A が成立しなくなることを防ぐ

3則は経験的普遍法則ではない。経験的に検証可能な仮説は、projection 側で objective / priority / weight / constraint / threshold / horizon 等を具体化して形成する。

同一 actor が3則を同時に考慮し、文脈・制度・役割・組織構造・時間 horizon に応じて比重・分担が変わる。

---

## 12. 経済学への射影

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

- use-value：K が特定 A / transformation を可能にする機能
- labor measure：physical / productive flow としての labor activity / labor time
- Marxian labor-value：SNLT 等を追加した specialized projection
- exchange-value / price：market / monetary valuation
- surplus：指定 P/L accounting boundary における monetary increment
- Marxian surplus value：Marx 固有の追加条件を満たす specialized interpretation
- accumulation：surplus の帰属・留保・分配による B/S 上の K_i の変化

---

## 13. ミクロ／マクロ接続

ミクロとマクロは、同じ physical K と、そこから形成される P/L・B/S の monetary representations を異なる scope で観測・集約することで接続する。

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

`K_i` は K の partition ではないため、micro-to-macro 接続は単純な集合和ではなく、ownership / valuation / accounting / consolidation rule に依存する。

---

## 14. Core で固定しないもの

- K の標準 resource coordinates
- monetary measurement / valuation function μ
- ownership / attribution / recognition rule
-具体的 accounting standard
- P/L と B/S の closing rule
- surplus の普遍的算出式
- P の普遍的更新式
- A の deterministic choice function
- E[ΔK] の確率測度・期待形成式
- 3則の具体的 objective / weight / priority / threshold
- market equilibrium の普遍的条件
- micro-to-macro aggregation / consolidation rule

---

## 15. 関連ノート

- [計測](02_measurement.md)
- [既存概念・応用への射影](../notes/projections.md)
- [拡張・再検討ノート](../notes/future_topics.md)

---

© T. Nuno  
Licensed under CC BY 4.0