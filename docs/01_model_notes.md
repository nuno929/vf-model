# 価値場理論 — モデルノート

## 1. 目的

本ノートは、価値場理論（Value-Field Theory; VFT）のコア変数と基本動学を README より形式的に整理する。

VFT は、個人・組織・社会で生じる経済・社会変化を、**共通の資源・資本 K、主体ごとの保有・帰属 K_i、主観的な評価・期待状態 P_i、actor-side process / event A_i、およびその結果として実現する資源・資本変化 ΔK** を同一構造で記述する structural framework である。

Core は K / P から A を一意に予測する普遍的 choice function、状態遷移式、均衡式、会計式を固定しない。具体的な予測・計測・会計は projection / empirical model 側で与える。

その上に、管理・意思決定を方向づける **3つの管理合理性公理**を置く。

---

## 2. K と K_i：資源・資本

### K

`K_t` は、時点 `t` に存在する**資源・資本の状態**を表す。

```text
K_t
```

K は主体ごとに別々の世界として存在するのではなく、同じ経済・社会の資源・資本を参照する。

K の範囲は projection に依存する。設備、在庫、土地、時間、身体、技能、知識、労働力、貨幣・金融資産、インフラ等、対象理論が resource / capital として扱うものを含みうる。

ここで K を「外部に実在するものすべて」へ拡張しない。契約、制度、規範、権利関係等を、それだけを理由に K へ含めることもしない。K の役割はあくまで **resource / capital** である。

### K_i

`K_i,t` は、共通 K のうち、経済学上の所有・保有・帰属の観点から主体 `i` に帰属すると扱う資源・資本を表す。

```text
K_t
├─ K_1,t
├─ K_2,t
└─ ...
```

`K_i` は actor が「利用可能だと認識している K」ではない。その認識は P 側に属する。

また、`K_i` の完全な真値が主体本人や観測者に常に把握されているとは仮定しない。未把握資産、債務、評価差、複雑な帰属関係等により、実際の保有状態と認識・記帳値はずれうる。これは K_i の定義問題ではなく、計測・会計上の問題として扱う。

所有・帰属をどの法域・会計境界・集約単位で判断するかは projection-specific であり、Core は普遍的な所有判定関数を置かない。

---

## 3. P：主観的評価・期待 state

各主体 `i` の `P_i,t` は、**将来の見通し、評価、選好、信用、信念、期待、規範認識等を含み、意思決定と A を条件づける主観状態**である。

```text
P_t = (P_i,t)_{i in I}
```

P はどれだけ多数主体に共有されても、主観状態であることをやめない。多数主体が同じ契約、制度、規範、価格観、将来期待等を共有していても、それを客観的な P の真値とはみなさない。

必要な projection では、主体集合 `G` の P に共通する部分・整合度・共有度を「共有 P」として扱える。ただし共有 P は独立した客観 state ではなく、`(P_i)_{i∈G}` から記述・推定する集団的構造である。

したがって「P を最大化する」という表現を使う場合も、それは**指定した主体集合・次元・proxy における共有 P を高める**という意味に限られ、客観的な社会価値の真値を最大化することを意味しない。P の真値は直接観測できず、実証では proxy を用いる。

P は一つのスカラーではなく、必要に応じて概念上、

```text
P_i
├─ belief / outlook
├─ evaluation / preference
├─ trust / credit expectation
├─ norm / institutional expectation
└─ other projection-specific components
```

のような内部型を区別できる。ただし独立 primitive を増やす必要はない。

他主体 `a` について主体 `j` が持つ評価・信用・見通し等を区別したい場合は `P_j(a)` と書く。

### 契約・制度

契約・制度は、VFT では resource / capital そのものとして K へ押し込まない。

契約には法的効力があり、制度には執行・制裁・手続等の外部作用がありうる。しかし、その経済的な行動効果は、主体が契約・制度をどう認識し、どの程度履行・執行・継続を期待するかという P と、それに基づく A を通じて現れる。

契約書・法令・判決・制度変更等は observable event / record になりうるが、それらの法的効力そのものを K の資源量と同一視しない。執行の結果として実際に資源・資本の移転や損失が生じた場合、その実現結果は ΔK として記述する。

