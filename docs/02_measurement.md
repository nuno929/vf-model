# 価値場理論 — 計測

## 1. 目的

本書は VFT Core を実証・観測・会計へ落とす際の境界を整理する。

計測上は、real-resource / capability state K、actor-specific K_i、structured subjective state P_i、field-derived action sets、actor-side A records、shared event identity / reconciliation、projection-defined endpoint difference ΔK、realized-use outcome、exchange-value representation を区別する。

---

## 2. K の観測

K は real-resource / capability state である。

候補 observable には原材料量、製品量、設備、稼働、エネルギー使用、土地等の physical resources に加え、時間、労働時間、技能・人的能力、利用可能 capability 等がある。

K の完全観測は前提とせず、resource / capability coordinates と観測単位は projection ごとに定める。

A を通らない K 変化を扱う必要がある場合、自然劣化、災害、偶発故障等を `Ω_τ` 等の exogenous / environmental process として projection-local に観測する。

---

## 3. K_i の計測

`K_i` は actor-specific exchange-value / capital stock representation である。

計測には projection に応じて、

1. ownership / holding / attribution
2. recognition rule
3. valuation rule
4. unit of account / comparison scale

等が必要になる。

`K_i` は K の subset / partition ではない。

### valuation の境界

```text
P_i valuation
= subjective desirability / appraisal / belief-side evaluation

K_i valuation
= exchange-value representation under specified
  recognition / comparison / unit-of-account / valuation rules
```

### accounting implementation

企業会計等では K_i を ledger / B/S 上の monetary positions として形式化できるが、`K_i ≡ B/S` とはしない。

正式な B/S projection では assets / liabilities / equity 等の account types と accounting identity を representation の定義条件として明示する。

帳簿は actor-specific であり、財務報告・連結・統計は別の external representation とする。

---

## 4. realized-use outcome / use-value の計測

`U^use_i(τ)` は resource stock 自体ではなく、**主体が interval `τ` 内に resource を実際に利用・消費し、その経験に帰属される形で ex post に realized した主観的 outcome** である。

resource stock / capability 自体は K として時点観測できるが、それは realized-use outcome ではない。瞬間的な快・満足等を観測できても、それ自体を当該 resource の realized-use outcome と同一視しない。

同じ主体・同じ resource・同じ利用量でも、充足状態、利用順序、文脈、他の経験等によって結果は変わりうる。したがって一般的な再現性や interval 間の加法性を仮定しない。

```text
actual use over τ=(t0,t1]
        ↓
subjective experience / fulfillment
        ↓
U^use_i(τ)
```

離散時間で時点 `t` を置く場合、時点 `t` で参照できる realized-use outcome は前区間までのものとする。将来の利用結果について主体が持つものは P_i,t 上の belief / expectation である。

計測では少なくとも、

- actor
- interval
- actual use / consumption
- subjective utility / experience proxy
- attribution to the resource / use episode
- reference timing
- 必要に応じて substitute / complement / use category

を指定する。

異なる interval 間・主体間で比較する場合、同一尺度上で再現可能な真値を測っているとは仮定せず、projection-specific な比較可能性を別途定義する。

### instantaneous rate を使う場合

一般の非加法的 `U^use_i(τ)` から instantaneous rate を直接導出しない。

rate が必要な projection では別途、cumulative realized-use process `C_i(t)` を定義する。その `C_i(t)` が当該 projection で必要な加法性・絶対連続性等の正則性を満たす場合にのみ、

```text
u_i(t) = dC_i(t) / dt
```

等を導入する。

`use-value quantity` は Marxian category との接続名として用い、数理・計測上は realized-use outcome を優先してよい。

---

## 5. exchange-value の計測

exchange-value は resource を他の resource / money との比較関係から共通尺度へ写像した representation である。

exchange-value は point-in-time position にも interval event valuation にも現れうる。

```text
point-in-time valuation -> capital / asset position
interval valuation      -> transaction / revenue / expense etc.
```

異質な resource stock を共通交換尺度で比較・集計する評価は exchange-value representation として扱う。

---

## 6. P / outcome forecast / evaluation の計測

`P_i` は structured subjective state であり、belief / expectation、preference / valuation、trust / reputation、norm recognition 等を含みうる。

候補 proxy には期待調査、選好・評価調査、発話、信用・信頼指標、制度・契約への履行期待、将来見通し等がある。

