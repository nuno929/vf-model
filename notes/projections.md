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

`K_i` は集合論的な部分集合を必ずしも意味しない。共有情報、権利、信用枠等を含むため、共通 K 上の資源・権利・資格・契約・制度状態等から導かれる actor-relative access / usability view とする。

他主体 `a` について主体 `j` が保持する評価・信用・見通し等を区別する必要がある場合は、`P_j(a)` と書く。これは `a` 自身の P ではなく、評価者 `j` の `P_j` に含まれる主観状態である。

`S` は対象資源・主体だけでなく、resource coordinates、accounting boundary、transformation convention を含む観測・会計仕様である。

state change は、

```text
Y_S(t) = M_S(K_t)
ΔK(S, τ) = δ_S(Y_S(t0), Y_S(t1)) ∈ D_S
```

として表す。`δ_S` は必ずしも算術差ではなく、加法的 quantitative projection の場合にのみ `δ_S(y0,y1)=y1-y0` と置く。

一般形で `Y_S(t0)=Y_S(t1)=y` なら `δ_S(y,y)` を no-change descriptor とみなす。**加法的な在庫 projection では**、生産100・消費100で在庫が元に戻る場合 `ΔK(S,τ)=0` となる。

一方、gross production、gross consumption、transaction volume 等の区間活動量は `ΔK` へ含めず、必要に応じて

```text
H_S(τ) = h_S((K_t)_{t in τ}, A_τ)
```

のような derived path functional として分離する。`A_τ` は区間内 actor-side event / process と必要な event ordering を保持する。`H_S` は Core の primitive ではない。

期待値を取る場合は quantitative representation を

```text
q_S : D_S -> V_S
```

とし、記法上 `E_i[ΔK(S,τ)] := E_i[q_S(ΔK(S,τ))]` と略記する。

---

## 2. 経済学への射影候補

### 資源・期待・実現

```text
K_t               : 共通の実資源状態
K_i,t             : 主体 i の access / usability view
P_i,t             : 主体 i の主観的評価・期待状態
A_i,τ             : 主体 i 側の actor-side process / event
ΔK(S, τ)          : K の state / resource change descriptor
H_S(τ)            : projection-local な interval activity descriptor
ΔP_i              : 主体 i の P の change descriptor / state transition
E_i[ΔK(S, τ)]     : q_S を介した expected realized resource change
```

Core の K / P を経済学上の real / nominal と同一視しない。K は resource / capability side、P は subjective evaluation / expectation side として置き、real / nominal の語は対象とする経済理論への具体的射影でのみ用いる。

### 主体別期待と意思決定

経済射影では、`K_i` を主体 `i` の予算・保有資源・供給能力等の制約側、`P_i` を価格、他主体の生産・消費、信用、将来条件等についての見通し・評価を含む主観状態として読める。

主体 `i` は、自らが利用可能な `K_i` と `P_i` のもとで A を選択し、その結果として実現する資源変化について `E_i[ΔK(S_i, τ)]` を形成しうる。

必要な economic projection では、A に含まれる planned / chosen net resource change を補助的に `x_i` と書く。

```text
x_i          = planned / chosen net resource change
E_i[ΔK(...)] = expected realized resource change
```

`x_i` は projection-local な補助記法であり、Core の新しい原始変数ではない。

`S_i` は共通 K 上の主体 `i` の経済的な観測・会計 scope であり、主体ごとの別資源世界を意味しない。

### 会計的予算制約

`x_i` を取得を正・処分／供給を負とする planned net resource change とし、価格・会計換算ベクトルを `p` とする純粋交換の基本例では、概念的に

```text
p · x_i <= 0
```

のように budget feasibility を表せる。

`p · x_i = 0` は self-financing / budget exhaustion 等を追加仮定する場合の特殊形である。所得、生産収入、投資、借入、移転、税、補助金等を含む場合は、対象理論側で一般予算式を与える。

`E_i[ΔK]` は expected realized change であり、plan / choice 側の `x_i` と一致するとは限らない。

### 主体間整合条件

**VFT notation を用いる最小経済射影では**、各主体の予算・資源制約を満たした `x_i` が、価格・取引条件等のもとで相互に実行可能・両立可能であるという inter-agent compatibility / feasibility condition を追加できる。

compatibility 自体も economic projection 側の条件であり、VFT Core から自動的に導出されるものではない。この compatibility を標準的な意味で market equilibrium と呼ぶためには、さらに射影先の経済理論が choice / optimality / best response / market-clearing 等の追加条件を与える必要がある。

価格、取引、契約、在庫、信用条件等の observable は各主体の `P_i` を更新し、それに応じて `A_i` / `x_i` / `E_i[ΔK]` が修正されることで、主体間の不整合が調整されうる。

この分散調整を古典経済学の「神の見えざる手」へ射影することは可能だが、VFT Core の普遍則とはしない。

### 会計整合

会計整合、主体間 compatibility、market equilibrium、定常状態は別概念である。

