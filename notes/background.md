# 価値場理論 — 背景と整理の経緯

> この文書は理論コアではなく、価値場理論が現在の K / P / A 構造へ至るまでの整理経緯を保存する履歴ノートである。以下に登場する X / V 等は過去の検討段階の変数であり、現行 Core では独立変数として用いない。**また、以下の数式・surplus 解釈等には旧案が含まれ、現行 Core / Measurement / Projections の定義が優先される。**

## 1. 発想の出発点

価値場理論は、社会・経済・組織・個人の変化を、既存分野ごとの語彙に閉じず、同じ構造で記述できないかという問題意識から始まった。

初期段階では、

- P：背景構造
- K：自由度
- X：選好
- A：行為

を置き、

```text
P -> K -> X -> A -> K -> P
```

という循環構造を検討した。

その後、P / K / X の境界重複と中間変数の過剰さを減らし、より少ない原始概念で記述する方向へ整理した。

---

## 2. K：自由度から共通の実資源世界へ

初期の K は自由度・選択可能域に近い概念だった。

その後、自由度そのものを原始量とするより、**現実に存在する資源・能力・権利・情報等が、主体の行為可能性を支える**と捉える方が一般的だと整理した。

現行 Core では、K が参照する資源世界は主体ごとに別々に存在するのではなく、**同一の物理的・社会的な実資源世界**として置く。

一方、主体ごとに利用可能な範囲は異なるため、共通 K から主体 `i` のアクセス・利用・行使・参照可能性を `K_i` として導く。

```text
K_t
├─ K_1,t
├─ K_2,t
└─ ...
```

ここで actor-relative なのは K の存在そのものではなく、主体ごとの access / usability view である。現行 Core では `K_i` を独立 state ではなく、K に含まれる資源・権利・資格・契約・制度状態等から導かれる view として扱う。

---

## 3. P：背景構造から主観的評価・期待 state へ

P は最も意味が変化した概念である。

初期には制度・文化・環境等をまとめた背景構造だったが、議論を進める中で、信用、評価、選好、信念、将来見通し、ナラティブ等が、同じ資源条件でも行動を変える側として整理された。

現行では `P_i` を、**主体 i の将来の見通し・評価・選好・信用・信念等を保持し、期待や行動を形成する多次元の subjective evaluation / expectation state** とする。

P を「期待 stock」と呼ぶ場合も、期待値そのものを蓄積した量という意味ではなく、将来価値への期待・評価や行動を生成する側の蓄積構造に着目した呼称である。

---

## 4. X：独立した選好変数から P への統合

初期モデルでは選好方向 X を独立変数として置いていた。

しかし、

- 選好は P の構成要素として扱える
- 将来価値の具体的な見込みは `E[ΔK]` として必要な場合のみ明示できる
- 実現した行動は A として観測できる

ため、X を独立した普遍変数として置く必要性が薄れた。

現行 Core では X を廃止し、選好差は P の構造差へ統合している。

---

## 5. V：価値場変数の廃止

途中では K / P / X から価値場状態 V を生成する案も検討した。

しかし V を独立 state とすると、説明用の中間変数が増える一方、V 自体を独立に観測・同定する必要性が弱かった。

そこで現行 Core では V を置かず、価値場を、**共通 K、主体ごとの利用可能範囲 K_i、主体ごとの P_i の配置・関係が各 A を条件づける構造**として扱う。

「方向性」「引力」という語は action space 上の幾何学的ベクトルを意味しない。

---

## 6. actor-relative の意味の整理

途中の整理では K / P / A / ΔK / ΔP をすべて actor-relative と読める表現を採用していた。

しかし、これは K の存在論を必要以上に相対化する余地があった。

現行では、

- K：共通の実資源世界
- K_i：共通 K から導かれる主体 i の access / usability view
- P_i：主体 i の主観的評価・期待状態
- A_i：主体 i の actor-side process / event
- E_i[ΔK]：主体 i が見込む expected realized resource change

