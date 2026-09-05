# 価値場理論（Value-Field Theory）

**Theory refresh — Draft**  
Author: **T. Nuno**  
License: **CC BY 4.0**

---

## 1. 概要

価値場理論（Value-Field Theory; VFT）は、個人・組織・社会で生じる変化を、**実物・物理側の資源状態 K、主体別の交換価値・資本表現 K_i、主体ごとの主観的評価・期待状態 P_i、actor-side action / process record A_i** の関係として記述する構造的フレームワークである。

VFT における **field（場）** は独立した価値スカラーではない。ある時点における K、各主体の K_i / P_i と projection-specified な主体間・資源間の関係・制約から導かれる **action-generating configuration** を指す。

```text
F_t
= configuration(K_t, (K_i,t)_i, (P_i,t)_i ; projection-specified relations / constraints)
        ↓
Γ_i^feas(F_t) = feasible action set
        ↓
Γ_i^ind(F_t) ⊆ Γ_i^feas(F_t) = inducible / behaviorally available action set
        ↓
actual action a_i ∈ Γ_i^ind(F_t)
```

`Γ_i^feas` は physical / resource / institutional feasibility を、`Γ_i^ind` は P_i と projection-specific decision structure の下で主体が実際に取りうる behavioral candidate を表す。`Γ_i^ind` は realized action を見て事後的に定義するのではなく、projection 側で ex ante に定める correspondence とする。

`F_t` / `Γ_i^feas` / `Γ_i^ind` は field の意味を示す derived notation であり、新たな universal state primitive や deterministic choice function を追加するものではない。

VFT Core は、普遍的な deterministic choice function、会計則、均衡則、利益最大化則を固定しない。

---

## 2. Core variables / records

- **K**：生産・消費・労働・利用・変換等の対象となる physical / real-resource state
- **K_i**：主体 `i` が保持する actor-specific exchange-value / capital stock representation
- **P_i**：主体 `i` の structured subjective evaluation / expectation state
- **A_i**：主体 `i` 側の action / process record
- **ΔK_τ**：projection-defined endpoint resource-state difference
- **Ŷ_i(a; I_i)**：主体 `i` が candidate action `a` と情報 `I_i` に基づいて形成する generic outcome forecast

`K_i` は K の subset / partition ではない。common K と economic events に ownership / holding / attribution、recognition、valuation 等を適用した actor-indexed exchange-value / capital representation であり、共同所有・重複帰属・複雑な attribution を排除しない。

形式的な企業会計では `K_i` を B/S・ledger 上の monetary position として実装できるが、**`K_i ≡ B/S` とは置かない**。B/S は assets / liabilities / equity 等を持つ制度的 accounting representation であり、K_i を形式化する代表的な projection の一つである。

---

## 3. K：実物・物理側の resource state

K は、設備、原材料、製品、土地、時間、身体、技能、知識、労働力、エネルギー等の resource coordinates を projection に応じて含みうる。

K を「外部に実在するものすべて」へ拡張しない。契約、制度、規範、法的権利関係等は、それだけを理由に K へ含めない。

契約・制度そのものの客観状態が必要な projection では、institutional / legal state を projection-local に追加してよい。Core はその専用 state を必須 primitive としない。

K の変化は A だけから生じるとは仮定しない。自然劣化、災害、偶発的故障等の exogenous / environmental process が必要な projection では `Ω_τ` 等を追加できる。

---

## 4. 使用価値と交換価値

同一 resource について、少なくとも次の表現を区別する。

```text
same resource r
├─ physical state / capability           → K
├─ realized use experience               → VFT-specific use-value quantity
└─ comparative exchange representation   → exchange-value / K_i
```

### use-value quantity

VFT における **use-value quantity** は、resource stock 自体や technical service potential ではなく、**主体がある interval 内にその resource を実際に利用・消費し、その経験に帰属される形で realized した主観的効用量**を指す。

VFT は potential / capability と realized experience を混同しないため、use-value quantity を **interval-indexed outcome** として定義する。時点で観測できる physical stock / capability は K であり、瞬間的な快・満足等の subjective state を観測できるとしても、それ自体を当該 resource の use-value quantity とはみなさない。