対象 scope の net state change は `ΔK`、gross production / consumption / transaction volume / transformation 等は必要に応じて `H_S` として分離して記録する。

加法的な在庫 projection では、生産100・消費100で在庫が元に戻る場合 `ΔK=0` でも、production / consumption を表す `H_S` はそれぞれ100となりうる。

市場が不均衡でも会計恒等式は成立しうる一方、市場が均衡していても資本蓄積・在庫変化・投資等によって `ΔK` は非ゼロになりうる。また、定常的な在庫のもとでも `H_S` は非ゼロになりうる。

### ミクロ／マクロの共通 K 接続

VFT ではミクロとマクロを別々の資源世界として置かない。**両者は同じ common K と同じ K transition を異なる観測・会計仕様 `S` から記述したもの**である。

```text
                 common K
                /        \
          S_micro        S_macro
             ↓              ↓
      micro observation  macro observation
```

したがって、存在論的な接続のために `micro -> macro` の普遍的 aggregation map を要求しない。micro observable から macro observable を再構成する場合にのみ、projection-local な aggregation / coarsening rule を追加する。

これは単に同じ記法を使うという意味ではなく、**観測対象として同じ K を共有することが接続の基礎**である。

### 機能的最適化則

VFT ontology は「個人・企業・国家」を別種の actor として固定しない。その上で、経済・社会 projection では次の3つを functional optimization hypothesis として分離できる。

#### 1. resource-realization

主体は、自らの P と期待のもとで、望む／見込む `ΔK` の実現へ向けて A を選ぶ。

```text
A_i* ∈ argmax_A R_i(A ; P_i, E_i[ΔK])
```

`R_i` は、どの A が主体の望む resource change の実現に寄与すると評価されるかを表す projection-local objective である。これは realized `ΔK` が必ず expectation と一致することを意味しない。

#### 2. activity-flow

主体は、K / P の配置を再構成し、持続可能な A-flow を最大化する。

```text
(K_f*, P_f*)
  ∈ argmax_(feasible K_f,P_f)
      F_f(A-flow | K_f, P_f)
```

企業はこの機能の典型的な担い手として読める。採用、設備投資、資金調達、R&D、組織再編、ブランド形成、契約構成等は、K / P 配置を変えて現在または将来の A-flow を増やす行為として記述できる。

利益は A-flow から生じる resource/accounting outcome の一面であり、objective と自動的に同一視しない。短期的な資源減少・赤字を伴う投資や市場獲得も、将来 A-flow の拡張として説明できる。

#### 3. P-downside

主体群の P の大幅な負側・悪化側を抑えるよう、K / A を配分・調整する。

```text
A_g* ∈ argmin_A L_g^-(P ; observable proxies)
```

国家はこの機能の典型的な担い手として読める。P の真値は直接観測できず、支持率、失業、犯罪、景況感、出生、健康、移住、市場指標等の proxy 間に普遍的な加法則もない。そのため aggregate P の直接最大化より、明確に識別可能な負側・悪化側を抑える operational rule の方が置きやすい。

この downside minimization は、国家が P の上方改善を目的にしないという意味ではない。**異質な P proxy を一つの加法的尺度へ統合できないため、下方の毀損を抑え、上方の改善を個々人・企業の分散的最適化へ委ねる**という制度的構造を表す。

`R_i` / `F_f` / `L_g^-` は Core primitive ではなく、各 projection が具体化する objective functional である。

### 自給自足と制度的分業

3つの最適化則は actor type ではなく機能なので、**市場や企業や国家が存在しない自給自足でも適用できる**。

```text
single actor
  ├─ resource-realization
  ├─ activity-flow
  └─ P-downside
```

自給自足では単一 actor が、望む `ΔK` を目指して A を選び、K / P 配置を組み替えて A-flow を確保し、将来不安・欠乏等の P-downside を抑える。

一方、資本主義ではこれらが概ね、

```text
individuals  -> resource-realization
firms        -> activity-flow
state        -> P-downside
```

へ制度的に分業されると解釈できる。

この見方では市場・企業・国家は理論の前提ではなく、**単一 actor 内でも成立する最適化機能が社会的に分化した制度形態**として後から説明される。

### 期待変化の集約と余剰

同一の共通 scope `S` に対する複数主体の予測 `E_i[ΔK(S, τ)]` は、単純和して aggregate resource change と解釈しない。

異なる主体の `E_i[ΔK(S_i, τ)]` を集約する場合は、各 `S_i`、`q_S`、値空間 `V_S`、会計・換算規則を先に定める。

標準経済学上の consumer surplus / producer surplus / total surplus と接続する場合は、対象理論側で valuation、utility、WTP / WTA、cost 等との mapping を追加的に明示する。

---

## 3. 評価経済・信用経済への射影候補

VFT では、評価・信用に関係する現象を一つの変数へ潰さず、**公開された評価情報、評価者側の主観状態、実際のアクセス可能性を分離したまま接続できる**。

