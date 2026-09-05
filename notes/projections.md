# 価値場理論 — 既存概念・応用への射影ノート

> この文書は Core 定義ではなく、既存概念・応用領域への projection candidate を保存する。

## 1. 基本構造

VFT の経済射影では、

- `K`：physical / real-resource state
- `K_i`：actor-specific exchange-value / capital representation
- `P_i`：structured subjective state
- `A_i`：actor-side action / process record
- `ΔK_τ := δ_K(K_t0,K_t1)`：projection-defined endpoint resource-state difference
- `Ŷ_i(a;I_i)`：generic forecast of a projection-selected outcome bundle

を区別する。

field は K / K_i / P_i と projection-specified relations / constraints から導かれる action-generating configuration として扱う。

```text
F_t := configuration(...)
Γ_i^feas(F_t) := feasible action set
Γ_i^ind(F_t)  := inducible / behaviorally available action set
Γ_i^ind(F_t) ⊆ Γ_i^feas(F_t)
```

`Γ_i^feas` と `Γ_i^ind` は deterministic choice rule ではない。actual action は `Γ_i^ind` から生じる realized record として扱う。

---

## 2. 使用価値 / 交換価値

同一 resource について、physical capability / realized use experience / exchange-value representation を区別する。

### use-value

VFT-specific use-value quantity は、resource stock 自体ではなく、**主体が interval 内に resource を実際に利用・消費し、その経験に帰属される形で ex post に realized した主観的効用量**とする。

physical stock / capability は K として時点観測できるが、それは use-value quantity そのものではない。

同じ主体・同じ resource・同じ利用量でも、充足状態、順序、文脈、他の経験等によって realized outcome は変わりうるため、一般的な再現性や interval 間の加法性を仮定しない。

```text
actual use over τ=(t0,t1]
        ↓
subjective experience
        ↓
U^use_i(τ)
        ↓
P_i update
```

瞬間 rate を必要とする projection では interval quantity の極限・微分的表現として導入できるが、point-in-time stock valuation とは扱わない。

用語衝突を避ける必要がある箇所では `U^use_i(τ)` を realized-use outcome と呼ぶ。

### exchange-value

resource を他の resource / money との比較関係から共通尺度へ写像した representation とする。

exchange-value は point-in-time position にも interval transaction valuation にも現れうるため、stock 専用とはしない。

physical capability / realized use experience / exchange-value representation の多面的記述は会計的表現を想起させるが、借方・貸方や複式簿記との対応を意味しない。

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

formal accounting では、physical/resource events、contract / financial events、valuation-only events 等を recognition / valuation の対象にできる。

---

## 4. 契約・制度・金融資産

契約・制度・法的権利関係それ自体は physical K としない。

預金、債券、売掛債権等は recognized exchange-value / financial position として K_i / accounting projection 上に表現できる。

主体が契約・制度の履行・執行・継続をどう期待するかは P に属する。

客観的な institutional / legal state が必要な projection では `C_t` 等を projection-local に追加してよい。

---

## 5. P / generic outcome forecast

P_i は belief / expectation、preference / valuation、trust / reputation、norm recognition 等を含む structured subjective state とする。

Core の forecast は physical ΔK のみに限定しない。

```text
Y_i^proj(τ)
:= projection-selected outcome bundle
   { ΔK_τ, K_i,t1, U^use_i(τ), P_i,t1, activity outcomes, ... }

Ŷ_i(a;I_i)
:= forecast of Y_i^proj under candidate action a
```

確率・因果構造を採用する projection では、bundle の各 component を期待値・分布・causal estimand 等として具体化してよい。

`ΔK̂_i(a;I_i)` は必要な projection における `Ŷ_i` の physical-resource component として使える。

---

## 6. A / shared event / ΔK / exogenous change

A は actor-side action / process record とする。

交換・移転・契約等、一つの realized event に複数主体が参加する場合、対応する actor records は shared `event_id` と participant / role relation を持つ。

```text
event_id(A_i) = event_id(A_j) = e
participants(e) = {i,j,...}
```

必要な場合、shared event history を、

