# 価値場理論 — 拡張・再検討ノート

> この文書は Core 定義ではなく、今後の展望・具体化候補・再検討事項を保存するためのノートである。

## 1. 集約と分布化

Core では、K は共通の実資源世界、`K_i` は主体ごとの access / usability view、`P_i` / `A_i` は主体ごとの state / process として扱う。

今後の検討候補：

- どの条件で分布化が有効か
- 平均・代表主体で失われる情報
- 多峰性・非対称性
- ネットワーク構造をどこまで残すか
- 集約後の ΔK / ΔP / H が何を代理しているか
- 共有資源・重複アクセスの扱い

---

## 2. K と K_i の表現粒度

K は共通の実資源世界である。

`K_i` は集合論的な部分集合に限定せず、共通 K に含まれる資源・権利・資格・契約・制度状態等から導かれる actor-relative access / usability view とする。

今後の検討候補：

- K の標準次元を設けるか
- 物理資源、時間、技能、情報、関係、権利等の分解
- `K_i` の access / usability の操作化
- relational resource / right の表現
- 共有・排他的アクセスの表現
- stock / flow の境界
- earning capacity、請求権、所得受取等の整理
- 資本概念との対応

---

## 3. P の表現粒度

P は主体ごとの subjective evaluation / expectation state として Core で定義済みである。

他主体 `a` に対する主体 `j` の評価・信用・見通しは `P_j(a)` として区別できる。

今後の検討候補：

- P の標準次元を設けるか
- belief-like / valuation-like / preference-like / credit-assessment-like substate の型区分
- `P_i = (B_i, V_i, C_i, ...)` のような内部型を導入する必要性
- 特定応用でどの期待・評価・信用・信念を抽出するか
- P proxy の操作化
- 同一 observable が K / P の両方に関係する場合の識別
- 他主体・価格・将来条件についての期待をどの粒度で保持するか
- projection ごとの P 次元を観測前に固定する方法

独立した X 等を復活させず、P 一つのまま内部型を持たせる可能性を検討する。

---

## 4. ΔK / ΔP と scope S

Core では `ΔK(S, τ)` を、観測・会計仕様 `S` について K に実現した **state / resource change descriptor** として扱う。

`S` は単なる対象集合ではなく、少なくとも以下を含む。

- 対象資源・主体
- resource coordinates
- accounting boundary
- transformation convention

一般形として、

```text
Y_S(t) = M_S(K_t)
ΔK(S, τ) = δ_S(Y_S(t0), Y_S(t1)) ∈ D_S
```

を用いる。`δ_S` は必ずしも算術差ではなく、加法的 quantitative projection の場合にのみ `δ_S(y0,y1)=y1-y0` とする。

一般形で `Y_S(t0)=Y_S(t1)=y` の場合は `δ_S(y,y)` を no-change descriptor とみなす。数値ゼロを用いるのは加法的 quantitative projection に限る。

`ΔP_i` も一般には算術差ではなく、P の change descriptor / state transition とする。

一方、gross production、gross consumption、transaction volume、resource transformation 等の区間活動量は `ΔK` と分離し、必要に応じて projection-local に

```text
H_S(τ) = h_S((K_t)_{t in τ}, A_τ)
```

のような derived path functional を使う。`A_τ` が区間内 event/process と必要な ordering を保持する。

今後の検討候補：

- `S` の標準的な記述形式
- `M_S` / `δ_S` の型付け
- `H_S` / `h_S` の最小インターフェース
- state change と gross flow / interval activity の会計対応
- 加法表現を採用できる条件
- 非加法成分の quantitative projection
- 個別実現変化と集約 `ΔK` の会計対応
- 共有資源変化と `K_i` 変化の対応
- ΔP proxy の測定誤差

---

## 5. 期待区間変化 E[ΔK]

`E_i[ΔK(S, τ)]` は、主体 `i` が対象 scope / interval について形成する expected realized resource change として Core で区別済みである。

Core では quantitative representation を

```text
q_S : D_S -> V_S
```

と置き、記法上

```text
E_i[ΔK(S, τ)] := E_i[q_S(ΔK(S, τ))]
```

と略記する。`q_S`、値空間 `V_S`、確率測度、情報集合、期待形成式の具体形は projection / measurement model 側で定める。

今後の検討候補：

