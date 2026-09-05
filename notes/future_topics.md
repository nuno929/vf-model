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

K_i を B/S そのものとは定義しない。formal accounting projection での実装境界は別途検討する。

---

## 2. use-value / exchange-value

同一 resource の use-value / exchange-value 二重表現を採る。

今後の検討候補：

- realized use-value の utility proxy
- 限界効用逓減をどこまで明示的に置くか
- substitute / complement / use category
- physical stock / capability と realized utility の接続
- exchange-value の comparison scale
- exchange-value の point-in-time / interval representation
- 複式簿記アナロジーの適用範囲

use-value / exchange-value と stock / flow を完全な一対一対応とはしない。

---

## 3. A / ΔK

`ΔK` は endpoint resource-state change とする。

```text
ΔK_[t0,t1] = K_t1 - K_t0
```

今後の検討候補：

- heterogeneous K coordinates の差分定義
- A event history と gross activity の表現
- production / consumption / depreciation / depletion の event semantics
- exogenous change の分離
- partial observability

独立した gross-flow primitive は Core に置かない。

---

## 4. P / forecast

P は structured subjective state とする。

今後の検討候補：

- belief / expectation
- preference / valuation
- trust / reputation
- norm recognition
- shared P の推定
- market outcome を proxy に用いる際の endogeneity
- use-value expectation と realized use-value の更新関係
- `E_i[ΔK | a,I_i]` の causal semantics

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

---

## 7. surplus / accumulation

surplus は physical primitive ではなく、exchange-value の比較可能尺度上で成立する差分 / residual とする。

今後の検討候補：

- comparison / accounting boundary
- recognition timing
- internal transfer elimination
- surplus / profit / income / wealth change の関係
- surplus attribution / retention / distribution
- K_i accumulation dynamics
- valuation rule が surplus に与える差

---

## 8. field

field は action-generating configuration とする。

今後の検討候補：

- field boundary
- actor-resource graph / relation structure
- action inducibility / feasibility の formalization
- field stability / resilience
- field formation / dissolution
- multiple overlapping fields
- organization / business / market / institution の field representation

独立 scalar V や物理学的 field を自動的に仮定しない。

---

## 9. business / entrepreneurship

business entity は、一定の目的・機能に向けた A を継続的に誘発・再生産する局所 field structure とする。

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

今後の検討候補：

- 独立性・完備性・最小性
- 第4の独立合理性が必要になる条件
- projection-specific objective / priority / weight / constraint / threshold
- activity-flow と field formation の関係
- actor / institution / hierarchy 間の機能分担
- empirical falsifiability

---

## 11. Marxian projection

今後の検討候補：

- realized use-value と Marxian use-value の関係
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
- K_i distribution / capital concentration
- shared P と macro demand / investment / credit
- actor-specific ledger → reporting / statistical representation
- field formation / dissolution の macro dynamics
- policy A → field / P / K / K_i への経路

---

## 13. 実証・計量化

- physical K / ΔK measurement
- A event history
- realized use-value measurement
- exchange-value measurement
- K_i measurement
- P / shared P proxy
- surplus / accumulation measurement
- field continuity / formation proxy
- labor-time measurement
- 3則の projection-specific estimation
- micro / macro reporting consistency

---

© T. Nuno  
Licensed under CC BY 4.0