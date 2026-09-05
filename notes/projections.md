# 価値場理論 — 既存概念・応用への射影ノート

> この文書は価値場理論のコア定義ではなく、既存概念・応用領域への射影候補を保存するためのノートである。

## 1. 射影の基本方針

価値場理論では、

- `K`：共通の実資源世界
- `K_i`：共通 K に対する主体 `i` の access / usability view
- `P_i`：主体 `i` の subjective evaluation / expectation state
- `A_i`：主体 `i` 側の actor-side process / event
- `ΔK(S, τ)`：観測・会計仕様 `S`・時間区間 `τ` における K の state / resource change descriptor
- `ΔP_i`：主体 `i` の P に実現した change descriptor / state transition
- `E_i[ΔK(S, τ)]`：主体 `i` が対象範囲・区間について形成する expected realized resource change

を用いる。

K の資源世界そのものは主体ごとに別々に存在しない。actor-relative なのは `K_i`、`P_i`、およびそこから形成される期待評価である。

本理論でいう resource は物的資源に限られず、外部に実在し行使・利用・参照可能な情報、権利、資格、契約、制度状態、金融請求権等を含みうる。

`K_i` は集合論的な部分集合を必ずしも意味しない。共有情報、権利、信用枠等を含むため、共通 K 上の条件から導かれる actor-relative access / usability view とする。

P は projection-specific な内部型を持ちうる多次元 state であり、belief-like / evaluative / preference-like / relational-trust-like な成分を概念上区別できる。独立 primitive を追加する意味ではない。

他主体 `a` について主体 `j` が保持する評価・信用・見通し等は `P_j(a)` と書く。これは `a` 自身の P ではなく、評価者 `j` の `P_j` に含まれる主観状態である。

`S` は対象資源・主体だけでなく、resource coordinates、accounting boundary、transformation convention を含む観測・会計仕様である。

state change は、

```text
Y_S(t) = M_S(K_t)
ΔK(S, τ) = δ_S(Y_S(t0), Y_S(t1)) ∈ D_S
```

として表す。`δ_S` は必ずしも算術差ではなく、加法的 quantitative projection の場合にのみ通常の差分を用いる。

gross production、gross consumption、transaction volume 等の区間活動量は `ΔK` へ含めず、必要に応じて

```text
H_S(τ) = h_S((K_t)_{t in τ}, A_τ)
```

のような derived path functional として分離する。

期待値を取る場合は quantitative representation を

```text
q_S : D_S -> V_S
```

とし、記法上 `E_i[ΔK(S,τ)] := E_i[q_S(ΔK(S,τ))]` と略記する。

候補 action を比較する場合は、必要に応じて

```text
E_i[ΔK(S,τ) | A=a, I_i]
```

のような action-contingent forecast を用いる。P 内の outlook / belief と、特定 `(S,τ,a)` に対する forecast は区別する。

---

## 2. 3つの管理合理性公理

VFT の管理・意思決定記述では、合理性を次の3則へ集約する。

1. **resource-realization rule**：望ましい resource outcome / state change の実現へ向けて A を動かす。
2. **activity-flow rule**：K / P / A の配置を調整し、必要な activity / process の流れを維持・拡張する。
3. **P-downside rule**：主体・組織・系の行動成立を阻害するほどの P の負側・毀損を抑える。

3則は actor type ではなく、**意思決定合理性の公理系**である。同一 actor が3則を同時に考慮しうる。

3則の管理対象は、概念的には

```text
resource-realization -> outcome / resource-state realization
activity-flow        -> process / activity continuity and expansion
P-downside            -> viability / breakdown prevention on the P side
```

と区別する。

同じ A が複数則へ寄与することはありうる。したがって、A を3種へ排他的に分類するのではなく、**意思決定が outcome / process / viability のどこを、どの程度の優先度で制御しようとしているか**を区別する。

この outcome / process / viability の3対象を、現行 VFT では管理合理性の最小公理系として採用する。形式的な独立性・完備性・最小性の証明は今後の課題だが、現行理論上は3則を前提として意思決定を構成する。

### 文脈依存の比重

各 actor が3則へ置く比重・優先順位は、文脈、役割、組織構造、制度、時間 horizon によって変わる。

quantitative projection では必要に応じて、

```text
w_i,c = (w_R, w_F, w_D)
```

のような context `c` に依存する priority / weight を導入できる。ただしこれは Core primitive ではなく、線形加重和や `Σw=1` を普遍的に要求しない。lexicographic priority、constraint、threshold 等でもよい。

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

