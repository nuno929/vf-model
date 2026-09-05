# 価値場理論（Value-Field Theory）

**Theory refresh — Draft**  
Author: **T. Nuno**  
License: **CC BY 4.0**

---

## 1. 概要

価値場理論（Value-Field Theory; VFT）は、個人・組織・社会で生じる変化を、**実物・物理側の資源状態 K、主体別の交換価値・資本表現 K_i、主体ごとの主観的評価・期待状態 P_i、actor-side process / event A_i** の関係として記述する構造的フレームワークである。

VFT における **field（場）** は独立した価値スカラーではない。ある時点における K、各主体の K_i / P_i と projection-specified な主体間・資源間の関係・制約から導かれる配置構造であり、**その配置が主体の A を条件づけ、誘発し、継続的に再生産する**ことを指す。

```text
field state
K_t, (K_i,t)_i, (P_i,t)_i, projection-specified relations / constraints
        ↓ induces / conditions
      (A_i)_i
        ↓
resource use / transformation / exchange / learning
        ↓
K_t+1, K_i,t+1, P_i,t+1
```

VFT Core は、普遍的な deterministic choice function、会計則、均衡則、利益最大化則を固定しない。

---

## 2. Core variables

- **K**：生産・消費・労働・利用・変換等の対象となる physical / real-resource state
- **K_i**：主体 `i` が保持する actor-specific exchange-value / capital stock representation
- **P_i**：主体 `i` の structured subjective evaluation / expectation state
- **A_i**：主体 `i` 側で生じる action / process / event
- **ΔK**：区間端点における physical K の net state change
- **E_i[ΔK]**：主体 `i` が形成する expected realized resource-state change

`K_i` は K の subset / partition ではない。common K と economic events に ownership / holding / attribution、recognition、valuation 等を適用した actor-indexed exchange-value / capital representation であり、共同所有・重複帰属・複雑な attribution を排除しない。

形式的な企業会計では `K_i` を B/S・ledger 上の monetary position として実装できるが、**`K_i ≡ B/S` とは置かない**。B/S は assets / liabilities / equity 等を持つ制度的 accounting representation であり、K_i を形式化する代表的な projection の一つである。

---

## 3. K：実物・物理側の resource state

K は、設備、原材料、製品、土地、時間、身体、技能、知識、労働力、エネルギー等の resource coordinates を projection に応じて含みうる。

K を「外部に実在するものすべて」へ拡張しない。契約、制度、規範、法的権利関係等は、それだけを理由に K へ含めない。

契約・制度そのものの客観状態が必要な projection では、institutional / legal state を projection-local に追加してよい。Core はその専用 state を必須 primitive としない。

---

## 4. 使用価値と交換価値の二重表現

同一 resource は、主体にとって use-value side と exchange-value side の二重表現を持ちうる。

```text
same resource r
├─ use-value      : 実際の利用を通じてどの程度の効用を実現したか
└─ exchange-value : 他の resource / money とどの程度交換可能と評価されるか
```

### use-value quantity

VFT における **use-value quantity** は、resource stock 自体や technical service potential ではなく、**主体がある期間内にその resource を実際に利用・消費し、体験として実現した主観的効用量**を指す。

したがって use-value quantity は resource に内在する固定量ではなく、**interval を指定しない時点量としては評価できない**。physical stock / capability は K として時点観測できるが、それは use-value quantity そのものではない。

同じ主体・同じ resource・同じ利用量であっても、充足状態、利用順序、文脈、他の経験等によって体験結果は変わりうる。限界効用逓減もこの一例である。このため use-value quantity には一般的な再現性を仮定せず、実際の利用後にのみ realized value として観測できる。

離散時間で時点 `t` を考える場合、`t` で直接参照できる use-value は前区間までに実現した flow である。

```text
previous interval
actual use / consumption
        ↓
realized subjective use-value
        ↓
P_i,t update / reference
        ↓
expected future use-value
```

将来区間の use-value はまだ実現していないため、それ自体を時点 stock として保持するのではなく、P_i の belief / expectation として予測される。つまり **realized use-value は interval outcome、future use-value は P 上の expectation** と区別する。

この意味で VFT-specific use-value quantity は **P/L-like** である。ここで P/L-like とする理由は、単に「flow に見える」からではなく、**主観的体験価値であるため point-in-time valuation が成立せず、区間内で realized した値としてしか評価できない**からである。これは時間形式についてのアナロジーであり、use-value quantity を会計上の P/L entry と同一視するものではない。

### exchange-value representation

exchange-value は、resource を他の resource / money との比較関係から共通尺度へ写像した表現である。

