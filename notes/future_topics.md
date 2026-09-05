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

K は共通の実資源世界である。本理論でいう resource は物的資源に限られず、外部に実在し行使・利用・参照可能な情報、権利、資格、契約、制度状態、金融請求権等を含みうる。

`K_i` は集合論的な部分集合に限定せず、共通 K に含まれる条件から導かれる actor-relative access / usability view とする。

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

概念上は、

```text
P_i
├─ epistemic / belief-like components
├─ evaluative / preference-like components
├─ relational / trust-like components
└─ other projection-specific components
```

のような内部型を区別できる。これは独立 primitive を増やす意味ではない。

他主体 `a` に対する主体 `j` の評価・信用・見通しは `P_j(a)` として区別できる。

今後の検討候補：

- P の標準次元を設けるか
- belief-like / valuation-like / preference-like / credit-assessment-like substate の型区分
- `P_i = (B_i, V_i, C_i, ...)` のような内部表記を導入する必要性
- 特定応用でどの期待・評価・信用・信念を抽出するか
- P proxy の操作化
- 同一 observable が K / P の両方に関係する場合の識別
- P 内の general outlook / belief と、特定 `(S,τ,a)` に対する forecast の関係
- projection ごとの P 次元を観測前に固定する方法

独立した X 等を復活させず、P 一つのまま内部型を持たせる方向を基本とする。

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

を用いる。`δ_S` は必ずしも算術差ではなく、加法的 quantitative projection の場合にのみ通常の差分を用いる。

`ΔP_i` も一般には算術差ではなく、P の change descriptor / state transition とする。

一方、gross production、gross consumption、transaction volume、resource transformation 等の区間活動量は `ΔK` と分離し、必要に応じて projection-local に

```text
H_S(τ) = h_S((K_t)_{t in τ}, A_τ)
```

のような derived path functional を使う。

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

と略記する。

candidate action ごとの forecast が必要な場合は、

```text
E_i[ΔK(S, τ) | A=a, I_i]
```

のような action-contingent representation を使える。

今後の検討候補：

- `V_S` に要求する代数構造
- `q_S` の同定可能性と座標変換依存性
- expectation operator の確率測度・情報集合
- planned resource change と expected realized resource change の区別
- ex-ante feasible action / contingent plan と expected outcome の区別
- action-contingent forecast の conditioning / causal semantics
- state-wise / almost-sure feasibility
- 確率的期待値と定性的 forecast の接続
- 実測可能な expectation survey 等との対応
- P 内の belief / outlook から特定 action forecast をどう生成するか
- `E_i[ΔK]` と実現 `ΔK` の乖離分解

---

## 6. 3つの管理合理性公理

VFT の管理・意思決定記述では、合理性を次の3則へ集約する。

1. **resource-realization**：望ましい resource outcome / state change の実現へ向けて A を動かす
2. **activity-flow**：K / P / A の配置を調整し、必要な activity / process の流れを維持・拡張する
3. **P-downside**：主体・組織・系の行動成立を阻害するほどの P の負側・毀損を抑える

3則は actor type ではなく、**意思決定合理性の公理系**である。同一 actor が3則を同時に考慮し、文脈・制度・役割・時間 horizon に応じて比重や優先順位が変わる。

管理対象は概念的に、

```text
resource-realization -> outcome / resource-state realization
activity-flow        -> process / activity continuity and expansion
P-downside            -> viability / breakdown prevention on the P side
```

と区別する。

必要な quantitative projection では、例えば context-dependent priority を

```text
w_i,c = (w_R, w_F, w_D)
```

と置き、candidate action `a` に対する各則の評価を `J_R(a)`, `J_F(a)`, `J_D(a)` として、

```text
A_i* ∈ argmax_{a ∈ feasible actions}
       Φ_i(J_R(a), J_F(a), -J_D(a); w_i,c)
```

のような decision rule を置ける。`J_*` / `Φ_i` / `w_i,c` は3則そのものではなく projection-specific な数理化である。線形加重和や `Σw=1` は要求せず、lexicographic priority、constraint、threshold 等も候補となる。

### 3則の形式的境界

現行 VFT では outcome / process / viability の3対象を管理合理性の最小公理系として採用する。一方、形式的な独立性・完備性・最小性の証明は未了である。

今後の検討候補：

- outcome / process / viability の3対象が相互にどう独立するか
- 第4の独立した管理合理性が必要になる条件があるか
- 3則の membership criterion / exclusion criterion
- 同一 A が複数則に寄与するときの識別方法
- 観察後に任意の則へ帰属させることを防ぐ事前分類条件
- context-dependent weight / priority の同定可能性
- weight、lexicographic priority、constraint、threshold の使い分け

### resource-realization の具体化

今後の検討候補：

- 「望ましい帰結」と「見込まれる帰結」を P と `E_i[ΔK|A=a]` にどう分離するか
- outcome valuation と action-contingent forecast の接続
- utility 等を outcome valuation として使う場合の情報損失

### activity-flow の具体化

今後の検討候補：

- A-flow を event count と同一視せず、`H_S` 等の path functional としてどう定義するか
- sustainable A-flow の horizon / viability constraint
- activity-flow と profit / revenue / throughput / market share の関係
- 短期的な ΔK 悪化を許容する intertemporal 条件
- going-concern と liquidation / asset stripping 等の区別

### P-downside の具体化

R3 は、P proxy の異質性だけから導入するものではなく、P 側の毀損が将来の A の成立や組織・制度・社会の viability を壊すことを防ぐ合理性として置く。