と分ける。

相対性が中心になるのは、主体ごとのアクセス可能性、P、期待評価である。

---

## 7. K / P の境界

P を広い主観的評価・期待構造として扱うと、情報、契約、信用等が K / P の双方に見える問題が生じた。

このため現行では、対象の種類ではなく主体との関係で分ける。

- K：実際に存在し、主体が利用・行使・参照できる資源・能力・権利・情報等
- P：それらを含む環境について主体が保持する見通し・評価・選好・信用・信念等

例えば、行使可能な契約上の権利は K、契約が履行される見込みは P となる。

---

## 8. ΔK / ΔP と基本動学

実現変化を明示するため、K / P の状態変化を ΔK / ΔP として記述するようになった。

現行では `ΔK(S,τ)` を K の state / resource change に予約し、観測仕様 `S` に応じて

```text
Y_S(t) = M_S(K_t)
ΔK(S, τ) = δ_S(Y_S(t0), Y_S(t1)) ∈ D_S
```

と記述する。gross production / consumption / transaction volume 等の区間活動量は `ΔK` に含めず、必要な projection / measurement で

```text
H_S(τ) = h_S((K_t)_{t in τ}, A_τ)
```

のような derived path functional として分離する。

A は K / P を変化させる主要な actor-side process であるが、K の減価償却、自然損耗、災害等の非主体的変化もありうる。

`K_i` は K から導かれる view であるため、K 上の権利・資格・契約・制度状態等が変われば `K_i` も変化しうる。現行 Core では `ΔK_i` を独立原始量として置かない。

---

## 9. P と E[ΔK] の分離

P を主観的評価・期待 state として広く定義すると、特定時点・対象・区間に対する具体的な期待値との区別が必要になった。

途中段階では、期待実資源変化を概念的に

```text
E_i,t[ΔK] = f_i(K_i,t, P_i,t, ...)
```

のように書く案も用いた。

**これは履歴上の概念式であり、現行 Core では普遍的な期待形成関数 `f_i`、確率測度、情報集合を固定しない。**

現在は `ΔK(S,τ) ∈ D_S` に対して quantitative representation

```text
q_S : D_S -> V_S
```

を projection / measurement 側で定め、記法上

```text
E_i[ΔK(S,τ)] := E_i[q_S(ΔK(S,τ))]
```

と略記する。

また、`E[ΔK]` は plan / choice や desire ではなく、特定対象・区間について主体が見込む expected realized resource change として扱う。

---

## 10. 経済学への射影整理

VFT 独自の均衡則を作るのではなく、既存経済学の理論へ K / K_i / P_i / A_i / ΔK / ΔP_i / `E_i[ΔK]` を接続する方針に整理した。

### ミクロ

初期の射影案では `E_i[ΔK]` と A の相互作用を中心に既存ミクロ経済学の均衡・調整過程へ接続する表現を用いた。

その後、**plan / choice と expected realized outcome は別物**と整理し、必要な economic projection では A に含まれる planned / chosen resource change を補助的に `x_i` と書き、予算制約・compatibility は `x_i` 側へ置く方針へ修正した。

compatibility 自体も VFT Core から自動導出される条件ではなく、economic projection が追加する条件として扱う。

VFT では消費と供給を別の存在論として置かない。

また、過去には「主体間移転を相殺した後に残る期待実資源変化」を期待総余剰へ射影する案も検討したが、**これは現行方針では採用していない。** 現在は consumer surplus / producer surplus / total surplus へ接続する場合、valuation、utility、WTP / WTA、cost 等の追加 mapping を射影先で明示する。

### マクロ

政策金利変更、通貨供給量操作、制度変更等をまず政策主体の A とし、それが各主体の P を変え、`ΔP_i` を誘発する経路として整理した。

前区間の資源変化と当期の主観状態側変化との相互作用を既存マクロ経済学へ接続することは、一つの射影候補であり、VFT がミクロ／マクロ一般の時間構造や集約則を定義するものではない。

