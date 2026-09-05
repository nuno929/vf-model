# 価値場理論（Value-Field Theory）

**Theory refresh — Draft**  
Author: **T. Nuno**  
License: **CC BY 4.0**

---

## 1. 概要

価値場理論（Value-Field Theory; VFT）は、個人・組織・社会で生じる変化を、**共通の資源・資本 K、主体ごとの保有・帰属 K_i、各主体が保持する主観的な評価・期待状態 P_i、および actor-side process / event A_i** の関係として記述する構造的フレームワークである。

VFT Core は普遍的な deterministic choice function、状態遷移則、均衡則、会計則を固定しない。その上に、管理・意思決定を記述するための **3つの管理合理性公理**を置く。

### K / K_i

- **K**：資源・資本の状態
- **K_i**：そのうち主体 `i` に所有・保有・帰属すると扱う資源・資本

`K_i` は actor が「利用可能だと認識している K」ではない。その認識は P に属する。また、K / K_i の完全な真値を主体本人や観測者が常に把握できるとは仮定しない。

K を「外部に実在するものすべて」へ拡張しない。契約、制度、規範、権利関係等を、それだけを理由に K へ含めず、K は resource / capital に限定する。

### P

各 `P_i,t` は、主体 `i` が保持する将来見通し、評価、選好、信用、信念、規範認識等からなる **subjective evaluation / expectation state** である。

P は多数主体に共有されても主観状態であることをやめない。契約や制度も、経済行動を条件づける共有された規範認識・履行期待・執行期待等として P 側で扱いうる。共有 P は客観的な社会価値の真値ではなく、複数主体の P の共通性・整合性として記述・推定する。

P の真値は直接観測できるとは仮定せず、必要な projection で proxy を用いる。

### ΔK と期待値

`ΔK` は、K の利用・移転・変換・消費・生成等の結果として**実現した資源・資本変化**を表す。

主体は行為前に、その結果として生じる ΔK について期待を持ちうる。

```text
E_i[ΔK(S, τ)]
```

これは expected realized resource / capital change であり、desire / preference / plan とは区別する。

---

## 2. コア変数

```text
K_t
(K_i,t)_{i in I}
P_t = (P_i,t)_{i in I}
A_τ = (A_i,τ)_{i in I}
```

- **K**：共通の resource / capital state
- **K_i**：主体 `i` に所有・保有・帰属する resource / capital
- **P_i**：主体 `i` の subjective evaluation / expectation state
- **A_i**：主体 `i` 側で生じる process / event
- **ΔK**：A 等の結果として実現した resource / capital change
- **ΔP_i**：主体 `i` の P に実現した変化
- **E_i[ΔK]**：実現 ΔK について主体 `i` が形成する forecast

### ΔK record と会計

一つの A が複数の資源変化を生む場合、それぞれを ΔK record として保持する。

```text
A
├─ material       -10
├─ labor input     -5
├─ equipment wear  -2
└─ product         +20
```

区間活動量を表すための独立変数 `H` は Core に置かない。gross activity が必要なら、区間内の A と ΔK records の系列を利用する。

異質な ΔK はそのまま加算できない場合がある。指定した valuation / bookkeeping rule と accounting boundary で共通尺度へ写像し、差し引いた最終差分を surplus / deficit として扱える。

```text
realized ΔK records
        ↓ valuation / bookkeeping
accounting entries
        ↓ aggregation
surplus / deficit
```

surplus は K の primitive でも物理世界に独立して存在する物体でもなく、**実現した資源・資本変化の会計的派生量**である。

---

## 3. K / P / A の時間型

主体側の主要な時間型は、普遍的な状態遷移関数を固定せず、

```text
(K_t0, P_t0)
      ↓ conditions
A_(t0,t1]
      ↓ realized processes / resource use
(K_t1, P_t1)
```

と置く。

K には減価償却、自然損耗、災害等、A を介さない変化もありうる。

---

## 4. 3つの管理合理性公理

VFT の管理・意思決定記述では、合理性を次の3則へ集約する。

1. **resource-realization rule**：望ましい resource / capital outcome の実現へ向けて A を動かす。
2. **activity-flow rule**：必要な activity / process の流れを維持・拡張できるよう K / P / A を調整する。
3. **P-downside rule**：P 側の大幅な毀損により主体・組織・系の A が成立しなくなることを防ぐ。

3則は actor type ではなく、**意思決定合理性の公理系**である。同一 actor が3則を同時に考慮しうる。