---

## 4. K / P の境界

K / P の基本境界は次の通りである。

- **K**：資源・資本
- **P**：主体が持つ主観的な評価・期待・認識・信念・規範認識

したがって、同じ現象についても役割を分ける。

```text
resource / capital state in K
        ↓ perceived / interpreted by actor i
subjective representation in P_i
        ↓
A_i
        ↓
realized resource / capital change ΔK
```

例えば、主体が100万円を保有していることは K_i の対象になりうるが、「自分は100万円を自由に使える」「この投資で増える」と考えることは P_i である。

また、貨幣は役割によって区別する。

- 保有される貨幣・金融資産 → K
- 価格表示・会計単位としての貨幣 → valuation / accounting representation

同じ「円」が両方に現れても、理論上の役割は異なる。

---

## 5. A：actor-side process / event

A は各主体側で生じる process / event を表す。

```text
A_τ = (A_i,τ)_{i in I}
```

外部行動、意思決定、生産、消費、交換、投資、労働、情報伝達、契約締結、政策実施等を必要な粒度で A として記述できる。

観測・情報受容・解釈等を A に含める必要がある projection では、それらを actor-side process として扱える。ただし、情報受容そのものを必ず能動的行為とみなすわけではない。

複数主体の A を必要なく単一 actor へ還元しない。区間中の順序が重要なら event ordering を保持する。

---

## 6. 価値場

価値場は、**K / K_i と P_i の配置・関係が A_i を条件づけ、特定の行動・process を生じやすく／生じにくくする構造**である。

```text
common K
  └─ ownership / attribution -> (K_i)_i

(K_i)_i, (P_i)_i
        ↓  value field
      (A_i)_i
```

独立した価値場変数 V、引力量、普遍的な deterministic choice function は置かない。

---

## 7. ΔK / ΔP：実現変化と記帳

### ΔK

`ΔK` は、K の利用・移転・変換・消費・生成等の結果として**実現した資源・資本の変化**を表す。

K の利用そのものは経済活動の原始的な事象として扱える。一方、その結果として何がどれだけ増減したかは、通常、

1. 会計・台帳・取引記録等による記帳
2. 利用・活動後の資源・資本状態の観測

のいずれか、または両方から事後的にトレースする。

Core は K や ΔK が常に完全観測可能だとは仮定しない。

### 複数の ΔK と活動履歴

一つの A が複数の資源変化を生む場合、それぞれを ΔK の記録として保持できる。

```text
A
├─ raw material   -10
├─ labor input     -5
├─ equipment wear  -2
└─ product         +20
```

区間活動量を表すための独立変数 `H` は Core に置かない。必要なら、観測区間内に生じた ΔK の系列・集合と A の event history をそのまま利用する。

例えば「生産100」と「消費100」が同じ区間に起き、最終在庫が変わらない場合、net change は0になりうるが、二つの ΔK record は履歴として残る。gross activity と net state change の違いは、この記録粒度と会計集約で表現する。

### 会計集約と surplus

異質な ΔK をそのまま加算できるとは限らない。会計・評価規則を用いて共通尺度へ写像し、同じ accounting boundary で差し引いたときに残る最終差分を surplus / deficit として扱える。

```text
realized ΔK records
        ↓ valuation / bookkeeping
comparable accounting entries
        ↓ aggregation
surplus / deficit
```

surplus は K の primitive でも、物理世界に独立して存在する物体でもない。**実現した資源・資本変化を特定の会計・評価体系で表現・集約した派生量**である。

VFT は surplus の物理的実在性を要件にしない。経済理論として必要なのは、どの ΔK を、どの valuation / accounting rule と boundary で集約したかを区別することである。

### ΔP

`ΔP_i` は主体 `i` の主観状態に実現した変化を表す。

```text
P_i,t0 -> P_i,t1
```

P は一般に非加法的であり、ΔP を普遍的な算術差として定義しない。

---

## 8. 時間型と E[ΔK]

