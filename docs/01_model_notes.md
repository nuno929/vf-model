# 価値場理論 — モデルノート

## 1. 目的

本ノートは、価値場理論（Value-Field Theory; VFT）の Core を README より形式的に整理する。

VFT は、**real-resource / capability state K、actor-specific exchange-value / capital representation K_i、structured subjective state P_i、actor-side action / process record A_i** の関係として経済・事業活動を記述する。

VFT における field は独立したスカラー V ではない。K、(K_i)_i、(P_i)_i と projection-specified relations / constraints から導かれる action-generating configuration である。

---

## 2. Core state / process

```text
K_t
(K_i,t)_{i in I}
(P_i,t)_{i in I}
(A_i,τ)_{i in I}
```

- `K_t`：real-resource / capability state
- `K_i,t`：actor-specific exchange-value / capital stock representation
- `P_i,t`：structured subjective evaluation / expectation state
- `A_i,τ`：actor-side action / process record

field はこれらを単純に足した新変数ではない。

```text
F_t
:= configuration(K_t, (K_i,t)_i, (P_i,t)_i ; R_t^proj, C_t^proj)

Γ_i^feas(F_t)
:= feasible action set

Γ_i^avail(F_t)
:= cognitively / behaviorally available action set

Γ_i^adm(F_t)
:= admissible action set

Γ_i^adm(F_t) ⊆ Γ_i^avail(F_t) ⊆ Γ_i^feas(F_t)
```

`R_t^proj` / `C_t^proj` は projection-specified relations / constraints を表す記法であり、Core の universal state primitive ではない。`F_t`、`Γ_i^feas`、`Γ_i^avail`、`Γ_i^adm` も derived notation であり、deterministic choice rule を仮定しない。

- `Γ_i^feas`：physical / resource / institutional feasibility
- `Γ_i^avail`：主体が認知・検討・behavioral candidate として持ちうる consideration / availability
- `Γ_i^adm`：forecast と projection-specific rationality / admissibility rules を通過した candidate set

これらは realized action を見て事後的に定義しない。projection 側で ex ante に operationalize する。

actual action / choice の生成則は projection-specific とし、Core では固定しない。

---

## 3. K：real-resource / capability state

`K_t` は時点 `t` における real-resource / capability state を表す。

対象 projection に応じて、設備、土地、原材料、製品、エネルギー等の physical resources に加え、available time budget / remaining workable capacity、身体、技能、知識、労働能力等を含みうる。

calendar time `t` はモデル上の index であり K の resource coordinate ではない。また、interval `τ` 内に実際に投入された labor time / hours worked は K_t の stock ではなく、A / labor measure 側の interval activity として扱う。

K は external world state 全体ではない。契約、制度、規範、法的権利関係等を、それだけを理由に K へ含めない。

institutional / legal state が必要な projection では、`C_t` 等を projection-local に追加してよい。Core はそれを必須 primitive としない。

また K の変化は A のみから生じるとは仮定しない。自然劣化、災害、偶発故障等の exogenous / environmental process が必要な projection では `Ω_τ` 等を projection-local に追加できる。

---

## 4. K_i：actor-specific exchange-value / capital representation

`K_i,t` は主体 `i` が保持する exchange-value / capital stock representation である。

```text
common K / economic events
        ↓ ownership / holding / attribution
        ↓ recognition / valuation
      K_i,t
```

`K_i` は K の subset でも、互いに素な partition でもない。共同所有・重複帰属・複雑な claim / attribution を排除しない。

### accounting projection との関係

`K_i` を B/S そのものとは定義しない。

企業会計等の formal accounting projection では、`K_i` を ledger / B/S 上の monetary positions として形式化できる。ただし B/S は assets / liabilities / equity 等を含む制度的 accounting representation であり、`K_i ≡ B/S_i` とは置かない。

正式な B/S projection を採用する場合、accounting identity はその representation の定義条件として従う。これは全主体の普遍的認知公理ではない。

### valuation の意味

`P_i` と `K_i` の双方で valuation という語を使いうるが、意味は異なる。

```text
P_i valuation
= subjective desirability / appraisal / belief-side evaluation

K_i valuation
= exchange-value representation produced under specified
  recognition / comparison / unit-of-account / valuation rules
```

