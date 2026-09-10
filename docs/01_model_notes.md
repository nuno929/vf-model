# 価値場理論 — モデルノート

## 1. 目的

本ノートは、価値場理論（Value-Field Theory; VFT）の Core を README より形式的に整理する。

VFT は、resource state `K`、actor-specific resource state `K_i`、unrealized relation に対する credit / reference state `P_i`、actor-side activity `A_i` の関係として経済・事業活動を記述する。

制度カテゴリーは原則として primitive に置かず、これらと field relation の組み合わせから derived structure として記述する。

---

## 2. Core state / process

時点 `t`、区間 `τ=(t0,t1]` に対して、

```text
K_t
(K_i,t)_{i∈I}
(P_i,t)_{i∈I}
(A_i,τ)_{i∈I}
```

を基本表現とする。

- `K_t`：対象系の resource / capability state
- `K_i,t`：actor `i` に帰属する resource state
- `P_i,t`：actor `i` が未実現関係を成立可能と信用し、現在参照している非物理的状態
- `A_i,τ`：actor `i` が interval `τ` 内に実行した activity / action record

calendar time `t` は model index であり、actual labor time / hours worked 等の区間 activity は `A_i,τ` 側に置く。

---

## 3. K / K_i / ΔK

### 3.1 K

`K_t` は対象となる系に存在する resource quantity / capability state を表す。

projection に応じて、physical resources、設備、energy、available time、技能、知識、労働能力等を coordinate として選ぶ。

K は制度、契約、信用、期待そのものを含む一般的 external world state ではない。

### 3.2 K_i

`K_i,t` は actor `i` に帰属する resource position を表す。

所有・保有・利用可能性等、どの relation を「帰属」とみなすかは projection で定める。

K_i は基本的に stock として扱う。区間差分は、

```text
ΔK_i(τ)
:= δ_K(K_i,t0, K_i,t1)
```

と書く。

additive representation が成立する場合は、

```text
ΔK_i(τ)
= K_i,t1 - K_i,t0
```

を特殊形として使える。

gross production / consumption / exchange / transfer は `A_i,τ` 側に記録し、net change `ΔK_i` と区別する。

### 3.3 exogenous change

K の変化が A のみによって生じるとは仮定しない。自然劣化、災害、偶発故障等を扱う場合は、projection-local な `Ω_τ` 等を追加できる。

---

## 4. P と proxy

`P_i,t` は、まだ実現していない relation / outcome が将来成立すると actor `i` が信用し、現在の A の形成に利用している reference state である。

P は価格、残高、契約額、評価指標等の observable そのものではない。

P の真値・内部構造・次元は直接観測できない。P を支える observable / reference proxy を、

```text
X_i,t = {x_i,t,1, x_i,t,2, ..., x_i,t,n}
```

と書ける。

```text
realized ΔK / realized events
        ↓
      X_i,t
        ↓
      P_i,t
        ↓
      A_i,t
```

金融・経済 projection では、観測と集約を単純化するため、P を単一スカラーへ近似してよい。

```text
P̂_i,t ∈ R
```

これは true P が本質的に一-dimensional であるという仮定ではない。

経済関係が複雑化すると、P の primitive dimension を増やすことよりも、P を支える proxy / relation が追加される形で記述できる。

```text
X^(stage+1) ⊇ X^(stage)
```

P の標準更新式、真の内部構造、scalar approximation の標準推定式は Core では固定しない。

---

## 5. A / shared event

A は actor-side activity / process record とする。

生産、消費、使用、交換、投資、労働、移転、契約、決済、政策、探索、学習等を必要な粒度で記述する。

multi-actor event では、participant-side records に shared event identity を持たせる。

```text
realized event e
participants(e) = {i, j, ...}
event_id(A_i,e) = event_id(A_j,e) = e
```

shared event view は participant-side records を reconcile / compose して構成する。

```text
E_e^shared
:= reconcile({ A_i,e | i ∈ participants(e) })
```

`E^shared` は universal primitive ではなく derived event view である。

---

## 6. Field / action sets

field は独立した価値スカラーではない。

```text
F_t
:= configuration(
    K_t,
    (K_i,t)_i,
    (P_i,t)_i;
    R_t^proj,
    C_t^proj
  )
```

`R_t^proj` / `C_t^proj` は projection-specified relations / constraints を表す。

必要な projection では、

```text
Γ_i^feas(F_t)
:= physically / institutionally feasible actions

Γ_i^avail(F_t)
:= cognitively / behaviorally available actions

Γ_i^adm(F_t)
:= actions remaining after projection-specific judgment

Γ_i^adm ⊆ Γ_i^avail ⊆ Γ_i^feas
```

と分ける。

final choice / deterministic choice function は Core では固定しない。

---

## 7. 使用価値

VFT では use-value を resource の物理的利用・消費として扱う。

```text
resource K
↓
A^use / A^consumption
↓
physical realization
```

resource `r` の interval `τ` における realized use を、必要に応じて、

```text
C_i,r(τ)
= actor i が τ 内に resource r を実際に使用・消費した量
```

として測定できる。

この quantity は resource-specific であり、異種 resource 間で一つの use-value scale へ還元することを Core は要求しない。

subjective satisfaction / utility を測定する projection を追加することはできるが、それを use-value の定義条件にはしない。