同じ主体・同じ resource・同じ利用量であっても、充足状態、利用順序、文脈、他の経験等によって realized outcome は変わりうる。限界効用逓減もこの一例である。そのため、use-value quantity に一般的な再現性や interval 間の加法性を仮定しない。

```text
actual use over τ=(t0,t1]
        ↓
subjective experience / fulfillment
        ↓
U^use_i(τ) = realized use-value quantity
```

離散時間で時点 `t` を考える場合、時点 `t` で参照できるのは前区間までに realized した use-value outcome である。将来区間の use-value はまだ realized していないため、それ自体を use-value quantity として保持せず、P_i 上の belief / expectation として表現する。

瞬間的な use-value rate を必要とする projection では、interval quantity の極限・微分的表現として導入してよい。ただし、それを point-in-time stock valuation とは扱わない。

この時間形式は **P/L-like** である。すなわち VFT-specific use-value quantity は point-in-time stock ではなく、区間内に realized した outcome として評価される。P/L-like はあくまで時間形式についてのアナロジーであり、use-value quantity を会計上の P/L entry と同一視しない。

用語衝突を避ける必要がある箇所では、`U^use_i(τ)` を **realized-use outcome** と呼ぶ。Marxian use-value と自動的に同一視しない。

### exchange-value representation

exchange-value は、resource を他の resource / money との比較関係から共通尺度へ写像した representation である。

exchange-value は、時点の資本 position `K_i` としても、取引・売上・費用等の期間 event valuation としても現れうる。したがって **use-value / exchange-value と stock / flow を完全な一対一対応とはしない**。

ただし VFT-specific use-value quantity は interval realization としてのみ定義する。一方、異質な resource stock を共通交換尺度で比較・集計する場合、その評価は use-value quantity ではなく exchange-value representation に属する。

### 会計アナロジー

VFT は、同一 resource について physical capability、realized use experience、exchange-value representation を区別して記述する。このように複数の表現を併存させる構造は会計的な多面的記述を想起させるが、**借方・貸方や複式簿記との対応を Core の構造として仮定しない**。

---

## 5. P：structured subjective state / forecast

各 `P_i,t` は、将来見通し、belief / expectation、preference / valuation、trust / reputation、norm recognition 等を含む structured subjective state である。

P はどれだけ共有されても主観状態である。shared P は複数主体の P の共通性・整合性・分布として扱い、客観的な社会価値の真値とはみなさない。

### generic outcome forecast

Core の forecast は physical ΔK のみに限定せず、projection が decision に必要とする outcome bundle を対象にする。

```text
Y_i^proj(τ)
= projection-selected outcome bundle
  { ΔK_τ, K_i,t1, U^use_i(τ), P_i,t1, activity outcomes, ... }

Ŷ_i(a; I_i)
= forecast of Y_i^proj under candidate action a
```

`Ŷ_i(a; I_i)` は P_i の belief / expectation component と情報集合 I_i から導出され、desire / preference / plan とは区別する。`ΔK̂_i(a;I_i)` は必要な projection における `Ŷ_i` の一 component として扱う。

確率構造や causal model を採用する projection では、bundle の各 component を条件付き期待値・分布等として specialize してよい。Core は probability measure や causal semantics を固定しない。

P_i に含まれる `valuation` と K_i の valuation は別物である。

```text
P_i valuation
= subjective desirability / appraisal / belief-side evaluation

K_i valuation
= exchange-value representation produced under specified
  recognition / comparison / unit-of-account / valuation rules
```

加工・変換によって同一由来の resource でも利用可能性は変化する。加工後 use-value quantity は加工時点で確定せず、後続 interval の実利用経験として realized し、その結果が P_i を更新する。

---

## 6. A・shared event identity・ΔK

A は主体ごとの **actor-side action / process record** とする。生産、消費、交換、投資、労働、移転、契約、政策、探索、学習等を必要な粒度で記述する。

### multi-actor event identity

交換・移転・契約等、一つの realized event に複数主体が参加する場合、各 `A_i` record は同じ `event_id` と participant relation を共有する。

