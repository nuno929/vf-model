# 価値場理論 — 拡張・再検討ノート

> この文書は Core 定義ではなく、今後の展望・具体化候補・再検討事項を保存する。

## 1. K / K_i

Core では、K は physical / real-resource state、K_i は actor-specific exchange-value / capital representation とする。

今後の検討候補：

- K の標準 resource coordinates
- ownership / holding / attribution の形式化
- joint ownership / overlapping attribution
- K_i の vector / object representation
- book value / market value / replacement value の関係
- financial asset / liability position の表現
- P_i valuation と K_i valuation の empirical discrimination

K_i を B/S そのものとは定義しない。

---

## 2. use-value / exchange-value

VFT-specific use-value quantity は interval-indexed realized outcome として、exchange-value は比較可能な representation として扱う。

今後の検討候補：

- realized-use outcome の utility / experience proxy
- resource-use episode への attribution rule
- path dependence / sequence dependence
- interval 間の非加法性
- 瞬間的 use-value rate の微分的表現
- substitute / complement / use category
- physical stock / capability と realized use の接続
- exchange-value の comparison scale
- exchange-value の point-in-time / interval representation
- VFT-specific use-value と Marxian use-value の関係
- P/L-like analogy の適用範囲

---

## 3. A / shared event / ΔK / exogenous change

Core では actor-side A records と multi-actor shared event identity を区別する。

```text
event_id(A_i) = event_id(A_j) = e
E_τ^shared := deduplicate( ⋃_i A_i,τ , by = event_id )
```

`E_τ^shared` は derived view であり universal state primitive ではない。

`ΔK_τ := δ_K(K_t0,K_t1)` とし、`δ_K` を projection-defined difference operator とする。

今後の検討候補：

- A record の標準 schema
- event identity / participant / role semantics
- partial participation / nested event
- transaction / contract / policy event の identity rule
- macro aggregation における deduplication
- heterogeneous K coordinates に対する `δ_K` の標準候補
- `Ω_τ` 等の exogenous / environmental process の標準化要否
- A と Ω の識別
- partial observability

---

## 4. field / feasibility / inducibility

field は K / K_i / P_i と projection-specified relations / constraints から導かれる action-generating configuration とする。

```text
F_t := configuration(...)
Γ_i^feas(F_t) := feasible action set
Γ_i^ind(F_t)  := inducible / behaviorally available action set
Γ_i^ind(F_t) ⊆ Γ_i^feas(F_t)
```

今後の検討候補：

- field boundary
- actor-resource graph / relation structure
- `Γ_i^feas` の formalization
- `Γ_i^ind` の formalization
- feasibility と behavioral availability の empirical discrimination
- consideration-set / choice-set models との接続
- field stability / resilience
- field formation / dissolution
- multiple overlapping fields
- organization / business / market / institution の field representation

`Γ_i^ind` は realized action を見て事後的に定義しない。

---

## 5. P / outcome forecast

P は structured subjective state とする。

Core の generic forecast は、

```text
Y_i^proj(τ) := projection-selected outcome bundle
Ŷ_i(a;I_i)  := forecast of Y_i^proj under candidate action a
```

とする。

今後の検討候補：

- outcome bundle の coordinate selection rule
- ΔK / K_i / realized use / P / activity outcome の dependency
- belief / expectation component の形式化
- shared P の推定
- forecast horizon / information set
- probabilistic forecast / distributional forecast
- causal specialization
- forecast calibration / uncertainty
- forecast と preference / desirability の分離

Core は outcome bundle の標準 coordinates、probability measure、causal semantics を固定しない。

---

## 6. institutional / legal state

契約・制度・法的権利関係を physical K に押し込まない。

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
- shared event identity と accounting entry identity の関係
- statistical transformation

---

## 8. exchange-value residual / surplus / accumulation

Core-level の中立的差分を exchange-value residual として記述し、surplus / deficit 等は projection-specific な経済的解釈として扱える。

今後の検討候補：

- 対象 economic changes の選択規則
- comparison / accounting boundary
- recognition timing
- internal transfer elimination
- shared event deduplication
- production surplus / profit / income / valuation gain / wealth change の関係
- surplus attribution / retention / distribution
- K_i accumulation dynamics
- valuation rule が residual に与える差

---

## 9. business / entrepreneurship

business entity は、一定の目的・機能に向けた A を継続的に誘発・再生産する局所 field structure とする。

起業は business-oriented field formation の一類型とする。

今後の検討候補：

- business boundary
- recurring action set
- feasible / inducible action range
- activity continuity
- resource replenishment
- participant / customer / beneficiary relations
- field formation threshold
- 起業と新規事業開発の識別
- existing-business optimization と field formation の差
- NPO / public business / state business への適用

profit maximization は business existence の普遍定義とはしない。

---

## 10. 3つの管理合理性公理

3則は constitutive rationality assumptions とする。

Core では各 dimension を `Ŷ_i(a;I_i)` の outcome components と projection-specific comparison / admissibility rules に接続する。

今後の検討候補：

- 独立性・完備性・最小性
- 第4の独立合理性が必要になる条件
- resource / capital / realized-use outcome の関係
- objective / priority / weight / constraint / threshold
- P-downside の loss / viability functional
- activity-flow と field formation の関係
- dimension ごとの exclusion condition
- dominance / admissibility rule の候補
- empirical falsifiability
- actor / institution / hierarchy 間の機能分担

「axiom / constitutive assumption」という名称自体の再検討は、独立性・排除条件の形式化後に行う。

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

- actor-side A records → shared realized events
- shared events → macro physical aggregate
- event identity の cross-system reconciliation
- exogenous process Ω の macro treatment
- K_i distribution / capital concentration
- shared P と macro demand / investment / credit
- actor-specific ledger → reporting / statistical representation
- field formation / dissolution の macro dynamics
- policy A → field / P / K / K_i への経路

---

## 13. 実証・計量化

- physical K measurement
- projection-defined `δ_K` measurement
- `Γ^feas` / `Γ^ind` operationalization
- actor-side A records
- shared event identity / deduplication
- exogenous Ω measurement where required
- realized-use / attribution measurement
- exchange-value measurement
- K_i measurement
- P / shared P proxy
- generic outcome bundle `Y_i^proj`
- generic forecast `Ŷ_i` estimation
- exchange-value residual / surplus measurement
- field continuity / formation proxy
- P-downside viability criterion estimation
- rationality-dimension exclusion rule estimation
- labor-time measurement
- micro / macro reporting consistency

---

© T. Nuno  
Licensed under CC BY 4.0