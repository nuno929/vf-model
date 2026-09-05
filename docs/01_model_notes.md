# 価値場理論 — モデルノート

## 1. 目的

本ノートは、価値場理論（Value-Field Theory; VFT）の Core を README より形式的に整理する。

VFT は、**physical / real-resource state K、actor-specific exchange-value / capital representation K_i、structured subjective state P_i、actor-side process / event A_i** の関係として経済・事業活動を記述する。

VFT における field は独立したスカラー V ではない。K、(K_i)_i、(P_i)_i、主体間・資源間の関係・制約が形成する配置構造であり、その配置が A を条件づけ、誘発し、再生産することを指す。

---

## 2. Core state / process

```text
K_t
(K_i,t)_{i in I}
(P_i,t)_{i in I}
(A_i,τ)_{i in I}
```

- `K_t`：physical / real-resource state
- `K_i,t`：actor-specific exchange-value / capital stock representation
- `P_i,t`：structured subjective evaluation / expectation state
- `A_i,τ`：actor-side action / process / event

field はこれらを単純に足した新変数ではなく、A を発生させる actor-resource 間の配置・関係構造である。

---

## 3. K：physical / real-resource state

`K_t` は時点 `t` の実物・物理側 resource state を表す。

対象 projection に応じて、設備、土地、原材料、製品、時間、身体、技能、知識、労働力、エネルギー等を含みうる。

K は external world state 全体ではない。契約、制度、規範、法的権利関係等を、それだけを理由に K へ含めない。

institutional / legal state が必要な projection では、`C_t` 等を projection-local に追加してよい。Core はそれを必須 primitive としない。

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

### 金融資産との境界

預金、債券、売掛債権等は、その根拠となる契約・法的権利関係そのものを physical K とみなすのではなく、recognized exchange-value / financial position として K_i / accounting projection 上に表現できる。

---

## 5. 使用価値と交換価値

同一 physical resource `r` は、主体にとって use-value / exchange-value の二重表現を持ちうる。

```text
same resource r
├─ use-value representation
└─ exchange-value representation
```

### 5.1 use-value quantity

VFT における use-value quantity は、resource stock 自体や technical service potential ではなく、**主体がある interval 内に resource を実際に利用・消費し、その体験として実現した主観的効用量**を指す。

したがって、use-value quantity は resource に内在する fixed property でも、時点 `t` に stock として直接保持される量でもない。physical stock / capability は K として時点観測できるが、それは use-value quantity そのものではない。

同じ主体・同じ resource・同じ利用量でも、充足状態、順序、文脈、他の経験等により体験結果は変わりうる。限界効用逓減はその一例である。よって **use-value quantity には一般的な再現性を仮定しない**。

use-value は利用前に真値として観測できず、利用後に ex post の realized outcome としてのみ評価できる。

```text
A / actual use over τ=(t0,t1]
        ↓
subjective experience / fulfillment
        ↓
U^use_i(τ) = realized use-value quantity
```

離散時間で時点 `t` を考える場合、時点 `t` で直接参照可能なのは前区間までに realized した use-value flow である。

```text
U^use_i((t-1,t])
        ↓
reference / update of P_i,t
        ↓
expectation about future use
```

将来区間の use-value はまだ実現していないため、それ自体を use-value quantity として保持しない。将来について主体が持つのは P_i の belief / expectation である。

したがって、

```text
realized use-value = subjective interval outcome
future use-value   = not yet realized; represented only as expectation in P_i
```

と区別する。

この意味で VFT-specific use-value quantity は **P/L-like** である。理由は単に flow-oriented だからではなく、**主観的体験価値であるため point-in-time valuation が成立せず、interval 内で realized した値としてしか評価できない**ことにある。P/L-like はこの時間形式を示すアナロジーであり、use-value quantity を会計上の P/L entry と同一視するものではない。

個別用途の効用関数、substitute / complement、代替可能性は Core では固定しない。

### 5.2 exchange-value representation

exchange-value は、resource を他の resource / money との比較関係から共通尺度へ写像した representation である。

exchange-value は、

- point-in-time capital / asset position
- interval transaction / revenue / expense valuation

の双方に現れうる。

したがって use-value / exchange-value と stock / flow を完全な一対一対応とはしない。ただし、**VFT-specific use-value quantity は interval realization としてのみ定義する**。

異質な resource stock を共通交換尺度で比較・集計した評価は、use-value quantity ではなく exchange-value representation に属する。

### 5.3 複式簿記アナロジー

同一 resource を「利用可能性」と「交換可能性」の二側面から保持する構造は複式簿記を想起させるが、これは説明上のアナロジーである。

VFT は、全主体が借方・貸方や会計恒等式を内的に保持すると仮定しない。個人では感覚的な利用可能量・交換可能量、企業では在庫管理・valuation / accounting 等として形式化の程度が異なりうる。

---

## 6. P：structured subjective state

各 `P_i,t` は、少なくとも概念上、

- belief / expectation
- preference / valuation
- trust / reputation
- norm recognition

等を含む structured subjective state である。

primitive を内部 component ごとに分割することは Core では要求しない。

P はどれだけ共有されても主観状態である。shared P は複数主体の P の共通性・整合性・分布として扱い、客観的な社会価値の真値とはみなさない。

### forecast との関係

`E_i[ΔK | a, I_i]` は、P_i の belief / expectation component と情報集合 I_i から導出される action-contingent forecast である。

したがって、

```text
forecast = derived from belief / expectation
preference / desirability = P_i の別 component
plan / choice = A / x_i 側
```

と区別する。

