# 価値場理論 — 既存概念・応用への射影ノート

> この文書は Core 定義ではなく、既存概念・応用領域への projection candidate を保存する。

## 1. 基本構造

VFT の経済射影では、

- `K`：physical / real-resource state
- `K_i`：actor-specific exchange-value / capital representation
- `P_i`：structured subjective state
- `A_i`：actor-side action / process / event
- `ΔK_τ := δ_K(K_t0,K_t1)`：projection-defined endpoint resource-state difference
- `ΔK̂_i(a;I_i)`：generic action-contingent forecast

を区別する。

field は K / K_i / P_i と projection-specified relations / constraints から導かれる action-generating configuration として扱う。

必要な projection では、

```text
F_t := configuration(...)
Γ_i(F_t) := feasible / inducible action correspondence
```

という derived notation を使える。

---

## 2. 使用価値 / 交換価値

同一 resource について、physical capability / realized use experience / exchange-value representation を区別する。

### use-value

VFT の use-value quantity は resource stock 自体ではなく、**主体が interval 内に resource を実際に利用・消費し、その経験に帰属される形で ex post に realized した主観的効用量**とする。

physical stock / capability は K として時点観測できるが、それは use-value quantity そのものではない。

同じ主体・同じ resource・同じ利用量でも、充足状態、順序、文脈、他の経験等によって realized outcome は変わりうるため、一般的な再現性や interval 間の加法性を仮定しない。

したがって use-value quantity は interval-indexed outcome として定義する。

```text
actual use over τ=(t0,t1]
        ↓
subjective experience
        ↓
realized use-value U^use_i(τ)
        ↓
P_i update
```

時点 `t` で参照できる use-value は前区間までの realized outcome である。将来区間の use-value はまだ realized しておらず、P_i 上の expectation としてのみ表現される。

瞬間 rate を必要とする projection では、interval quantity の極限・微分的表現として導入できるが、point-in-time stock valuation とは扱わない。

この interval-indexed な時間形式を P/L-like と呼びうるが、会計上の P/L entry と同一視しない。

### exchange-value

resource を他の resource / money との比較関係から共通尺度へ写像した representation とする。

exchange-value は point-in-time position にも interval transaction valuation にも現れうるため、stock 専用とはしない。

したがって use-value / exchange-value と stock / flow を完全な一対一対応とはしない。ただし **VFT-specific use-value quantity は interval realization としてのみ扱う**。

異質な resource stock を共通交換尺度で比較・集計した評価は exchange-value representation に属する。

### accounting analogy

physical capability / realized use experience / exchange-value representation を別々に保持する多面的記述は会計的表現を想起させるが、借方・貸方や複式簿記との対応を意味しない。

---

## 3. K_i / accounting projection

`K_i` は K の subset / partition ではなく、ownership / attribution / valuation 等を経た actor-specific exchange-value / capital representation である。

企業会計 projection では K_i を ledger / B/S 上の monetary positions として形式化できるが、`K_i ≡ B/S` とはしない。

formal accounting では、

```text
physical/resource events ─────┐
contract/financial events ────┼→ recognition / valuation → accounting entries
valuation-only events ────────┘
                                      ↓
                                   P/L / B/S
```

のように複数種の economic events を扱いうる。

帳簿そのものは actor-specific であり、財務報告・連結・統計は別の external representation とする。

### valuation の境界

```text
P_i valuation
= subjective desirability / appraisal / belief-side evaluation

K_i valuation
= exchange-value representation under specified
  recognition / comparison / unit-of-account / valuation rules
```

と区別する。

---

## 4. 契約・制度・金融資産

契約・制度・法的権利関係それ自体は physical K としない。

一方、預金、債券、売掛債権等は recognized exchange-value / financial position として K_i / accounting projection 上に表現できる。

主体が契約・制度の履行・執行・継続をどう期待するかは P に属する。

客観的な institutional / legal state が必要な projection では `C_t` 等を projection-local に追加してよい。

---

## 5. P / forecast

P_i は belief / expectation、preference / valuation、trust / reputation、norm recognition 等を含む structured subjective state とする。

