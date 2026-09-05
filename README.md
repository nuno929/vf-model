# 価値場理論（Value-Field Theory）

**Theory refresh — Draft**  
Author: **T. Nuno**  
License: **CC BY 4.0**

---

## 1. 概要

価値場理論（Value-Field Theory; VFT）は、個人・組織・社会で生じる変化を、**real-resource / capability state K、actor-specific exchange-value / capital representation K_i、structured subjective state P_i、actor-side action / process record A_i** の関係として記述する構造的フレームワークである。

VFT における **field（場）** は独立した価値スカラーではない。ある時点における K、各主体の K_i / P_i と projection-specified な主体間・資源間の関係・制約から導かれる **action-generating configuration** を指す。

```text
F_t
= configuration(K_t, (K_i,t)_i, (P_i,t)_i ; projection-specified relations / constraints)
        ↓
Γ_i^feas(F_t) = feasible action set
        ↓
Γ_i^avail(F_t) ⊆ Γ_i^feas(F_t)
= cognitively / behaviorally available action set
        ↓ forecast + projection-specific rationality rules
Γ_i^adm(F_t) ⊆ Γ_i^avail(F_t)
= admissible action set
        ↓ projection-specific selection
actual action a_i
```

- `Γ_i^feas`：physical / resource / institutional feasibility
- `Γ_i^avail`：主体が認知・検討・実行候補として持ちうる behavioral availability / consideration set
- `Γ_i^adm`：forecast と projection-specific rationality / admissibility rules を通過した action candidates

これらは realized action を見て事後的に定義する集合ではない。projection 側で ex ante に operationalize する derived correspondence であり、universal state primitive や deterministic choice function を追加するものではない。

VFT Core は、普遍的な choice function、会計則、均衡則、利益最大化則を固定しない。

---

## 2. Core variables / records

- **K**：生産・消費・労働・利用・変換等の対象となる real-resource / capability state
- **K_i**：主体 `i` が保持する actor-specific exchange-value / capital stock representation
- **P_i**：主体 `i` の structured subjective evaluation / expectation state
- **A_i**：主体 `i` 側の action / process record
- **ΔK_τ**：projection-defined endpoint resource-state difference
- **Ŷ_i,t(a; I_i,t)**：主体 `i` が candidate action `a` と時点 `t` の情報に基づいて形成する generic outcome forecast

K は physical resources を含むが、それに限定しない。available time budget / remaining workable capacity、技能、知識、労働能力等の real-resource / capability coordinates も projection に応じて含みうる。

`K_i` は K の subset / partition ではない。common K と economic events に ownership / holding / attribution、recognition、valuation 等を適用した actor-indexed exchange-value / capital representation であり、共同所有・重複帰属・複雑な attribution を排除しない。

形式的な企業会計では `K_i` を B/S・ledger 上の monetary position として実装できるが、**`K_i ≡ B/S` とは置かない**。B/S は制度的 accounting representation であり、K_i を形式化する projection の一つである。

---

## 3. K：real-resource / capability state

K は設備、原材料、製品、土地、エネルギー等の physical resources に加え、available time budget / remaining workable capacity、身体、技能、知識、労働能力等の capability coordinates を projection に応じて含みうる。

calendar time `t` はモデル上の index であり K の resource coordinate ではない。また、interval `τ` 内に実際に投入された labor time / hours worked は K_t の stock ではなく、A / labor measure 側の interval activity として扱う。

K を external world state 全体へ拡張しない。契約、制度、規範、法的権利関係等は、それだけを理由に K へ含めない。

契約・制度そのものの客観状態が必要な projection では institutional / legal state を projection-local に追加してよい。Core はその専用 state を必須 primitive としない。

K の変化は A だけから生じるとは仮定しない。自然劣化、災害、偶発的故障等の exogenous / environmental process が必要な projection では `Ω_τ` 等を追加できる。

---

