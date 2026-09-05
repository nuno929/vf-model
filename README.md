# 価値場理論（Value-Field Theory）

**Theory refresh — Draft**  
Author: **T. Nuno**  
License: **CC BY 4.0**

---

## 1. 概要

価値場理論（Value-Field Theory; VFT）は、個人・組織・社会で生じる変化を、**共通の実資源状態 K と、各主体が保持する主観的な評価・期待状態 P の関係が、各主体の actor-side process / event A をどのように条件づけるか**として記述する構造的フレームワークである。

VFT Core は、単独で経験的予測を与える仮説というより、**ontology / modeling language / common state representation** として位置づける。Core 自体は普遍的な選択則・更新則・均衡則・集約則を固定せず、反証可能な経験的制約は各 projection / empirical model が担う。

**Core の目的は単独で行動を予測することではなく、各 projection が検証可能な制約・選択則・観測モデルを記述するための共通状態表現を与えることである。**

### K の存在論

K が参照する資源世界は主体ごとに別々に存在するのではなく、**同一の物理的・社会的な実資源世界**を前提とする。

各 `K_i,t` は、その共通の K のうち、主体 `i` が時点 `t` に実際にアクセス・利用・行使・参照可能な範囲を表す actor-relative view である。したがって、同じ設備・情報・インフラ等が複数主体の `K_i` に関係しうるが、資源そのものが主体ごとに複製されていることを意味しない。

`K_i` は独立した資源世界や独立 state ではなく、**共通 K に含まれる資源・権利・資格・契約・制度状態等から導かれる access / usability view** として扱う。したがって、K 自体の物量が変わらなくても、アクセス権や資格等の K 上の条件が変化すれば `K_i` は変化しうる。

### P と期待値

各 `P_i,t` は、主体 `i` が保持する将来の見通し・評価・選好・信用・信念等からなる多次元の **subjective evaluation / expectation state** である。

他主体 `a` に対して主体 `j` が保持する評価・信用・見通し等を区別して書く必要がある場合は、`P_j(a)` と表す。これは **評価対象 `a` の P ではなく、評価者 `j` の `P_j` に含まれる `a` についての主観状態**である。

P を「期待 stock」と呼ぶ場合も、P 自体を特定時点の期待値とみなすためではなく、**将来価値への期待・評価や行動を生成する側の蓄積構造であることに着目した呼称**である。

観測・会計仕様 `S` と時間区間 `τ=[t0,t1]` を明示した実資源状態の変化を `ΔK(S, τ)` とする。`S` は対象資源・主体だけでなく、**resource coordinates、accounting boundary、transformation convention** を含む。文脈上 scope が明らかな場合は `ΔK` と省略する。

主体 `i` が対象範囲・区間について形成する期待実資源変化を、`E_i[ΔK(S, τ)]` として区別する。ただしこの記法は、対象 `ΔK` に quantitative representation が定義され、期待値が取れる場合に限って用いる。

---

## 2. コア変数

概念的には、

```text
K_t
K_i,t = access / usability view derived from K_t
P_t = (P_i,t)_{i in I}
A_τ = (A_i,τ)_{i in I}
```

と表す。

- **K**：共通の実資源世界を構成する多次元の資源・資本状態
- **K_i**：共通 K に対する主体 `i` のアクセス・利用・行使・参照可能性によって導かれる actor-relative view
- **P_i**：主体 `i` の将来見通し・評価・選好・信用・信念等を保持する多次元の主観的評価・期待 state
- **A_i**：主体 `i` 側で生じる process / event。外部行動、意思決定、観測、情報受容、解釈等を必要に応じて含む
- **ΔK(S, τ)**：観測・会計仕様 `S` における K の state / resource change descriptor
- **ΔP_i**：観測区間内に主体 `i` の P に実現した change descriptor / state transition
- **E_i[ΔK(S, τ)]**：主体 `i` が対象範囲・区間について形成する expected realized resource change の quantitative representation

`P_t` / `A_τ` は集合ではなく actor identity を保持する indexed family として表す。