### 金融資産との境界

預金、債券、売掛債権等は、その根拠となる契約・法的権利関係そのものを K とみなすのではなく、recognized exchange-value / financial position として K_i / accounting projection 上に表現できる。

---

## 5. 使用価値と交換価値

同一 resource `r` について、少なくとも次の表現を区別する。

```text
same resource r
├─ resource state / capability            → K
├─ realized use experience                → realized-use outcome / VFT-specific use-value quantity
└─ comparative exchange representation    → exchange-value / K_i
```

### 5.1 realized-use outcome / use-value quantity

`U^use_i(τ)` は、resource stock 自体や technical service potential ではなく、**主体が interval `τ` 内に resource を実際に利用・消費し、その経験に帰属される形で realized した主観的 outcome** を指す。

potential / capability と realized experience を混同しない。resource stock / capability は K として時点観測できるが、それは realized-use outcome そのものではない。

瞬間的な快・満足等の subjective state を観測できるとしても、それ自体を当該 resource の realized-use outcome とはみなさない。

同じ主体・同じ resource・同じ利用量でも、充足状態、順序、文脈、他の経験等により realized outcome は変わりうる。よって一般的な再現性や interval 間の加法性を仮定しない。

```text
actual use over τ=(t0,t1]
        ↓
subjective experience / fulfillment
        ↓
U^use_i(τ) = realized-use outcome
```

離散時間で時点 `t` を考える場合、時点 `t` で直接参照可能なのは前区間までに realized した use outcome である。将来区間の outcome はまだ realized していないため、P_i,t の belief / expectation として表現する。

一般の非加法的 interval outcome から instantaneous rate が自動的に導けるとは仮定しない。瞬間 rate が必要な projection では、別途 cumulative realized-use process `C_i(t)` を定義し、必要な加法性・正則性を満たす場合にのみ、例えば、

```text
u_i(t) = dC_i(t) / dt
```

を導入してよい。

この interval-indexed な時間形式を P/L-like と呼びうるが、会計上の P/L entry と同一視しない。

`use-value quantity` は Marxian category との接続名として用いる。数理・計測上は `realized-use outcome` を優先してよい。VFT-specific realized-use outcome は Marxian use-value と自動的に同一視しない。

### 5.2 exchange-value representation

exchange-value は、resource を他の resource / money との比較関係から共通尺度へ写像した representation である。

exchange-value は point-in-time capital / asset position にも interval transaction / revenue / expense valuation にも現れうる。

異質な resource stock を共通交換尺度で比較・集計した評価は、realized-use outcome ではなく exchange-value representation に属する。

### 5.3 会計アナロジー

VFT は resource capability、realized use experience、exchange-value representation を区別して記述する。この多面的記述は会計的な複数表現を想起させるが、借方・貸方や複式簿記との対応を Core の構造として仮定しない。

---

## 6. P：structured subjective state / decision-time direction

各 `P_i,t` は、belief / expectation、preference / valuation、trust / reputation、norm recognition 等を含む structured subjective state である。

primitive を内部 component ごとに分割することは Core では要求しない。P はどれだけ共有されても主観状態であり、shared P は複数主体の P の共通性・整合性・分布として扱う。

### forecast と evaluation

時点 `t` の decision では、P_i,t の component を役割上区別する。

```text
P_i,t belief / expectation component
        ↓ generates / conditions
Ŷ_i,t(a; I_i,t)

P_i,t preference / valuation component
        ↓ evaluates with projection-specific rules
Ŷ_i,t(a; I_i,t)
        ↓
Γ_i^adm(F_t)

Ŷ_i,t(a; I_i,t) may contain
P̂_i,t1(a)
```

現在の P_i,t が未来の P_i,t1 を予測・評価するという時間方向を持ち、同時点の P が自分自身を循環的に評価する構造を意味しない。

Core の forecast は physical / resource ΔK のみに限定しない。

```text
Y_i^proj(τ)
:= projection-selected outcome bundle
   { ΔK_τ, K_i,t1, U^use_i(τ), P_i,t1, activity outcomes, ... }

Ŷ_i,t(a; I_i,t)
:= forecast of Y_i^proj under candidate action a
```

