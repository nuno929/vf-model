# 価値場理論 — 既存概念・応用への射影ノート

> この文書は Core 定義ではなく、VFT の K / K_i / P_i / A_i / field を既存経済概念・制度・会計へどう射影するかを整理する。

---

## 1. 基本構造

Core では、

- `K`：resource / capability state
- `K_i`：actor-specific resource state
- `P_i`：未実現関係への credit / reference state
- `A_i`：actor-side activity / action
- `ΔK_i`：interval resource-state change
- `F_t`：action-generating configuration

を区別する。

exchange-value、money、capital valuation、accounting、firm、state 等は原則として derived projection とする。

---

## 2. use-value projection

use-value は resource が use / consumption A を通じて物理的に実現される側として扱う。

```text
resource r
→ A^use / A^consumption
→ realized physical use C_i,r(τ)
```

異種 resource を一つの use-value scale へ還元することは要求しない。

Marxian use-value との接続では、resource が具体的使用において実現されるという構造を保持し、subjective utility maximization を Core 条件にはしない。

---

## 3. exchange-value projection

exchange-value は、resource quantity や exchange activity を指定された comparison relation / common measure へ写像した representation とする。

```text
K_i / A_i
↓ exchange relation / valuation rule
exchange-value representation
```

貨幣以前には resource pair ごとの交換比率として現れうる。

貨幣成立後には、異種 resource / exchange を unit of account 上で比較・集約しやすくなる。

exchange-value は `K_i` 自体ではない。

---

## 4. surplus projection

surplus の基本構造は、required K を満たした後に残る available resource とする。

```text
surplus
= available K - required K
```

required K の境界は projection に依存する。

自給自足でも surplus は成立する。交換が成立すると resource-specific surplus を他 resource へ変換可能になり、貨幣が成立するとその exchangeability をより一般的に保存・計量できる。

money projection で surplus を共通尺度へ写像して集約することはできるが、これは surplus の別種類ではなく representation の変化である。

---

## 5. money projection

money は、

```text
surplus exchangeability の保存
+
shared P の common measure
```

として扱える。

money 自体を P と同一視しない。

価格、残高、交換レート等は observable proxy / reference として P を支持する。

```text
price / balance / exchange rate
→ X
→ P
```

currency field は state field と一致する必要はない。

```text
currency field
≠ necessarily state field
```

---

## 6. banking / credit projection

銀行では、observable record と credit state を分ける。

```text
deposit balance
= observable record / proxy

future withdrawability / settlement availability
= P
```

banking activity は、保管、決済、為替、信用供与等を通じて broader A を成立させる。

credit expansion は current physical K を超える future relation を先行して利用可能にする一方、default、liquidity shortage、run、settlement failure 等の P downside を増幅しうる。

---

## 7. capital projection

VFT では capital を一義的な独立 primitive として置かない。

既存の capital 概念には、現に存在する resource / capability と、その将来価値まで含めた評価が重なっている。

VFT では、

```text
actual / realized capital side
→ K

capital valuation including future value
→ K を基礎に P を含む projection
```

として分離する。

book value、market value、enterprise value 等は K / P そのものではなく、valuation / accounting rule による representation である。

machine capital は physical / productive K の特殊形として、financial capital は monetary / contractual / valuation projection として扱える。

---

## 8. capital accumulation / formation projection

surplus の再投入は capital の定義ではなく accumulation / formation の構造として扱う。

```text
repeated surplus
→ abstract degree of freedom
→ reinvestment
→ K / capability expansion or reconfiguration
→ P update
→ broader A_(t+1)
→ new surplus
```

surplus retention、investment A、productive K の変化、future A expansion を分けて観測する。

---

## 9. accounting projection

P/L・B/S・double-entry bookkeeping は VFT Core の普遍因果層ではない。

formal accounting projection では、physical/resource events、contract / financial events、valuation-only events 等を recognition / valuation rule によって monetary representation へ写像する。

```text
underlying K_i / A_i / relations / P references
↓ recognition / valuation
ledger / B/S / P/L
```

accounting profit / loss は指定された actor boundary、period、recognition、valuation rule に依存する representation である。

---

## 10. P scalar approximation

P の真値・内部構造・次元は直接観測できない。

金融・経済 projection では、観測・比較・集約のために、

```text
P̂_i,t ∈ R
```

という単一スカラー近似を置いてよい。

これは true P が一-dimensional であるという存在論的主張ではない。

価格、資産価値、信用指標、残高等は P そのものではなく、P を推定・参照するための proxy / representation とする。

---

## 11. business / firm projection

organization / company は actor `i` として扱える。

business field は、actor-resource transformation / exchange / service / beneficiary relation 等を反復可能にする local field とする。

```text
business actor / organization
= actor i

business field F^biz
= local action-generating configuration

business
= F^biz を中心として継続する activity system
```

profit maximization は business existence の universal definition ではない。

market share、customer count、transaction volume、distribution coverage 等は `A_(t+1)` の維持・拡張を観測する proxy になりうる。

---

## 12. state / institution projection

制度は ownership、contract、court、sanction、currency rule、custom 等を通じて shared P を安定化し、broader A を成立させる relation structure として扱える。

state は law、policy、security、diplomacy、resource access、infrastructure 等を通じて field を維持・拡張する actor / institutional structure として記述できる。

また state / religion / platform 等には、

```text
A_F
→ ΔP_i
```

という他主体 P への直接介入経路を置ける。

短期的には realized ΔK 前に P を変化させうるが、長期的な P 維持には後続 outcome との整合が必要になる。

---

## 13. platform projection

large platform は ranking、recommendation、rule、certification、account control、payment guarantee 等を通じて、参加 actor の P と A に介入できる。

```text
A_platform
→ P_i
→ A_i
```

platform usage、transaction volume、ecosystem participation 等は field が媒介・組織する A の proxy として扱える。

---

## 14. 3合理性の projection

### resource-realization

expected `ΔK` と realized `ΔK` の差として operationalize できる。

### activity-flow

actor / field に応じて、future action range、transaction volume、market share、participant continuity、resource access 等を proxy にできる。

### P-downside

default、contract failure、trust loss、customer exit、run、institutional breakdown 等を downside event / proxy として扱える。金融・経済 projection で scalar `P̂` を用いる場合は `ΔP̂^-` として近似できる。

3合理性は一つの universal utility function へ還元しない。

---

## 15. Marxian projection

VFT は以下の区別を保持する。

- use-value：resource の具体的使用における realization
- labor：interval activity / labor measure
- exchange-value：resource / exchange の comparative representation
- surplus：required K を超える residual resource / freedom
- accumulation：surplus の retention / reinvestment による future K / A expansion

Marx 固有の labor-value theory / surplus-value theory は socially necessary labor time、production relation 等の追加条件を持つ specialization とする。

---

## 16. micro / macro projection

micro と macro は別 primitive を要求しない。

```text
actor-side K_i / P_i / A_i
↓ shared event reconciliation / aggregation
field-level distributions / activity / concentration / continuity
```

aggregation rule、boundary、unit、event reconciliation は projection ごとに定義する。

金融・経済集計で P を scalar approximation する場合も、それは true P の内部構造を確定するものではない。

---

© T. Nuno  
Licensed under CC BY 4.0
