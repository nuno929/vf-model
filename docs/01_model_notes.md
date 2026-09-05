# 価値場理論 — モデルノート

## 1. 目的

本ノートは、価値場理論のコア変数と基本動学を README より形式的に整理する。

価値場理論は現段階では、K / P から A を一意に予測する普遍的な選択則を与える理論ではなく、**共通の実資源世界、主体ごとの主観的評価・期待状態、actor-side process / event、実現変化を同一の構造で記述する structural framework** として扱う。

VFT Core は、単独で経験的予測を与える仮説というより、**ontology / modeling language / common state representation** として位置づける。反証可能な経験的制約は projection / empirical model 側で与える。

Core の目的は単独で行動を予測することではなく、各 projection が検証可能な制約・選択則・観測モデルを記述するための共通状態表現を与えることである。

---

## 2. K：共通の実資源世界

K が参照する資源世界は主体ごとに別々に存在するのではなく、同一の物理的・社会的な実資源世界を前提とする。

```text
K_t
```

K は多次元であり、時間、身体、技能、知識、情報、関係、設備、資金、インフラ、権利、制度上利用可能な手段等を含みうる。

一方、各主体がその全てへ同じようにアクセスできるわけではない。主体 `i` が時点 `t` に実際にアクセス・利用・行使・参照可能な範囲を `K_i,t` とする。

```text
K_i,t = actor-relative access / usability view derived from K_t
```

`K_i` は主体ごとに別の資源世界を意味しない。また、`K_i` の “slice” は集合論的な部分集合を必ずしも意味しない。

`K_i` は独立 state ではなく、共通 K に含まれる資源・権利・資格・契約・制度状態等から導かれる actor-relative view として扱う。したがって、物量としての K が大きく変わらなくても、アクセス権や資格等の K 上の条件が変化すれば `K_i` は変化しうる。

同じ設備、公開情報、インフラ等が複数主体の `K_i` に関係しうるが、資源そのものが複製されたことを意味しない。

金融資源を K として扱う場合も、名目評価額そのものではなく、現金、行使可能な金融請求権、利用可能な信用枠等、**実際の行動可能性を増やす利用可能な資源・権利**として扱う。

---

## 3. P：主観的評価・期待 state

各主体 `i` の `P_i,t` は、**将来の見通し・評価・選好・信用・信念等を保持し、期待や行動を形成する多次元の subjective evaluation / expectation state** である。

```text
P_t = (P_i,t)_{i in I}
```

`P_t` は集合ではなく actor identity を保持する indexed family として扱う。

他主体 `a` について主体 `j` が保持する評価・信用・見通し等を区別して表す必要がある場合は、`P_j(a)` と書く。これは評価対象 `a` の P ではなく、**評価者 `j` の `P_j` に含まれる `a` についての主観状態**である。

P を「期待 stock」と呼ぶ場合も、P 自体を特定時点の期待値とみなすためではない。**将来価値への期待・評価や行動を生成する側の蓄積構造であることに着目した呼称**である。

P は履歴依存性を持ち、過去の期待、その実現結果、信用、評価、制度、経験等を通じて形成・強化・修正されうる。ただし、経験に裏付けられない初期的な選好・信念・見通しもありうるため、過去履歴だけから完全に決定されるとはしない。

信用、評価、契約、制度、慣行、公約、PR、ナラティブ等は、各主体の P の形成・固定・伝播に影響しうる。

---

## 4. K / P の境界

K / P は対象物の種類だけで分類しない。

- **K**：実際に存在し、主体が利用・行使・参照できる資源・能力・権利・情報等
- **P**：それらを含む環境について主体が保持する見通し・評価・選好・信用・信念等

例えば、契約上行使可能な権利は K、契約が履行される見込みは P となる。参照可能な情報そのものは K、その情報から形成される将来見通しは P となる。

公開レビュー値・rating 等は、公開されアクセス可能な情報として K 側に存在しうる。その情報を主体 `j` が観測して主体 `a` への評価・信用を形成した場合、その主観状態は `P_j(a)` に属する。

同じ現象が K / P の双方へ影響することはありうるが、同一 observable を根拠なく二重計上しない。

因果上の位置を明確にするため、必要な projection では

```text
actor-side event A
        ↓
persistent / accessible world state in K
        ↓ perception / interpretation
subjective representation in P
```