`ΔK̂_i(a;I_i)` は必要な projection で `Ŷ_i` の resource-state component として使える。

確率構造や causal model を採用する projection では、bundle の各 component を条件付き期待値・分布・causal estimand 等として specialize してよい。Core は probability measure や causal semantics を固定しない。

### 加工・変換と P 更新

同一由来 resource でも、A による加工・変換後には capability / utilization possibility が変わる。ただし加工後の realized-use outcome は加工時点で確定するのではなく、加工後 resource を実際に利用した interval の体験結果として初めて realized する。

---

## 7. A：actor-side action / process record

A は各主体側の action / process record を表す。

生産、消費、交換、投資、労働、移転、契約、政策、探索、学習、情報伝達等を必要な粒度で記述する。interval `τ` 内の actual labor time / hours worked も、必要な labor projection では A / labor measure として記述する。

A は actor-side に限定する。A を通らない K 変化が必要な projection では、`Ω_τ` 等の exogenous / environmental process を別に置く。

### multi-actor event identity / reconciliation

交換・移転・契約等、一つの realized event に複数主体が参加する場合、対応する `A_i` records は shared `event_id` と participant / role relation を持つ。

```text
realized event e
participants(e) = {i, j, ...}
event_id(A_i,e) = event_id(A_j,e) = e
```

shared realized event は actor record の片方を捨てる deduplication ではなく、participant-side records を reconcile / compose して構成する。

```text
E_e^shared
:= reconcile({ A_i,e | i ∈ participants(e) })
```

buyer の受領・支払と seller の引渡・受取のように、同一 event に属する複数 actor-side records は `E_e^shared` 内で保持される。

`deduplicate by event_id` は event count 等、event identity の重複のみを除く特定 aggregation の特殊形である。

`E^shared` は universal state primitive ではなく、multi-actor event identity から構成する derived event view である。

---

## 8. ΔK：endpoint resource-state difference

`ΔK_τ` は endpoint resource-state difference を表し、一般形を projection-defined difference operator `δ_K` で書く。

```text
ΔK_τ := δ_K(K_t0, K_t1)
```

K が additive vector space 等で表現される projection では、特殊形として `δ_K(K_t0,K_t1)=K_t1-K_t0` と置ける。

したがって gross activity と ΔK は別概念である。multi-actor activity の集計では `E^shared` と対象 coordinate に応じた aggregation rule を明示する。

`ΔK` は会計仕訳でもない。

---

## 9. exchange-value residual / surplus / accounting

surplus は physical primitive ではない。

Core-level の中立的な差分を exchange-value residual として、

```text
specified economic changes
        ↓ exchange-value representation
comparable values
        ↓ comparison under a specified boundary
exchange-value residual
```

と記述できる。

surplus / deficit、production surplus、accounting profit / income、valuation gain / wealth change 等は projection-specific な解釈とする。何を対象 change に含めるか、recognition timing、valuation rule、comparison boundary を projection 側で指定する。

### accounting projection

P/L・B/S・複式簿記は Core の普遍因果層ではなく、exchange-value を制度的に記録する formal accounting projection である。

physical/resource events、contract/financial events、valuation-only events 等が recognition / valuation を経て accounting entries を形成しうる。

帳簿そのものは actor-specific であり、external financial reporting / consolidation / statistics は個別帳簿とは別 representation である。

---

## 10. field / business actor / business field

### field

field は、K、(K_i)_i、(P_i)_i と projection-specified relations / constraints から導かれる action-generating configuration である。

```text
F_t
 ↓
Γ_i^feas(F_t)
 ↓
Γ_i^avail(F_t)
 ↓ forecast + rationality rules
Γ_i^adm(F_t)
 ↓ projection-specific selection
A_i
```

### business actor / organization

organization / company を actor として扱う場合、その主体は `i` として K_i / P_i / A_i 等の actor-specific representation を持ちうる。

### business field

`F^biz` は actor-resource transformation / exchange / service / beneficiary relation 等を反復可能にする局所 action-generating configuration とする。

### business

business は `F^biz` を中心として継続する activity system とする。

したがって business actor と business field は同一型ではない。同一 organization が複数 business fields を運営することも、一つの business field が複数 actor にまたがることも許す。