`S` は、対象とする資源・主体に加えて、どの resource coordinates で測るか、どの accounting boundary を採るか、資源変換をどう記録するかを含む観測・会計仕様である。`τ` は時間区間を表す。

K / P / A は単一スカラーを前提としない。分布化・平均化・集約は、必要に応じて観測・分析時に行う操作であり、コアの存在論ではない。

### 状態変化と区間活動量の分離

`ΔK` は K の **state / resource change** に予約する。観測・会計仕様 `S` に対応する state representation を `Y_S(t)` とすると、一般に

```text
Y_S(t) = M_S(K_t)
ΔK(S, τ) = δ_S(Y_S(t0), Y_S(t1)) ∈ D_S
```

と書く。`M_S` と `δ_S` は projection / measurement model 側で定める specification-local な写像・演算であり、Core の新しい原始変数ではない。

`ΔK` は必ずしも算術差を意味しない。加法的な quantitative projection が適用できる場合に限って、

```text
δ_S(y0, y1) = y1 - y0
Y_S(t1) = Y_S(t0) + ΔK(S, τ)
```

と書ける。`K_t1 = K_t0 + ΔK` は、さらに `M_S = id` で K 自体が同じ加法空間にある特殊ケースに限る。

一般形で始点と終点の state representation が同じ場合は、`δ_S(y,y)` をその仕様における no-change descriptor とみなす。**加法的な在庫 projection では**、生産 100・消費 100 で在庫が元に戻る場合 `ΔK(S,τ)=0` となる。

一方、gross production、gross consumption、transaction volume、resource transformation のような**区間中の活動量・flow statistic** は `ΔK` へ含めず、必要な projection / measurement で derived path functional として分離する。例えば、

```text
H_S(τ) = h_S((K_t)_{t in τ}, A_τ)
```

と書ける。`A_τ` 自体が区間内の actor-side event / process を保持し、必要な場合は event ordering を保持する。`H_S` は Core の新しい state / primitive ではなく、区間 path から導出する観測・会計量である。

したがって上の加法的在庫例でも、production / consumption を表す `H_S` はそれぞれ 100 と記録できる。

非加法的な P 成分では、`ΔP_i` は算術差ではなく、少なくとも

```text
P_i,t0 -> P_i,t1
```

という状態遷移を表す change descriptor として扱う。必要な quantitative mapping は各 projection / measurement model で定める。

### E[ΔK] の quantitative representation

`ΔK(S, τ)` の値域 `D_S` は非数量・非加法でありうるため、期待値を取る場合は quantitative representation を明示する。

```text
q_S : D_S -> V_S
```

ここで `V_S` は対象 projection で expectation が定義可能な quantitative value space とする。記法上、

```text
E_i[ΔK(S, τ)] := E_i[q_S(ΔK(S, τ))]
```

と略記する。左辺は qualitative / generic な change descriptor そのものへ直接期待演算を掛ける意味ではない。

`q_S`、確率測度、情報集合、期待形成式は projection / measurement model 側で定める。数量化しない forecast を無理に `E[...]` と表記しない。

`ΔK` はミクロ用・マクロ用に数学的な同一型を要求しない。各 `S` に対して `D_S`、`V_S`、座標、単位、集約規則等は異なりうる。共通なのは **S-indexed state-change schema** である。

---

## 3. K / P の境界

K / P は対象物の種類だけで分類しない。

- **K**：実際に存在し、主体が利用・行使・参照できる資源・能力・権利・情報等
- **P**：それらを含む環境について主体が保持する見通し・評価・選好・信用・信念等

例えば、契約上行使可能な権利は K、契約が履行される見込みは P となる。参照可能な情報は K、その情報から形成される将来見通しは P となる。

公開レビュー値・rating 等は、公開されアクセス可能な情報として K 側に存在しうる。その情報を主体 `j` が観測して主体 `a` への評価・信用を形成した場合、その主観状態は `P_j(a)` に属する。

同じ現象が K / P の双方へ影響することはありうるが、同一 observable を根拠なく二重計上しない。

### event / persistent state / subjective representation

同じ現象でも、因果上の位置は分ける。

