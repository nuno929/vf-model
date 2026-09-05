# 価値場理論 — 既存概念・応用への射影ノート

> この文書は Core 定義ではなく、既存概念・応用領域への projection candidate を保存する。

## 1. 基本構造

VFT の経済射影では、

- `K`：real-resource / capability state
- `K_i`：actor-specific exchange-value / capital representation
- `P_i`：structured subjective state
- `A_i`：actor-side action / process record
- `ΔK_τ := δ_K(K_t0,K_t1)`：projection-defined endpoint resource-state difference
- `Ŷ_i,t(a;I_i,t)`：generic forecast of a projection-selected outcome bundle

を区別する。

field は K / K_i / P_i と projection-specified relations / constraints から導かれる action-generating configuration として扱う。

```text
F_t := configuration(...)
Γ_i^feas(F_t)  := feasible action set
Γ_i^avail(F_t) := cognitively / behaviorally available action set
Γ_i^adm(F_t)   := admissible action set

Γ_i^adm(F_t) ⊆ Γ_i^avail(F_t) ⊆ Γ_i^feas(F_t)
```

`Γ_i^feas` は feasibility、`Γ_i^avail` は consideration / behavioral availability、`Γ_i^adm` は forecast と rationality rules を通過した candidate set とする。actual action の selection rule は projection-specific とする。

---

## 2. 使用価値 / 交換価値

同一 resource について、resource capability / realized use experience / exchange-value representation を区別する。

### realized-use outcome / use-value

VFT-specific use-value quantity は、resource stock 自体ではなく、**主体が interval 内に resource を実際に利用・消費し、その経験に帰属される形で ex post に realized した主観的 outcome** とする。

```text
actual use over τ=(t0,t1]
        ↓
subjective experience
        ↓
U^use_i(τ)
        ↓
P_i update
```

一般的な再現性や interval 間の加法性を仮定しない。

instantaneous rate が必要な projection では、`U^use_i(τ)` から直接微分せず、別途 cumulative realized-use process `C_i(t)` を定義し、必要な正則性が成立する場合に限って rate を導入する。

`use-value quantity` は Marxian category との接続名として使い、数理・計測上は realized-use outcome を優先してよい。

### exchange-value

resource を他の resource / money との比較関係から共通尺度へ写像した representation とする。

exchange-value は point-in-time position にも interval transaction valuation にも現れうる。

resource capability / realized use experience / exchange-value representation の多面的記述は会計的表現を想起させるが、借方・貸方や複式簿記との対応を意味しない。

---

## 3. K_i / accounting projection

`K_i` は K の subset / partition ではなく、ownership / attribution / recognition / valuation 等を経た actor-specific exchange-value / capital representation である。

企業会計 projection では K_i を ledger / B/S 上の monetary positions として形式化できるが、`K_i ≡ B/S` とはしない。

```text
P_i valuation
= subjective desirability / appraisal / belief-side evaluation

K_i valuation
= exchange-value representation under specified
  recognition / comparison / unit-of-account / valuation rules
```

formal accounting では physical/resource events、contract / financial events、valuation-only events 等を recognition / valuation の対象にできる。

---

## 4. 契約・制度・金融資産

契約・制度・法的権利関係それ自体は K としない。

預金、債券、売掛債権等は recognized exchange-value / financial position として K_i / accounting projection 上に表現できる。

主体が契約・制度の履行・執行・継続をどう期待するかは P に属する。

客観的な institutional / legal state が必要な projection では `C_t` 等を projection-local に追加してよい。

---

## 5. P / generic outcome forecast / evaluation

P_i は belief / expectation、preference / valuation、trust / reputation、norm recognition 等を含む structured subjective state とする。

時点 `t` の decision では、

```text
P_i,t belief / expectation
        ↓
Ŷ_i,t(a;I_i,t)

P_i,t preference / valuation
        ↓ evaluates
Ŷ_i,t(a;I_i,t)
        ↓
Γ_i^adm(F_t)
```

という役割分担を置ける。

Core の forecast は physical ΔK のみに限定しない。

```text
Y_i^proj(τ)
:= projection-selected outcome bundle
   { ΔK_τ, K_i,t1, U^use_i(τ), P_i,t1, activity outcomes, ... }

Ŷ_i,t(a;I_i,t)
:= forecast of Y_i^proj under candidate action a
```

forecast bundle に `P̂_i,t1(a)` を含める場合、current P_i,t から future P_i,t1 を予測していることを明示する。

確率・因果構造を採用する projection では、bundle の各 component を期待値・分布・causal estimand 等として具体化してよい。

---

## 6. A / shared realized event / ΔK / exogenous change

A は actor-side action / process record とする。

交換・移転・契約等、一つの realized event に複数主体が参加する場合、対応する actor records は shared `event_id` と participant / role relation を持つ。

```text
event_id(A_i,e) = event_id(A_j,e) = e
participants(e) = {i,j,...}
```

shared event は participant-side records を reconcile / compose して構成する。

```text
E_e^shared
:= reconcile({ A_i,e | i ∈ participants(e) })
```