exchange-value は、時点の資本 position `K_i` としても、取引・売上・費用等の期間 event valuation としても現れうる。したがって **use-value / exchange-value と stock / flow を完全な一対一対応とはしない**。

ただし VFT 固有の use-value quantity は interval realization としてのみ扱う。一方、異質な resource stock を共通交換尺度で比較・集計する場合、その評価は use-value quantity ではなく exchange-value representation に属する。

### 複式簿記アナロジー

各主体が同一 resource を「利用可能性」と「交換可能性」の二側面から捉える構造は複式簿記を想起させる。

ただし、これは **説明上のアナロジー** である。VFT は全主体が借方・貸方や会計恒等式を内的認知構造として保持すると仮定しない。個人では感覚的な利用可能量・交換可能量として、企業では在庫管理・評価・会計原則等によって形式化されうる。

---

## 5. P：structured subjective state

各 `P_i,t` は、将来見通し、belief / expectation、preference / valuation、trust / reputation、norm recognition 等を含む structured subjective state である。

P はどれだけ共有されても主観状態である。shared P は複数主体の P の共通性・整合性・分布として扱い、客観的な社会価値の真値とはみなさない。

`E_i[ΔK | a, I_i]` は P_i と別の主観世界ではなく、**P_i の belief / expectation component と情報集合 I_i から導出される action-contingent forecast** とする。desire / preference / plan とは区別する。

加工・変換によって同一由来の resource でも利用可能性は変化する。加工後の use-value は事前に確定した真値として存在するのではなく、利用後の体験として実現し、その結果が P_i を更新する。

```text
K_t
 ↓ A / transformation
K_t1
 ↓ actual use over interval
realized subjective use-value
 ↓
P_i,t -> P_i,t1
```

この経路により、主体は「どの A がどの利用可能状態と体験結果を生むか」という期待を、前区間までの実現結果から更新する。

---

## 6. A と ΔK

A は、生産、消費、交換、投資、労働、移転、契約、政策、探索、学習等の actor-side process / event を表す。

区間 `τ=(t0,t1]` の gross activity は A の event history として保持する。

`ΔK` は記号どおり endpoint state change とする。

```text
ΔK_[t0,t1] = K_t1 - K_t0
```

したがって、同一区間に 100 入荷・100 出荷があれば gross activity は存在するが `ΔK = 0` になりうる。gross activity を表す追加 primitive は Core に置かない。

`ΔK` は会計仕訳ではない。

---

## 7. exchange-value と surplus

surplus は physical primitive ではない。

物理的・使用価値側で起きた input / output / transformation を exchange-value の比較可能な尺度へ写像し、その差分を認識・集計したときに初めて surplus / deficit が成立する。

```text
physical / use-value activity
        ↓ exchange-value valuation
comparable input / output values
        ↓ comparison / accounting
surplus / deficit
```

したがって余剰は単なる物理量の増加ではない。同じ物理対象でも、その利用法・交換可能性を認識できる主体とできない主体では value representation が異なりうる。機械が利用法を知らない主体には単なる箱・物体としてしか見えない、という例がこの差を示す。

surplus の帰属・留保・分配は、次期の actor-specific exchange-value / capital position `K_i` を変える。

---

## 8. 会計への projection

P/L・B/S・複式簿記は VFT Core の普遍的因果層ではなく、exchange-value を制度的に記録する **formal accounting projection** である。

```text
physical/resource events ─────┐
contract/financial events ────┼→ recognition / valuation → accounting entries
valuation-only events ────────┘
                                      ↓
                                   P/L / B/S
```

- P/L：recognized interval events の monetary / exchange-value representation
- B/S：recognized point-in-time positions の monetary / exchange-value representation
- ledger：actor-specific accounting record

帳簿そのものは主体ごとに閉じており、recognition / valuation / bookkeeping は主体・制度によって異なりうる。財務報告・連結・統計は個別帳簿とは別の external representation である。

正式な accounting projection で B/S を採用する場合、assets / liabilities / equity 等の accounting identity はその representation の定義条件として従う。ただし、それを全主体の普遍的認知公理とはしない。

金融資産については、預金・債券・売掛債権等を成立させる契約・権利関係そのものを physical K とせず、recognized exchange-value / financial position として K_i / accounting projection 上に表現できる。

---

## 9. field と事業体

VFT では、事業体を「利益を最大化する法人」から定義しない。

**事業体は、一定の目的・機能に向けた A を継続的に誘発・再生産する局所的 field structure** として捉える。

