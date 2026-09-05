# 価値場理論 — 既存概念・応用への射影ノート

> この文書は価値場理論のコア定義ではなく、既存概念・応用領域への射影候補を保存するためのノートである。

## 1. 射影の基本方針

価値場理論では、

- `K`：共通の実資源世界
- `K_i`：共通 K から導かれる主体 `i` の access / usability view
- `P_i`：主体 `i` の subjective evaluation / expectation state
- `A_i`：主体 `i` 側の actor-side process / event
- `ΔK(S, τ)`：観測・会計仕様 `S`・時間区間 `τ` に実現した実資源量の差分
- `ΔP_i`：主体 `i` の P に実現した区間差分
- `E_i[ΔK(S, τ)]`：主体 `i` が対象範囲・区間について形成する期待実資源変化

を用いる。

K の資源世界そのものは主体ごとに別々に存在しない。actor-relative なのは `K_i`、`P_i`、およびそこから形成される期待評価である。

`K_i` は集合論的な部分集合や独立 state を必ずしも意味しない。共有情報、権利、信用枠等を含むため、共通 K に含まれる資源・権利・資格・契約・制度状態等から導かれる actor-relative view とする。

`S` は対象資源・主体だけでなく、resource coordinates、accounting boundary、transformation convention を含む観測・会計仕様である。

---

## 2. 経済学への射影候補

### 資源・期待・実現

```text
K_t               : 共通の実資源状態
K_i,t             : 主体 i の access / usability view
P_i,t             : 主体 i の主観的評価・期待状態
A_i,t             : 主体 i の actor-side process / event
ΔK(S, τ)          : 観測・会計仕様 S / 区間 τ で実現した実資源差分
ΔP_i,t            : 主体 i に実現した主観状態の差分
E_i[ΔK(S, τ)]     : 主体 i が形成する期待実資源差分
```

Core の K / P を経済学上の real / nominal と同一視しない。K は resource / capability side、P は subjective evaluation / expectation side として置き、real / nominal の語は対象とする経済理論への具体的射影でのみ用いる。

### 主体別 plan / choice と期待

経済射影では、`K_i` を主体 `i` の予算・保有資源・供給能力等の制約側、`P_i` を価格、他主体の生産・消費、信用、将来条件等についての見通し・評価を含む主観状態として読める。

必要な economic projection では、A に含まれる planned / chosen resource change を補助的に `x_i` と書く。

```text
x_i          = planned / chosen resource change
E_i[ΔK(...)] = expected realized resource change
```

`x_i` は projection-local な補助記法であり、Core の新しい原始変数ではない。

主体 `i` は `K_i` / `P_i` のもとで `x_i` を選択し、その plan を含む状況から実際に起こると見込む資源変化を `E_i[ΔK(S_i, τ)]` として形成しうる。両者は一致するとは限らない。

`S_i` は共通 K 上の主体 `i` の経済的な観測・会計 scope であり、主体ごとの別資源世界を意味しない。

### 会計的予算制約

予算制約・実行可能性が直接制約するのは plan / choice 側である。

価格・会計換算ベクトルを `p` とし、純粋な交換を同一会計境界内で扱う場合には、概念的に

```text
p · x_i = 0
```

のように planned resource change の会計的予算整合を表せる。

所得、生産収入、投資、借入、移転、税、補助金等を含む場合は、対象理論側で一般予算式を与える。

### 主体間整合条件

VFT 単独で記述するのは、各主体の予算・資源制約を満たした `x_i` が、価格・取引条件等のもとで**相互に実行可能・両立可能であるという inter-agent compatibility / feasibility condition** までとする。

この compatibility を標準的な意味で market equilibrium と呼ぶためには、射影先の経済理論が choice / optimality / best response / market-clearing 等の追加条件を与える必要がある。

価格、取引、契約、在庫、信用条件等の observable は各主体の `P_i` を更新し、それに応じて A / `x_i` / `E_i[ΔK]` が修正されることで、主体間の不整合が調整されうる。

