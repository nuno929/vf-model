# 価値場理論 — 計測

## 1. 目的

本書は VFT Core を実証・観測へ落とす際の境界を整理する。

計測上は、

- resource state `K`
- actor-specific resource state `K_i`
- actor-side activity `A_i`
- unrealized relation に対する credit / reference state `P_i`
- P を支える observable proxy `X_i`
- interval resource change `ΔK_i`
- use / consumption の physical realization
- surplus と future activity freedom
- capital valuation / accumulation の projection
- 3つの管理合理性

を区別する。

---

## 2. K / K_i の観測

### 2.1 K

K は対象系に存在する resource / capability state である。

候補 observable には、原材料量、製品量、設備、稼働可能 capacity、energy、土地、available time、技能・人的能力等がある。

resource coordinate と単位は projection ごとに定める。

### 2.2 K_i

`K_i,t` は actor `i` に帰属する resource position である。

計測では少なくとも、

1. actor
2. resource coordinate
3. quantity / unit
4. attribution / ownership / access rule
5. observation time

を明示する。

区間 `τ=(t0,t1]` に対して、

```text
ΔK_i(τ)
:= δ_K(K_i,t0, K_i,t1)
```

を観測する。

additive representation では、

```text
ΔK_i(τ)
= K_i,t1 - K_i,t0
```

を使える。

### 2.3 gross flow との区別

`ΔK_i` は net resource-state change であり、production / consumption / exchange / transfer 等の gross activity とは異なる。

区間内の gross activity は `A_i,τ` を用いる。

---

## 3. A の観測

A は actor-side activity / process record として観測する。

候補：

- production
- consumption / use
- labor
- exchange
- transfer
- investment
- contract
- payment
- search / learning
- policy / institutional action

multi-actor event では shared event identity を持たせる。

```text
event_id(A_i,e) = event_id(A_j,e) = e
participants(e) = {i,j,...}
```

必要な分析では participant-side records を reconcile / compose した `E_e^shared` を作る。

```text
E_e^shared
:= reconcile({ A_i,e | i ∈ participants(e) })
```

---

## 4. 使用価値の観測

使用価値は resource が use / consumption A を通じて物理的にどの程度利用されたかとして観測する。

```text
resource K
↓
A^use / A^consumption
↓
physical realization
```

resource `r` の interval `τ` における realized use を、

```text
C_i,r(τ)
= actor i が τ 内に resource r を実際に使用・消費した量
```

として記録できる。

例：

- food：kg consumed
- electricity：kWh used
- machine：operating hours / output
- land：utilized area / period

異種 resource を一つの use-value scale へ還元することは要求しない。

subjective satisfaction / utility を観測する場合は別の projection として追加する。

---

## 5. surplus の観測

単純な projection では、actor `i` の surplus を、

```text
S_i,t
= K_i,t^available - K_i,t^required
```

として表せる。

`required` は生存、維持、再生産等、対象 projection が指定する基準である。

重要なのは単一時点の surplus 量だけではなく、**surplus が反復的に生成されているか**である。

観測候補：

- repeated surplus amount
- surplus persistence
- required K に対する余裕率
- surplus の用途分布
- surplus から新たに選択された A

反復的 surplus が future A の選択余地をどの程度広げるかを、projection ごとに activity range / option count / resource-allocation freedom 等で operationalize できる。

---

## 6. P / X の観測

P は直接 observable ではない。

P の真値・内部構造・次元は不明であり、observable / reference proxy を、

```text
X_i,t = {x_i,t,1, ..., x_i,t,n}
```

として扱う。

候補 proxy：

- past production / consumption realization
- exchange history
- price / exchange rate
- deposit balance
- contract performance
- default history
- rating / reputation indicator
- institutional continuity
- stated expectation / trust survey

観測上は、

```text
realized outcome
→ X_i,t
→ estimated P_i,t
```

という関係を置くことができる。

金融・経済 projection では、観測と集約を単純化するため、

```text
P̂_i,t ∈ R
```

という scalar approximation を置いてよい。

これは true P が本質的に一-dimensional であることを意味しない。P の真値や標準推定式は Core では固定しない。

shared P は actor set 上の共通性・分布・整合性として推定する。

---

## 7. expected ΔK / realized ΔK

resource-realization を観測する場合、candidate A に対して主体が期待した resource outcome と realized outcome を区別する。

```text
candidate A
↓
expected ΔK_i(a)
↓ execution
realized ΔK_i
```

計測では少なくとも、

1. candidate / chosen A
2. expectation timing
3. expected resource coordinates
4. expected amount / range / distribution
5. realized amount
6. forecast horizon

を明示する。

最も単純には、

```text
E_i(τ)
= distance(expected ΔK_i, realized ΔK_i)
```