## 4. 使用価値と交換価値

同一 resource について、少なくとも次の表現を区別する。

```text
same resource r
├─ resource state / capability            → K
├─ realized use experience                → realized-use outcome / VFT-specific use-value quantity
└─ comparative exchange representation    → exchange-value / K_i
```

### realized-use outcome / use-value quantity

VFT における `U^use_i(τ)` は、resource stock 自体や technical service potential ではなく、**主体が interval `τ` 内に resource を実際に利用・消費し、その経験に帰属される形で realized した主観的 outcome** を指す。

したがって、potential / capability と realized experience を混同しない。時点で観測できる resource stock / capability は K であり、瞬間的な快・満足等の subjective state を観測できるとしても、それ自体を当該 resource の realized-use outcome とはみなさない。

同じ主体・同じ resource・同じ利用量でも、充足状態、利用順序、文脈、他の経験等によって結果は変わりうる。そのため、一般的な再現性や interval 間の加法性を仮定しない。

```text
actual use over τ=(t0,t1]
        ↓
subjective experience / fulfillment
        ↓
U^use_i(τ) = realized-use outcome
```

離散時間で時点 `t` を考える場合、時点 `t` で参照できるのは前区間までに realized した use outcome である。将来区間の use outcome はまだ realized しておらず、P_i,t 上の belief / expectation として表現する。

**一般の非加法的 interval outcome から instantaneous rate が自動的に導けるとは仮定しない。** 瞬間 rate が必要な projection では、別途 cumulative realized-use process `C_i(t)` を定義し、必要な加法性・正則性を満たす場合にのみ `u_i(t)=dC_i(t)/dt` 等を導入してよい。

この interval-indexed な時間形式は P/L-like と呼びうるが、会計上の P/L entry と同一視しない。

`use-value quantity` は Marxian category との接続名として用いる。数理・計測上は `realized-use outcome` を優先してよい。VFT-specific realized-use outcome と Marxian use-value は自動的に同一視しない。

### exchange-value representation

exchange-value は resource を他の resource / money との比較関係から共通尺度へ写像した representation である。

exchange-value は point-in-time capital position `K_i` にも interval transaction / revenue / expense valuation にも現れうる。異質な resource stock を共通交換尺度で比較・集計する評価は realized-use outcome ではなく exchange-value representation に属する。

### 会計アナロジー

VFT は resource capability、realized use experience、exchange-value representation を区別して記述する。この多面的記述は会計的な複数表現を想起させるが、借方・貸方や複式簿記との対応を Core の構造として仮定しない。

---

## 5. P：structured subjective state / decision-time direction

各 `P_i,t` は belief / expectation、preference / valuation、trust / reputation、norm recognition 等を含む structured subjective state である。

P はどれだけ共有されても主観状態である。shared P は複数主体の P の共通性・整合性・分布として扱い、客観的な社会価値の真値とはみなさない。

### forecast と evaluation

時点 `t` の decision では、P_i,t の component を役割上区別する。

```text
P_i,t belief / expectation component
        ↓ generates / conditions
Ŷ_i,t(a; I_i,t)

P_i,t preference / valuation component
        ↓ evaluates together with projection-specific rules
Ŷ_i,t(a; I_i,t)
        ↓
Γ_i^adm(F_t)

Ŷ_i,t(a; I_i,t) may contain
P̂_i,t1(a)
```

したがって、現在の P_i,t が未来の P_i,t1 を予測・評価することは時間方向を持つ。P が同時点の自分自身を循環的に評価する構造を意味しない。

Core の forecast は physical ΔK のみに限定せず、projection が decision に必要とする outcome bundle を対象にする。

```text
Y_i^proj(τ)
= projection-selected outcome bundle
  { ΔK_τ, K_i,t1, U^use_i(τ), P_i,t1, activity outcomes, ... }

Ŷ_i,t(a; I_i,t)
= forecast of Y_i^proj under candidate action a
```

