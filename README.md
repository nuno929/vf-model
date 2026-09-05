# 価値場理論（Value-Field Theory）

**Theory refresh — Draft**  
Author: **T. Nuno**  
License: **CC BY 4.0**

---

## 1. 概要

価値場理論（Value-Field Theory; VFT）は、個人・組織・社会で生じる変化を、**共通の実資源状態 K と、各主体が保持する主観的な評価・期待状態 P の関係が、各主体の actor-side process / event A をどのように条件づけるか**として記述する構造的フレームワークである。

VFT Core は、単独で経験的予測を与える仮説というより、**ontology / modeling language / common state representation** として位置づける。Core 自体は普遍的な deterministic choice function、更新則、均衡則、集約則を固定せず、具体的な経験予測は各 projection / empirical model が担う。

その上で VFT は、管理・意思決定を記述するための **3つの管理合理性公理**を置く。3則は actor type を定義するものではなく、意思決定が何を合理性の対象として考慮するかを定める上位原則である。

### K の存在論

K が参照する資源世界は主体ごとに別々に存在するのではなく、**同一の物理的・社会的な実資源世界**を前提とする。

本理論でいう resource は物的資源に限定されない。時間、身体、技能、知識、情報、関係、設備、資金、インフラに加え、**外部に実在し行使・利用・参照可能な権利、資格、契約、制度状態、金融請求権等**も K に含みうる。

各 `K_i,t` は、その共通 K のうち、主体 `i` が時点 `t` に実際にアクセス・利用・行使・参照可能な範囲を表す actor-relative view である。`K_i` は独立した資源世界や独立 state ではなく、共通 K に含まれる条件から導かれる access / usability view として扱う。

### P と期待値

各 `P_i,t` は、主体 `i` が保持する将来の見通し・評価・選好・信用・信念等からなる多次元の **subjective evaluation / expectation state** である。

概念上、P は少なくとも belief-like / evaluative / preference-like / relational-trust-like な成分を含みうる。これは新しい primitive を追加する意味ではなく、projection ごとにどの P 成分を参照するかを型として区別するための整理である。

他主体 `a` に対して主体 `j` が保持する評価・信用・見通し等は `P_j(a)` と表す。これは評価対象 `a` の P ではなく、評価者 `j` の `P_j` に含まれる主観状態である。

P 内の belief / outlook と、特定の scope・時間窓・candidate action に対する forecast は区別する。観測・会計仕様 `S` と時間区間 `τ=[t0,t1]` における expected realized resource change を、必要な quantitative projection では

```text
E_i[ΔK(S, τ)] := E_i[q_S(ΔK(S, τ))]
```

と略記する。候補 action を比較する場合は、必要に応じて

```text
E_i[ΔK(S, τ) | A = a, I_i]
```

のような action-contingent forecast を用いる。

---

## 2. コア変数

```text
K_t
K_i,t = access / usability view derived from K_t
P_t = (P_i,t)_{i in I}
A_τ = (A_i,τ)_{i in I}
```

- **K**：共通の実資源世界を構成する多次元の resource / capability state
- **K_i**：共通 K に対する主体 `i` の access / usability view
- **P_i**：主体 `i` の subjective evaluation / expectation state
- **A_i**：主体 `i` 側で生じる process / event
- **ΔK(S, τ)**：観測・会計仕様 `S` における K の state / resource change descriptor
- **ΔP_i**：主体 `i` の P に実現した change descriptor / state transition
- **E_i[ΔK(S, τ)]**：quantitative representation を介した expected realized resource change

`P_t` / `A_τ` は集合ではなく actor identity を保持する indexed family として扱う。

### state change と interval activity の分離

`ΔK` は K の state / resource change に予約する。

```text
Y_S(t) = M_S(K_t)
ΔK(S, τ) = δ_S(Y_S(t0), Y_S(t1)) ∈ D_S
```

`δ_S` は必ずしも算術差ではない。加法的 quantitative projection の場合に限って通常の差分や数値ゼロを用いる。