```text
actor-side event A
        ↓
persistent / accessible world state in K
        ↓ perception / interpretation
subjective representation in P
```

例えば政策条件の変更そのものは政策主体の A、変更後に持続して他主体が参照・利用可能な制度条件は必要に応じて K、その条件を主体がどう解釈・予測するかは P として区別する。観測データ上同じ指標が複数段階の proxy になりうる場合も、measurement mapping で因果上の位置を固定する。

---

## 4. A と価値場

A は単一の「社会全体の行為」を意味しない。

```text
A_τ = (A_i,τ)_{i in I}
```

各 `A_i,τ` は、主体 `i` 側で観測区間内に生じた一つ以上の process / event を含みうる。外部行動・意思決定と、観測・情報受容・解釈等の perception / update process は、必要な projection で区別する。

区間内の順序が重要な場合はイベント順序を保持し、粗い時間粒度では順序を捨象した coarse-grained representation として扱う。

価値場は、**共通の K、その主体が利用可能な K_i、および各主体の P の配置・関係が、各 A を条件づけ、特定の行動・process を生じやすく／生じにくくする構造**を指す。

ここでいう「方向性」「引力」は action space 上の幾何学的ベクトルを意味しない。独立した価値場変数、引力量、普遍的な選択関数は置かない。

他主体や環境について主体 `i` がどう認識・予測しているかは、必要な範囲で `P_i` に含める。別の普遍的な観測写像を Core には追加しない。

---

## 5. K / P の変化

主体側の主要な時間型は、選択関数・更新関数を固定せず、概念的に

```text
(K_t0, P_t0)
      ↓ conditions
A_(t0,t1]
      ↓ realized interval processes
(K_t1, P_t1)
```

と置く。これは **actor-side channel の因果・時間順序を示す typing** であり、普遍的な状態遷移関数を意味しない。

A は K / P を変化させる主要な actor-side process である。`K_i` は K から導かれる view であるため、権利・資格・契約・制度状態等を含む K の変化に応じて access / usability が変わりうる。`K_i` 専用の独立した差分変数は Core に置かない。

政策変更、価格提示、契約条件変更、情報伝達、観測・情報受容・解釈等による P の変化も、必要に応じて A の経路として記述できる。

P と A の因果関係を検証する projection で、`A_(t0,t1]` 内の情報受容・解釈等が途中で P を更新し、その後の decision / action に影響する場合は、**区間を分割するか event ordering を保持する**。`P_t0 -> A_(t0,t1]` と粗く書いたまま途中の P 更新を事前状態として扱わない。

一方、記憶減衰等の微小・非主体的な P の変化や、減価償却・老朽化・自然消耗・災害等の A を介さない K の変化もありうる。これらは上の actor-side channel 図に含めず、必要な projection で扱う。

---

## 6. 経済学への射影

経済均衡は VFT 固有の普遍則として定義しない。以下は既存経済学への**射影候補**である。

### 主体別期待と意思決定

経済射影では、`K_i` を主体 `i` の予算・保有資源・供給能力等の制約側、`P_i` を価格、他主体の生産・消費、信用、将来条件等についての見通し・評価を含む主観状態として読める。

主体 `i` はそれらのもとで A を選択し、その結果として実現する資源変化について `E_i[ΔK(S_i, τ)]` を形成しうる。

必要な economic projection では、A に含まれる planned / chosen resource change を補助的に `x_i` と書く。

```text
x_i          = planned / chosen resource change
E_i[ΔK(...)] = expected realized resource change
```

`x_i` は projection-local な補助記法であり、Core の新しい原始変数ではない。

### 会計的予算制約

予算制約・実行可能性が直接制約するのは plan / choice 側である。

`x_i` を、取得を正・処分／供給を負とする planned net resource change とし、価格・会計換算ベクトルを `p` とする純粋交換の基本例では、

```text
p · x_i <= 0
```

のように budget feasibility を表せる。`p · x_i = 0` は self-financing / budget exhaustion 等を追加仮定する場合の特殊形である。所得、生産収入、投資、借入、移転等を含む場合は、対象とする経済理論の会計規則に従って予算式へ組み込む。

