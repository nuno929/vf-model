# 価値場理論 — 拡張・再検討ノート

> この文書は Core 定義ではなく、今後の展望・具体化候補・再検討事項を保存する。

## 1. K / K_i

Core では、K は real-resource / capability state、K_i は actor-specific exchange-value / capital representation とする。

時間関連 coordinate は、

- calendar time `t`：model index
- available time budget / remaining workable capacity：K_t coordinate
- actual labor time / hours worked during `τ`：A / labor measure

と区別する。

今後の検討候補：

- K の標準 resource / capability coordinates
- physical resource と capability coordinate の境界
- available-time resource / labor-capacity coordinate の形式化
- ownership / holding / attribution の形式化
- joint ownership / overlapping attribution
- K_i の vector / object representation
- book value / market value / replacement value の関係
- financial asset / liability position の表現
- P_i valuation と K_i valuation の empirical discrimination

K_i を B/S そのものとは定義しない。

---

## 2. realized-use outcome / exchange-value

VFT-specific realized-use outcome は interval-indexed outcome、exchange-value は比較可能な representation として扱う。

今後の検討候補：

- realized-use outcome の utility / experience proxy
- resource-use episode への attribution rule
- path dependence / sequence dependence
- interval 間の非加法性
- substitute / complement / use category
- resource capability と realized use の接続
- exchange-value の comparison scale
- exchange-value の point-in-time / interval representation
- VFT-specific realized-use outcome と Marxian use-value の関係
- P/L-like analogy の適用範囲

### instantaneous rate

一般の non-additive interval outcome から rate を自動導出しない。

今後の検討候補：

- cumulative realized-use process `C_i(t)` を導入する必要性
- `C_i(t)` の加法性 / absolute continuity 等の正則性条件
- rate representation が必要になる projection
- interval outcome と instantaneous state / rate の識別

---

## 3. A / shared event / ΔK / exogenous change

Core では actor-side A records と multi-actor shared event identity を区別する。

```text
E_e^shared
:= reconcile({ A_i,e | i ∈ participants(e) })
```

`E^shared` は derived view であり universal state primitive ではない。

実際に投入された labor time / hours worked も、必要な labor projection では A / labor measure の interval activity とする。

今後の検討候補：

- A record の標準 schema
- event identity / participant / role semantics
- participant-side records の reconciliation rule
- partial participation / nested event
- transaction / contract / policy event の identity rule
- event-count deduplication と resource-flow aggregation の分離
- cross-system event reconciliation
- heterogeneous K coordinates に対する `δ_K` の標準候補
- `Ω_τ` 等の exogenous / environmental process の標準化要否
- A と Ω の識別
- partial observability

---

## 4. field / feasibility / availability / admissibility

field は K / K_i / P_i と projection-specified relations / constraints から導かれる action-generating configuration とする。

```text
Γ_i^feas(F_t)  := feasible action set
Γ_i^avail(F_t) := cognitively / behaviorally available action set
Γ_i^adm(F_t)   := admissible action set

Γ_i^adm ⊆ Γ_i^avail ⊆ Γ_i^feas
```

今後の検討候補：

- field boundary
- actor-resource graph / relation structure
- `Γ_i^feas` の formalization
- `Γ_i^avail` の formalization
- consideration-set / option-awareness model との接続
- `Γ_i^adm` の admissibility / exclusion rule
- final choice / intention state を Core 外でどう表すか
- feasibility / availability / admissibility の empirical discrimination
- field stability / resilience
- field formation / dissolution
- multiple overlapping fields
- organization / business / market / institution の field representation

---

## 5. P / outcome forecast / evaluation

P は structured subjective state とする。

Core の generic forecast は、

```text
Y_i^proj(τ) := projection-selected outcome bundle
Ŷ_i,t(a;I_i,t) := forecast of Y_i^proj under candidate action a
```

とする。

今後の検討候補：

- outcome bundle の coordinate selection rule
- ΔK / K_i / realized use / P / activity outcome の dependency
- current P belief / expectation component の形式化
- current P preference / valuation component の形式化
- forecast generation と evaluation の empirical discrimination
- forecasted future `P̂_i,t1(a)` の扱い
- shared P の推定
- forecast horizon / information set
- probabilistic / distributional forecast
- causal specialization
- forecast calibration / uncertainty

P primitive を分割する必要性は未確定だが、decision-time の役割差は明示する。

---

## 6. institutional / legal state

契約・制度・法的権利関係を K に押し込まない。

今後の検討候補：