### 加工・変換と P 更新

同一由来 resource でも、A による加工・変換後には利用可能性が変わる。ただし加工後の use-value quantity は加工時点で確定するのではなく、**加工後 resource を実際に利用した interval の体験結果として初めて realized する**。

```text
K_t
 ↓ A / transformation
K_t1
 ↓ actual use in later interval
U^use_i(τ) realized
 ↓
P_i update
```

主体は A が K をどのような利用可能状態へ変え、どのような体験結果を生みうるかについて期待を持つ。前区間までの realized use-value がその期待を更新し、次の A を条件づける。

---

## 7. A：actor-side process / event

A は各主体側で生じる action / process / event を表す。

生産、消費、交換、投資、労働、移転、契約、政策、探索、学習、情報伝達等を必要な粒度で A として記述する。

区間中の gross activity は A の event history / sequence から記述する。独立した interval-flow primitive は Core に追加しない。

---

## 8. ΔK：endpoint resource-state change

`ΔK` は記号どおり endpoint state change とする。

```text
ΔK_[t0,t1] = K_t1 - K_t0
```

ここで差は対象 projection が定める K coordinates 上の state difference を意味する。

例えば同一区間で、

```text
+100 入荷
-100 出荷
```

という gross activity があっても、endpoint stock が同一なら `ΔK = 0` になりうる。

したがって、

```text
A history ≠ ΔK
```

である。

`ΔK` は会計仕訳でもない。

---

## 9. exchange-value / surplus / accounting

surplus は physical primitive ではない。

物理・使用価値側で生じた input / output / transformation を exchange-value の比較可能尺度へ写像し、その差分を認識・集計したときに surplus / deficit が成立する。

```text
physical / use-value activity
        ↓ exchange-value valuation
comparable input / output values
        ↓ comparison / accounting
surplus / deficit
```

したがって surplus は単なる物理的増加ではない。同じ physical K でも、主体の知識、交換体系、valuation rule、recognition boundary が異なれば exchange-value / surplus は異なりうる。

### accounting projection

P/L・B/S・複式簿記は Core の普遍因果層ではなく、exchange-value を制度的に記録する formal accounting projection である。

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

帳簿そのものは actor-specific であり、主体ごとに recognition / valuation / bookkeeping が異なりうる。external financial reporting / consolidation / statistics は個別帳簿とは別 representation である。

---

## 10. field と事業体

### field

field は、K、(K_i)_i、(P_i)_i、主体間・資源間の関係・制約がつくる **action-generating configuration** である。

```text
field_t
  ↓ induces / conditions
A_i
```

field の存在意義は「値が存在すること」ではなく、特定の action set を成立・誘発させることにある。

### 事業体

事業体は、利益最大化主体としてではなく、**一定の目的・機能に向けた A を継続的に誘発・再生産する局所的 field structure** として定義する。

この定義により、営利企業、NPO、協同組合、公共事業、国家・自治体の事業等を同じ型で扱える。

profit / surplus は事業の定義条件ではなく、exchange-value 側で活動継続・蓄積を評価する重要指標の一つである。

### field formation

```text
起業           = 新しい action-generating field の形成
新規事業開発   = 既存 field から新しい field を形成・分岐させる活動
既存事業運営   = 成立済み field の維持・再生産・改善
```

既存事業では既存の顧客・商品・価格・組織・収益構造があるため profit / surplus を含む既存評価関数で運営を説明しやすい。

一方、起業時にはそれら自体が未形成である。したがって起業を「既存 profit function の最大化」とだけ定義すると、事業体そのものの成立を説明できない。VFT はこれを field formation として扱う。

---

## 11. 3つの管理合理性公理

VFT の decision model は次の3則を constitutive rationality assumptions として置く。

1. **resource-realization**：望ましい resource / capital outcome の実現へ向けて A を動かす
2. **activity-flow**：必要な activity / process の流れを維持・拡張し、必要なら新しい action-generating field を形成する
3. **P-downside**：P 側の大幅な毀損により主体・組織・系の A が成立しなくなることを防ぐ

3則は経験的普遍法則ではない。projection 側で objective / priority / weight / constraint / threshold / horizon 等を具体化して empirical hypothesis を形成する。

profit / utility は3則の特殊化ではなく、具体的 decision problem の metric / objective / proxy として使いうる。

---

## 12. 経済学への射影

### plan / forecast

```text
x_i                  = planned / chosen resource change
E_i[ΔK | a, I_i]     = action-contingent forecast of endpoint resource change
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

- use-value：主体が interval 内の実利用を通じて体験として realized した主観的効用量
- labor measure：labor activity / labor time
- Marxian labor-value：socially necessary labor time 等の追加条件を持つ specialization
- exchange-value / price：resource 間の比較・market / monetary valuation
- surplus：exchange-value の比較可能尺度上で成立する差分 / residual
- Marxian surplus value：Marx 固有条件を持つ specialized interpretation
- accumulation：surplus 等の帰属・留保・分配による K_i の変化

VFT-specific use-value quantity は Marxian use-value と自動的に同一視しない。

---

## 13. ミクロ／マクロ接続

```text
micro
field_i -> A_i -> resource activity
              -> ΔK
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

主体ごとの帳簿そのものが共通化されることは仮定しない。

---

## 14. Core で固定しないもの

- K の標準 resource coordinates
- institutional / legal state の普遍 primitive
- use-value の標準効用関数・代替可能性
- exchange-value / monetary valuation function
- K_i の標準 accounting implementation
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

© T. Nuno  
Licensed under CC BY 4.0