# 価値場理論 — 既存概念・応用への射影ノート

> この文書は価値場理論のコア定義ではなく、既存概念・応用領域への射影候補を保存するためのノートである。

## 1. 射影の基本方針

価値場理論では、

- `K`：共通の resource / capital state
- `K_i`：主体 `i` に所有・保有・帰属する resource / capital
- `P_i`：主体 `i` の subjective evaluation / expectation state
- `A_i`：主体 `i` 側の actor-side process / event
- `ΔK`：A 等の結果として実現した resource / capital change
- `ΔP_i`：主体 `i` の P に実現した変化
- `E_i[ΔK]`：主体 `i` が形成する expected realized resource / capital change

を用いる。

K / K_i / P / ΔK の完全観測は前提としない。特に `K_i` は主観的な access / usability view ではなく、所有・保有・帰属する resource / capital を表す。主体がそれをどう認識しているかは P に属する。

P はどれだけ共有されても主観状態である。shared P は、複数主体の P の共通性・整合性・分布として記述・推定する。

契約・制度・規範・権利関係等は、それだけを理由に K へ入れない。法的・制度的事実、主体の履行・執行期待、実際の資源移転を分けて扱う。

---

## 2. 3つの管理合理性公理

VFT の管理・意思決定記述では、合理性を次の3則へ集約する。

1. **resource-realization rule**：望ましい resource / capital outcome の実現へ向けて A を動かす。
2. **activity-flow rule**：必要な activity / process の流れを維持・拡張できるよう K / P / A を調整する。
3. **P-downside rule**：P 側の大幅な毀損により主体・組織・系の A が成立しなくなることを防ぐ。

3則は actor type ではなく、意思決定合理性の公理系である。同一 actor が3則を同時に考慮しうる。

必要な quantitative projection では、context-dependent priority / weight / constraint を置けるが、具体形は projection-specific とする。

### P-downside と shared P

R3 が対象とする P は客観的な社会価値ではない。

対象主体集合の P の共有部分、信頼、期待、規範認識等が大きく毀損すると、将来の A が成立しにくくなる。その downside を抑える合理性として R3 を扱う。

P の真値は直接観測不可とし、shared P の最大化を使う場合も、指定した actor set / dimension / proxy 上の共通性・支持・信頼等を高めるという意味に限定する。

---

## 3. 自給自足・制度的分業・組織階層

### 自給自足

```text
single actor
  ├─ resource-realization
  ├─ activity-flow
  └─ P-downside
```

単一 actor が3則すべてを担える。

### 国家レベルの制度的分業

資本主義社会を国家レベルで粗視化すると、典型的には

```text
individuals -> resource-realization heavy
firms       -> activity-flow heavy
state       -> P-downside heavy
```

と主たる比重が分化して見える。ただし固定 assignment ではない。

### 組織階層

operational / managerial / governance の各層も、3則の比重・分担の差として記述できる。

```text
operational / execution -> resource-realization heavy
managerial              -> activity-flow heavy
governance              -> P-downside heavy
```

これは既知の階層構造の存在を新規に予測する主張ではなく、管理合理性の違いを共通記述するための射影である。

---

## 4. 経済学への射影

### 主体別期待と意思決定

経済射影では、`K_i` を主体の保有資源・資本・予算制約側、`P_i` を価格、他主体、信用、制度、将来条件等についての認識・期待・評価側として読める。

必要なら A に含まれる planned / chosen resource change を `x_i` と書く。

```text
x_i          = planned / chosen resource change
E_i[ΔK(...)] = expected realized resource change
```

予算制約・feasibility は `x_i` 側へ置き、forecast と区別する。

### budget / compatibility / equilibrium

純粋交換の基本例では、射影先の符号規約・価格体系のもとで

```text
p · x_i <= 0
```

のような budget feasibility を置ける。

- **inter-agent compatibility / feasibility**：各主体の plan が相互に実行可能・両立可能であること
- **market equilibrium**：compatibility に加え、射影先理論の choice / optimality / best response / clearing 条件が成立すること
- **会計整合**：同じ実現事象を同一 accounting boundary / rule で記帳した結果が整合すること
- **定常状態**：対象 K の増減等について別途定める状態条件

これらは別概念である。

---

## 5. ΔK records と一般化された仕訳

一つの A が複数の resource / capital change を生む場合、それぞれを ΔK record として保持する。

```text
A
├─ raw material   -10
├─ labor input     -5
├─ equipment wear  -2
└─ product         +20
```

この意味で、A に伴う ΔK records の列は、**資源・資本変化を追う一般化された仕訳**として読むことができる。

ただし VFT の ΔK record 自体は必ずしも既存会計の借方・貸方や貨幣評価済み勘定科目ではない。会計体系へ射影することで、勘定科目、評価額、認識時点、借方・貸方等を与える。

区間活動量を表す独立変数 `H` は置かない。gross production / consumption / transaction 等は、A と ΔK records の event history から必要な accounting / measurement projection を行う。

