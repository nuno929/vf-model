# 価値場理論 — 既存概念・応用への射影ノート

> この文書は価値場理論のコア定義ではなく、既存概念・応用領域への射影候補を保存するためのノートである。

## 1. 射影の基本方針

価値場理論では、

- `K`：共通の実資源世界
- `K_i`：共通 K に対する主体 `i` の access / usability view
- `P_i`：主体 `i` の subjective evaluation / expectation state
- `A_i`：主体 `i` 側の actor-side process / event
- `ΔK(S, τ)`：観測・会計仕様 `S`・時間区間 `τ` に実現した K の change descriptor
- `ΔP_i`：主体 `i` の P に実現した change descriptor / state transition
- `E_i[ΔK(S, τ)]`：主体 `i` が対象範囲・区間について形成する expected realized resource change

を用いる。

K の資源世界そのものは主体ごとに別々に存在しない。actor-relative なのは `K_i`、`P_i`、およびそこから形成される期待評価である。

`K_i` は集合論的な部分集合を必ずしも意味しない。共有情報、権利、信用枠等を含むため、共通 K 上の資源・権利・資格・契約・制度状態等から導かれる actor-relative access / usability view とする。

他主体 `a` について主体 `j` が保持する評価・信用・見通し等を区別する必要がある場合は、`P_j(a)` と書く。これは `a` 自身の P ではなく、評価者 `j` の `P_j` に含まれる主観状態である。

`S` は対象資源・主体だけでなく、resource coordinates、accounting boundary、transformation convention を含む観測・会計仕様である。

一般には、

```text
Y_S(t) = M_S(K_t)
ΔK(S, τ) = δ_S(Y_S(t0), Y_S(t1)) ∈ D_S
```

とみなせる。`δ_S` は必ずしも算術差ではなく、加法的 quantitative projection の場合にのみ `y1 - y0` と置く。

---

## 2. 経済学への射影候補

### 資源・期待・実現

```text
K_t               : 共通の実資源状態
K_i,t             : 主体 i の access / usability view
P_i,t             : 主体 i の主観的評価・期待状態
A_i,t             : 主体 i 側の actor-side process / event
ΔK(S, τ)          : 観測・会計仕様 S / 区間 τ における K の change descriptor
ΔP_i,t            : 主体 i の P の change descriptor / state transition
E_i[ΔK(S, τ)]     : 主体 i が形成する expected realized resource change
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

VFT 単独で記述するのは、各主体の予算・資源制約を満たした `x_i` が、価格・取引条件等のもとで**相互に実行可能・両立可能であるという inter-agent compatibility / feasibility condition** までとする。

この compatibility を標準的な意味で market equilibrium と呼ぶためには、射影先の経済理論が choice / optimality / best response / market-clearing 等の追加条件を与える必要がある。

価格、取引、契約、在庫、信用条件等の observable は各主体の `P_i` を更新し、それに応じて `A_i` / `x_i` / `E_i[ΔK]` が修正されることで、主体間の不整合が調整されうる。

この分散調整を古典経済学の「神の見えざる手」へ射影することは可能だが、VFT Core の普遍則とはしない。

### 会計整合

会計整合、主体間 compatibility、market equilibrium、定常状態は別概念である。

主体間の交換、生産、消費、在庫、投資等を同一の resource coordinates / accounting boundary / transformation convention で記録した結果は、対象 scope の実現 `ΔK` と会計的に整合する。

市場が不均衡でも会計恒等式は成立しうる一方、市場が均衡していても資本蓄積・在庫変化・投資等によって共通 K の `ΔK` は非ゼロになりうる。

### ミクロ／マクロの接続面

VFT はミクロとマクロで数学的に同一の `ΔK` 値型を要求しない。

主体レベルの期待・行動・実現変化を、共通の観測・会計規則のもとで `ΔK(S, τ)` として記録し、`S` / `τ` / aggregation rule を拡張することで、市場・産業・社会・マクロの観測単位へ接続する。

```text
individual K_i / P_i / A_i
          ↓
realized changes
          ↓ common observation / accounting schema
      ΔK(S, τ) ∈ D_S
          ↓ broader S / τ / aggregation
macro-scale observation
```

中心的な可能性は、ミクロからマクロを自動導出することではなく、**異なるスケールの変化を共通の S-indexed observation / accounting schema 上で記述できること**にある。

### 期待変化の集約と余剰

同一の共通 scope `S` に対する複数主体の予測 `E_i[ΔK(S, τ)]` は、単純和して aggregate resource change と解釈しない。

異なる主体の `E_i[ΔK(S_i, τ)]` を集約する場合は、各 `S_i` の意味と会計・換算規則を先に定める。

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

主体ごとの `x_i` は plan / choice 側の planned resource change、`E_i[ΔK(S_i, τ)]` は expected realized change を表しうる。

### 効用

効用は独立した普遍的原始量とはせず、特定理論・目的で K / P / `E[ΔK]` をスカラーへ射影する表現として扱う候補とする。

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

市場では、共通 K に対する主体ごとの access / usability 差 `K_i`、主観状態 `P_i`、planned change `x_i`、期待実現変化 `E_i[ΔK(S_i, τ)]`、行動 `A_i`、価格・取引条件、実現 `ΔK` の相互作用を扱う。

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
- 政策実施による資源変化：ΔK
- 政策等により誘発された主観状態変化：ΔP_i

単一主体へ還元する場合は近似条件と集約規則を明示する。

---

## 8. 射影時に明示するもの

1. 共通 K の対象範囲
2. 対象主体集合
3. 各主体の K への access / usability relation
4. P に用いる proxy
5. 他者評価を扱う場合の評価者 `j` と評価対象 `a`
6. A の観測単位
7. 時間窓 `τ`
8. `S` / `S_i` の resource coordinates / accounting boundary / transformation convention
9. `M_S` / `δ_S` または対応する change mapping
10. ΔK / ΔP の操作化
11. `E_i[ΔK]` の expectation operator / 推定方法
12. planned / chosen change `x_i` の定義と符号規約
13. 価格・会計換算規則
14. 主体別予算制約
15. compatibility を扱う場合の相互両立条件
16. market equilibrium と呼ぶ場合の choice / optimality / best response / clearing 条件
17. 会計恒等式の境界
18. surplus へ射影する場合の valuation / utility / WTP / WTA / cost mapping
19. P の採用次元・proxy・事前固定した検証条件
20. 評価・信用を扱う場合の public information → `P_j(a)` → K / `K_a` 経路
21. 情報損失

---

© T. Nuno  
Licensed under CC BY 4.0