という区別を用いる。例えば政策条件の変更そのものは政策主体の A、変更後に持続して参照・利用可能な制度条件は必要に応じて K、その条件を主体がどう解釈・予測するかは P とする。

---

## 5. A：actor-side process / event

A は単一の社会的行為ではなく、各主体側で生じる process / event を表す。

```text
A_τ = (A_i,τ)_{i in I}
```

`A_τ` は actor identity を保持する indexed family として扱う。

各 `A_i,τ` は、主体 `i` が観測区間内に行った外部行動・意思決定に加えて、必要に応じて観測、情報受容、解釈等の perception / update process を含みうる。

これは、情報受容そのものを必ず能動的行為とみなすという意味ではない。外部 action と内部の perception / update process は projection 側で区別できる。

区間内で `A_1 -> change -> A_2` のようなフィードバックが重要な場合はイベント順序を保持する。粗い時間粒度では、順序を捨象した coarse-grained representation として扱うことができる。

組織・市場・社会を扱う場合も、必要がない限り複数主体の A を一つの主体行動へ還元しない。

---

## 6. 価値場

価値場は、**共通の K、その主体が利用可能な K_i、および各主体の P の配置・関係が、各 A を条件づけ、特定の行動・process を生じやすく／生じにくくする構造**である。

```text
K_t
├─ K_1,t
├─ K_2,t
└─ ...

(K_i,t)_i, (P_i,t)_i
        ↓  value field
      (A_i,τ)_i
```

ここでいう「方向性」「引力」は action space 上の幾何学的ベクトルを意味しない。独立した価値場変数、引力量、普遍的な選択関数は置かない。

他主体や環境について主体 `i` がどう認識・予測しているかは、必要な範囲で `P_i` に含める。別の普遍的観測写像は Core に追加しない。

---

## 7. ΔK / ΔP：状態変化

観測・会計仕様 `S` と時間区間 `τ=[t0,t1]` を明示した K の state / resource change を `ΔK(S, τ)` とする。

`S` は対象資源・主体だけでなく、**resource coordinates、accounting boundary、transformation convention** を含む。

観測・会計仕様 `S` に対応する state representation を `Y_S(t)` とすると、

```text
Y_S(t) = M_S(K_t)
ΔK(S, τ) = δ_S(Y_S(t0), Y_S(t1)) ∈ D_S
```

と書ける。`M_S` と `δ_S` は projection / measurement model 側で定める specification-local な写像・演算であり、Core の新しい原始変数ではない。

`ΔK` は必ずしも算術差ではない。加法的な quantitative projection が適用できる場合に限って、

```text
δ_S(y0, y1) = y1 - y0
Y_S(t1) = Y_S(t0) + ΔK(S, τ)
```

と書ける。`K_t1 = K_t0 + ΔK` は、さらに `M_S = id` で K 自体が同じ加法空間にある特殊ケースに限る。

一方、gross production、gross consumption、transaction volume、resource transformation 等の**区間活動量・flow statistic** は `ΔK` へ含めない。必要な projection / measurement で、例えば

```text
H_S(τ) = h_S((K_t)_{t in τ}, (A_t)_{t in τ})
```

のような derived path functional として分離する。`H_S` は Core の primitive / state ではなく、区間 path から導出する観測・会計量である。

このため、生産 100・消費 100 で在庫が元に戻る場合、在庫についての `ΔK` は 0 でも、production / consumption を表す `H_S` はそれぞれ 100 と記録できる。

`ΔP_i` も一般には算術差ではなく、主体 `i` の P に実現した change descriptor / state transition を表す。非加法的な場合には少なくとも

```text
P_i,t0 -> P_i,t1
```

として扱い、必要な quantitative mapping は projection / measurement model 側で与える。

`ΔK` はミクロ用・マクロ用に数学的な同一型を要求しない。各 `S` に対して値域 `D_S`、座標、単位、集約規則等は異なりうる。共通なのは **S-indexed state-change schema** である。

`K_i` は K から導かれる view であるため、K 上のアクセス条件が変われば `K_i` も変化しうる。`K_i` 専用の独立した差分変数は Core に置かない。

---

## 8. 時間型と E[ΔK]

主体側の主要な時間型は、選択関数・更新関数を固定せず、概念的に

```text
(K_t0, P_t0)
      ↓ conditions
A_(t0,t1]
      ↓ realized interval processes
(K_t1, P_t1)
```