Core の generic forecast は、

```text
ΔK̂_i(a;I_i)
```

とし、P_i の belief / expectation component と情報集合から導出される action-contingent forecast とする。

確率・因果構造を採用する projection では、例えば、

```text
ΔK̂_i(a;I_i) = E_i[ΔK | do(a),I_i]
```

のように具体化してよい。

use-value については、

```text
previous realized use-value
        ↓
P_i,t update
        ↓
expectation about future use
        ↓
A / actual use
        ↓
next realized use-value
```

という時間方向を取る。

加工・変換は resource の利用可能性を変えるが、加工後 use-value quantity は加工時点で確定せず、後続 interval の実利用体験で初めて realized する。

---

## 6. A / ΔK / exogenous change

A は生産、消費、交換、投資、労働、移転、契約、政策、探索、学習等の actor-side event history を持つ。

`ΔK` は projection-defined endpoint resource-state difference とする。

```text
ΔK_τ := δ_K(K_t0,K_t1)
```

additive vector projection では、

```text
δ_K(K_t0,K_t1) = K_t1 - K_t0
```

と specialize できる。

したがって gross activity と ΔK は別概念であり、gross activity は A history から読む。

A を通らない K change が必要な projection では、自然劣化、災害、偶発故障等を `Ω_τ` などの exogenous / environmental process として追加する。

---

## 7. surplus / accumulation

surplus は physical primitive ではない。

指定された economic changes を exchange-value の比較可能尺度へ写像し、その差分を specified comparison boundary の下で集計したときに成立する。

```text
specified economic changes
   ↓ exchange-value representation
comparable values
   ↓ comparison under specified boundary
surplus / deficit
```

production projection では physical / use activity の input / output が主対象になりうる。一方、accounting projection では contract / financial events や valuation-only events を含みうる。

production surplus / accounting profit / income / valuation gain / wealth change は Core で同一視しない。

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

P-downside は P 全体の universal ordering を意味しない。projection-specific な P component と threshold / loss / viability criterion を指定して、将来の action-generating viability の重大な劣化を定義する。

profit / utility は3則の特殊化ではなく、projection-specific metric / objective / proxy とする。

---

## 10. plan / forecast / equilibrium

```text
x_i              = planned / chosen resource change
ΔK̂_i(a;I_i)     = generic action-contingent forecast
```

compatibility / market equilibrium / accounting consistency / steady state は別概念とする。

---

## 11. Marxian categories

VFT は use-value / labor / exchange-value / surplus / accumulation を一般化構造上で保持する。

- VFT-specific use-value quantity：主体が interval 内の実利用体験を通じて ex post に realized した主観的効用量
- labor measure：labor activity / labor time
- Marxian labor-value：socially necessary labor time 等の追加条件を持つ specialization
- exchange-value / price：resource 間の comparison / market / monetary valuation
- generic surplus：指定 boundary と exchange-value scale 上の差分 / residual
- Marxian surplus value：Marx 固有条件を持つ specialization
- accumulation：surplus 等の帰属・留保・分配による K_i の変化

VFT-specific use-value quantity と Marxian use-value は自動的に同一視しない。

---

## 12. ミクロ／マクロ

```text
micro
field_i -> Γ_i(F_t) -> A_i -> resource activity
                         -> ΔK
                         -> realized use-value over interval -> P_i update
                         -> exchange valuation -> K_i update

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
3. A の event unit / ordering
4. `δ_K` の endpoint difference rule
5. exogenous K change を扱う場合の `Ω` 等の定義
6. use-value の actor / realized interval / subjective proxy / attribution / reference timing
7. exchange-value / valuation rule
8. K_i の representation rule
9. P / shared P の proxy
10. generic forecast `ΔK̂` の推定・specialization
11. institutional state が必要な場合の追加定義
12. accounting projection の recognition / identity rule
13. surplus の対象 economic changes / comparison / attribution / distribution
14. field / business continuity / inducibility の proxy
15. P-downside の viability criterion
16. Marxian specialization の追加条件
17. micro / macro reporting / aggregation rule

---

© T. Nuno  
Licensed under CC BY 4.0