```text
E_τ^shared := deduplicate( ⋃_i A_i,τ , by = event_id )
```

という derived view として構成する。

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

## 8. field / business projection

field は action-generating configuration とする。

business entity は **一定の目的・機能に向けた A を継続的に誘発・再生産する局所 field structure** として記述できる。

```text
起業           = business-oriented field formation の一類型
新規事業開発   = 既存 field から business-oriented field を形成・分岐
既存事業運営   = 成立済み business field の維持・再生産・改善
```

この定義では営利企業、NPO、協同組合、公共事業、国家・自治体の事業等を同じ型で扱える。

profit / surplus は business existence の定義条件ではなく、exchange-value 側の重要 metric の一つである。

---

## 9. 3つの管理合理性公理

1. resource-realization
2. activity-flow
3. P-downside

3則は constitutive rationality assumptions とする。

resource-realization は resource / capital outcome だけでなく、resource の利用による desired realized-use outcome を含む。

activity-flow は既存 activity の継続だけでなく、必要に応じた field formation / renewal を含みうる。

P-downside は P 全体の universal ordering を意味しない。projection-specific な P component と threshold / loss / viability criterion を指定する。

各 dimension は `Ŷ_i(a;I_i)` のどの outcome component をどの比較規則で評価するかを projection 側で定める。

VFT decision projection では、採用した dimension ごとに admissibility / exclusion condition または比較規則を事前に明示する。

---

## 10. plan / forecast / equilibrium

```text
x_i                = planned / chosen resource change
Ŷ_i(a;I_i)         = generic outcome forecast
ΔK̂_i(a;I_i)       = optional physical-resource component of Ŷ_i
```

compatibility / market equilibrium / accounting consistency / steady state は別概念とする。

---

## 11. Marxian categories

VFT は use-value / labor / exchange-value / surplus / accumulation を一般化構造上で保持する。

- VFT-specific use-value quantity / realized-use outcome：主体が interval 内の実利用体験を通じて ex post に realized した主観的効用量
- labor measure：labor activity / labor time
- Marxian labor-value：socially necessary labor time 等の追加条件を持つ specialization
- exchange-value / price：resource 間の comparison / market / monetary valuation
- exchange-value residual / surplus：指定 boundary と exchange-value scale 上の差分
- Marxian surplus value：Marx 固有条件を持つ specialization
- accumulation：surplus 等の帰属・留保・分配による K_i の変化

VFT-specific use-value quantity と Marxian use-value は自動的に同一視しない。

---

## 12. ミクロ／マクロ

```text
micro
F_t
 ↓
Γ_i^feas(F_t)
 ↓
Γ_i^ind(F_t)
 ↓
A_i actor-side records
 ↓ shared event identity when multi-actor
E_τ^shared (derived)
 ↓
ΔK / realized-use outcomes / K_i changes / P_i updates

                     ↓ external reporting / aggregation where needed

macro
physical production / consumption
exchange-value distribution / surplus
capital accumulation
shared P
field formation / dissolution
```

主体ごとの帳簿自体が共通化されることは仮定しない。

---

## 13. 射影時に明示するもの

1. K の resource coordinates
2. actor set
3. projection-specified relations / constraints
4. `Γ_i^feas` の feasibility rule
5. `Γ_i^ind` の behavioral availability rule
6. A の record unit / ordering
7. multi-actor event の event identity / participants / roles / deduplication
8. `δ_K` の endpoint difference rule
9. exogenous K change を扱う場合の `Ω` 等の定義
10. use-value の actor / realized interval / subjective proxy / attribution / reference timing
11. exchange-value / valuation rule
12. K_i の representation rule
13. P / shared P の proxy
14. outcome bundle `Y_i^proj` の coordinates
15. generic forecast `Ŷ_i` の推定・specialization
16. institutional state が必要な場合の追加定義
17. accounting projection の recognition / identity rule
18. exchange-value residual / surplus の対象 changes / comparison / attribution / distribution
19. field / business continuity / inducibility の proxy
20. P-downside の viability criterion
21. Marxian specialization の追加条件
22. micro / macro reporting / aggregation rule

---

© T. Nuno  
Licensed under CC BY 4.0