現行ではミクロとマクロを別 K として置かず、**同じ common K / K transition を異なる `S` から観測する**ことで存在論的に接続する。micro observable から macro observable を再構成する場合のみ aggregation / coarsening rule を追加する。

また、Core の K / P と経済学上の real / nominal は同一視せず、real / nominal は射影先でのみ用いる。

---

## 11. 最適化機能の分離

経済学への射影を検討する中で、個人・企業・国家を別種の存在として定義するより、**同じ K / P / A ontology 上で異なる最適化機能を分離する**方が一般的だと整理した。

候補となる3機能は、

1. resource-realization：望む／見込む `ΔK` の実現へ向けて A を選ぶ
2. activity-flow：K / P 配置を再構成して持続可能な A-flow を最大化する
3. P-downside：主体群の P の大幅な負側・悪化側を抑えるよう K / A を配分する

である。

この整理では、企業の利益は activity-flow から生じる resource/accounting outcome の一面であり、短期赤字を伴う投資・採用・R&D・市場獲得等を例外扱いせず、将来 A-flow の拡張として読める。

国家については、P の真値を直接観測できず、支持率、失業、犯罪、景況感、出生、健康、移住、市場指標等の異質な proxy 間に普遍的加法則がないため、aggregate P の直接最大化より P-downside minimization の方が operational な形として現れやすい、と整理した。

### 自給自足から制度的分業へ

3機能は actor type ではないため、市場・企業・国家が存在しない自給自足でも、単一 actor が全部を担える。

```text
single actor
  ├─ resource-realization
  ├─ activity-flow
  └─ P-downside
```

したがって自給自足を市場経済の例外として置く必要はなく、むしろ最適化機能がまだ制度的に分業されていない最小形として記述できる。

資本主義では概ね、

```text
individuals -> resource-realization
firms       -> activity-flow
state       -> P-downside
```

へ重点が分化した制度形態として読む候補が生じた。

これは現行 Core の普遍法則ではなく、Core ontology 上の explanatory projection として整理している。

---

## 12. 生成構造と計測の分離

Core は、概念的には

```text
K_t, (P_i,t)_i
      ↓ conditions
(A_i,τ)_i
      ↓
K_t1, (P_i,t1)_i
```

という actor-side channel の時間構造を記述する。

一方、実証ではすべてを直接観測できるわけではない。

外部に実現した action event は直接観測できる場合があるが、内部の意思決定、観測、解釈過程は proxy を要する場合がある。P も全構造を直接観測できるとは仮定しない。

`ΔK` / `ΔP` は A の結果 proxy として利用できる場合があるが、A を一意に同定する量ではない。gross activity は必要に応じて `H_S` として別に観測する。

P proxy が価格・金利・信用条件等の market outcome である場合は、target A / ΔK との時間順序、同時決定、post-treatment、outcome leakage を識別する必要がある。

---

## 13. 現行 Core

現在の最小構造は、

```text
common K_t
   ↓ derived access / usability
(K_i,t)_i, (P_i,t)_i
        ↓ conditions
      (A_i,τ)_i
        ↓
K_t1, (P_i,t1)_i
```

である。

K の state / resource change は `ΔK(S,τ)`、P の change / state transition は `ΔP_i` として表す。gross production / consumption / transaction volume 等は Core primitive にせず、必要な projection / measurement で `H_S(τ)` のような derived path functional として記述する。

必要な quantitative projection では `q_S : D_S -> V_S` を定め、`E_i[ΔK(S,τ)]` を `E_i[q_S(ΔK(S,τ))]` の略記として使う。必要な economic projection では A に含まれる planned / chosen resource change を補助的に `x_i` と記述できる。

独立した X / V、普遍的な A 選択関数、P 更新関数、期待形成関数、compatibility 条件、独自の均衡式、3最適化機能の具体的 objective function は Core に置かない。

---

© T. Nuno  
Licensed under CC BY 4.0