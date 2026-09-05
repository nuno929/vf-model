# 価値場理論 — 計測

## 1. 目的

本書は VFT Core を実証・観測・会計へ落とす際の境界を整理する。

計測上は、physical K、actor-specific K_i、structured subjective state P_i、A の event history、projection-defined endpoint difference ΔK、use-value realization、exchange-value representation を区別する。

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

`P_i` 上の valuation と `K_i` 上の valuation を区別する。

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

## 4. use-value の計測

VFT における use-value quantity は、resource stock 自体ではなく、**主体がある interval 内に resource を実際に利用・消費し、その経験に帰属される形で ex post に realized した主観的効用量**である。

physical stock / capability 自体は K として時点観測できるが、それは use-value quantity ではない。瞬間的な快・満足等を観測できても、それ自体を当該 resource の use-value quantity と同一視しない。

同じ主体・同じ resource・同じ利用量でも、充足状態、利用順序、文脈、他の経験等によって realized outcome は変わりうる。限界効用逓減はその一例である。したがって **use-value quantity に一般的な再現性や interval 間の加法性を仮定しない**。

```text
actual use over τ=(t0,t1]
        ↓
subjective experience / fulfillment
        ↓
realized use-value U^use_i(τ)
```

離散時間で時点 `t` を置く場合、時点 `t` で参照できる use-value は前区間までに realized した outcome である。

```text
U^use_i((t-1,t])
        ↓
reference / update of P_i,t
        ↓
expectation about future use
```

将来区間について realized use-value quantity はまだ存在しない。将来の利用結果について主体が持つものは P_i 上の belief / expectation である。

瞬間 rate を必要とする projection では interval quantity の極限・微分的表現を導入できるが、point-in-time stock valuation として扱わない。

したがって use-value quantity の計測では少なくとも、

- actor
- interval
- actual use / consumption
- subjective utility / experience proxy
- attribution to the resource/use episode
- reference timing
- 必要に応じて substitute / complement / use category

を指定する。

異なる interval 間・主体間で use-value proxy を比較する場合、それが同一尺度上で再現可能な真値を測っているとは仮定せず、projection-specific な比較可能性を別途定義する。

この interval-indexed な時間形式を P/L-like と呼びうるが、会計上の P/L entry と同一視しない。

---

## 5. exchange-value の計測

exchange-value は resource を他の resource / money との比較関係から共通尺度へ写像した representation である。

exchange-value は point-in-time position にも interval event valuation にも現れうる。

```text
point-in-time valuation -> capital / asset position
interval valuation      -> transaction / revenue / expense etc.
```

したがって exchange-value を stock 専用とはしない。一方、**VFT-specific use-value quantity は interval realization としてのみ扱う**。

異質な resource stock を共通交換尺度で比較・集計する評価は exchange-value representation として扱う。

VFT は physical capability / realized use experience / exchange-value representation を別表現として保持するが、これを借方・貸方や複式簿記の普遍対応とはしない。

---

## 6. P の計測

`P_i` は structured subjective state であり、belief / expectation、preference / valuation、trust / reputation、norm recognition 等を含みうる。

候補 proxy には期待調査、選好・評価調査、発話、信用・信頼指標、制度・契約への履行期待、将来見通し等がある。

shared P は actor set 上の共通性・整合性・分布として推定する。

Core の generic forecast は `ΔK̂_i(a; I_i)` とし、P_i の belief / expectation component と情報集合から導出される forecast とする。確率・因果モデルを採用する projection では、条件付き期待値等として具体化してよい。

use-value と P の時系列を観測する場合、

```text
P_i,t        : future use への expectation
A / use      : interval experience
U^use_i(τ)   : ex post realized subjective use-value
P_i,t+1      : realized experience を反映した updated state
```

を区別する。

加工・変換によって resource の利用可能性が変わっても、その加工後 use-value quantity は加工時点ではなく、後続 interval の実利用後に realized する。

---

## 7. A と ΔK

A は生産、消費、交換、投資、労働、移転、契約、政策、探索、学習等の actor-side action / process / event である。

区間中の gross activity は A の event history として記録する。

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

```text
+100 inflow
-100 outflow
=> gross activity exists
=> additive stock projection では endpoint ΔK may be 0
```