---

## 6. 使用価値・労働価値・交換価値・余剰

VFT は、マルクス経済学が区別した経済現象の骨格を、特定の政治的・規範的結論を前提にせずモデル化することを狙う。

### 使用価値

使用価値は、ある K が特定目的の A / resource transformation を実際に可能にする機能・有用性として射影できる。

```text
use-value
≠ price
≠ utility
≠ subjective P
```

何を目的とするか、何を望ましいと評価するかは P に依存しうるが、K が何を可能にするかという機能と市場価格は区別する。

### 労働価値

労働価値は、生産・変換過程へ投入された labor activity / labor time を価値記述の尺度として用いる射影として扱う。

必要に応じて socially necessary labor time 等の benchmark を導入できるが、Core は「労働だけが価値の唯一の源泉である」という形而上学的・規範的主張を置かない。

労働投入は A / ΔK records として追跡し、物量、時間、技能補正等の具体的な尺度は projection 側で定める。

### 交換価値・価格

交換価値・価格は、市場交換・会計上の valuation / representation として扱う。

使用価値、労働投入量、価格は互いに別の表現であり、同一量とは仮定しない。

### surplus

異質な ΔK records を指定した valuation / bookkeeping rule で共通尺度化し、同一 accounting boundary 内で差し引いた後に残る最終差分を surplus / deficit として扱える。

```text
realized ΔK records
        ↓ valuation / bookkeeping
accounting entries
        ↓ aggregation
surplus / deficit
```

surplus は物理的 primitive ではなく accounting residual である。その存在だけから搾取等の規範判断を導かない。

### accumulation / distribution

surplus の帰属・分配が次期 `K_i` を変える場合、

```text
ΔK records
    ↓ accounting
surplus
    ↓ attribution / distribution
K_i(t+1)
```

として資本蓄積・所有分布の変化を追える。

これにより、使用価値、労働投入、交換価値、余剰、蓄積を同じ K / P / A / ΔK 構造上で接続できる。

---

## 7. ミクロ／マクロ接続

VFT ではミクロとマクロを別々の K として置かない。

```text
micro:
(K_i, P_i) -> A_i -> ΔK records

              ↓ same common K

macro:
ownership distribution
production / consumption
surplus distribution
capital accumulation
shared P
```

個別主体の A_i が同じ K の構成・所有分布を変える。マクロでは、その同じ K と ΔK records を別の accounting boundary / aggregation scope から観測する。

micro observable から macro observable を再構成する場合のみ、projection-local な aggregation / coarsening rule を追加する。

この構造により、主体の期待・意思決定と、資本蓄積・分配・生産構造等のマクロ現象を同じ状態系列で接続することを目指す。

---

## 8. 契約・制度・評価・信用

### 契約・制度

契約・制度を resource / capital そのものとして K へ押し込まない。

```text
contract / institution event or record
        ↓ interpreted by actor j
      P_j
        ↓
      A_j
        ↓
realized ΔK
```

契約には法的効力がありうるが、それを K の資源量と同一視しない。

### 評価・信用

他主体 `a` について主体 `j` が持つ信用・評価・見通しは `P_j(a)` として表現する。

公開 rating / review は observable information であり、それ自体を P とみなさない。主体がそれをどう解釈したかが P に属する。

---

## 9. 選好・消費・生産・市場

### 選好

選好は P の evaluative / preference-like component として扱う。

### 消費 / 生産 / 交換

消費・生産・交換は、A とそれに伴う ΔK records の組として記述する。

### utility / profit / supply-demand

utility / profit は3則の特殊化ではなく、具体的な意思決定を数量化・評価するときの評価関数・指標・proxy として扱う。

price / supply / demand / market equilibrium は複数主体の planned change を相互調整する mechanism であり、第4の合理性公理ではない。

---

## 10. 国家・政治・組織

国家・組織を自動的に単一主体へ還元しない。

- 政策・公約・宣言 → A / observable event
- それを主体がどう解釈・期待するか → P_i
- 執行・履行による実資源・資本変化 → ΔK
- 共有された支持・信頼・期待 → shared P proxy

単一主体へ還元する場合は近似条件と情報損失を明示する。

---

## 11. 射影時に明示するもの

1. K の対象範囲
2. 対象主体集合
3. K_i の ownership / attribution rule
4. P の採用次元・proxy
5. shared P を扱う場合の actor set と集約方法
6. A の観測単位と event ordering
7. ΔK records の認識方法
8. time window
9. valuation / bookkeeping rule
10. accounting boundary
11. unit of account
12. surplus / deficit の集約規則
13. labor-value を使う場合の labor measure / benchmark
14. use-value を扱う場合の機能・目的の定義
15. planned / expected / realized change の区別
16. budget / compatibility / equilibrium の追加条件
17. 3則の priority / constraint / horizon
18. ownership distribution / accumulation の集約規則
19. 欠測・測定誤差・情報損失

---

© T. Nuno  
Licensed under CC BY 4.0