必要な quantitative model では、各則に対応する projection-specific な評価 `J_R(a)`, `J_F(a)`, `J_D(a)` と、それらを文脈に応じて統合する decision rule を置ける。

```text
A_i* ∈ argmax_{a ∈ feasible actions}
       Φ_i(J_R(a), J_F(a), -J_D(a); w_i,c)
```

`J_R` / `J_F` / `J_D` / `Φ_i` / `w_i,c` は3則そのものではなく、対象 projection における数理化である。

### P-downside の位置づけ

P-downside は、P が観測しにくいから導入するのではない。局所的な resource-realization / activity-flow が進んでも、不信、離反、破綻期待、将来不安等が大きく悪化すれば、その後の A 自体が成立しにくくなり、組織・制度・社会の viability が損なわれうる。

したがって R3 は、**P 側の毀損が action system の成立条件を壊すことを防ぐ管理合理性**として置く。異質な P proxy 間に普遍的加法則がないことは、具体的操作化で aggregate-P maximization より downside / threshold / viability constraint が使いやすい理由の一つであり、R3 の唯一の論拠ではない。

---

## 3. 自給自足・制度的分業・組織階層

### 自給自足

3則は actor type ではないため、市場や企業や国家が存在しない自給自足でも適用できる。

```text
single actor
  ├─ resource-realization
  ├─ activity-flow
  └─ P-downside
```

自給自足では単一 actor が3則を同時に担う。

### 国家レベルのマクロでの制度的分業

資本主義制度を国家レベルのマクロで粗視化すると、**3則の主たる比重・担当が概ね次のように分化して見える**。

```text
individuals -> resource-realization heavy
firms       -> activity-flow heavy
state       -> P-downside heavy
```

これは actor type と3則を一対一対応させる主張ではない。individual も R2/R3、firm も R1/R3、state も R1/R2 を担いうる。制度・文脈に応じて、どの actor がどの合理性を主として引き受けるかが変わる。

したがって市場・企業・国家は3則の定義ではなく、**同じ公理系の比重と機能分担が制度化された形**として読む。

### マネジメント三階層としての解釈

実行・中間管理・統治に相当する階層的な機能分化は、近代企業に限らず長期にわたる組織制度の中で反復して観察される。VFT が三階層の存在を新規に予測するのではなく、**既知の階層構造を3則の比重・担当の分化として記述する**。

典型的には、

```text
operational / execution -> resource-realization heavy
managerial              -> activity-flow heavy
governance              -> P-downside heavy
```

と読める。

ただし各階層は他の2則も担いうる。小規模組織、owner-manager、自給自足では同一 actor に3則が重なり、危機時・成長時・再編時には同じ役割でも比重が変化しうる。

---

## 4. 経済学への射影

### 主体別期待と意思決定

経済射影では、`K_i` を予算・保有資源・供給能力等の制約側、`P_i` を価格、他主体、生産・消費、信用、将来条件等についての見通し・評価を含む主観状態として読める。

必要な economic projection では、A に含まれる planned / chosen net resource change を補助的に `x_i` と書く。

```text
x_i          = planned / chosen net resource change
E_i[ΔK(...)] = expected realized resource change
```

`x_i` は projection-local な補助記法であり、Core primitive ではない。

### 会計的予算制約

`x_i` を取得を正・処分／供給を負とする planned net resource change とし、価格・会計換算ベクトルを `p` とする純粋交換の基本例では、

```text
p · x_i <= 0
```

のように budget feasibility を表せる。`p · x_i = 0` は self-financing / budget exhaustion 等を追加仮定する場合の特殊形である。

### 主体間整合条件

各主体の budget-feasible な `x_i` が、価格・取引条件等のもとで相互に実行可能・両立可能であることを inter-agent compatibility / feasibility condition として追加できる。

compatibility 自体は economic projection 側の条件であり、VFT Core や3則から自動的に導出されるものではない。market equilibrium と呼ぶには、さらに射影先理論の choice / optimality / best response / market-clearing 等の条件が必要である。

### utility / profit / supply-demand との関係

utility / profit 等は3則の特殊化そのものではなく、**3則をもとに具体的な意思決定を数量化するときに使われる評価関数・指標・proxy** として扱う。

- utility は、resource-realization を考える際に候補 outcome の望ましさをスカラー化する一つの方法である。
- profit は、activity-flow を考える際に使いうる accounting / performance 指標の一つである。going-concern の文脈で sustained activity と整合する場合に強い proxy になりうるが、R2 自体を profit maximization と同一視しない。
- price / supply / demand / market equilibrium は、複数主体が各自の文脈依存の3則配分のもとで形成した planned change `x_i` を相互に調整する仕組みとして扱う。

