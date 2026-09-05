# 価値場理論 — 計測

## 1. 目的

本書は VFT Core を実証・観測・会計へ落とす際の境界を整理する。

計測上は、physical K、actor-specific K_i、structured subjective state P_i、actor-side A records、shared event identity、projection-defined endpoint difference ΔK、realized-use outcome、exchange-value representation を区別する。

---

## 2. K の観測

K は physical / real-resource state である。

候補 observable には原材料量、製品量、設備、稼働、労働時間、エネルギー使用、土地、時間、技能・人的能力等がある。

K の完全観測は前提とせず、resource coordinates と観測単位は projection ごとに定める。

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

## 4. use-value / realized-use outcome の計測

VFT における use-value quantity は、resource stock 自体ではなく、**主体がある interval 内に resource を実際に利用・消費し、その経験に帰属される形で ex post に realized した主観的効用量**である。

physical stock / capability 自体は K として時点観測できるが、それは use-value quantity ではない。瞬間的な快・満足等を観測できても、それ自体を当該 resource の use-value quantity と同一視しない。

同じ主体・同じ resource・同じ利用量でも、充足状態、利用順序、文脈、他の経験等によって realized outcome は変わりうる。したがって一般的な再現性や interval 間の加法性を仮定しない。

```text
actual use over τ=(t0,t1]
        ↓
subjective experience / fulfillment
        ↓
U^use_i(τ)
```

離散時間で時点 `t` を置く場合、時点 `t` で参照できる use-value は前区間までに realized した outcome である。将来の利用結果について主体が持つものは P_i 上の belief / expectation である。

瞬間 rate を必要とする projection では interval quantity の極限・微分的表現を導入できるが、point-in-time stock valuation として扱わない。

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

用語衝突を避ける必要がある箇所では `U^use_i(τ)` を realized-use outcome と呼ぶ。

---

## 5. exchange-value の計測

exchange-value は resource を他の resource / money との比較関係から共通尺度へ写像した representation である。

exchange-value は point-in-time position にも interval event valuation にも現れうる。

```text
point-in-time valuation -> capital / asset position
interval valuation      -> transaction / revenue / expense etc.
```

異質な resource stock を共通交換尺度で比較・集計する評価は exchange-value representation として扱う。

VFT は physical capability / realized use experience / exchange-value representation を別表現として保持するが、これを借方・貸方や複式簿記の普遍対応とはしない。

---

## 6. P / outcome forecast の計測

`P_i` は structured subjective state であり、belief / expectation、preference / valuation、trust / reputation、norm recognition 等を含みうる。

候補 proxy には期待調査、選好・評価調査、発話、信用・信頼指標、制度・契約への履行期待、将来見通し等がある。

shared P は actor set 上の共通性・整合性・分布として推定する。

Core の generic forecast は、

