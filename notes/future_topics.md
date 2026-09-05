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

K_i を B/S そのものとは定義しない。formal accounting projection での実装境界は別途検討する。

---

## 2. use-value / exchange-value

VFT-specific use-value quantity は interval-indexed realized outcome として、exchange-value は比較可能な representation として扱う。

今後の検討候補：

- realized use-value の utility / experience proxy
- resource-use episode への attribution rule
- path dependence / sequence dependence
- interval 間の非加法性をどのように扱うか
- 瞬間的 use-value rate を極限・微分的表現として導入する必要性
- 限界効用逓減をどこまで明示的に置くか
- substitute / complement / use category
- physical stock / capability と realized utility の接続
- exchange-value の comparison scale
- exchange-value の point-in-time / interval representation
- P/L-like analogy の適用範囲

use-value / exchange-value と stock / flow を完全な一対一対応とはしない。ただし VFT-specific use-value quantity は point-in-time stock ではなく interval realization として定義する。

---

## 3. A / ΔK / exogenous change

Core では、

```text
ΔK_τ := δ_K(K_t0,K_t1)
```

とし、`δ_K` を projection-defined difference operator とする。

additive vector projection では `K_t1-K_t0` を特殊形として使える。

今後の検討候補：

- heterogeneous K coordinates に対する `δ_K` の標準候補
- A event history と gross activity の表現
- production / consumption / depreciation / depletion の event semantics
- `Ω_τ` 等の exogenous / environmental process の標準化要否
- A と Ω の識別
- partial observability

独立した gross-flow primitive は Core に置かない。

---

## 4. P / forecast

P は structured subjective state とする。

Core の generic forecast は `ΔK̂_i(a;I_i)` とし、probability measure / causal semantics は固定しない。

今後の検討候補：

- belief / expectation
- preference / valuation
- trust / reputation
- norm recognition
- shared P の推定
- market outcome を proxy に用いる際の endogeneity
- use-value expectation と realized use-value の更新関係
- generic forecast の確率的 specialization
- `do(a)` 等を用いた causal specialization

必要なら P の内部 component を projection-specific に明示するが、Core primitive の分割は必須としない。

---

## 5. institutional / legal state

契約・制度・法的権利関係を physical K に押し込まない。

今後の検討候補：

- `C_t` 等の projection-local institutional state
- contract / claim / legal status の event/state representation
- enforcement / default / recognition
- institutional state → P / A / K_i への作用

Core の普遍 primitive とする必要性は未確定。

---

## 6. accounting projection

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
- statistical transformation

use-value の P/L-like 性は時間形式のアナロジーに限定し、formal accounting projection と混同しない。

---

## 7. surplus / accumulation

surplus は physical primitive ではなく、specified economic changes を exchange-value scale へ写像し、specified comparison boundary の下で定義する差分 / residual とする。

今後の検討候補：

- 対象 economic changes の選択規則
- comparison / accounting boundary
- recognition timing
- internal transfer elimination
- production surplus / profit / income / valuation gain / wealth change の関係
- surplus attribution / retention / distribution
- K_i accumulation dynamics
- valuation rule が surplus に与える差

---

## 8. field

field は K / K_i / P_i と projection-specified relations / constraints から導かれる action-generating configuration とする。

Core では必要に応じて、

```text
F_t := configuration(...)
Γ_i(F_t) := feasible / inducible action correspondence
```

という derived notation を使える。

今後の検討候補：

- field boundary
- actor-resource graph / relation structure
- `Γ_i` の formalization
- action inducibility と feasibility の識別
- field stability / resilience
- field formation / dissolution
- multiple overlapping fields
- organization / business / market / institution の field representation

独立 scalar V や物理学的 field を自動的に仮定しない。

---

## 9. business / entrepreneurship

business entity は、一定の目的・機能に向けた A を継続的に誘発・再生産する局所 field structure とする。

起業は business-oriented field formation の一類型とする。

今後の検討候補：

- business boundary
- recurring action set
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

Core では、resource-realization に realized-use outcome を含め、P-downside は universal ordering ではなく projection-specific viability criterion によって定める。

今後の検討候補：

- 独立性・完備性・最小性
- 第4の独立合理性が必要になる条件
- resource / capital / realized-use outcome の関係
- projection-specific objective / priority / weight / constraint / threshold
- P-downside の loss / viability functional
- activity-flow と field formation の関係
- actor / institution / hierarchy 間の機能分担
- empirical falsifiability

---

## 11. Marxian projection

今後の検討候補：

- VFT-specific realized use-value と Marxian use-value の関係
- labor activity / labor time
- socially necessary labor time
- direct / indirect labor
- exchange-value / price
- generic surplus と Marxian surplus value の差
- reproduction / accumulation

---

## 12. ミクロ／マクロ

今後の検討候補：

- micro A histories → macro physical aggregate
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
- A event history
- exogenous Ω measurement where required
- realized use-value / attribution measurement
- exchange-value measurement
- K_i measurement
- P / shared P proxy
- generic forecast `ΔK̂` estimation
- surplus / accumulation measurement
- field continuity / `Γ_i` proxy
- P-downside viability criterion estimation
- labor-time measurement
- 3則の projection-specific estimation
- micro / macro reporting consistency

---

© T. Nuno  
Licensed under CC BY 4.0