主体側の主要な時間型は、普遍的な状態遷移関数を固定せず、概念的に

```text
(K_t0, P_t0)
      ↓ conditions
A_(t0,t1]
      ↓ realized processes / resource use
(K_t1, P_t1)
```

と置く。

K には減価償却・自然損耗・災害等、A を介さない変化もありうる。これは必要な projection で別途扱う。

### 期待実現変化

主体は K を利用する前に、その利用・行為によって生じる ΔK について期待を持ちうる。

```text
E_i[ΔK(S, τ)]
```

は、対象 scope `S`・区間 `τ` における**実現資源・資本変化について主体 i が形成する forecast** を表す。

`E_i[ΔK]` は desire / preference / plan ではない。望ましさや選好は P_i に属する。

ΔK が多次元・異質で expectation を直接定義できない場合は、projection 側で必要な quantitative representation を定める。Core は普遍的な確率測度・数量化・期待形成式を固定しない。

候補 action の比較が必要なら、必要な projection で action-contingent forecast を置ける。

```text
E_i[ΔK(S, τ) | a, I_i]
```

---

## 9. 3つの管理合理性公理

VFT の管理・意思決定記述では、合理性を次の3則へ集約する。

1. **resource-realization rule**：望ましい resource / capital outcome の実現へ向けて A を動かす。
2. **activity-flow rule**：必要な activity / process の流れを維持・拡張できるよう K / P / A を調整する。
3. **P-downside rule**：P 側の大幅な毀損により主体・組織・系の A が成立しなくなることを防ぐ。

3則は actor type ではなく、**意思決定合理性の公理系**である。同一 actor が3則を同時に考慮し、文脈・制度・役割・組織構造・時間 horizon に応じて比重・優先順位・分担が変わる。

```text
resource-realization -> resource outcome
activity-flow        -> process continuity / expansion
P-downside            -> shared-P / expectation-side viability
```

### P-downside と共有 P

R3 が対象とする P は、客観的な社会価値ではない。対象主体集合の `P_i` の分布・共有部分・信頼・期待等のうち、将来の A の成立に必要なものを projection ごとに定める。

したがって R3 の実装は、aggregate P の真値最大化ではなく、共有 P の毀損、離反、不信、破綻期待、将来不安等が system viability を壊すことを防ぐ形になる。

P の真値は直接観測できないため、計測では対象主体・P 次元・proxy・threshold 等を事前に定める。

### 文脈依存の比重

必要な quantitative projection では、context-dependent priority / weight / constraint を置ける。ただし具体的 objective、weight、lexicographic priority、threshold 等は projection-specific であり、3則そのものではない。

自給自足では単一 actor が3則をすべて担える。国家レベルの資本主義社会を粗視化すると、典型的には

```text
individuals -> resource-realization heavy
firms       -> activity-flow heavy
state       -> P-downside heavy
```

と分化して見えるが、固定的な actor-type assignment ではない。

組織内部でも operational / managerial / governance の各層で同様の比重差が現れうる。

---

## 10. 経済学への射影

### plan / choice と forecast

必要な economic projection では、A に含まれる planned / chosen net resource change を補助的に `x_i` と書ける。

```text
x_i          = planned / chosen resource change
E_i[ΔK(...)] = expected realized resource change
```

予算制約・feasibility は plan / choice 側へ置き、forecast と区別する。

純粋交換の基本例では、射影先の符号規約・価格体系のもとで

```text
p · x_i <= 0
```

のような budget feasibility を置ける。これは VFT Core の普遍式ではない。

### compatibility / market equilibrium

- **inter-agent compatibility / feasibility**：各主体の plan が相互に実行可能・両立可能であること
- **market equilibrium**：compatibility に加え、射影先理論の choice / optimality / best response / clearing 条件が成立すること
- **会計整合**：同じ実現事象を同一 accounting boundary / rule で記帳した結果が整合すること
- **定常状態**：対象 K の増減等について別途定める状態条件

これらは別概念である。

### 使用価値・労働価値・交換価値

VFT は、マルクス経済学が区別した使用価値・労働・交換価値・余剰・蓄積の骨格を、特定の政治的・規範的結論を前提にせず経済射影へ取り込める。