一方、`E_i[ΔK]` は、その plan を含む状況から主体が見込む**実現結果の期待値**であり、plan と一致するとは限らない。

### 主体間整合条件

**VFT notation を用いる最小経済射影では**、各主体の予算・資源制約を満たした `x_i` が、価格・取引条件等のもとで相互に実行可能・両立可能であるという inter-agent compatibility / feasibility condition を追加できる。

この compatibility 自体も economic projection 側の条件であり、VFT Core から自動的に導出されるものではない。これを標準的な意味で **market equilibrium** と呼ぶためには、さらに射影先の経済理論が choice / optimality / best response / market-clearing 等の条件を与える必要がある。

### 会計整合と実現 ΔK / H

会計恒等式と主体間整合・市場均衡は区別する。主体間の交換や生産・消費を共通の会計規則で記録した結果は、対象 scope の state change `ΔK` や、必要に応じて区間活動量 `H_S` と会計的に対応づける。

例えば在庫の net change は `ΔK`、gross production / consumption / transaction volume は `H_S` として分ける。市場が不均衡でも会計恒等式は成立しうる一方、市場が均衡していても `ΔK` や `H_S` は非ゼロになりうる。

### ミクロ／マクロの共通 K 接続

VFT ではミクロとマクロを別々の資源世界として置かない。**両者は同じ common K と同じ K transition を、異なる観測・会計仕様 `S` から記述したもの**である。

```text
                 common K
                /        \
          S_micro        S_macro
             ↓              ↓
      micro observation  macro observation
```

したがって、存在論的な接続のために `micro -> macro` の普遍的 aggregation map を要求しない。micro observable から macro observable を再構成する場合にのみ、projection-local な aggregation / coarsening rule を追加する。

### 評価・信用経済への射影可能性

評価・信用経済では、評価対象と評価者を区別する。主体 `a` の評判・信用は一つの `P_a` として存在するのではなく、評価者 `j` ごとの `P_j(a)` として表現される。

```text
public rating / review information in K
        ↓ observed by j
      P_j(a)
        ↓
  decision A_j
        ↓
rights / contract / credit conditions in K
        ↓
      K_a
        ↓
   realized ΔK
```

このように、公開評価情報、他者が保持する評価・信用、実際に行使可能な信用枠・請求権・取引アクセスを区別することで、いわゆる**評価経済・信用経済**における波及を同一状態表現上で射影できる可能性がある。

### 機能的最適化則の候補

VFT の ontology 自体は主体を「個人・企業・国家」という別種の存在として固定しない。その上で、経済・社会 projection では、次の3つを **functional optimization hypothesis** として分離できる。

1. **resource-realization function**：主体は、自らが形成する期待・評価のもとで、望む／見込む `ΔK` の実現へ向けて A を選ぶ。
2. **activity-flow function**：主体は、K / P の配置を再構成し、持続可能な A-flow を最大化する。
3. **P-downside function**：主体群の P の大幅な負側・悪化側を抑えるよう、K / A を配分・調整する。

概念的な最適化記法としては、projection-local な objective を用いて、

```text
resource-realization:
A_i* ∈ argmax_A R_i(A ; P_i, E_i[ΔK])

activity-flow:
(K_f*, P_f*) ∈ argmax_(feasible K_f,P_f) F_f(A-flow | K_f, P_f)

P-downside:
A_g* ∈ argmin_A L_g^-(P ; observable proxies)
```

のように書ける。`R_i` / `F_f` / `L_g^-` は Core primitive ではなく、各 projection が具体化する objective functional である。

ここで「個人・企業・国家」は最適化機能の典型的な担い手であって、機能そのものと同一ではない。**自給自足では単一 actor が3つの最適化機能をすべて担いうる。** 一方、資本主義では概ね、個人が resource-realization、企業が A-flow、国家が P-downside を重点的に担う制度的分業として記述できる。