と置く。これは因果・時間順序を示す typing であり、普遍的な状態遷移関数を意味しない。K には減価償却・老朽化・自然消耗・災害等、A を介さない変化もありうる。P にも記憶減衰等の微小・非主体的変化はありうるが、必要な応用でのみ扱う。

P と A の時間的・因果的関係を検証する projection で、`A_(t0,t1]` 内の情報受容・解釈等が途中で P を更新し、その後の decision / action に影響する場合は、**区間を分割するか event ordering を保持する**。

### quantitative representation

`ΔK(S, τ)` の値域 `D_S` は非数量・非加法でありうる。期待値を取る場合は quantitative representation を

```text
q_S : D_S -> V_S
```

として明示し、`V_S` を expectation が定義可能な quantitative value space とする。

記法上、

```text
E_i[ΔK(S, τ)] := E_i[q_S(ΔK(S, τ))]
```

と略記する。左辺は generic change descriptor へ直接期待演算を掛ける意味ではない。

`q_S`、確率測度、情報集合、期待形成式は対象 projection / measurement model で与える。数量化しない forecast を無理に `E[...]` と表記しない。

`E[...]` は主体が形成する見込み値・期待値を表し、主体の望みそのものではない。選好、望ましさ、評価等は `P_i` に保持され、期待形成や A に影響しうる。

同じ対象区間について「10ほしいが2しか実現しないと見込む」場合、`E_i[ΔK]` は見込み値側を表し、「10ほしい」という選好・評価は P 側に属する。

`E[ΔK]` を A 生成の普遍的な必須中間変数とはしない。

---

## 9. 経済学への射影

経済均衡は VFT 固有の普遍則として定義しない。以下は既存経済学への射影候補である。

### 主体別期待と意思決定

経済射影では、`K_i` を主体 `i` の予算・保有資源・供給能力等の制約側、`P_i` を価格、他主体の生産・消費、信用、将来条件等についての見通し・評価を含む主観状態として読める。

主体 `i` は `K_i` と `P_i` のもとで A を選択し、その結果として実現する資源変化について `E_i[ΔK(S_i, τ)]` を形成しうる。`S_i` は共通 K 上の主体 `i` の経済的な観測・会計 scope であり、主体ごとの別資源世界を意味しない。

必要な economic projection では、A に含まれる planned / chosen resource change を補助的に `x_i` と書く。

```text
x_i          = planned / chosen resource change
E_i[ΔK(...)] = expected realized resource change
```

`x_i` は projection-local な補助記法であり、Core の新しい原始変数ではない。

### 会計的予算制約

予算制約・実行可能性が直接制約するのは plan / choice 側である。

`x_i` を取得を正・処分／供給を負とする planned net resource change とし、価格・会計換算ベクトルを `p` とする純粋交換の基本例では、

```text
p · x_i <= 0
```

のように budget feasibility を表せる。`p · x_i = 0` は self-financing / budget exhaustion 等を追加仮定する場合の特殊形である。所得、生産収入、投資、借入、移転等を含む場合は、対象とする経済理論の会計規則に従って予算式へ組み込む。

`E_i[ΔK]` はその plan を含む状況から主体が見込む実現結果の期待値であり、`x_i` と一致するとは限らない。

### 主体間整合と market equilibrium

**VFT notation を用いる最小経済射影では**、各主体の予算・資源制約を満たした `x_i` が、価格・取引条件等のもとで相互に実行可能・両立可能であるという inter-agent compatibility / feasibility condition を追加できる。

この compatibility 自体も economic projection 側の条件であり、VFT Core から自動的に導出されるものではない。これを標準的な意味で market equilibrium と呼ぶためには、さらに射影先の経済理論が choice / optimality / best response / market-clearing 等の追加条件を与える必要がある。

### 会計整合とミクロ／マクロの接続面

会計恒等式と主体間整合・市場均衡は区別する。

対象 scope の state change は `ΔK`、gross production / consumption / transaction volume 等の区間活動量は `H_S` として分けて会計的に対応づける。

主体レベルの state change と interval activity を、共通の `S` / `τ` / accounting rule のもとで市場・産業・社会・マクロ観測へ接続できるが、これはミクロからマクロを自動導出する普遍的 aggregation law を意味しない。

### 評価・信用経済への射影可能性

評価対象 `a` と評価者 `j` を区別する。主体 `a` の評判・信用は一つの `P_a` として存在するのではなく、評価者 `j` ごとの `P_j(a)` として表現される。

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