今後の検討候補：

- 誰のどの P を対象にするか
- downside / unacceptable region の定義
- loss functional / threshold / viability constraint の選択
- 異質な P proxy 間で加法則を仮定しない形式
- 個人間 P の比較可能性・加減算可能性の条件
- rights / minimum guarantee / satisficing / lexicographic constraint 等との関係

### 自給自足と制度的分業

3則は actor type ではないため、自給自足では単一 actor が全部を担いうる。

```text
single actor
  ├─ resource-realization
  ├─ activity-flow
  └─ P-downside
```

国家レベルの資本主義社会を粗視化すると、典型的には

```text
individuals -> resource-realization heavy
firms       -> activity-flow heavy
state       -> P-downside heavy
```

と主たる比重が分化して見える。ただし固定的な actor-type assignment ではない。

今後の検討候補：

- actor/context ごとの3則 priority の推定
- 自給自足 household / family unit で3則がどう遂行されるか
- 市場形成前後で比重・機能分担がどう変わるか
- 資本主義以外の制度での分業パターン
- 国家機能が弱い社会で P-downside を誰が担うか
- cooperative / commune / family business の複合機能
- 危機・成長・縮小局面で同一 actor の比重がどう変わるか

### マネジメント階層への再帰

実行・中間管理・統治に相当する階層的な機能分化は、近代企業だけでなく長期にわたる組織制度で反復して観察される。VFT が新たに三階層の存在を予測するのではなく、**既知の階層構造を3則の比重・分担の差として共通記述する**。

典型的には、

```text
operational / execution -> resource-realization heavy
managerial              -> activity-flow heavy
governance              -> P-downside heavy
```

と読めるが、各層は他の2則も担いうる。

今後の検討候補：

- 実行・管理・統治の比重差を actor / objective / time horizon のどこで識別するか
- 管理層が R1 / R2 / R3 を同時に担う場合の conflict
- governance 層が対象とする P の scope
- 組織規模の拡大に伴う機能分化・再統合
- flat organization / owner-manager / family business の比重構造
- 企業以外の行政・非営利・プロジェクト・共同体での比較

### 既存経済学の評価関数・調整機構との対応

utility / profit は3則の特殊化そのものではなく、3則に基づく意思決定を数量化する評価関数・指標・proxy として扱う。

今後の検討候補：

- utility を R1 の outcome valuation として使う条件
- profit / revenue / throughput を R2 の performance proxy として使う条件
- utility / profit によるスカラー化で失われる P / K / A-flow の情報
- 需給調整を planned change `x_i` 間の compatibility として記述する条件
- 価格変化による `P_i -> A_i / x_i` の更新と market clearing の動学
- forecast `E_i[ΔK]` と desire / planned change `x_i` を混同しない定式化

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

compatibility 自体も Core や3則から自動的には導出されない。

---

## 9. 分散的調整と「見えざる手」

各主体が `K_i` / `P_i` と文脈依存の3則 priority のもとで budget-feasible な `x_i` を選び、価格・取引・信用等を介してその選択を修正することで、主体間の不整合が分散的に調整される可能性がある。

この構造を古典経済学の「神の見えざる手」へ射影することは可能だが、現時点では projection candidate であり、Core の普遍的帰結ではない。

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

現行 Core では、価値場を K / K_i / P の配置・関係が A を条件づける structural framework として定義し、独立した V や普遍的 deterministic choice function を置かない。

今後、説明力・操作化のために最低限の形式化が必要になった場合は、例えば

```text
Γ_i(K_i, P_i) ⊆ 𝒜_i
```

のような action correspondence / admissible or plausible action set の導入を検討できる。

3則はこの Core state representation の上で意思決定を方向づける公理系として扱い、具体的な `Γ_i` や decision rule との接続方法を projection ごとに定める。

---

## 15. P の反証可能性

P が観察後の residual state にならないよう、projection / empirical model ごとに、採用する P 次元・型、proxy、proxy admissibility、A / action-contingent `E[ΔK]` への mapping、事前予測・識別条件を観測前に固定する必要がある。

---

## 16. spillover / externality の区別

主体間の影響はまず spillover / cross-agent effect として記述する。

---

## 17. 組織・国家等の集約主体近似

組織・国家等を単一主体として扱うことは Core 前提ではない。

必要な場合は近似として導入し、対象主体、共通 K の対象範囲、各主体の `K_i` / `P_i`、A の集約方法、3則の priority / division、ΔK / H の会計・集約規則、情報損失、内部対立を明示する。

---

## 18. 実証・計量化

今後の具体化候補：

- 共通 K の観測設計
- `K_i` の access / usability
- P の内部型 / proxy / admissibility
- K / P 識別
- `P_j(a)` の評価者・評価対象の識別
- A の直接観測と潜在 decision の proxy
- temporal typing / event ordering の操作化
- ΔK / ΔP の generic change mapping
- `H_S` / `h_S` の操作化
- `M_S` / `δ_S` の操作化
- gross flow / net stock change の同時計測
- `q_S : D_S -> V_S` の操作化
- action-contingent `E[ΔK|A=a]` の expectation operator / 推定
- actor/context ごとの3則 priority / weight / constraint の推定
- candidate action → future trajectory → three-rule evaluation の識別
- 自給自足と制度的分業における3則の比重・遂行・分担・重複の比較
- 国家レベルでの individual / firm / state の主担当分化の比較
- マネジメント三階層における3則の比重・分担と管理成果の比較
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