gross production / consumption / transaction volume / transformation 等の区間活動量は `ΔK` へ含めず、必要な projection / measurement で

```text
H_S(τ) = h_S((K_t)_{t in τ}, A_τ)
```

のような derived path functional として分離する。

---

## 3. K / P / A の時間型

主体側の主要な時間型は、普遍的な状態遷移関数を固定せず、

```text
(K_t0, P_t0)
      ↓ conditions
A_(t0,t1]
      ↓ realized interval processes
(K_t1, P_t1)
```

と置く。これは **actor-side channel の temporal typing** であり、減価償却・自然消耗・災害・記憶減衰等の A を介さない変化は別経路として必要な projection で扱う。

---

## 4. 3つの管理合理性公理

VFT の管理・意思決定記述では、合理性を次の3則へ集約する。

1. **resource-realization rule**：望ましい resource outcome / state change の実現へ向けて A を動かす。
2. **activity-flow rule**：K / P / A の配置を調整し、必要な activity / process の流れを維持・拡張する。
3. **P-downside rule**：主体・組織・系の行動成立を阻害するほどの P の負側・毀損を抑える。

3則は actor type ではなく、**意思決定合理性の公理系**である。同一 actor が3則を同時に考慮しうる。

概念的な管理対象は、

```text
resource-realization -> outcome / resource-state realization
activity-flow        -> process / activity continuity and expansion
P-downside            -> viability / breakdown prevention on the P side
```

と区別する。同じ A が複数則へ寄与することはありうるため、A を排他的に3分類するのではなく、**意思決定がどの管理対象をどの程度の優先度で制御しようとしているか**を見る。

### 文脈依存の比重と分業

3則の比重・優先順位は、actor、文脈、制度、役割、組織構造、時間 horizon によって変わる。

必要な quantitative projection では、例えば

```text
w_i,c = (w_R, w_F, w_D)
```

のような context `c` に依存する priority / weight を導入できる。ただし線形加重和や `Σw=1` は普遍的に要求しない。lexicographic priority、constraint、threshold 等でもよい。

自給自足では単一 actor が3則を同時に担う。企業内部でも operational / managerial / governance の各層で比重が分化しうるが、役職と3則を一対一には固定しない。

### 意思決定の共通型

3則をもとに具体的な意思決定を記述する場合、candidate action が将来の K / P / A-flow / ΔK 等をどう変えるかを評価する。

```text
current K / P
    + candidate action a
          ↓
induced / expected future trajectory
(K', P', A-flow, ΔK, ...)
          ↓
R1 / R2 / R3 に照らした評価
          ↓
decision
```

必要な quantitative model では、各則に対応する `J_R(a)`, `J_F(a)`, `J_D(a)` と、それらを文脈に応じて統合する projection-specific な decision rule を置ける。

```text
A_i* ∈ argmax_{a ∈ feasible actions}
       Φ_i(J_R(a), J_F(a), -J_D(a); w_i,c)
```

`J_R` / `J_F` / `J_D` / `Φ_i` / `w_i,c` は3則そのものではなく、対象 projection の数理化である。

### P-downside の位置づけ

R3 は、P が観測しにくいから導入するのではない。局所的な resource-realization / activity-flow が進んでも、不信、離反、破綻期待、将来不安等が大きく悪化すれば、その後の A 自体が成立しにくくなり、組織・制度・社会の viability が損なわれうる。

したがって P-downside は、**P 側の毀損が action system の成立条件を壊すことを防ぐ管理合理性**として置く。具体的な quantitative projection では downside loss、threshold、viability constraint 等を選べる。

---

## 5. 経済学への射影

### plan / choice と forecast

Economic projection では、A に含まれる planned / chosen net resource change を `x_i` と書ける。

```text
x_i          = planned / chosen net resource change
E_i[ΔK(...)] = expected realized resource change
```

`x_i` は projection-local な補助記法であり、Core primitive ではない。

純粋交換の基本例では、取得を正・処分／供給を負とする符号規約のもと、

```text
p · x_i <= 0
```