---

## 8. 余剰と自由度

actor `i` の required resource level を `K_i^req` と書けば、単純な projection では、

```text
S_i
= K_i^avail - K_i^req
```

として surplus を表せる。

重要なのは surplus の単発発生ではなく、required K を満たした後の surplus が反復的に生成されることである。

```text
A_t
→ K_(t+1)
→ required K を満たす
→ surplus
→ next A
```

反復的 surplus は、次期の resource allocation / A を required reproduction のみに拘束しない余地を生む。

VFT ではこれを、**次期 A に対する abstract degree of freedom** として扱う。

交換は resource-specific な余剰を他 resource へ変換可能にし、貨幣はその exchangeability をより一般的に保存・計量する構造として記述できる。

---

## 9. 資本概念と資本蓄積

VFT では capital を独立した一義的 primitive として置かない。

既存の capital 概念には、現に存在する resource / capability と、その将来価値を含んだ評価が重なっている。

VFT では、現実に成立している資源・能力の側を K、将来価値・未実現関係への信用側を P として分離する。

```text
realized / actual capital side
→ K

capital valuation including future value
→ K を基礎に P を含む projection
```

book value、market value、enterprise value 等は K / P そのものではなく、valuation / accounting projection による representation とする。

一方、surplus が生む自由度を future K / A の拡張へ再投入する反復は、capital accumulation / formation の構造として扱う。

```text
repeated surplus
→ abstract degree of freedom
→ reinvestment
→ K / capability expansion or reconfiguration
→ P update
→ broader A_(t+1)
→ new surplus
```

---

## 10. candidate A / expected ΔK

actor は candidate A に対して、主体固有の preference / expectation を通じて expected resource outcome を形成する。

```text
candidate A
        ↓ preference / expectation
expected ΔK
        ↓ execution
realized ΔK
```

preference / expectation の普遍的関数形は Core では固定しない。

production、consumption、labor、investment、career choice 等を同じ resource-outcome structure 上で扱うことはできるが、具体的な coordinate と評価規則は projection に委ねる。

---

## 11. 3つの管理合理性

VFT では、管理・意思決定に少なくとも次の3合理性が反復して現れると考える。

### 11.1 resource-realization

```text
expected ΔK
≈
realized ΔK
```

期待した resource outcome と実現結果の乖離を抑える合理性。

### 11.2 activity-flow

```text
maximize / maintain A_(t+1)
```

現在の A ではなく、次期にも成立可能な A を維持・拡張する合理性。

`A_(t+1)` は、projection に応じて activity count、activity range、action space、field-level activity mass 等で operationalize できる。

### 11.3 P-downside

```text
minimize ΔP^-
```

将来 A の成立を支える信用・期待・関係の重大な毀損を避ける合理性。

P の真の内部構造を Core で固定しないため、downside の具体的な projection / proxy / viability criterion は projection 側で定める。

### 11.4 非還元性

3合理性は一つの目的関数へ還元しない。

```text
1. expected ΔK と realized ΔK の一致
2. A_(t+1) の維持・拡張
3. P downside の抑制
```

これらは相互に衝突しうる。A の選別は第4の独立合理性ではなく、3合理性の競合結果として生じる。

危機・停滞・失敗は、主体の非合理性だけでなく、3合理性を同時に満たせない構造としても説明できる。

---

## 12. 制度主体による P への直接介入

通常の更新では realized `ΔK` や realized event が proxy を通じて P を更新する。

一方、国家・宗教・大規模 platform 等の field-managing actor は、

```text
A_F
→ ΔP_i
```

という直接経路を強く持つ。

法律、政策発表、保証、制裁、認証、推薦、ランキング、account suspension 等は、対応する physical ΔK の実現前に他主体 P を変化させうる。

```text
A_F
→ P_i
→ A_i
```

ただし先行形成された P を長期維持するためには、後続する realized outcome との整合が必要になる。制度的 A を信用の先行形成、realized ΔK を事後検証として区別できる。

---

## 13. 経済形態の successive construction

VFT は、

```text
autarky
→ division of labour
→ interdependence
→ exchange
→ money
→ banking / credit
→ machine capital
→ capital accumulation
→ institution / state / platform
```

を歴史的必然としてではなく、logical construction / successive model extension として扱う。

各段階で確認するのは、

1. 前段階から保持される K / K_i / P_i / A_i
2. 新たに安定化する relation / proxy
3. surplus / exchangeability / activity range の変化
4. 新 primitive を追加せず derived structure として記述できるか

である。

---

## 14. Core で固定しないもの

- K / K_i の標準 resource coordinates
- `δ_K` の標準 difference rule
- P の真の内部構造・次元
- P の標準 proxy・普遍的更新式
- P の scalar approximation の標準推定式
- preference / expectation の普遍的関数形
- `Γ^feas / Γ^avail / Γ^adm` の標準生成式
- deterministic choice function
- `A_(t+1)` の単一 operationalization
- 3合理性の weighting function
- exchange-value / monetary valuation function
- accounting identity / B/S / P/L / double-entry bookkeeping
- market equilibrium の普遍条件
- Marxian labor-value / surplus-value theory
- micro-to-macro aggregation の普遍 rule

---

© T. Nuno  
Licensed under CC BY 4.0