3則の比重・優先順位は actor、文脈、制度、役割、組織構造、時間 horizon によって変わる。

自給自足では単一 actor が3則をすべて担える。国家レベルの資本主義社会を粗視化すると、典型的には

```text
individuals -> resource-realization heavy
firms       -> activity-flow heavy
state       -> P-downside heavy
```

と分化して見えるが、固定的な actor-type assignment ではない。

---

## 5. 経済学への射影

### plan / choice と forecast

必要な economic projection では、A に含まれる planned / chosen net resource change を `x_i` と書ける。

```text
x_i          = planned / chosen resource change
E_i[ΔK(...)] = expected realized resource change
```

予算制約・feasibility は plan / choice 側へ置き、forecast と区別する。

### compatibility / market equilibrium / 会計整合

- **inter-agent compatibility / feasibility**：各主体の plan が相互に実行可能・両立可能であること
- **market equilibrium**：compatibility に加え、射影先理論の choice / optimality / best response / clearing 条件が成立すること
- **会計整合**：同じ実現事象を同一 accounting boundary / rule で記帳した結果が整合すること
- **定常状態**：対象 K の増減等について別途定める状態条件

これらは別概念として扱う。

### 使用価値・労働価値・交換価値・余剰

VFT は、マルクス経済学が区別した経済現象の骨格を、特定の政治的・規範的結論を前提にせず射影できる。

- **使用価値**：K が特定目的の A / resource transformation を可能にする機能・有用性
- **労働価値**：生産・変換過程へ投入された labor activity / labor time を価値記述の尺度として用いる射影
- **交換価値・価格**：市場交換・会計上の valuation / representation
- **余剰**：実現した複数の ΔK を指定した valuation / accounting rule で共通尺度化し、差し引いた最終 accounting residual

使用価値、労働投入、価格、利益、余剰を一つの “value” に潰さず、同じ K / P / A / ΔK 構造上で比較する。

### ミクロ／マクロ接続

ミクロとマクロは別々の K ではない。

```text
micro:
(K_i, P_i) -> A_i -> ΔK records

              ↓ same common K

macro:
ownership distribution / production / accumulation / shared P
```

個別主体の A_i が同じ K の構成・所有分布を変え、その結果を異なる accounting boundary / aggregation scope から観測することでミクロとマクロを接続する。

surplus の帰属・分配が次期 K_i を変えるなら、個別主体の蓄積と社会全体の資本構成を同じ系列で追跡できる。

### utility / profit / supply-demand

utility / profit 等は3則の特殊化ではなく、具体的な意思決定を数量化・評価するときの関数・指標・proxy として扱う。

price / supply / demand / market equilibrium は複数主体の planned change を相互調整する economic mechanism であり、第4の合理性公理ではない。

---

## 6. 計測

VFT は K / K_i / P / ΔK の完全観測を前提としない。

- K / K_i：会計記録、資産台帳、物量観測等から部分的に把握
- P_i：調査、発話、選択、信用・期待 proxy 等から推定
- shared P：複数主体の P proxy の共通性・分布として推定
- A_i：外部 event は直接観測できる場合があり、内部 decision / interpretation は proxy を要する
- ΔK：記帳または利用後の最終結果からトレース
- surplus：指定した会計・評価規則により ΔK records を集約して算出

---

## 7. スケールと理論境界

個人・組織・社会・文明を、固定された独立実体ではなく、観測スケールと accounting / ownership boundary の違いとして扱う。

価値場理論は、以下を普遍的に固定しない。

- K / P / A の単一スカラー化
- K_i の普遍的な所有・帰属判定関数
- K / P の完全観測可能性
- A の普遍的 deterministic choice function
- E[ΔK] の普遍的形成式・確率測度
- ΔK records の普遍的会計・評価・集約則
- surplus / profit / price / labor-value の普遍的換算式
- 3則を数量化する具体的 objective / weight / priority rule
- inter-agent compatibility / market equilibrium の普遍的条件
- ミクロ／マクロの普遍的 aggregation rule
- 特定の観測方法・proxy・統計手法

---

## 8. ドキュメント

### Core

- [モデルノート](docs/01_model_notes.md)
- [計測](docs/02_measurement.md)

### Notes / 今後の展望・応用

- [背景・整理経緯](notes/background.md)
- [既存概念・応用への射影](notes/projections.md)
- [拡張・再検討ノート](notes/future_topics.md)

---

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)  
© T. Nuno