`ΔK` は accounting entry ではない。

---

## 8. surplus の計測

surplus は physical primitive ではなく、**指定された economic changes を exchange-value の比較可能尺度へ写像し、specified comparison boundary の下で取る差分 / residual** とする。

```text
specified economic changes
   ↓ exchange-value representation
comparable values
   ↓ comparison under specified boundary
surplus / deficit
```

少なくとも、

1. actor set / scope
2.対象 economic changes
3. comparison / accounting boundary
4. unit of account
5. recognition timing
6. valuation rule
7. internal transaction treatment
8. attribution / distribution rule

を明示する。

production input / output、contract / financial events、valuation-only events のどれを含めるかによって、production surplus / accounting income / valuation gain 等との関係は変わる。Core では同一視しない。

---

## 9. accounting projection

formal accounting を用いる場合、physical flow だけでなく、contract / financial events、valuation-only events 等も recognition / valuation を経て accounting entries を形成しうる。

```text
physical/resource events ─────┐
contract/financial events ────┼→ recognition / valuation → accounting entries
valuation-only events ────────┘
```

P/L は recognized interval events、B/S は recognized point-in-time positions の monetary / exchange-value representation とする。

accounting identity は当該 projection の representation rule として検証する。

---

## 10. field / business の計測

field は、K / K_i / P_i と projection-specified relations / constraints から導かれる action-generating configuration として扱う。

必要に応じて、

```text
F_t := configuration(...)
Γ_i(F_t) := feasible / inducible action correspondence
```

という derived notation を用いる。直接1変数へ縮約することや deterministic choice function を Core では要求しない。

business / organization projection では、例えば、

- recurring action set
- feasible / inducible action range
- activity continuity
- resource replenishment
- participant retention
- customer / beneficiary interaction
- learning / exploration activity
- field formation / dissolution

等を観測できる。

起業は business-oriented field formation の一類型、新規事業開発は既存 field から business-oriented field を形成・分岐させる過程として測る。

profit はその一指標であり、business existence の定義変数とはしない。

---

## 11. 3つの管理合理性の計測

3則は constitutive rationality assumptions とする。

- resource-realization では resource / capital outcome に加えて realized-use outcome を含めうる。
- activity-flow では recurring activity と field formation / renewal を観測する。
- P-downside では P 全体の上下を仮定せず、projection-specific な loss / threshold / viability criterion を指定する。

経験的には、projection-specific な objective / priority / weight / constraint / threshold / horizon が action / outcome をどの程度説明するかを検証する。

---

## 12. Marxian projection の計測

- VFT-specific use-value quantity：主体が interval 内の実利用を通じて ex post に realized した主観的効用量
- labor measure：labor activity / labor time
- Marxian labor-value：socially necessary labor time 等の追加条件を伴う specialization
- exchange-value / price：resource 間の comparison / market / monetary valuation
- generic surplus：指定 boundary と exchange-value scale 上の差分 / residual
- Marxian surplus value：Marx 固有条件を含む specialization

VFT-specific use-value quantity と Marxian use-value を自動的に同一視しない。

---

## 13. ミクロ／マクロ

ミクロとマクロは、同じ physical K と、actor-specific K_i / P_i / A histories を異なる scope で観測し、必要に応じて external reporting / statistical transformation で接続する。

主体ごとの帳簿自体が共通化されることは仮定しない。

---

## 14. 実証上の原則

少なくとも以下を明示する。

1. K の resource coordinates
2. A の event unit / ordering
3. `δ_K` の endpoint difference rule
4. exogenous K change を扱う場合の `Ω` 等の定義
5. use-value の actor / realized interval / subjective proxy / attribution / reference timing
6. exchange-value / valuation rule
7. K_i の representation rule
8. P / shared P の proxy
9. generic forecast `ΔK̂` の推定法
10. surplus の対象 economic changes / comparison boundary
11. accounting projection を用いる場合の recognition / identity rule
12. field / business continuity / inducibility の proxy
13. P-downside の projection-specific viability criterion
14. micro / macro reporting / aggregation rule
15. 欠測・測定誤差・情報損失

---

© T. Nuno  
Licensed under CC BY 4.0