```text
Y_i^proj(τ)
:= projection-selected outcome bundle

Ŷ_i(a;I_i)
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

`ΔK̂_i(a;I_i)` は `Ŷ_i` の optional physical-resource component とする。

計測時には、forecast 対象 coordinates、forecast horizon、information set、推定法、確率分布を用いる場合の calibration 等を明示する。

---

## 7. field / feasibility / inducibility の計測

field は、K / K_i / P_i と projection-specified relations / constraints から導かれる action-generating configuration として扱う。

必要に応じて、

```text
F_t := configuration(...)
Γ_i^feas(F_t) := feasible action set
Γ_i^ind(F_t)  := inducible / behaviorally available action set
Γ_i^ind(F_t) ⊆ Γ_i^feas(F_t)
```

を用いる。

`Γ_i^feas` の候補 observable は、physical capacity、resource availability、legal / institutional permission、budget / access constraints 等。

`Γ_i^ind` の候補 observable は、consideration set、choice set、stated intention、behavioral availability、policy / organizational decision rules 等である。

`Γ_i^ind` は realized action を見て事後的に定義せず、可能な限り action realization 前の情報から operationalize する。

---

## 8. A と shared event identity

A は actor-side action / process record である。

複数主体にまたがる交換・移転・契約等では、対応する actor records に shared `event_id` と participant / role relation を記録する。

```text
event_id(A_i) = event_id(A_j) = e
participants(e) = {i,j,...}
```

これにより、

- actor-level analysis：各主体の A_i records を使う
- shared-event / macro analysis：event_id で重複排除する

と分ける。

必要な場合、

```text
E_τ^shared := deduplicate( ⋃_i A_i,τ , by = event_id )
```

を derived observable とする。

multi-actor event の計測では少なくとも、

1. event identity
2. participant set
3. participant role / direction
4. event timing
5. actor-specific action / position
6. aggregation 時の deduplication rule

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

multi-actor gross activity を集計する場合は actor-side A records を単純加算せず、shared event identity を使って必要な単位へ変換する。

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
8. shared-event deduplication rule where relevant
9. attribution / distribution rule

を明示する。

---

## 11. accounting projection

formal accounting を用いる場合、physical flow だけでなく、contract / financial events、valuation-only events 等も recognition / valuation を経て accounting entries を形成しうる。

```text
physical/resource events ─────┐
contract/financial events ────┼→ recognition / valuation → accounting entries
valuation-only events ────────┘
```

P/L は recognized interval events、B/S は recognized point-in-time positions の monetary / exchange-value representation とする。

accounting identity は当該 projection の representation rule として検証する。

---

## 12. business / organization の計測

business entity は、一定の目的・機能に向けた A を継続的に誘発・再生産する局所 field structure として扱う。

候補 observable には、

- recurring action set
- feasible / inducible action range
- activity continuity
- resource replenishment
- participant retention
- customer / beneficiary interaction
- learning / exploration activity
- field formation / dissolution

等がある。

起業は business-oriented field formation の一類型、新規事業開発は既存 field から business-oriented field を形成・分岐させる過程として測る。

profit はその一指標であり、business existence の定義変数とはしない。

---

## 13. 3つの管理合理性の計測

3則は constitutive rationality assumptions とする。

- resource-realization：resource / capital / realized-use outcome に関する比較規則
- activity-flow：activity continuity / formation / renewal に関する比較規則
- P-downside：projection-specific loss / threshold / viability criterion

`Ŷ_i(a;I_i)` のどの component を各 rationality dimension が評価するかを明示する。

VFT decision projection では、採用した dimension ごとに少なくとも admissibility / exclusion condition または比較規則を事前に定義する。

---

## 14. Marxian projection の計測

- VFT-specific use-value quantity / realized-use outcome：主体が interval 内の実利用を通じて ex post に realized した主観的効用量
- labor measure：labor activity / labor time
- Marxian labor-value：socially necessary labor time 等の追加条件を伴う specialization
- exchange-value / price：resource 間の comparison / market / monetary valuation
- exchange-value residual / surplus：指定 boundary と exchange-value scale 上の差分
- Marxian surplus value：Marx 固有条件を含む specialization

VFT-specific use-value quantity と Marxian use-value を自動的に同一視しない。

---

## 15. ミクロ／マクロ

ミクロとマクロは、同じ physical K と actor-specific K_i / P_i / A records を異なる scope で観測し、必要に応じて shared event identity、external reporting / statistical transformation で接続する。

主体ごとの帳簿自体が共通化されることは仮定しない。

---

## 16. 実証上の原則

少なくとも以下を明示する。

1. K の resource coordinates
2. actor set
3. `Γ^feas` / `Γ^ind` の operationalization
4. A の record unit / ordering
5. multi-actor event の `event_id` / participant / deduplication rule
6. `δ_K` の endpoint difference rule
7. exogenous K change を扱う場合の `Ω` 等の定義
8. use-value の actor / realized interval / subjective proxy / attribution / reference timing
9. exchange-value / valuation rule
10. K_i の representation rule
11. P / shared P の proxy
12. outcome bundle `Y_i^proj` の coordinates
13. generic forecast `Ŷ_i` の推定法
14. exchange-value residual / surplus の対象 economic changes / comparison boundary
15. accounting projection を用いる場合の recognition / identity rule
16. business continuity / formation の proxy
17. P-downside の projection-specific viability criterion
18. micro / macro reporting / aggregation rule
19. 欠測・測定誤差・情報損失

---

© T. Nuno  
Licensed under CC BY 4.0