のような予実差を projection-specific metric として置ける。

Core は distance function を固定しない。

---

## 8. activity-flow の観測

activity-flow は現在の activity amount ではなく、次期にも成立可能な `A_(t+1)` の維持・拡張を対象とする。

operationalization 候補：

- feasible / available action count
- action-space volume
- activity range
- recurring activity count
- participant retention
- customer / supplier / partner continuity
- market share
- transaction volume
- platform usage
- resource access range
- strategic options

どれを使うかは actor / field / projection に依存する。

単一の universal metric は置かない。

---

## 9. P-downside の観測

P-downside は、将来 A の成立を支える信用・期待・関係に生じる重大な毀損を対象とする。

候補 observable / proxy：

- default
- liquidity shortage
- contract failure
- customer / partner exit
- reputation decline
- institutional trust decline
- withdrawal / run
- relationship discontinuation

projection ごとに、

1. 対象 P projection / proxy
2. viability threshold
3. downside event
4. observation horizon

を定める。

金融・経済 projection で scalar `P̂` を用いる場合には `ΔP̂^-` として近似してよいが、P の真の内部構造を前提とはしない。

---

## 10. 3合理性の同時観測

3合理性は別々に観測し、単一スカラーへ強制的に集約しない。

```text
resource-realization
→ expected / realized ΔK difference

activity-flow
→ future A viability / range / mass

P-downside
→ credit / relation downside risk
```

実証では、それぞれが改善・悪化する組み合わせを見ることで、3合理性間の trade-off を観測できる。

例：

```text
A expansion ↑
forecast error ↑
P downside risk ↑
```

のような組み合わせを、単一 utility の失敗ではなく複数合理性の競合として扱う。

---

## 11. field / action-stage の観測

必要な projection では、

```text
F_t := configuration(...)
Γ_i^feas(F_t)
Γ_i^avail(F_t)
Γ_i^adm(F_t)
```

を operationalize する。

### Γ^feas

候補：physical capacity、resource availability、legal permission、technical compatibility 等。

### Γ^avail

候補：recognized options、consideration set、reachable alternatives、option awareness 等。

### Γ^adm

候補：organizational decision rule、threshold、exclusion condition、comparison rule 等。

これらは realized action を見て事後的に定義するのではなく、可能な限り action realization 前の情報から構成する。

---

## 12. exchange-value / capital valuation / accounting projection

exchange-value は K_i そのものではない。

resource quantity や exchange activity を、指定された common exchange measure / unit of account へ写像した representation として扱う。

```text
K_i / A_i
↓ valuation / exchange mapping
exchange-value representation
```

money が成立した projection では、異種 resource / exchange を共通単位で比較・集約しやすくなる。

capital valuation を行う場合も、actual resource / capability 側の K と、未実現の将来価値・信用側の P を区別する。

```text
actual capital side
→ K

valuation including future value
→ K + P を参照する projection
```

book value、market value、enterprise value 等は projection-specific representation である。

formal accounting を用いる場合、B/S・P/L・複式簿記は制度的な recognition / valuation / reporting rule を持つ projection とする。

---

## 13. capital accumulation の観測

capital accumulation / formation を扱う場合は、capital という一義的 stock を新たに置くのではなく、surplus の再投入とその結果を見る。

```text
repeated surplus
→ reinvestment A
→ ΔK / K reconfiguration
→ P update
→ future A expansion
```

観測候補：

- surplus retention
- reinvestment amount / destination
- productive K / capability の増減
- future activity range / volume の変化
- reinvestment 後の P proxy / scalar approximation の変化

---

## 14. 制度主体による P 介入の観測

国家・宗教・platform 等について、

```text
A_F
→ ΔP_i
→ ΔA_i
```

の経路を観測できる。

候補 event：

- policy announcement
- legal change
- guarantee / sanction
- certification
- ranking / recommendation change
- platform suspension

即時的な P proxy の変化と、その後の A / ΔK の変化を分けて観測する。

---

## 15. 実証時に最低限明示するもの

1. actor set / field boundary
2. K / K_i の resource coordinates と単位
3. attribution / access rule
4. interval definition
5. `δ_K` / ΔK measurement rule
6. A record unit / event identity
7. use / consumption quantity
8. required K / surplus definition
9. P proxy `X`
10. P を scalar approximation する場合の推定ルール
11. expected ΔK の observation timing
12. resource-realization metric
13. `A_(t+1)` operationalization
14. P-downside criterion
15. exchange-value / capital valuation mapping を使う場合の unit / valuation rule
16. accounting projection を使う場合の recognition rule
17. missingness / measurement error / aggregation rule

---

© T. Nuno  
Licensed under CC BY 4.0