- projection-local institutional state
- contract / claim / legal status の event/state representation
- enforcement / default / recognition
- institutional state → feasibility / P / A / K_i への作用

Core の普遍 primitive とする必要性は未確定。

---

## 7. accounting projection

P/L・B/S・複式簿記は Core の普遍因果層ではなく formal accounting projection とする。

今後の検討候補：

- physical/resource events
- contract / financial events
- valuation-only events
- recognition timing
- ledger state
- P/L / B/S identities
- actor-specific ledger と external reporting の関係
- consolidation / elimination
- shared event reconciliation と accounting entry identity の関係
- statistical transformation

---

## 8. exchange-value residual / surplus / accumulation

Core-level の中立的差分を exchange-value residual として記述し、surplus / deficit 等は projection-specific な経済的解釈として扱える。

今後の検討候補：

- 対象 economic changes の選択規則
- comparison / accounting boundary
- recognition timing
- internal transfer elimination
- shared event reconciliation
- production surplus / profit / income / valuation gain / wealth change の関係
- surplus attribution / retention / distribution
- K_i accumulation dynamics
- valuation rule が residual に与える差

---

## 9. business actor / business field / entrepreneurship

Core では business actor と business field を別型として扱う。

```text
business actor / organization = actor i
business field F^biz          = actor-resource transformation / exchange / service / beneficiary relation 等を反復可能にする local field
business                      = F^biz を中心とする activity system
```

今後の検討候補：

- organization / actor boundary
- business field boundary
- actor-field membership / control relation
- 一法人・複数 business fields
- 複数 actor・単一 business field
- recurring action set
- resource replenishment
- participant / customer / beneficiary relations
- field formation threshold
- 起業と新規事業開発の識別
- existing-business optimization と field formation の差
- business field persistence / death
- NPO / public business / state business への適用

profit maximization は business existence の普遍定義とはしない。

---

## 10. 3つの管理合理性公理

resource-realization / activity-flow / P-downside の3公理は、VFT の management / decision rationality における必須構成条件とする。

Core では3公理すべてを `Ŷ_i,t(a;I_i,t)` の outcome components と projection-specific comparison / admissibility rules に接続し、`Γ_i^adm` を形成する段階へ置く。

3公理の評価・判断・実行は単一 actor に集中する必要はなく、複数 actor、役割、組織階層、制度へ分業・分散してよい。

今後の検討候補：

- 3公理の独立性・最小性・非還元性
- 第4の独立公理が必要になる条件
- resource / capital / realized-use outcome の関係
- objective / priority / weight / constraint / threshold
- P-downside の loss / viability functional
- activity-flow と field formation の関係
- 各公理の exclusion / comparison rule
- dominance / admissibility rule の候補
- empirical falsifiability
- actor / institution / hierarchy 間の機能分担

公理として置くこと自体は維持し、今後の検討対象はその具体的 operationalization、独立性、非還元性とする。

---

## 11. Marxian projection

今後の検討候補：

- VFT-specific realized-use outcome と Marxian use-value の関係
- labor activity / labor time
- socially necessary labor time
- direct / indirect labor
- exchange-value / price
- exchange-value residual と Marxian surplus value の差
- reproduction / accumulation

---

## 12. ミクロ／マクロ

今後の検討候補：

- actor-side A records → reconciled shared events
- shared events → macro physical / resource aggregates
- event identity の cross-system reconciliation
- exogenous process Ω の macro treatment
- K_i distribution / capital concentration
- shared P と macro demand / investment / credit
- actor-specific ledger → reporting / statistical representation
- field formation / dissolution の macro dynamics
- policy A → field / P / K / K_i への経路

---

## 13. 実証・計量化

- real-resource / capability K measurement
- available time / labor-capacity measurement
- actual labor-time interval measurement
- projection-defined `δ_K` measurement
- `Γ^feas` / `Γ^avail` / `Γ^adm` operationalization
- actor-side A records
- shared event identity / reconciliation
- exogenous Ω measurement where required
- realized-use / attribution measurement
- optional cumulative process `C_i(t)` / rate estimation
- exchange-value measurement
- K_i measurement
- P / shared P proxy
- current belief / valuation role discrimination
- generic outcome bundle `Y_i^proj`
- generic forecast `Ŷ_i` estimation
- exchange-value residual / surplus measurement
- business actor / business field boundary measurement
- field continuity / formation proxy
- 3公理それぞれの operationalization
- actor / role 間の rationality-function division of labor
- P-downside viability criterion estimation
- labor-time measurement
- micro / macro reporting consistency

---

© T. Nuno  
Licensed under CC BY 4.0