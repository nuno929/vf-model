# 価値場理論（Value-Field Theory）

**Theory refresh — Draft**  
Author: **T. Nuno**  
License: **CC BY 4.0**

---

## 1. 概要

価値場理論（Value-Field Theory; VFT）は、個人・組織・社会で生じる変化を、**実物・物理側の資源状態 K、主体別の簿価資本状態 K_i、主体ごとの主観的評価・期待状態 P_i、actor-side process / event A_i** の関係として記述する構造的フレームワークである。

VFT は、実物世界と通貨・会計世界を同一視しない。

```text
physical / resource world
K_t
  ↓ A_i
physical flows / transformations
  ↓ monetary measurement / bookkeeping
P/L representation
  ↓ period aggregation / closing / attribution
B/S representation: (K_i,t)_i
```

- **K**：生産・消費・労働・利用・変換等の対象となる実物・物理側の resource state
- **K_i**：主体 `i` の所有・保有・帰属を、B/S 上で通貨単位により定量表現した book-value capital position
- **P_i**：主体 `i` の subjective evaluation / expectation state
- **A_i**：主体 `i` 側で生じる process / event
- **ΔK**：K に実現した resource change
- **ΔP_i**：主体 `i` の主観状態 P_i に実現した変化
- **E_i[ΔK]**：実現 ΔK について主体 `i` が形成する forecast

`K_i` は K の subset / partition ではない。common K に ownership / holding / attribution と monetary valuation / bookkeeping を適用した **actor-indexed monetary representation** であり、共同所有・重複帰属・複雑な attribution を排除しない。

---

## 2. 実物側 K と会計側 K_i

### K：実物・物理側

K は、経済活動の対象となる資源状態を表す。設備、原材料、製品、土地、時間、身体、技能、知識、労働力、エネルギー等を projection に応じて含みうる。

K を「外部に実在するものすべて」へ拡張しない。契約、制度、規範、権利関係、金融 claim の法的構造等は、それだけを理由に K へ含めない。

### K_i：B/S 側の簿価資本

`K_i` は、主体 `i` の資本 position を B/S 上の通貨単位で表現したものとする。

```text
common K / economic events
        ↓ ownership / attribution
        ↓ valuation / bookkeeping
      K_i  (B/S)
```

したがって `K_i` は K の物理的 slice ではなく、K と経済事象を所有・帰属・評価・記帳した結果である。

金融資産もこの層で扱う。例えば預金、債券、売掛債権等は、それを成立させる契約・法的権利そのものを K とみなすのではなく、**会計 projection が financial asset position として認識・評価した B/S 上の K_i** として表現できる。

---

## 3. P：主観的評価・期待 state

各 `P_i,t` は、将来見通し、評価、選好、信用、信念、規範認識等からなる subjective state である。

P は多数主体に共有されても主観状態である。shared P は複数主体の P の共通性・整合性・分布として記述・推定し、客観的な社会価値の真値とはみなさない。

契約や制度についても、

- 法的・制度的 event / record
- その履行・執行・継続を主体がどう期待するかという P
- 実際に生じた resource change / accounting effect

を分けて扱う。

---

## 4. A / ΔK と P/L・B/S 接続

A は生産、消費、交換、投資、労働、移転、契約、政策等の actor-side process / event を表す。

`ΔK` は A 等により K に実現した resource change である。**ΔK は必ずしも `K(t1)-K(t0)` という単一の interval endpoint difference を意味しない。** 異質な資源については各 resource coordinate の実現変化として扱い、必要に応じて endpoint の net change を別途集約する。

物理世界で生じた期間中の activity / flow は、通貨単位へ計量されることで P/L に接続する。

```text
physical K
   ↓ A
physical flows / resource changes
   ↓ monetary measurement μ
P/L entries
   ↓ period aggregation
profit / loss / surplus measure
   ↓ closing / attribution / distribution
B/S positions K_i
```

ここで、

- **P/L 側**：期間中に物理・実物世界で起きた activity / flow を通貨単位で表現する
- **B/S 側**：主体別の資本 stock / position を抽象的な通貨単位で表現する
- **monetary unit**：P/L と B/S を接続する共通の計量単位