公開レビュー・rating はアクセス可能な情報として K、主体 `j` が主体 `a` に対して形成する評価・信用は `P_j(a)`、その結果として `a` に実際に付与された信用枠・請求権・契約上の権利等は K / `K_a` として区別する。

これは現時点では VFT Core の普遍則ではなく、VFT の共通状態表現を用いた projection / empirical modeling の候補である。

### 期待変化の集約と余剰

異なる主体の `E_i[ΔK(S_i, τ)]` を集約する場合は、各 `S_i`、`q_S`、会計・換算規則が比較可能であることを明示する。同一の共通 scope に対する複数主体の予測 `E_i[ΔK(S, τ)]` は、単純和して aggregate resource change と解釈しない。

標準経済学上の consumer surplus / producer surplus / total surplus と対応づける場合は、対象理論側で valuation、utility、WTP / WTA、cost 等との mapping を追加的に明示する。

### マクロ政策への射影

政策金利の変更、通貨供給量の操作、制度変更等は、まず政策主体の A として扱う。その A が K 上の制度・契約条件等を変化させ、各主体の観測・解釈を通じて `P_i` の変化を誘発しうる。

前区間までに実現した `ΔK` と、当期 A が誘発する主観状態側の変化との相互作用を既存マクロ経済学へ対応させることは、一つの射影候補である。

Core の K / P を経済学上の real / nominal と同一視しない。K は resource / capability side、P は subjective evaluation / expectation side として置き、real / nominal の語は経済学への具体的射影でのみ用いる。

---

## 10. 計測

A のうち外部に実現した action event は直接観測できる場合がある。一方、内部の意思決定、観測、情報受容、解釈等は直接観測できず、proxy を要する場合がある。

個々の `P_i` の全構造も直接観測できるとは仮定しない。価格、金利、スプレッド、信用条件等の market outcome を P proxy として用いる場合は、P 自体ではなく K / A / institution / market process との同時決定結果である可能性を考慮する。

P proxy の admissibility では少なくとも、

- target A / ΔK より前に観測された proxy か
- 同時決定の場合に joint structural / measurement model を明示しているか
- target outcome を使って latent P を事後的に構成していないか
- proxy validity を別データまたは追加制約で検証できるか

を確認する。

`ΔK` / `ΔP` は A の結果 proxy として利用できる場合があるが、複数の A が相殺・重複しうるため、A を一意に同定する量ではない。gross activity を観測する場合は `H_S` 等の path functional と state change `ΔK` を区別する。

実証では projection ごとに、P の採用次元、observable / proxy、A への mapping、`q_S`、観測前に固定する予測・検証条件を明示する。観察後に任意の P 差を追加して A を説明することは避ける。

---

## 11. スケール

個人・組織・社会・文明を、固定された独立世界としてではなく、観測スケールと内生／外生境界の違いとして扱う。

スケールを変えると `S` に応じて `ΔK(S, τ)` の値域 `D_S`、`q_S` の値域 `V_S`、座標、単位、集約規則等は変わりうる。一方、観測・会計仕様に対する **state-change schema** は共通に保つ。区間活動量は必要に応じて別の `H_S` として定義する。

組織・国家等を単一主体として扱う場合は近似であり、対象主体、K へのアクセス範囲、P の対象範囲、集約規則、情報損失を明示する。

---

## 12. コアで固定しないもの

以下は応用・実証・追加議論で決める。

- K / P の標準次元
- A の普遍的な選択則
- K / P の普遍的な状態遷移関数
- `q_S` の普遍的定義
- `E[ΔK]` の普遍的な形成式・確率測度
- `H_S` 等の区間活動量の普遍的定義
- inter-agent compatibility の普遍的条件
- market equilibrium の普遍的 choice / optimality / clearing 条件
- ミクロ／マクロの具体的均衡・調整過程
- K / P / A / ΔK / ΔP / H の普遍的集約規則
- 階層間写像
- 資本・市場等の既存概念との具体対応
- 組織・国家等を一つの主体として扱う近似条件
- proxy と理論変数の具体的な対応

また、価値場理論は K / P / A を単一スカラーや確率分布として定義しない。

---

## 13. 関連ノート

- [計測](02_measurement.md)
- [既存概念・応用への射影](../notes/projections.md)
- [拡張・再検討ノート](../notes/future_topics.md)

---

© T. Nuno  
Licensed under CC BY 4.0