```text
realized event e
participants(e) = {i, j, ...}

event_id(A_i) = event_id(A_j) = e
```

これにより、actor-side では各主体の role / action を別々に保持しつつ、macro / shared-event aggregation では同一 event を二重計上しない。

必要な場合、shared realized event history を次の derived view として構成できる。

```text
E_τ^shared
:= deduplicate( ⋃_i A_i,τ , by = event_id )
```

`E_τ^shared` は新しい universal state primitive ではなく、multi-actor event identity を用いた derived event view である。

### ΔK

`ΔK_τ` は endpoint resource-state difference を表し、一般形を projection-defined difference operator `δ_K` で書く。

```text
ΔK_τ := δ_K(K_t0, K_t1)
```

K が additive vector space 等で表現される projection では、特殊形として `δ_K(K_t0,K_t1)=K_t1-K_t0` と置ける。

したがって gross activity と ΔK は別概念である。multi-actor gross activity を集計する場合は actor records の単純和ではなく、必要に応じて shared event identity を参照する。

また、K の endpoint difference は A だけに由来するとは限らない。必要な projection では `Ω_τ` 等の exogenous / environmental process を明示する。

`ΔK` は会計仕訳ではない。

---

## 7. exchange-value と surplus

surplus は physical primitive ではない。

VFT Core では、**指定された comparison boundary の下で選択された economic changes を exchange-value の比較可能尺度へ写像し、その差分 / residual を surplus / deficit と呼ぶ**。

```text
specified economic changes
        ↓ exchange-value representation
comparable values
        ↓ comparison under a specified boundary
surplus / deficit
```

production input / output を対象にする projection では physical / use activity が主要入力になりうる。一方、formal accounting projection では contract / financial events や valuation-only events を含みうる。何を対象 change に含めるかによって production surplus / accounting income / valuation gain 等との関係は変わるため、Core では同一視しない。

より中立的な型名が必要な場合は **exchange-value residual** と記述し、surplus / deficit は projection-specific な経済的解釈として扱う。

surplus の帰属・留保・分配は、次期の actor-specific exchange-value / capital position `K_i` を変えうる。

---

## 8. 会計への projection

P/L・B/S・複式簿記は VFT Core の普遍的因果層ではなく、exchange-value を制度的に記録する **formal accounting projection** である。

```text
physical/resource events ─────┐
contract/financial events ────┼→ recognition / valuation → accounting entries
valuation-only events ────────┘
                                      ↓
                                   P/L / B/S
```

- P/L：recognized interval events の monetary / exchange-value representation
- B/S：recognized point-in-time positions の monetary / exchange-value representation
- ledger：actor-specific accounting record

帳簿そのものは主体ごとに閉じており、recognition / valuation / bookkeeping は主体・制度によって異なりうる。財務報告・連結・統計は個別帳簿とは別の external representation である。

正式な accounting projection で B/S を採用する場合、assets / liabilities / equity 等の accounting identity はその representation の定義条件として従う。ただし、それを全主体の普遍的認知公理とはしない。

---

## 9. field と事業体

VFT では、事業体を「利益を最大化する法人」から定義しない。

**事業体は、一定の目的・機能に向けた A を継続的に誘発・再生産する局所的 field structure** として捉える。

この定義では、営利企業だけでなく、NPO、協同組合、公共事業、国家・自治体の事業等を同じ型で扱える。

利益は事業体を定義する目的ではなく、交換価値側で活動継続や蓄積を評価する重要な指標の一つである。

```text
起業             = business-oriented field formation の一類型
新規事業開発     = 既存 field から business-oriented field を形成・分岐させる活動
既存事業の運営   = 成立済み business field の維持・再生産・改善
```

field formation 自体は事業に限らない。起業はそのうち business-oriented な field formation として扱う。

---

## 10. 3つの管理合理性公理

VFT の decision model は次の3則を constitutive rationality assumptions として置く。