国家レベルの典型的分業では、需要側の individual は R1 比重が高く、供給側の firm は R2 比重が高いことが多い。市場はそれらを含む planned change 間の compatibility を調整する。

したがって需給均衡は第4の管理則ではない。また、正式な `E_i[ΔK]` は forecast であるため、需給調整を expectation と realized `ΔK` の一致最大化とは置かない。

### 会計整合

会計整合、主体間 compatibility、market equilibrium、定常状態は別概念である。

対象 scope の net state change は `ΔK`、gross production / consumption / transaction volume / transformation 等は必要に応じて `H_S` として分離して記録する。

### ミクロ／マクロの共通 K 接続

VFT ではミクロとマクロを別々の資源世界として置かない。**両者は同じ common K と同じ K transition を異なる観測・会計仕様 `S` から記述したもの**である。

```text
                 common K
                /        \
          S_micro        S_macro
             ↓              ↓
      micro observation  macro observation
```

micro observable から macro observable を再構成する場合にのみ、projection-local な aggregation / coarsening rule を追加する。

---

## 5. 評価経済・信用経済への射影候補

評価対象を `a`、評価者を `j` とする。

- 公開レビュー、rating、公開された評判情報 → K 上の accessible information / observable
- 主体 `j` が主体 `a` に対して形成する評価・信用・返済見込み・将来見通し → `P_j(a)`
- その結果として実際に `a` に付与された信用枠、金融請求権、契約上の権利、取引アクセス → K / `K_a`

候補経路：

```text
public rating / review information in K
              ↓ observed by j
            P_j(a)
              ↓
            A_j
              ↓
rights / contract / credit conditions in K
              ↓
            K_a
              ↓
        realized ΔK
```

これにより、公開情報 → 他者の主観評価 → 行動 → 実アクセス条件 → 実資源変化という経路で評価・信用経済を記述できる可能性がある。

---

## 6. 選好・消費・生産・市場

### 選好

選好を独立した Core 変数には置かない。主体ごとの選好差は P の evaluative / preference-like component として扱う。

### 消費 / 生産 / 交換

消費・生産・交換を別の存在論として置かず、主体が共通 K のどの resource coordinates / accounting boundary へどう関与するかを表す economic action / accounting interpretation として扱う。

### spillover / cross-agent effect

```text
A_i -> change in K affecting K_j
A_i -> change in P_j   (i != j)
```

主体 `i` の A が他主体 `j` の K へのアクセス条件や P に影響する場合、まず spillover / cross-agent effect として記述する。externality と呼ぶ場合は、対象 economic projection 側の定義条件を追加する。

---

## 7. 国家・政治・組織

国家や組織を自動的に単一主体として扱わない。

- 政策・公約・宣言：主体の A
- 公開された支持率・評価値：K 上の observable / accessible information
- それを他主体がどう評価・解釈するか：各 `P_j(a)` / `P_j`
- 政策実施による state / resource change：ΔK
- 政策実施量等の interval activity：必要に応じて `H_S`
- 政策等により誘発された主観状態変化：ΔP_i

単一主体へ還元する場合は近似条件と集約規則を明示する。

---

## 8. 射影時に明示するもの

1. 共通 K の対象範囲
2. 対象主体集合
3. 各主体の K への access / usability relation
4. P の採用次元・型・proxy と proxy admissibility
5. 他者評価を扱う場合の評価者 `j` と評価対象 `a`
6. A の観測単位と event ordering
7. 時間窓 `τ`
8. temporal typing と actor-side channel の範囲
9. `S` / `S_i` の resource coordinates / accounting boundary / transformation convention
10. `M_S` / `δ_S` または対応する state-change mapping
11. `H_S` を使う場合の `h_S` / path functional
12. ΔK / ΔP / H の操作化
13. `q_S : D_S -> V_S`
14. `E_i[ΔK]` の expectation operator / 推定方法
15. action-contingent forecast を使う場合の conditioning / information set
16. 3則の context-dependent priority / weight / constraint
17. candidate action / feasible set
18. action が誘導する future trajectory と各則の評価方法
19. planned / chosen change `x_i` の定義と符号規約
20. 価格・会計換算規則
21. 主体別予算制約
22. compatibility を扱う場合の相互両立条件
23. market equilibrium と呼ぶ場合の choice / optimality / best response / clearing 条件
24. 会計恒等式の境界
25. surplus へ射影する場合の valuation / utility / WTP / WTA / cost mapping
26. 評価・信用を扱う場合の public information → `P_j(a)` → K / `K_a` 経路
27. 情報損失

---

© T. Nuno  
Licensed under CC BY 4.0