- **使用価値**：ある K が、特定目的の A や resource transformation を実際に可能にする機能・有用性。目的の望ましさは P に依存しうるが、K が何を可能にするかという機能と価格は区別する。
- **労働価値**：生産・変換過程へ投入された labor activity / labor time を価値記述の尺度として用いる射影。必要なら socially necessary labor time 等の benchmark を追加できるが、「労働だけがすべての価値の唯一の源泉である」という規範・形而上学的主張を Core へ置かない。
- **交換価値・価格**：市場交換・会計上の valuation / representation。使用価値や労働投入量と同一ではない。
- **余剰**：実現した複数の ΔK を指定した valuation / accounting rule で共通尺度化し、差し引いた後に残る accounting residual。余剰の存在から直ちに搾取等の規範判断を導かない。

この分離により、使用価値、労働投入、価格、利益、余剰を一つの “value” へ潰さず、同じ K / P / A / ΔK 構造上で比較できる。

### ミクロ／マクロ接続

VFT ではミクロとマクロを別々の K として置かない。

```text
micro:
(K_i, P_i) -> A_i -> ΔK records

              ↓ same common K

macro:
ownership distribution / production / accumulation / shared P
```

個々の A_i が同じ K の保有分布・構成を変化させる。マクロでは、その同じ K と ΔK records を別の accounting boundary / aggregation scope から観測する。

surplus の帰属・分配が次期 `K_i` を変えれば、個別主体の蓄積と社会全体の資本構成を同じ系列上で追跡できる。

### utility / profit / supply-demand

utility / profit 等は3則の特殊化ではなく、具体的な意思決定を数量化・評価するときの関数・指標・proxy として扱う。

price / supply / demand / market equilibrium は、複数主体の planned change を相互調整する economic mechanism であり、第4の合理性公理ではない。

---

## 11. 計測

VFT は K / K_i / P / ΔK の完全観測を前提としない。

- K / K_i：会計記録、資産台帳、物量観測、調査、制度記録等から部分的に把握する
- P_i：調査、発話、選択、信用・期待 proxy 等から推定する
- shared P：複数主体の P proxy の共通性・分布として推定する
- A_i：外部 action event は直接観測できる場合があり、内部 decision / interpretation は proxy を要する
- ΔK：記帳または利用後の最終結果からトレースする
- surplus：指定した会計・評価規則により ΔK records を集約して算出する

P proxy が market outcome と同時決定される場合は、時間順序、post-treatment、outcome leakage を区別する。

3則を empirical decision model へ落とす場合は、対象 actor/context、P scope、candidate action、time horizon、評価 proxy、制約条件を事前に固定する。

---

## 12. スケール

個人・組織・社会・文明を、固定された独立世界ではなく、観測スケールと accounting / ownership boundary の違いとして扱う。

ミクロとマクロで K は共通だが、観測・集約する座標、単位、会計境界、対象 actor は変わりうる。

組織・国家等を単一主体として扱う場合は近似であり、内部主体・K_i 分布・P_i 分布・A の集約による情報損失を明示する。

---

## 13. Core で固定しないもの

以下は応用・実証・追加議論で決める。

- K / P の標準次元
- K_i の普遍的な所有・帰属判定関数
- K / P の完全観測可能性
- A の普遍的 deterministic choice function
- K / P の普遍的状態遷移関数
- E[ΔK] の普遍的確率測度・期待形成式
- ΔK records の普遍的な会計・評価・集約規則
- surplus / profit / price / labor-value 等の普遍的換算式
- 3則の具体的 objective / weight / priority / threshold
- inter-agent compatibility / market equilibrium の普遍的条件
- ミクロ／マクロの普遍的 aggregation rule
- 組織・国家等の単一主体近似条件
- proxy と理論変数の具体対応

---

## 14. 関連ノート

- [計測](02_measurement.md)
- [既存概念・応用への射影](../notes/projections.md)
- [拡張・再検討ノート](../notes/future_topics.md)

---

© T. Nuno  
Licensed under CC BY 4.0