企業の利益は A-flow の結果として生じる resource/accounting outcome の一面であり、短期的な `ΔK` の悪化を伴う投資・採用・R&D・市場獲得等も、将来 A-flow の拡張として記述できる。このため profit maximization より広い企業行動を扱える。

国家側で P の単一最大化を直接置きにくいのは、P の真値が直接観測できず、支持率・失業・犯罪・景況感・出生・健康・移住・市場指標等の proxy 間に普遍的な加法則がないためである。個々の悪化や負側は比較的識別しやすいため、operational rule として downside minimization を置き、上方の改善は個々人・企業の分散的努力へ委ねる形をとりうる。

この3則は現段階では VFT Core の普遍法則ではなく、**同一 actor 内にも制度的分業にも適用できる explanatory projection** として扱う。

### 期待変化の集約と余剰

異なる主体の `E_i[ΔK(S_i, τ)]` を集約する場合は、各 `S_i`、`q_S`、会計・換算規則が比較可能であることを明示する。同一の共通 scope に対する複数主体の予測 `E_i[ΔK(S, τ)]` は、単純和して aggregate resource change と解釈しない。

標準経済学上の consumer surplus / producer surplus / total surplus と接続する場合は、対象理論側で valuation、utility、WTP / WTA、cost 等との対応を追加的に明示する。

### マクロ政策への射影候補

政策金利の変更、通貨供給量の操作、制度変更等は、まず政策主体の A として扱う。その A が K 上の制度・契約条件等を変化させ、各主体の観測・解釈を通じて `P_i` の変化を誘発しうる。

前区間までに実現した資源変化と、当期の A が誘発する主観状態側の変化との相互作用を既存マクロ経済学へ対応させることは、一つの射影候補である。

Core の K / P を経済学上の real / nominal と同一視しない。K は resource / capability side、P は subjective evaluation / expectation side として置き、real / nominal の語は経済学への具体的射影でのみ用いる。

---

## 7. 計測

A のうち外部に実現した action event は直接観測できる場合がある。一方、内部の意思決定や観測・解釈過程は直接観測できず、proxy を要する場合がある。

個々の `P_i` の全構造も直接観測できるとは仮定しない。個人レベルでは選択・発話・調査等を、必要な範囲で proxy として扱う。価格・金利・スプレッド・信用条件等の market outcome を P proxy として用いる場合は、P 自体ではなく K / A / institution / market process との同時決定結果である可能性を考慮する。

P proxy の admissibility では少なくとも、

- target A / ΔK より前に観測された proxy か
- 同時決定の場合に joint structural / measurement model を明示しているか
- target outcome を使って latent P を事後的に構成していないか
- proxy validity を別データまたは追加制約で検証できるか

を確認する。

`ΔK` / `ΔP` は A の結果 proxy として利用できる場合があるが、A を一意に同定する量ではない。gross activity を観測する場合は `H_S` 等の path functional と state change `ΔK` を区別する。

実証では projection ごとに、P の採用次元、observable / proxy、A / E[ΔK] への mapping、`q_S`、観測前に固定する予測・検証条件を明示する。

---

## 8. スケールと理論境界

個人・組織・社会・文明といった区分は、固定された独立実体ではなく、観測スケールと内生／外生境界の違いとして扱う。

価値場理論は現段階では、以下を普遍的に固定しない。

- K / P / A の単一スカラー化
- 多主体 A の確率分布化
- 組織・市場・社会の単一主体化
- 主体間関係の独立した普遍的関係変数
- 独立した選好変数 X
- 独立した価値場変数 V
- 単一の普遍的効用関数
- P の普遍的更新式
- `q_S` の普遍的定義
- `E[ΔK]` の普遍的形成式・確率測度
- `E[ΔK]` を A 生成の必須中間変数とすること
- A の普遍的選択則
- `H_S` 等の区間活動量の普遍的定義
- functional optimization hypothesis の具体的 objective function
- inter-agent compatibility の普遍的条件
- market equilibrium の普遍的 choice / optimality / clearing 条件
- ミクロ／マクロの普遍的集約・導出則
- 特定の観測方法・proxy・統計手法

---

## 9. ドキュメント

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