`deduplicate by event_id` は event count 等、event identity だけを集計する特殊用途に限定する。

`ΔK` は projection-defined endpoint resource-state difference とする。

```text
ΔK_τ := δ_K(K_t0,K_t1)
```

additive vector projection では `δ_K(K_t0,K_t1)=K_t1-K_t0` と specialize できる。

A を通らない K change が必要な projection では、自然劣化、災害、偶発故障等を `Ω_τ` などの exogenous / environmental process として追加する。

---

## 7. exchange-value residual / surplus / accumulation

Core-level の中立的な差分を **exchange-value residual** として、

```text
specified economic changes
   ↓ exchange-value representation
comparable values
   ↓ comparison under specified boundary
exchange-value residual
```

と記述できる。

projection の意味論に応じて surplus / deficit、production surplus、profit、income、valuation gain 等へ解釈する。

surplus の attribution / retention / distribution は次期 K_i を変えうる。

---

## 8. business actor / business field / business projection

organization / company は actor `i` として表現できる。

```text
business actor / organization
= actor i
```

business field は、business activity を継続的に可能化・誘発・再生産する局所 action-generating configuration とする。

```text
business field F^biz
= local action-generating configuration for recurring business activity
```

business は `F^biz` を中心として継続する activity system とする。

同一 organization が複数 business fields を持つこと、一つの business field が複数 actors にまたがることを許す。

```text
起業           = business-oriented field formation を伴う activity
新規事業開発   = 既存 field から新しい business field を形成・分岐
既存事業運営   = 成立済み business field の維持・再生産・改善
```

profit / surplus は business existence の定義条件ではなく、exchange-value 側の重要 metric の一つである。

---

## 9. 3つの管理合理性公理

1. resource-realization
2. activity-flow
3. P-downside

3則は constitutive rationality assumptions とする。

各 dimension は `Ŷ_i,t(a;I_i,t)` のどの outcome component をどの比較規則で評価するかを projection 側で定め、`Γ_i^adm` の形成へ接続する。

VFT decision projection では、採用した dimension ごとに admissibility / exclusion condition または比較規則を ex ante に明示する。

---

## 10. plan / forecast / equilibrium

```text
x_i                  = planned / chosen resource change
Ŷ_i,t(a;I_i,t)       = generic outcome forecast
ΔK̂_i(a;I_i)         = optional resource-state component of Ŷ_i
```

compatibility / market equilibrium / accounting consistency / steady state は別概念とする。

---

## 11. Marxian categories

VFT は use-value / labor / exchange-value / surplus / accumulation を一般化構造上で保持する。

- VFT-specific use-value quantity / realized-use outcome：主体が interval 内の実利用体験を通じて ex post に realized した主観的 outcome
- labor measure：labor activity / labor time
- Marxian labor-value：socially necessary labor time 等の追加条件を持つ specialization
- exchange-value / price：resource 間の comparison / market / monetary valuation
- exchange-value residual / surplus：指定 boundary と exchange-value scale 上の差分
- Marxian surplus value：Marx 固有条件を持つ specialization
- accumulation：surplus 等の帰属・留保・分配による K_i の変化

VFT-specific realized-use outcome と Marxian use-value は自動的に同一視しない。

---

## 12. ミクロ／マクロ

```text
F_t
 ↓
Γ_i^feas(F_t)
 ↓
Γ_i^avail(F_t)
 ↓ forecast + rationality rules
Γ_i^adm(F_t)
 ↓
A_i actor-side records
 ↓ reconcile participant records when multi-actor
E_e^shared (derived)
 ↓
ΔK / realized-use outcomes / K_i changes / P_i updates

        ↓ external reporting / aggregation where needed

macro states / distributions / field formation-dissolution
```

主体ごとの帳簿自体が共通化されることは仮定しない。

---

## 13. 射影時に明示するもの

1. K の resource / capability coordinates
2. actor set
3. projection-specified relations / constraints
4. `Γ_i^feas` の feasibility rule
5. `Γ_i^avail` の consideration / availability rule
6. `Γ_i^adm` の admissibility / exclusion rule
7. selection / intention を扱う場合の追加 rule
8. A の record unit / ordering
9. multi-actor event の event identity / participants / roles / reconciliation rule
10. downstream aggregation rule
11. `δ_K` の endpoint difference rule
12. exogenous K change を扱う場合の `Ω` 等の定義
13. realized-use outcome の actor / interval / subjective proxy / attribution / reference timing
14. instantaneous rate を使う場合の `C_i(t)` と正則性条件
15. exchange-value / valuation rule
16. K_i の representation rule
17. P / shared P の proxy
18. current P belief / valuation role
19. outcome bundle `Y_i^proj` の coordinates
20. generic forecast `Ŷ_i` の推定・specialization
21. institutional state が必要な場合の追加定義
22. accounting projection の recognition / identity rule
23. exchange-value residual / surplus の対象 changes / comparison / attribution / distribution
24. business actor boundary / business field boundary
25. P-downside の viability criterion
26. Marxian specialization の追加条件
27. micro / macro reporting / aggregation rule

---

© T. Nuno  
Licensed under CC BY 4.0