この分散調整を古典経済学の「神の見えざる手」へ射影することは可能だが、VFT Core の普遍則とはしない。

### 会計整合

会計整合、主体間 compatibility、market equilibrium、定常状態は別概念である。

主体間の交換、生産、消費、在庫、投資等を同一の resource coordinates / accounting boundary / transformation convention で記録した結果は、対象 scope の実現 `ΔK` と会計的に整合する。

市場が不均衡でも会計恒等式は成立しうる一方、市場が均衡していても資本蓄積・在庫変化・投資等によって共通 K の `ΔK` は非ゼロになりうる。

### ミクロ／マクロの接続面

VFT は、ミクロとマクロで数学的に同一な `ΔK` の値型を要求しない。

各観測・会計仕様 `S` に応じて値域 `D_S` が異なりうるものとして、概念的には

```text
ΔK(S, τ) ∈ D_S
```

と扱う。

主体レベルの行動・実現変化を、共通の observation / accounting schema のもとで `ΔK(S, τ)` として記録し、`S` / `τ` / aggregation rule を変えることで、市場・産業・社会・マクロの観測単位と接続する。

```text
individual K_i / P_i / A_i
          ↓
realized resource changes
          ↓ observation / accounting specification
      ΔK(S, τ) ∈ D_S
          ↓ broader S / τ / aggregation
macro-scale observation
```

これはミクロからマクロを自動導出する普遍的 aggregation law ではなく、**異なるスケールを共通 schema 上で記述するための接続面**である。

### 期待変化の集約と余剰

同一の共通 scope `S` に対する複数主体の予測 `E_i[ΔK(S, τ)]` は、単純和して aggregate resource change と解釈しない。

異なる主体の `E_i[ΔK(S_i, τ)]` を集約する場合は、各 `S_i` の意味と会計・換算規則を先に定める。

標準経済学上の consumer surplus / producer surplus / total surplus と接続する場合は、対象理論側で valuation、utility、WTP / WTA、cost 等との mapping を追加的に明示する。

---

## 3. 評価経済・信用経済への射影候補

VFT では、評価・信用に関係する現象を一つの変数へ潰さず、**P 側の主観的評価・期待と K 側の実アクセス可能性を分離したまま接続できる**。

### 評価・評判・信用

- 評価、評判、ブランド評価、相手への信用、返済見込み、将来見通し → `P_i`
- 実際に行使可能な信用枠、金融請求権、契約上の権利、アクセス可能な取引機会 → `K_i`

例えば、評価・信用の変化が次のような経路を持つ projection を考えられる。

```text
rating / reputation / trust observable
              ↓
          P_i / ΔP_i
              ↓
 expectation / decision change
              ↓
             A_i
              ↓
rights / credit terms / contract conditions in K
              ↓
            K_i
              ↓
        realized ΔK
```

これにより、「評価や信用が経済的価値を持つ」という現象を、評価値そのものを K とみなすことなく、**主観状態 → 行動 → K 上のアクセス条件 → K_i → 実資源変化**という経路で記述できる可能性がある。

### 信用経済

信用経済では、同じ主体についても、

- 信用されているという評価・返済見込み → P
- その評価等を背景に実際に利用可能になった信用枠 → K / K_i

を分ける。

したがって、信用の変化が単なる名目評価ではなく、どの時点で実際の borrowing capacity / transaction capability に転換されるかを観測可能な境界として扱える。

### 評価経済

評価経済では、評判・レビュー・ブランド・社会的評価等が P を介して他主体の期待と A を変え、その結果として契約・権利・取引条件等の K 上の状態が変わり、`K_i` のアクセス可能性へ波及する経路を候補として扱う。

VFT は「評価そのものが資源である」と一律に定義せず、**評価が主観状態なのか、実際のアクセス可能性へ変換された資源・権利なのかを K / P 境界で識別できる**。