`ΔK̂_i(a;I_i)` は必要な projection における `Ŷ_i` の physical / resource component として扱える。Core は probability measure や causal semantics を固定しない。

P_i に含まれる valuation と K_i の valuation は別物である。

```text
P_i valuation
= subjective desirability / appraisal / belief-side evaluation

K_i valuation
= exchange-value representation produced under specified
  recognition / comparison / unit-of-account / valuation rules
```

---

## 6. A・shared realized event・ΔK

A は主体ごとの **actor-side action / process record** とする。生産、消費、交換、投資、労働、移転、契約、政策、探索、学習等を必要な粒度で記述する。interval `τ` 内の actual labor time / hours worked も、必要な labor projection では A / labor measure として記述する。

### multi-actor event identity

交換・移転・契約等、一つの realized event に複数主体が参加する場合、対応する `A_i` records は shared `event_id` と participant / role relation を持つ。

```text
realized event e
participants(e) = {i, j, ...}
event_id(A_i,e) = event_id(A_j,e) = e
```

shared realized event は actor records の片方を捨てる deduplication ではなく、participant-side records を **reconcile / compose** して構成する。

```text
E_e^shared
:= reconcile({ A_i,e | i ∈ participants(e) })
```

buyer の受領・支払と seller の引渡・受取のように、同一 event に属する複数の actor-side records は E_e^shared 内で保持される。

`deduplicate by event_id` は transaction count 等、event identity の重複だけを除く特定 aggregation の特殊形として用いてよい。

`E^shared` は universal state primitive ではなく、multi-actor event identity から得る derived event view である。

### ΔK

`ΔK_τ` は endpoint resource-state difference を表し、一般形を projection-defined difference operator `δ_K` で書く。

```text
ΔK_τ := δ_K(K_t0, K_t1)
```

K が additive vector space 等で表現される projection では、特殊形として `δ_K(K_t0,K_t1)=K_t1-K_t0` と置ける。

したがって gross activity と ΔK は別概念である。multi-actor activity の集計では shared event composition と対象 coordinate に応じた aggregation rule を明示する。

---

## 7. exchange-value residual / surplus

surplus は physical primitive ではない。

Core-level の中立的な差分は **exchange-value residual** として記述できる。

```text
specified economic changes
        ↓ exchange-value representation
comparable values
        ↓ comparison under a specified boundary
exchange-value residual
```

surplus / deficit、production surplus、profit、income、valuation gain 等は projection-specific な経済的解釈として扱う。Core では同一視しない。

---

## 8. 会計への projection

P/L・B/S・複式簿記は VFT Core の普遍的因果層ではなく、exchange-value を制度的に記録する formal accounting projection である。

physical/resource events、contract / financial events、valuation-only events 等が recognition / valuation を経て accounting entries を形成しうる。

帳簿そのものは actor-specific であり、財務報告・連結・統計は別の external representation とする。

---

## 9. business actor / business field / business

VFT では organization / company を actor として扱うことと、business を field level で記述することを分離する。

```text
business actor / organization
= actor i
= decision / ownership / accounting / action attribution の主体

business field F^biz
= actor-resource transformation / exchange / service / beneficiary relation 等を
  反復可能にする局所 action-generating configuration

business
= F^biz を中心として継続する activity system
```

したがって、**business actor と business field は同一型ではない**。同一法人が複数 business fields を運営することも、business field が複数 actor にまたがることも許す。

「事業」は field level で初めて、顧客・資源・能力・期待・関係・制約が recurring activity を再生産する構造として記述できる。法人格・組織・資産の存在だけでは business existence を定義しない。

```text
起業             = business-oriented field formation を伴う activity
新規事業開発     = 既存 field から新しい business field を形成・分岐させる activity
既存事業の運営   = 成立済み business field の維持・再生産・改善
```