とする。

surplus は物理世界の primitive ではない。指定した accounting boundary で P/L 上の通貨的増減を集約・相殺・計量した residual / increment として扱う。surplus の帰属・留保・分配は次期 `K_i` を変化させる。

---

## 5. 3つの管理合理性公理

VFT の意思決定合理性は次の3則へ集約する。

1. **resource-realization rule**：望ましい resource / capital outcome の実現へ向けて A を動かす。
2. **activity-flow rule**：必要な activity / process の流れを維持・拡張できるよう K / P / A を調整する。
3. **P-downside rule**：P 側の大幅な毀損により主体・組織・系の A が成立しなくなることを防ぐ。

3則は経験的普遍法則ではなく、**VFT の decision model を構成する constitutive rationality assumptions** である。経験的に検証可能な仮説は、projection 側で objective / weight / constraint / threshold / horizon 等を具体化して形成する。

3則は actor type ではない。同一 actor が3則を同時に考慮し、文脈・制度・役割・時間 horizon に応じて比重・分担が変わる。

---

## 6. 経済学への射影

### plan / choice と forecast

必要な economic projection では planned / chosen resource change を `x_i` と書ける。

```text
x_i          = planned / chosen resource change
E_i[ΔK(...)] = expected realized resource change
```

`E_i[ΔK(S,τ) | a, I_i]` の `| a` は observational conditioning を意味せず、candidate action `a` を採った場合について主体が形成する **action-contingent forecast** の略記である。

### Marxian categories

VFT は、Marxian economics が区別した use-value / labor / exchange-value / surplus / accumulation を一般化された構造上で表現できる。一方、Marx 固有の value theory は projection-specific な追加条件を必要とする。

- **use-value**：K が特定の A / transformation を可能にする機能・有用性
- **labor measure**：labor activity / labor time による production flow の記述
- **Marxian labor-value projection**：socially necessary labor time 等の追加条件を導入した specialization
- **exchange-value / price**：market / monetary valuation
- **surplus**：指定した P/L accounting boundary と monetary measurement に基づく期間増分
- **accumulation / distribution**：surplus の帰属・留保・分配を通じた B/S 上の `K_i` の変化

したがって generic labor time をそのまま Marxian value と同一視せず、generic surplus をそのまま Marxian surplus value とも同一視しない。

### ミクロ／マクロ接続

```text
micro
K, K_i, P_i
    ↓
   A_i
    ↓
physical flows
    ↓ monetary measurement
P/L_i
    ↓ closing / attribution
K_i(t+1)

          ↓ aggregation / consolidation

macro
physical production / consumption
capital-stock distribution
aggregate P/L increment / surplus
capital accumulation
shared P
```

ミクロとマクロは、同じ physical K と、そこから会計的に形成される主体別 P/L・B/S 表現を異なる scope で観測・集約することで接続する。

---

## 7. compatibility / equilibrium / accounting

- **inter-agent compatibility / feasibility**：各主体の plan が相互に実行可能・両立可能であること
- **market equilibrium**：compatibility に加え、射影先理論の choice / optimality / best response / clearing 条件が成立すること
- **accounting consistency**：同じ economic event を指定した recognition / valuation / consolidation rule で記帳した結果が整合すること
- **steady state**：対象状態について別途定める動学条件

これらは別概念である。

---

## 8. 理論境界

VFT Core は以下を普遍的に固定しない。

- K の標準 resource coordinates
- monetary measurement / valuation function
- B/S 上の ownership / attribution / recognition rule
- P/L / B/S の具体的 accounting standard
- surplus の普遍的算出式
- P の普遍的更新式
- A の deterministic choice function
- E[ΔK] の確率測度・期待形成式
- 3則の objective / weight / priority / threshold
- market equilibrium の普遍的条件
- micro-to-macro aggregation / consolidation rule

---

## 9. ドキュメント

- [モデルノート](docs/01_model_notes.md)
- [計測](docs/02_measurement.md)
- [背景・整理経緯](notes/background.md)
- [既存概念・応用への射影](notes/projections.md)
- [拡張・再検討ノート](notes/future_topics.md)

---

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)  
© T. Nuno