- `V_S` に要求する代数構造
- `q_S` の同定可能性と座標変換依存性
- expectation operator の確率測度・情報集合
- planned resource change と expected realized resource change の区別
- ex-ante feasible action / contingent plan と expected outcome の区別
- state-wise / almost-sure feasibility
- 期待対象となる消費・生産等の範囲
- `S` / `S_i` / `τ`
- 確率的期待値と定性的 forecast の接続
- 実測可能な expectation survey 等との対応
- 他主体の期待・行動についての予測が P にどう入るか
- `E_i[ΔK]` と実現 `ΔK` の乖離分解

---

## 6. 機能的最適化則

経済・社会 projection では、主体種別ではなく以下の3つの機能を optimization hypothesis として置く候補がある。

1. **resource-realization**：P / expectation のもとで、望む／見込む `ΔK` の実現へ向けて A を選ぶ
2. **activity-flow**：K / P の配置を再構成して持続可能な A-flow を最大化する
3. **P-downside**：主体群の P の大幅な負側・悪化側を抑えるよう K / A を配分・調整する

概念記法：

```text
A_i* ∈ argmax_A R_i(A ; P_i, E_i[ΔK])

(K_f*, P_f*)
  ∈ argmax_(feasible K_f,P_f)
      F_f(A-flow | K_f, P_f)

A_g* ∈ argmin_A L_g^-(P ; observable proxies)
```

`R_i` / `F_f` / `L_g^-` は Core primitive ではなく projection-local objective functional とする。

今後の検討候補：

- resource-realization で「望む」と「見込む」をどう分離するか
- `R_i` が P と E[ΔK] をどの型で参照するか
- A-flow の定義、単位、異質な A 間の比較可能性
- sustainable A-flow の horizon / viability constraint
- activity-flow と profit / revenue / throughput / market share の関係
- 短期的な ΔK 悪化を許容する intertemporal 条件
- P-downside の loss functional と downside の閾値
- 異質な P proxy 間で加法則を仮定しない optimization の形式
- 個人間 P の比較可能性・加減算可能性の条件
- 単一 actor が複数機能を同時に最適化する場合の trade-off
- 機能分業が成立する条件
- 機能間の conflict / coordination
- 3則が falsifiable な予測をどこまで生むか

### 自給自足と制度的分業

3機能は actor type ではないため、自給自足では単一 actor が全部を担いうる。

```text
single actor
  ├─ resource-realization
  ├─ activity-flow
  └─ P-downside
```

資本主義では概ね、individual / firm / state に重点が分化する候補がある。

今後の検討候補：

- 自給自足 household / family unit で3則をどう観測するか
- household production と firm production の境界
- 市場形成前後で最適化機能の分業がどう変わるか
- 資本主義以外の制度での分業パターン
- 国家機能が弱い社会で P-downside を誰が担うか
- cooperative / commune / family business の複合機能

---

## 7. 会計的予算制約

経済射影では、A に含まれる planned / chosen net resource change を projection-local に `x_i` と置ける。

取得を正・処分／供給を負とする符号規約、価格・会計換算ベクトルを `p` とする純粋交換の基本例では、

```text
p · x_i <= 0
```

として budget feasibility を表せる。`p · x_i = 0` は self-financing / budget exhaustion 等を追加仮定した特殊形である。

今後の検討候補：

- `x_i` の標準的な符号規約
- 所得・生産収入・投資・借入・移転を含む一般予算式
- intertemporal budget constraint
- 信用枠・金融請求権を含む予算制約
- 非市場資源の会計換算
- planned action と expected outcome の分離

---

## 8. compatibility / market equilibrium / 会計整合 / 定常状態

以下を分離して扱う。

- **inter-agent compatibility / feasibility**：economic projection が追加する、各主体の budget-feasible な `x_i` が相互に実行可能・両立可能であるという条件
- **market equilibrium**：compatibility に加え、射影先理論が choice / optimality / best response / market-clearing 等を与えた状態
- **会計整合**：同一事象の state change / interval activity を共通の会計境界・換算規則で記録した結果が収支上整合すること
- **定常状態**：対象 K の増減が小さい等、別途定める状態条件

compatibility 自体も Core からは導出されない。

---

## 9. 分散的調整と「見えざる手」

各主体が `K_i` / `P_i` のもとで budget-feasible な `x_i` を選び、価格・取引・信用等を介してその選択を修正することで、主体間の不整合が分散的に調整される可能性がある。

この構造を古典経済学の「神の見えざる手」へ射影することは可能だが、現時点では projection candidate であり、Core の確立済み主張ではない。

---

## 10. ミクロ／マクロ接続の操作化

VFT ではミクロとマクロを別々の K として置かない。**同じ common K / K transition を異なる `S` から観測する**ことが存在論的な接続である。