profit / surplus は business existence の定義条件ではなく exchange-value 側の重要 metric の一つである。

---

## 10. 3つの管理合理性公理

VFT の management / decision rationality は、次の3則を**必須の構成公理**として持つ。

1. **resource-realization**：resource / capital / realized-use outcome の望ましい実現
2. **activity-flow**：必要な activity / process の継続・拡張、必要なら field formation / renewal
3. **P-downside**：projection が指定した将来 P component / action-generating viability の重大な downside を回避

3公理は `Ŷ_i,t(a;I_i,t)` の outcome components を projection-specific objective / constraint / threshold / comparison rule で評価し、`Γ_i^adm` を形成する段階に接続する。

3公理はすべて構成条件であり、任意に採否を選ぶ dimension ではない。一方、その評価・判断・実行は単一 actor に集中する必要はなく、複数 actor、役割、組織階層、制度へ分業・分散してよい。VFT decision projection では3公理それぞれについて admissibility / exclusion condition または比較規則を **ex ante** に明示する。

P-downside は P 全体に universal ordering を仮定しない。profit / utility は3公理の特殊化ではなく、具体的 decision problem の metric / objective / proxy として使いうる。

---

## 11. 経済学への射影

必要な economic projection では planned / chosen resource change を `x_i` と書ける。

```text
x_i                 = planned / chosen resource change
Ŷ_i,t(a; I_i,t)     = generic forecast of projection-selected outcome bundle
ΔK̂_i(a; I_i)       = optional resource-state component of Ŷ_i
```

compatibility / market equilibrium / accounting consistency / steady state は別概念とする。

### Marxian categories

VFT は use-value / labor / exchange-value / surplus / accumulation の区別を一般化構造上で保持する。

- VFT-specific use-value quantity / realized-use outcome：主体が interval 内の実利用を通じて realized した主観的 outcome
- labor measure：interval 内に実際に投入された labor activity / labor time
- Marxian labor-value：socially necessary labor time 等の追加条件を持つ specialization
- exchange-value / price：resource 間の comparison / market / monetary valuation
- exchange-value residual / surplus：指定 boundary と exchange-value scale 上の差分
- Marxian surplus value：Marx 固有条件を持つ specialization
- accumulation：surplus 等の帰属・留保・分配による K_i の変化

VFT-specific use-value quantity と Marxian use-value は自動的に同一視しない。

---

## 12. ミクロ／マクロ接続

```text
state / field
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
state transition / realized-use outcome / K_i change / P_i update

        ↓ reporting / aggregation

macro states / distributions / field formation-dissolution
```

主体ごとの帳簿そのものが共通化されることは仮定しない。

---

## 13. Core で固定しないもの

- K の標準 resource / capability coordinates
- `δ_K` の標準 difference rule
- institutional / legal state の普遍 primitive
- exogenous / environmental process の標準表現
- realized-use outcome の標準効用関数・加法性・rate representation
- exchange-value / monetary valuation function
- K_i の標準 representation / accounting implementation
- P の標準内部次元・universal ordering
- P の普遍的更新式
- `Γ_i^feas` / `Γ_i^avail` / `Γ_i^adm` の標準生成式
- A の deterministic choice function
- shared event reconciliation の標準 rule
- generic outcome bundle `Y_i^proj` の標準 coordinates
- generic forecast `Ŷ_i` の確率測度・期待形成式・causal semantics
- exchange-value residual の普遍的算出式
- 3公理の projection-specific operationalization と actor / role 間の分業形態
- market equilibrium の普遍的条件
- micro-to-macro aggregation rule

---

## 14. ドキュメント

- [モデルノート](docs/01_model_notes.md)
- [計測](docs/02_measurement.md)
- [背景・整理経緯](notes/background.md)
- [既存概念・応用への射影](notes/projections.md)
- [拡張・再検討ノート](notes/future_topics.md)

---

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)  
© T. Nuno