```text
resources / capabilities / relations / expectations
                    ↓
              action-generating field
                    ↓
      procurement / production / service / learning / etc.
                    ↓
              field reproduction
```

この定義では、営利企業だけでなく、NPO、協同組合、公共事業、国家・自治体の事業等を同じ型で扱える。

利益は事業体を定義する目的ではなく、交換価値側で活動継続や蓄積を評価する重要な指標の一つである。

### 起業・新規事業・既存事業

```text
起業             = business-oriented field formation の一類型
新規事業開発     = 既存 field から business-oriented field を形成・分岐させる活動
既存事業の運営   = 成立済み business field の維持・再生産・改善
```

field formation 自体は事業に限らない。起業はそのうち business-oriented な field formation として扱う。

既存事業の運営は profit / surplus 等の既存評価関数でもかなり説明できるが、起業時には顧客、商品、価格、組織、収益構造そのものが未形成であり、既存の profit function の最適化だけでは事業体の成立を十分に定義できない。

---

## 10. 3つの管理合理性公理

VFT の decision model は次の3則を constitutive rationality assumptions として置く。

1. **resource-realization**：望ましい resource / capital outcome の実現へ向けて A を動かす
2. **activity-flow**：必要な activity / process の流れを維持・拡張し、必要なら新たな action-generating field を形成する
3. **P-downside**：P 側の大幅な毀損により主体・組織・系の A が成立しなくなることを防ぐ

3則は経験的普遍法則ではない。projection 側で objective / weight / constraint / threshold / horizon 等を具体化することで empirical hypothesis を形成する。

profit / utility は3則の特殊化ではなく、具体的な decision problem を評価する metric / objective / proxy として使いうる。

---

## 11. 経済学への射影

### plan / forecast

必要な economic projection では planned / chosen resource change を `x_i` と書ける。

```text
x_i                  = planned / chosen resource change
E_i[ΔK | a, I_i]     = action-contingent forecast of endpoint resource change
```

`| a` は observational conditioning の主張ではなく、「candidate action a を採った場合」の forecast を表す略記である。

### Marxian categories

VFT は Marxian economics が区別した use-value / labor / exchange-value / surplus / accumulation を一般化された構造上で表現する。

- use-value：主体が期間内の実利用を通じて体験として実現した主観的効用量
- labor measure：labor activity / labor time による production activity の記述
- Marxian labor-value projection：socially necessary labor time 等の追加条件を導入した specialization
- exchange-value / price：resource 間の比較・market / monetary valuation
- surplus：exchange-value の比較可能尺度上で成立する差分 / residual
- accumulation / distribution：surplus 等の帰属・留保・分配による K_i の変化

VFT-specific use-value quantity は Marxian use-value と自動的に同一視しない。VFT Core 自体を Marx 固有の labor-value theory / surplus-value theory とも同一視しない。

---

## 12. ミクロ／マクロ接続

```text
micro
field_i -> A_i -> resource activity
              -> realized use-value over interval -> P_i update
              -> exchange valuation -> K_i update

                     ↓ external reporting / aggregation where needed

macro
physical production / consumption
exchange-value distribution / surplus
capital accumulation
shared P
field formation / dissolution
```

主体ごとの帳簿そのものが共通化されることは仮定しない。macro representation は、必要な projection で reporting / statistical transformation / aggregation を通じて構成する。

---

## 13. compatibility / equilibrium / accounting

- **inter-agent compatibility / feasibility**：各主体の plan が相互に実行可能・両立可能であること
- **market equilibrium**：compatibility に加え、射影先理論の choice / optimality / best response / clearing 条件が成立すること
- **accounting consistency**：指定 accounting representation の recognition / valuation / identity / closing rule が整合すること
- **steady state**：対象状態について別途定める動学条件

これらは別概念である。

---

## 14. Core で固定しないもの

- K の標準 resource coordinates
- institutional / legal state の普遍 primitive
- use-value の標準効用関数・代替可能性
- exchange-value / monetary valuation function
- K_i の標準 representation / accounting implementation
- P の標準内部次元
- P の普遍的更新式
- A の deterministic choice function
- gross activity の追加 primitive
- E[ΔK] の確率測度・期待形成式
- surplus の普遍的算出式
- 3則の objective / weight / priority / threshold
- market equilibrium の普遍的条件
- micro-to-macro aggregation rule

---

## 15. ドキュメント

- [モデルノート](docs/01_model_notes.md)
- [計測](docs/02_measurement.md)
- [背景・整理経緯](notes/background.md)
- [既存概念・応用への射影](notes/projections.md)
- [拡張・再検討ノート](notes/future_topics.md)

---

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)  
© T. Nuno