これらは Core の普遍則ではなく、評価経済・信用経済を実証可能な projection として構成する候補である。

---

## 4. 選好・効用・消費・生産

### 選好

選好を独立した Core 変数には置かない。主体ごとの選好差は P の構造差として扱う。

### 消費 / 生産 / 交換

消費・生産・交換を別の存在論として置かず、主体が共通 K のどの resource coordinates / accounting boundary へどう関与するかを表す経済射影上の action / accounting interpretation として扱う。

planned / chosen resource change は必要な projection で `x_i` として表し、その実現見込みは `E_i[ΔK(S_i, τ)]` として区別する。

### 効用

効用は独立した普遍的原始量とはせず、特定理論・目的で K / P / A / `E[ΔK]` 等をスカラーへ射影する表現として扱う候補とする。

---

## 5. 資本・外部性・市場

### 資本

設備、知識、権利、現金、行使可能な金融請求権、利用可能な信用枠等、実際に利用可能で行動可能性を増やすものは K の構成要素として扱える。名目評価額そのものと K を同一視しない。

### 外部性

```text
A_i -> ΔK
A_i -> ΔP_j   (i != j)
```

主体 i の A が実資源差分 `ΔK` を生み、その結果として他主体の `K_j` や `P_j` が変化する場合を外部性として記述できる。

### 市場・ネットワーク

市場では、共通 K に対する主体ごとの access / usability 差 `K_i`、主観状態 `P_i`、planned / chosen resource change `x_i`、期待差分 `E_i[ΔK(S_i, τ)]`、actor-side process `A_i`、価格・取引条件、実現差分 `ΔK` の相互作用を扱う。

ネットワークのノード・エッジは応用上の表現であり、Core の独立関係変数とはしない。

---

## 6. 通貨・金利・信用

### 通貨

通貨を価値判断・交換を同期するプロトコルとして機能的に読むことはできるが、Core 定義ではない。

### 金利

金利を P と同一視しない。政策金利の変更や金利条件の提示は A として扱い、その結果として主体の主観的評価・期待状態に変化を誘発する経路へ射影する。

### 信用

- 実際に利用可能な信用枠 → K / K_i
- 返済見込み・相手への信用・将来評価 → P_i

### 信用崩壊

P 上で成立していた見通しが実現 `ΔK` によって十分に裏づけられず、その後の P の形成・維持が変化し、契約・権利・信用条件等の K 上の状態を通じて `K_i` へ波及する現象として記述できる。

---

## 7. 国家・政治・組織

国家や組織を自動的に単一主体として扱わない。

- 政策・公約・宣言：主体の A
- 支持率・評価等：P の proxy 候補
- 政策実施による資源差分：ΔK
- 政策等により誘発された主観状態変化：ΔP_i

単一主体へ還元する場合は近似条件と集約規則を明示する。

---

## 8. 射影時に明示するもの

1. 共通 K の対象範囲
2. 対象主体集合
3. 各主体の K への access / usability の導出条件
4. P に用いる proxy
5. A の観測単位
6. 時間窓 `τ`
7. `S` / `S_i` の resource coordinates / accounting boundary / transformation convention
8. ΔK / ΔP の操作化と `D_S`
9. `E_i[ΔK]` の expectation operator / 推定方法
10. economic projection で plan / choice を扱う場合の `x_i`
11. 価格・会計換算規則
12. 主体別予算制約
13. compatibility を扱う場合の相互両立条件
14. market equilibrium と呼ぶ場合の choice / optimality / best response / clearing 条件
15. 会計恒等式の境界
16. surplus へ射影する場合の valuation / utility / WTP / WTA / cost mapping
17. P の採用次元・proxy・事前固定した検証条件
18. 評価・信用を扱う場合の P → K 上の条件 → K_i の経路
19. 情報損失

---

© T. Nuno  
Licensed under CC BY 4.0