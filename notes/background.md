# 価値場理論 — 背景と整理の経緯

> この文書は理論コアではなく、価値場理論が現在の K / K_i / P / A / field 構造へ至るまでの整理経緯を保存する履歴ノートである。現行定義は README / Model Notes / Measurement / Projections を優先する。

---

## 1. field の責務分離

初期には独立した価値場変数を置く案もあったが、現行では field を独立スカラーとはしない。

```text
F_t
= configuration(K_t, (K_i,t)_i, (P_i,t)_i ; relations / constraints)
```

field は、ある時点でどの A が成立しうるかを規定する action-generating configuration とする。

必要な projection では、

```text
Γ_i^feas
Γ_i^avail
Γ_i^adm
```

へ分け、physical / institutional feasibility、behavioral availability、decision-time admissibility を区別する。

---

## 2. K / K_i の整理

途中では `K_i` を actor-specific exchange-value / capital representation として扱った。

しかし経済発展系列を自給自足から通す過程で、resource quantity 自体と exchange-value representation を同じ記号へ載せる必要はないと整理した。

現行では、

- `K`：対象系の resource / capability state
- `K_i`：actor `i` に帰属する resource state

とする。

exchange-value、monetary valuation、accounting representation は `K_i / A_i` を共通交換尺度へ写像する projection として分離する。

K_i は基本的に stock として扱い、区間差分 `ΔK_i` と actor-side activity `A_i,τ` によって flow を記述する。

---

## 3. 使用価値の整理

一時期、VFT-specific use-value を subjective realized experience として厳密化した。

しかし今回の整理では、使用価値について必要なのは、resource が use / consumption A を通じて物理的にどのように実現されるかを区別することであるとした。

```text
resource K
→ use / consumption A
→ physical realization
```

subjective satisfaction / utility は必要な projection で追加できるが、use-value の Core 定義には含めない。

異種 resource を一つの use-value scale へ還元することも要求しない。

---

## 4. P と X

P は、未実現 relation / outcome が成立すると actor が信用し、現在参照している非物理的状態として整理した。

price、balance、contract amount、rating 等の observable 自体を P としない。

```text
realized outcomes
→ observable proxies X
→ P
→ A
```

P の真値・内部構造・次元は直接観測できない。

一方、金融・経済分析では観測と集約の単純化のため、P を単一スカラーへ近似してよい。

```text
P̂_i,t ∈ R
```

これは true P が本質的に一-dimensional であることを意味しない。

経済発展に伴う複雑化は、P primitive を際限なく増やすよりも、P を支える proxy / relation の増加として捉える。

---

## 5. A / shared event / ΔK

A は actor-side activity / process record とする。

multi-actor event では shared `event_id` と participant / role relation を持たせ、participant-side records を reconcile / compose して shared event view を構成する。

```text
E_e^shared
:= reconcile({ A_i,e | i ∈ participants(e) })
```

`ΔK` は resource-state endpoint difference であり、gross activity や accounting entry とは区別する。

---

## 6. surplus の整理

以前は physical surplus、exchange residual、profit 等を別々に強く型分けする方向があった。

現在は、surplus の基本構造を、required K を満たした後に残る available K として置く。

```text
surplus
= available K - required K
```

重要なのは単発の余りではなく、surplus が反復的に生成されることである。

反復 surplus は、次期 A を required reproduction のみに拘束しない abstract degree of freedom を生む。

交換はその自由度を他 resource へ変換可能にし、貨幣はさらに一般的な exchangeability / common measure として保存する。

---

## 7. 資本概念の分離

既存の「資本」という語には、現に存在する resource / capability と、その将来価値まで含めた評価が重なっている。

VFT では capital を独立した一義的 primitive として置かず、

```text
actual / realized capital side
→ K

capital valuation including future value
→ K を基礎に P を含む projection
```

として分離する。

簿価、時価、企業価値等は K / P そのものではなく、valuation / accounting rule による representation とする。

また、surplus が生む自由度を future K / A の拡張へ再投入する反復は、capital そのものの定義ではなく accumulation / formation の構造として扱う。

---

## 8. 3つの管理合理性

現行整理では、管理・意思決定に次の3合理性が反復して現れる。

```text
resource-realization
= expected ΔK と realized ΔK の予実一致

activity-flow
= A_(t+1) の維持・拡張

P-downside
= 将来 A を支える P の重大な毀損回避
```

これらを単一目的関数へ還元しない。

A の選別は第4の独立合理性ではなく、3合理性の競合結果として生じると整理した。

危機・停滞・失敗も、単なる非合理性ではなく、3合理性を同時に満たせない構造として説明できる可能性がある。

---

## 9. 経済発展系列

現行 VFT は、

```text
autarky
→ division of labour
→ exchange
→ money
→ banking / credit
→ machine capital
→ capital accumulation
→ institution / state / platform
```

を historical inevitability ではなく logical construction / successive model extension として扱う。

各段階で新 primitive を増やすことより、

- relation の追加
- P を支える proxy の増加
- exchangeability の抽象化
- A_(t+1) の拡張

として説明できるかを優先する。

---

## 10. 制度主体による P への直接介入

通常の循環では realized outcome が P を更新するが、国家・宗教・platform 等には、

```text
A_F
→ ΔP_i
```

という他主体 P への直接介入経路を置ける。

ただし長期的に P を維持するには、その後の realized outcome との整合が必要になる。

制度的 A は信用の先行形成、realized ΔK は事後検証として区別する。

---

## 11. 既存理論との関係

VFT は既存理論を一つに合成するものではなく、部分構造を K / K_i / P / A / field 上へ再配置する。

Marxian categories の一部は明示的に参照する一方、Sen、Simon / Cyert & March、managerial theories、Anthony、North / Coase、Keynes、Minsky、control theory、REA 等は接続候補・比較対象として分離して整理する。

詳細は `notes/theoretical_connections.md` を参照する。

---

© T. Nuno  
Licensed under CC BY 4.0