法人格・組織・資産の存在だけでは business existence を定義しない。事業は field level で、顧客・資源・能力・期待・関係・制約が recurring activity を再生産する構造として記述する。

```text
起業           = business-oriented field formation を伴う activity
新規事業開発   = 既存 field から新しい business field を形成・分岐させる activity
既存事業運営   = 成立済み business field の維持・再生産・改善
```

profit / surplus は business existence の定義条件ではない。

---

## 11. 3つの管理合理性公理

VFT の management / decision rationality は、次の3則を**必須の構成公理**として持つ。

1. **resource-realization**：望ましい resource / capital / realized-use outcome の実現
2. **activity-flow**：必要な activity / process の流れを維持・拡張し、必要なら field formation / renewal を行う
3. **P-downside**：projection が指定した将来 P component / action-generating viability の重大な downside を回避する

3公理は `Ŷ_i,t(a;I_i,t)` の outcome components と、projection-specific objective / constraint / threshold / comparison rule を介して `Γ_i^adm` を形成する段階に接続する。

3公理はすべて構成条件であり、任意に採否を選ぶ dimension ではない。一方、その評価・判断・実行は単一 actor に集中する必要はなく、複数 actor、役割、組織階層、制度へ分業・分散してよい。

VFT decision projection を名乗る場合、3公理それぞれについて少なくとも admissibility / exclusion condition または比較規則を ex ante に明示し、観測後の任意行動を事後的に分類するだけのラベルとして使わない。

P-downside は P 全体に universal ordering を仮定しない。

3公理は経験的普遍法則ではない。profit / utility は具体的 decision problem の metric / objective / proxy として使いうる。

---

## 12. 経済学への射影

### plan / forecast

```text
x_i                 = planned / chosen resource change
Ŷ_i,t(a; I_i,t)     = generic forecast of projection-selected outcome bundle
ΔK̂_i(a; I_i)       = optional resource-state component of Ŷ_i
```

budget feasibility は plan / choice 側へ置き、forecast と区別する。

### compatibility / equilibrium / accounting

- compatibility / feasibility：主体間 plan が相互に実行可能であること
- market equilibrium：compatibility に射影先理論の choice / optimality / clearing 等を加えたもの
- accounting consistency：指定 accounting representation の recognition / valuation / identity / closing rule が整合すること
- steady state：対象状態について別途定める動学条件

これらは別概念である。

### Marxian categories

VFT は use-value / labor / exchange-value / surplus / accumulation の区別を一般化構造上で保持する。

- VFT-specific use-value quantity / realized-use outcome：主体が interval 内の実利用を通じて realized した主観的 outcome
- labor measure：interval 内に実際に投入された labor activity / labor time
- Marxian labor-value：socially necessary labor time 等の追加条件を持つ specialization
- exchange-value / price：resource 間の比較・market / monetary valuation
- exchange-value residual / surplus：指定 boundary と exchange-value scale 上の差分
- Marxian surplus value：Marx 固有条件を持つ specialized interpretation
- accumulation：surplus 等の帰属・留保・分配による K_i の変化

VFT-specific use-value quantity は Marxian use-value と自動的に同一視しない。

---

## 13. ミクロ／マクロ接続

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

主体ごとの帳簿そのものが共通化されることは仮定しない。

---

## 14. Core で固定しないもの

- K の標準 resource / capability coordinates
- `δ_K` の標準 difference rule
- institutional / legal state の普遍 primitive
- exogenous / environmental process の標準表現
- realized-use outcome の標準効用関数・代替可能性・加法性・rate representation
- exchange-value / monetary valuation function
- K_i の標準 accounting implementation
- P の標準内部次元・universal ordering
- P の普遍的更新式
- `Γ_i^feas` / `Γ_i^avail` / `Γ_i^adm` の標準生成式
- A の deterministic choice function
- shared event reconciliation の標準 rule
- generic outcome bundle `Y_i^proj` の標準 coordinates
- generic forecast `Ŷ_i` の確率測度・期待形成式・causal semantics
- exchange-value residual の普遍的算出式・対象 economic changes
- 3公理の projection-specific operationalization と actor / role 間の分業形態
- market equilibrium の普遍的条件
- micro-to-macro aggregation rule

---

© T. Nuno  
Licensed under CC BY 4.0