1. **resource-realization**：resource の取得・保持・変換・利用を通じて、望ましい resource / capital / realized-use outcome の実現へ向けて A を動かす
2. **activity-flow**：必要な activity / process の流れを維持・拡張し、必要なら新たな action-generating field を形成する
3. **P-downside**：projection が指定した P component の変化によって、将来の action-generating viability が重大に損なわれることを回避する

P-downside は P 全体に universal ordering を仮定しない。何を downside とみなすかは projection-specific な threshold / loss / viability criterion 等によって定める。

3則は `Ŷ_i(a;I_i)` のどの outcome component を、どの objective / constraint / threshold で評価するかを projection 側で具体化することで decision model に接続する。

3則は経験的普遍法則ではない。VFT decision projection を名乗る場合、少なくとも採用した rationality dimension ごとに **admissibility / exclusion condition または比較規則**を明示し、観測後に任意の行動を事後説明するだけのラベルとして用いない。

profit / utility は3則の特殊化ではなく、具体的な decision problem を評価する metric / objective / proxy として使いうる。

---

## 11. 経済学への射影

### plan / forecast

必要な economic projection では planned / chosen resource change を `x_i` と書ける。

```text
x_i                = planned / chosen resource change
Ŷ_i(a; I_i)        = generic forecast of projection-selected outcome bundle
ΔK̂_i(a; I_i)      = optional physical-resource component of Ŷ_i
```

Core は probability measure や causal semantics を固定しない。確率・因果構造を採用する projection では bundle の各 component を期待値・分布・causal estimand 等へ specialize できる。

### Marxian categories

VFT は Marxian economics が区別した use-value / labor / exchange-value / surplus / accumulation を一般化された構造上で表現する。

- VFT-specific use-value quantity / realized-use outcome：主体が interval 内の実利用を通じて体験として realized した主観的効用量
- labor measure：labor activity / labor time による production activity の記述
- Marxian labor-value projection：socially necessary labor time 等の追加条件を導入した specialization
- exchange-value / price：resource 間の比較・market / monetary valuation
- surplus：指定 boundary と exchange-value scale の下で解釈される差分 / residual
- accumulation / distribution：surplus 等の帰属・留保・分配による K_i の変化

VFT-specific use-value quantity は Marxian use-value と自動的に同一視しない。VFT Core 自体を Marx 固有の labor-value theory / surplus-value theory とも同一視しない。

---

## 12. ミクロ／マクロ接続

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

主体ごとの帳簿そのものが共通化されることは仮定しない。macro representation は、必要な projection で shared event identity、reporting / statistical transformation / aggregation を通じて構成する。

---

## 13. compatibility / equilibrium / accounting

- **inter-agent compatibility / feasibility**：各主体の plan が相互に実行可能・両立可能であること
- **market equilibrium**：compatibility に加え、射影先理論の choice / optimality / best response / clearing 条件が成立すること
- **accounting consistency**：指定 accounting representation の recognition / valuation / identity / closing rule が整合すること
- **steady state**：対象状態について別途定める動学条件

これらは別概念である。

---

## 14. Core で固定しないもの

- K の標準 resource coordinates
- `δ_K` の標準 difference rule
- institutional / legal state の普遍 primitive
- exogenous / environmental process の標準表現
- use-value の標準効用関数・代替可能性・加法性
- exchange-value / monetary valuation function
- K_i の標準 representation / accounting implementation
- P の標準内部次元・universal ordering
- P の普遍的更新式
- `Γ_i^feas` / `Γ_i^ind` の標準生成式
- A の deterministic choice function
- generic outcome bundle `Y_i^proj` の標準 coordinates
- generic forecast `Ŷ_i` の確率測度・期待形成式・causal semantics
- surplus / exchange-value residual の普遍的算出式・対象 economic changes
- 3則の objective / weight / priority / threshold / viability criterion
- market equilibrium の普遍的条件
- micro-to-macro aggregation rule

---

## 15. ドキュメント

- [モデルノート](docs/01_model_notes.md)
- [計測](docs/02_measurement.md)
- [背景・整理経緯](notes/background.md)
- [既存概念・応用への射影](notes/projections.md)
- [拡張・再検討ノート](notes/future_topics.md)

---

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)  
© T. Nuno