### 評価・評判・信用

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

これにより、「評価や信用が経済的価値を持つ」という現象を、評価値そのものを主体 `a` の P とみなすことなく、**公開情報 → 他者の主観評価 → 行動 → 実アクセス条件 → 実資源変化**という経路で記述できる可能性がある。

### 信用経済

信用経済では、同じ主体 `a` についても、

- 公開された信用情報 → K 上の情報
- 他主体 `j` が `a` に対して保持する返済見込み・信用評価 → `P_j(a)`
- その評価等を背景に `a` が実際に利用可能になった信用枠 → K / `K_a`

を分ける。

したがって、信用の変化が単なる名目評価ではなく、どの時点で実際の borrowing capacity / transaction capability に転換されるかを観測可能な境界として扱える。

### 評価経済

評価経済では、評判・レビュー・ブランド・社会的評価等の公開情報が、各評価者の `P_j(a)` を介して行動を変え、その結果として主体 `a` の取引機会、契約条件、アクセス可能性等の `K_a` を変える経路を候補として扱う。

VFT は「評価そのものが資源である」と一律に定義せず、**公開情報としての K、他者が形成する subjective evaluation としての P、実際のアクセス可能性としての K_i を識別する**。

これらは Core の普遍則ではなく、評価経済・信用経済を実証可能な projection として構成する候補である。

---

## 4. 選好・効用・消費・生産

### 選好

選好を独立した Core 変数には置かない。主体ごとの選好差は P の構造差として扱う。

### 消費 / 生産 / 交換

消費・生産・交換を別の存在論として置かず、主体が共通 K のどの resource coordinates / accounting boundary へどう関与するかを表す経済射影上の action / accounting interpretation として扱う。

主体ごとの `x_i` は plan / choice 側の planned resource change、`E_i[ΔK(S_i, τ)]` は expected realized state change を表しうる。gross activity を期待対象にする場合は `ΔK` ではなく、その activity 用に定義した quantitative `H_S` 等を使う。

### 効用

効用は独立した普遍的原始量とはせず、特定理論・目的で K / P / quantitative expectation をスカラーへ射影する表現として扱う候補とする。

---

## 5. 資本・spillover・市場

### 資本

設備、知識、権利、現金、行使可能な金融請求権、利用可能な信用枠等、実際に利用可能で行動可能性を増やすものは K の構成要素として扱える。名目評価額そのものと K を同一視しない。

### spillover / cross-agent effect

```text
A_i -> change in K affecting K_j
A_i -> change in P_j   (i != j)
```

主体 `i` の A が他主体 `j` の K へのアクセス条件や P に影響する場合、まず **spillover / cross-agent effect** として記述する。

標準経済学上の externality と呼ぶ場合は、市場価格・契約等を介さない影響、他主体の目的・feasible set への影響等、対象 projection 側の定義条件を追加する。

### 市場・ネットワーク

市場では、共通 K に対する主体ごとの access / usability 差 `K_i`、主観状態 `P_i`、planned change `x_i`、期待実現変化 `E_i[ΔK(S_i, τ)]`、区間活動量 `H_S`、行動 `A_i`、価格・取引条件の相互作用を扱う。

ネットワークのノード・エッジは応用上の表現であり、Core の独立関係変数とはしない。

---

## 6. 通貨・金利・信用

### 通貨

通貨を価値判断・交換を同期するプロトコルとして機能的に読むことはできるが、Core 定義ではない。

### 金利

金利を P と同一視しない。政策金利の変更 event は政策主体の A、変更後に持続する制度上の金利条件は必要に応じて K、その条件を主体がどう認識・予測するかは P として区別する。

### 信用

- 公開された信用情報 → K 上の情報
- 主体 `j` が主体 `a` に対して保持する返済見込み・信用評価 → `P_j(a)`
- 主体 `a` が実際に利用可能な信用枠 → K / `K_a`

### 信用崩壊

他主体が保持していた `P_j(a)` 上の見通しが実現変化によって十分に裏づけられず、その後の評価・信用が変化し、信用条件やアクセス可能性として `K_a` へ波及する現象として記述できる。

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
4. P に用いる proxy と proxy admissibility
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
15. functional optimization hypothesis を使う場合の actor / objective / feasible set / time horizon / alternative hypothesis
16. planned / chosen change `x_i` の定義と符号規約
17. 価格・会計換算規則
18. 主体別予算制約
19. compatibility を扱う場合の相互両立条件
20. market equilibrium と呼ぶ場合の choice / optimality / best response / clearing 条件
21. 会計恒等式の境界
22. surplus へ射影する場合の valuation / utility / WTP / WTA / cost mapping
23. P の採用次元・proxy・事前固定した検証条件
24. 評価・信用を扱う場合の public information → `P_j(a)` → K / `K_a` 経路
25. 情報損失

---

© T. Nuno  
Licensed under CC BY 4.0