shared P は actor set 上の共通性・整合性・分布として推定する。

時点 `t` の decision では、少なくとも role 上、

```text
P_i,t belief / expectation
        ↓
Ŷ_i,t(a;I_i,t)

P_i,t preference / valuation
        ↓ evaluates
Ŷ_i,t(a;I_i,t)
```

を区別して観測・推定する。

Core の generic forecast は、

```text
Y_i^proj(τ)
:= projection-selected outcome bundle

Ŷ_i,t(a;I_i,t)
:= forecast of Y_i^proj under candidate action a
```

とする。

projection が必要とする座標として、例えば、

```text
ΔK_τ
K_i,t1
U^use_i(τ)
P_i,t1
activity / continuity outcomes
```

等を選べる。

`P̂_i,t1(a)` を forecast bundle に含める場合、現在の P_i,t から将来 P_i,t1 を予測していることを明示する。

計測時には、forecast 対象 coordinates、forecast horizon、information set、推定法、確率分布を用いる場合の calibration 等を明示する。

---

## 7. field / action-stage の計測

field は、K / K_i / P_i と projection-specified relations / constraints から導かれる action-generating configuration として扱う。

必要に応じて、

```text
F_t := configuration(...)
Γ_i^feas(F_t)  := feasible action set
Γ_i^avail(F_t) := cognitively / behaviorally available action set
Γ_i^adm(F_t)   := admissible action set

Γ_i^adm(F_t) ⊆ Γ_i^avail(F_t) ⊆ Γ_i^feas(F_t)
```

を用いる。

### Γ^feas

候補 observable：

- physical capacity
- resource availability
- legal / institutional permission
- budget / access constraints
- technical compatibility

### Γ^avail

候補 observable：

- consideration set
- recognized options
- perceived behavioral availability
- reachable alternatives
- option awareness

`Γ^avail` は rationality evaluation 前の behavioral availability とする。

### Γ^adm

候補 observable / operationalization：

- ex ante admissibility rules
- organizational / policy decision rules
- threshold / exclusion conditions
- dominance / comparison rule
- rationality-dimension filters

stated intention / final choice は `Γ^adm` そのものではなく、`Γ^adm` から selection が行われた後の projection-specific state / record として扱う。

`Γ^avail` / `Γ^adm` は realized action を見て事後的に定義せず、可能な限り action realization 前の情報から operationalize する。

---

## 8. A と shared realized event

A は actor-side action / process record である。

複数主体にまたがる交換・移転・契約等では、対応する actor records に shared `event_id` と participant / role relation を記録する。

```text
event_id(A_i,e) = event_id(A_j,e) = e
participants(e) = {i,j,...}
```

shared realized event は participant-side records を reconcile / compose して構成する。

```text
E_e^shared
:= reconcile({ A_i,e | i ∈ participants(e) })
```

buyer の受領・支払、seller の引渡・受取等、同一 event の participant-side components は保持する。

分析目的ごとに、

- actor-level analysis：各 `A_i` records
- shared-event analysis：`E_e^shared`
- event-count aggregation：event_id 単位の deduplication
- resource-flow aggregation：`E_e^shared` 内の directed components を使用

と分ける。

multi-actor event の計測では少なくとも、

1. event identity
2. participant set
3. participant role / direction
4. event timing
5. actor-specific action / position
6. reconciliation rule
7. downstream aggregation rule

を明示する。

---

## 9. ΔK の計測

`ΔK_τ` は projection-defined endpoint resource-state difference とする。

```text
ΔK_τ := δ_K(K_t0, K_t1)
```

K が additive vector space 等で表現される projection では、

```text
δ_K(K_t0, K_t1) = K_t1 - K_t0
```

を特殊形として使える。

したがって gross activity と ΔK は別 observable である。

multi-actor gross activity を集計する場合は actor-side A records を単純加算せず、shared event reconciliation と対象 coordinate に応じた aggregation rule を用いる。

`ΔK` は accounting entry ではない。

---

## 10. exchange-value residual / surplus の計測

Core-level では、指定された economic changes を exchange-value の比較可能尺度へ写像し、specified comparison boundary の下で得られる差分を **exchange-value residual** として扱える。

```text
specified economic changes
   ↓ exchange-value representation
comparable values
   ↓ comparison under specified boundary
exchange-value residual
```

projection の意味論に応じて surplus / deficit、production surplus、profit、income、valuation gain 等へ解釈する。