micro observable から macro observable を再構成する場合には、projection-local な aggregation / coarsening rule が必要になる。

今後の検討候補：

- 同じ K transition を異なる `S` がどう記述するか
- micro / macro の measurement consistency
- gross flow / interval activity をどの `H_S` で表現するか
- `S` の拡張と aggregation rule の関係
- stock-flow consistent な観測再構成
- 個人期待と集計マクロ変数の識別
- 政策 A → K 上の制度条件 → ΔP_i → A_i → ΔK / H の経路
- macro observable から micro structure をどこまで逆推定できるか

---

## 11. 評価経済・信用経済への射影

VFT の有力な応用候補として、公開された評価情報が他主体の subjective evaluation / expectation を介して実資源アクセスへどう変換されるかを扱うことがある。

評価対象を `a`、評価者を `j` とすると、基本的な分離は以下。

- 公開レビュー、rating、公開された評判情報 → K 上の accessible information / observable
- 主体 `j` が主体 `a` に対して形成する評価・信用・返済見込み・将来見通し → `P_j(a)`
- 主体 `a` に実際に付与された信用枠、請求権、契約上の権利、取引アクセス → K / `K_a`

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

---

## 12. 期待変化の集約と余剰

同一共通 scope に対する複数主体の `E_i[ΔK(S, τ)]` を単純和して aggregate resource change としない。

異なる主体の `E_i[ΔK(S_i, τ)]` を集約する場合は、各 `S_i`、`q_S`、`V_S`、会計・換算規則を先に定める。

標準経済学上の surplus へ接続するには追加 mapping が必要である。

---

## 13. A の観測と順序

A の外部 action event は直接観測できる場合がある一方、内部 decision / observation / interpretation は proxy を要する場合がある。

Core の actor-side temporal typing は、

```text
(K_t0, P_t0)
      ↓ conditions
A_(t0,t1]
      ↓ realized interval processes
(K_t1, P_t1)
```

とする。A を介さない K / P 変化は別経路として必要な projection で扱う。

P → A の因果関係を検証する場合、A 区間内で情報受容・解釈による P 更新が起き、その後の decision / action に影響するなら、区間を分割するか event ordering を保持する。

---

## 14. 価値場の最小形式化

現行 Core では、価値場を K / K_i / P の配置・関係が A を条件づける structural framework として定義し、独立した V や普遍的選択関数を置かない。

したがって現時点の Core は、経験的選択則そのものより **ontology / modeling language / common state representation** としての性格が強い。

今後、説明力・反証可能性のために最低限の形式化が必要になった場合は、例えば

```text
Γ_i(K_i, P_i) ⊆ 𝒜_i
```

のような action correspondence / admissible or plausible action set の導入を検討できる。

---

## 15. P の反証可能性

P が観察後の residual state にならないよう、projection / empirical model ごとに、採用する P 次元、proxy、proxy admissibility、A / E[ΔK] への mapping、事前予測・識別条件を観測前に固定する必要がある。

---

## 16. spillover / externality の区別

主体間の影響はまず spillover / cross-agent effect として記述する。

---

## 17. 組織・国家等の集約主体近似

組織・国家等を単一主体として扱うことは Core 前提ではない。

必要な場合は近似として導入し、対象主体、共通 K の対象範囲、各主体の `K_i` / `P_i`、A の集約方法、ΔK / H の会計・集約規則、情報損失、内部対立を明示する。

---

## 18. 実証・計量化

今後の具体化候補：

- 共通 K の観測設計
- `K_i` の access / usability
- P proxy / admissibility
- K / P 識別
- `P_j(a)` の評価者・評価対象の識別
- A の直接観測と潜在 decision の proxy
- temporal typing / event ordering の操作化
- ΔK / ΔP の generic change mapping
- `H_S` / `h_S` の操作化
- `M_S` / `δ_S` の操作化
- gross flow / net stock change の同時計測
- `q_S : D_S -> V_S` の操作化
- `E[ΔK]` の expectation operator / 推定
- functional optimization hypothesis の objective / constraints / horizon
- 自給自足と制度的分業の比較実証
- planned / expected / realized change の分離
- compatibility / market equilibrium / accounting identity の同時計測
- common K に基づく micro / macro observation consistency
- 公開評価情報 → `P_j(a)` → K / `K_a` → ΔK の因果計測
- 測定誤差・欠測
- ケーススタディ
- 反実仮想設計

---

© T. Nuno  
Licensed under CC BY 4.0