として budget feasibility を表せる。`p · x_i = 0` は self-financing / budget exhaustion 等を追加仮定した特殊形である。

### compatibility / market equilibrium / 会計整合

- **inter-agent compatibility / feasibility**：各主体の budget-feasible な `x_i` が相互に実行可能・両立可能であること
- **market equilibrium**：compatibility に加えて射影先理論の choice / optimality / best response / clearing 条件が成立すること
- **会計整合**：同一事象の state change / interval activity を共通会計で記録した結果が整合すること
- **定常状態**：対象 K の増減が小さい等、別途定める状態条件

これらは別概念として扱う。

### ミクロ／マクロの共通 K 接続

VFT ではミクロとマクロを別々の資源世界として置かない。**同じ common K / K transition を異なる観測・会計仕様 `S` から記述する**ことで存在論的に接続する。

### 国家レベルのマクロでの制度的分業

3則は actor type と一対一対応しないが、**国家レベルの資本主義社会を粗視化すると、主たる比重が概ね次のように分化して見える**。

```text
individuals -> resource-realization heavy
firms       -> activity-flow heavy
state       -> P-downside heavy
```

これは individual が R2/R3 を、firm が R1/R3 を、state が R1/R2 を持たないという意味ではない。各 actor は3則を持ちうるが、制度的な分業によって主担当・比重が異なるという解釈である。

### utility / profit / supply-demand との関係

utility / profit 等は3則の特殊化そのものではなく、**3則をもとに具体的な意思決定を数量化するときに使われる評価関数・指標・proxy** として位置づける。

- utility は、resource-realization を考える際に候補 outcome の望ましさをスカラー化する一つの方法である。
- profit は、activity-flow を考える際に使いうる accounting / performance 指標の一つである。going-concern の文脈で sustained activity と整合する場合に強い proxy になりうるが、R2 自体を profit maximization と同一視しない。
- price / supply / demand / market equilibrium は、複数主体が各自の文脈依存の3則配分のもとで形成した planned change `x_i` を相互に調整する仕組みとして扱う。

需給均衡は第4の管理則ではない。`E_i[ΔK]` は forecast であるため、需給調整を expectation と realized `ΔK` の一致最大化とは置かない。

---

## 6. 計測

P proxy の admissibility では少なくとも、

- target A / ΔK より前に観測された proxy か
- 同時決定の場合に joint structural / measurement model を明示しているか
- target outcome を使って latent P を事後的に構成していないか
- proxy validity を別データまたは追加制約で検証できるか

を確認する。

3則を用いた意思決定モデルを計測する場合は、actor ごとの比重・優先順位、candidate action、action-contingent future state、各則の評価 proxy、制約集合、時間 horizon、代替モデルを事前に固定する。観察された A だけから事後的に「どの則が働いたか」を自由に割り当てない。

---

## 7. スケールと理論境界

個人・組織・社会・文明といった区分は、固定された独立実体ではなく、観測スケールと内生／外生境界の違いとして扱う。

価値場理論は、以下を普遍的に固定しない。

- K / P / A の単一スカラー化
- 組織・市場・社会の単一主体化
- 独立した選好変数 X
- 独立した価値場変数 V
- P の普遍的更新式
- `q_S` の普遍的定義
- `E[ΔK]` の普遍的形成式・確率測度
- A の普遍的 deterministic choice function
- `H_S` の普遍的定義
- 3則を数量化する具体的 objective / weight / priority rule
- inter-agent compatibility の普遍的条件
- market equilibrium の普遍的 choice / optimality / clearing 条件
- ミクロ／マクロの普遍的集約・導出則
- 特定の観測方法・proxy・統計手法

---

## 8. ドキュメント

### Core

- [モデルノート](docs/01_model_notes.md)
- [計測](docs/02_measurement.md)

### Notes / 今後の展望・応用

- [背景・整理経緯](notes/background.md)
- [既存概念・応用への射影](notes/projections.md)
- [拡張・再検討ノート](notes/future_topics.md)

---

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)  
© T. Nuno