少なくとも、

1. actor set / scope
2. 対象 economic changes
3. comparison / accounting boundary
4. unit of account
5. recognition timing
6. valuation rule
7. internal transaction treatment
8. shared-event reconciliation / elimination rule where relevant
9. attribution / distribution rule

を明示する。

---

## 11. accounting projection

formal accounting を用いる場合、physical/resource events だけでなく、contract / financial events、valuation-only events 等も recognition / valuation を経て accounting entries を形成しうる。

P/L は recognized interval events、B/S は recognized point-in-time positions の monetary / exchange-value representation とする。

accounting identity は当該 projection の representation rule として検証する。

---

## 12. business actor / business field / business の計測

organization / company を actor として扱う場合、business actor は actor `i` として観測する。

候補 observable：

- legal / organizational identity
- decision rights
- ownership / accounting attribution
- actor-specific K_i / P_i / A_i

business field は、business activity を継続的に可能化・誘発・再生産する局所 field として観測する。

候補 observable：

- recurring action set
- feasible / available / admissible action ranges
- customer / beneficiary relations
- resource replenishment
- participant retention
- capability reproduction
- learning / exploration activity
- field formation / dissolution

business は business field を中心として継続する activity system として扱う。

同一 actor が複数 business fields を持つ場合、一つの business field が複数 actors にまたがる場合を区別できるよう、actor boundary と field boundary を別々に定義する。

起業は business-oriented field formation を伴う activity、新規事業開発は既存 field から新しい business field を形成・分岐する過程として測る。

profit は一指標であり、business existence の定義変数とはしない。

---

## 13. 3つの管理合理性の計測

3則は constitutive rationality assumptions とする。

- resource-realization：resource / capital / realized-use outcome に関する比較規則
- activity-flow：activity continuity / formation / renewal に関する比較規則
- P-downside：projection-specific future P / viability に関する loss / threshold / exclusion rule

各 rationality dimension は `Ŷ_i,t(a;I_i,t)` のどの component を評価するかを明示し、`Γ_i^adm` の形成へ接続する。

VFT decision projection では、採用した dimension ごとに少なくとも admissibility / exclusion condition または比較規則を事前に定義する。

---

## 14. Marxian projection の計測

- VFT-specific use-value quantity / realized-use outcome：主体が interval 内の実利用を通じて ex post に realized した主観的 outcome
- labor measure：labor activity / labor time
- Marxian labor-value：socially necessary labor time 等の追加条件を伴う specialization
- exchange-value / price：resource 間の comparison / market / monetary valuation
- exchange-value residual / surplus：指定 boundary と exchange-value scale 上の差分
- Marxian surplus value：Marx 固有条件を含む specialization

VFT-specific realized-use outcome と Marxian use-value を自動的に同一視しない。

---

## 15. ミクロ／マクロ

ミクロとマクロは、同じ K と actor-specific K_i / P_i / A records を異なる scope で観測し、必要に応じて shared event reconciliation、external reporting / statistical transformation で接続する。

主体ごとの帳簿自体が共通化されることは仮定しない。

---

## 16. 実証上の原則

少なくとも以下を明示する。

1. K の resource / capability coordinates
2. actor set
3. projection-specified relations / constraints
4. `Γ^feas` の operationalization
5. `Γ^avail` の operationalization
6. `Γ^adm` の admissibility / exclusion rule
7. A の record unit / ordering
8. multi-actor event の `event_id` / participant / role / reconciliation rule
9. downstream aggregation rule
10. `δ_K` の endpoint difference rule
11. exogenous K change を扱う場合の `Ω` 等の定義
12. realized-use outcome の actor / interval / subjective proxy / attribution / reference timing
13. instantaneous rate を使う場合の `C_i(t)` と正則性条件
14. exchange-value / valuation rule
15. K_i の representation rule
16. P / shared P の proxy
17. current P belief / valuation role の識別
18. outcome bundle `Y_i^proj` の coordinates
19. generic forecast `Ŷ_i` の推定法
20. exchange-value residual / surplus の対象 economic changes / comparison boundary
21. accounting projection を用いる場合の recognition / identity rule
22. business actor boundary / business field boundary
23. P-downside の projection-specific viability criterion
24. micro / macro reporting / aggregation rule
25. 欠測・測定誤差・情報損失

---

© T. Nuno  
Licensed under CC BY 4.0