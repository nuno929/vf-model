# 価値場理論 — 拡張・再検討ノート

> この文書は Core 定義ではなく、今後の展望・具体化候補・再検討事項を保存するためのノートである。

## 1. 集約と分布化

Core では、K は共通の実資源世界、`K_i` は共通 K から導かれる主体ごとの access / usability view、`P_i` は主体ごとの subjective evaluation / expectation state、`A_i` は actor-side process / event として扱う。

今後の検討候補：

- どの条件で分布化が有効か
- 平均・代表主体で失われる情報
- 多峰性・非対称性
- ネットワーク構造をどこまで残すか
- 集約後の ΔK / ΔP が何を代理しているか
- 共有資源・重複アクセスの扱い

---

## 2. K と K_i の表現粒度

K は共通の実資源世界である。

`K_i` は集合論的な部分集合や独立 state に限定せず、共通 K に含まれる資源・権利・資格・契約・制度状態等から導かれる actor-relative access / usability view とする。

今後の検討候補：

- K の標準次元を設けるか
- 物理資源、時間、技能、情報、関係、権利等の分解
- `K_i` の access / usability の操作化
- relational resource / right の表現
- 共有・排他的アクセスの表現
- K 上の条件変化から K_i をどう導出するか
- 資本概念との対応

---

## 3. P の表現粒度

P は主体ごとの subjective evaluation / expectation state として Core で定義済みである。

今後の検討候補：

- P の標準次元を設けるか
- 特定応用でどの期待・評価・選好・信用・信念を抽出するか
- P proxy の操作化
- 同一 observable が K / P の両方に関係する場合の識別
- 他主体・価格・将来条件についての期待をどの粒度で保持するか
- projection ごとの P 次元を観測前に固定する方法

---

## 4. ΔK / ΔP と scope S

Core では `ΔK(S, τ)` を、観測・会計仕様 `S` について時間区間 `τ` 内に実現した実資源量の差分として扱う。

`S` は単なる対象集合ではなく、少なくとも以下を含む。

- 対象資源・主体
- resource coordinates
- accounting boundary
- transformation convention

`ΔK` はミクロ／マクロで数学的に同一の値型を要求しない。各 `S` ごとに値域 `D_S` が異なりうるものとして、同じ S-indexed schema を共有する。

```text
ΔK(S, τ) ∈ D_S
```

今後の検討候補：

- `S` の標準的な記述形式
- `D_S` の定義方法
- 各応用で始点・終点を比較可能にする表現
- 加法表現を採用できる条件
- 非加法成分の quantitative projection
- 個別実現変化と集約 `ΔK` の会計対応
- 共有資源変化と `K_i` 変化の対応
- ΔP proxy の測定誤差

---

## 5. 期待区間変化 E[ΔK]

`E_i[ΔK(S, τ)]` は、主体 `i` が対象 scope / interval について形成する expected realized resource change として Core で区別済みである。

`E[...]` を expectation operator として用いるのは、対象となる ΔK が quantitative projection 上で表現され、期待値が定義可能な場合である。Core は確率測度・情報集合・期待形成式を固定しない。

今後の検討候補：

- expectation operator の確率測度・情報集合
- planned resource change と expected realized resource change の区別
- state-wise / almost-sure feasibility
- 期待対象となる消費・生産等の範囲
- `S` / `S_i` / `τ`
- 確率的期待値と定性的 forecast の接続
- 実測可能な expectation survey 等との対応
- 他主体の期待・行動についての予測が P にどう入るか
- `E_i[ΔK]` と実現 `ΔK` の乖離分解

---

## 6. 会計的予算制約

必要な economic projection では、A に含まれる planned / chosen resource change を補助的に `x_i` と書く。

```text
x_i          = planned / chosen resource change
E_i[ΔK(...)] = expected realized resource change
```

`x_i` は projection-local な補助記法であり、Core の新しい原始変数ではない。

純粋な交換で価格・会計換算ベクトルを `p` とする場合、

```text
p · x_i = 0
```

のような planned resource change の会計的予算整合へ射影できる。

今後の検討候補：

- 所得・生産収入・投資・借入・移転を含む一般予算式
- intertemporal budget constraint
- 信用枠・金融請求権を含む予算制約
- 非市場資源の会計換算
- planned action と expected outcome の関係

---

## 7. compatibility / market equilibrium / 会計整合 / 定常状態

以下を分離して扱う。

- **inter-agent compatibility / feasibility**：各主体の予算・資源制約を満たした `x_i` が、価格・取引条件等のもとで相互に実行可能・両立可能であること
- **market equilibrium**：compatibility に加え、射影先理論が choice / optimality / best response / market-clearing 等を与えた状態
- **会計整合**：同一事象を共通の会計境界・換算規則で記録した結果が収支上整合すること
- **定常状態**：対象 K の増減が小さい等、別途定める状態条件

今後の検討候補：

- compatibility の形式化
- market equilibrium へ必要な追加条件
- 在庫・資本蓄積・投資を含む stock-flow accounting
- 会計恒等式と行動均衡を同じデータで識別する方法
- 均衡への収束性・複数均衡・不安定均衡
- 情報非対称・外部性・市場支配下の均衡
- 市場外制度での調整条件

---

## 8. 分散的調整と「見えざる手」

各主体が `K_i` / `P_i` のもとで budget-feasible な `x_i` を形成し、価格・取引・信用等を介してその選択を修正することで、主体間の不整合が分散的に調整される可能性がある。

この構造を古典経済学の「神の見えざる手」へ射影することは可能だが、現時点では projection candidate であり、Core の確立済み主張ではない。

今後の検討候補：

- どの市場制度で主体間不整合が縮小するか
- 価格がどの情報を伝達するか
- どの条件で調整が収束するか
- herd behavior / network dependence / common shock で調整がどう崩れるか
- 均衡と社会的最適の差
- 外部性・情報非対称・市場支配をどう表現するか

---

## 9. ミクロ／マクロ接続面の操作化

VFT が現時点で与えるのは、ミクロからマクロを自動的に導出する substantive aggregation law ではなく、異なるスケールを共通の observation / accounting schema 上で記述する接続面である。

中心課題は、主体レベルの A・実現変化を `ΔK(S, τ) ∈ D_S` として記録し、`S` / `τ` / aggregation rule を変えながら、既存の市場・産業・マクロ観測量とどう対応づけるかである。

今後の検討候補：

- 個人の realized change をどの会計規則で `ΔK` へ接続するか
- `S` の拡張と aggregation rule の関係
- stock-flow consistent な接続
- aggregation bias / nonlinearities / network effects の扱い
- 個人期待と集計マクロ変数の識別
- 政策 A → ΔP_i → A_i → ΔK の経路
- macro observable から micro structure をどこまで逆推定できるか

---

## 10. 評価経済・信用経済への射影

VFT の有力な応用候補として、評価・信用が主観状態と実資源アクセスへどう変換されるかを同一状態表現上で扱うことがある。

基本的な分離は以下。

- 評価、評判、ブランド、相手への信用、返済見込み、将来見通し → `P_i`
- 実際に行使可能な信用枠、請求権、契約上の権利、アクセス可能な取引機会 → `K / K_i`

候補経路：

```text
rating / reputation / trust
        ↓
      P_i
        ↓
subjective evaluation / expectation and decision
        ↓
       A_i
        ↓
rights / contract / credit conditions in K
        ↓
      K_i
        ↓
   realized ΔK
```

今後の検討候補：

- 評価 observable と P の measurement mapping
- 評価から信用条件への変換関数
- 信用評価と実際の borrowing capacity の識別
- レビュー・評判が契約機会や価格条件に与える影響
- P → K 上の条件 → K_i の時間遅延
- 評価ショック / 信用ショックから ΔK までの因果識別
- ネットワーク上の評判伝播
- 評価経済・信用経済でのミクロ／マクロ接続

---

## 11. 期待変化の集約と余剰

同一共通 scope に対する複数主体の `E_i[ΔK(S, τ)]` を単純和して aggregate resource change としない。

異なる主体の `E_i[ΔK(S_i, τ)]` を集約する場合は、各 `S_i` の意味と会計・換算規則を先に定める。

標準経済学上の surplus へ接続するには追加 mapping が必要である。

今後の具体化候補：

- utility / valuation mapping
- WTP / WTA / cost との対応
- consumer surplus / producer surplus / total surplus との対応条件

---

## 12. A の観測と順序

A は actor-side process / event として、外部 action、decision、perception / update process を必要に応じて含む。

今後の具体化候補：

- A のイベント単位
- 外部 action と perception / update process の区別
- 観測・情報受容・解釈の操作化
- 区間内イベント順序を保持する条件
- coarse-grained representation の情報損失
- ΔK / ΔP がどの範囲の A を代理するか
- A と結果 proxy の時間遅延

---

## 13. 価値場の最小形式化

現行 Core では、価値場を K / K_i / P の配置・関係が A を条件づける structural framework として定義し、独立した V や普遍的選択関数を置かない。

今後、説明力・反証可能性のために最低限の形式化が必要になった場合は、action correspondence や feasible / plausible action set の導入を検討できる。

ただし、これを Core に追加する場合は、feasible と plausible の区別、確率表現との関係、追加変数の必要性を先に検討する。

---

## 14. P の反証可能性

P が観察後の residual state にならないよう、projection / empirical model ごとに、採用する P 次元、proxy、A / E[ΔK] への mapping、事前予測・識別条件を観測前に固定する必要がある。

今後の具体化候補：

- pre-registration に相当する仕様記述
- P 次元の選択基準
- competing model との比較方法
- out-of-sample prediction
- action correspondence と P の識別

---

## 15. 組織・国家等の集約主体近似

組織・国家等を単一主体として扱うことは Core 前提ではない。

必要な場合は近似として導入し、対象主体、共通 K の対象範囲、各主体の `K_i` / `P_i`、A の集約方法、ΔK の会計・集約規則、情報損失、内部対立を明示する。

---

## 16. 実証・計量化

今後の具体化候補：

- 共通 K の観測設計
- `K_i` の導出・access / usability
- P proxy
- K / P 識別
- A の直接観測と潜在 decision / perception の proxy
- ΔK / ΔP の結果 proxy 設計
- `E[ΔK]` の expectation operator / 推定
- `S` / `D_S` / `τ` の定義
- planned / expected / realized change の分離
- compatibility / market equilibrium / accounting identity の同時計測
- ミクロ／マクロ接続面の実証
- 評価・信用 → P → K 上の条件 → K_i → ΔK の因果計測
- 測定誤差・欠測
- ケーススタディ
- 反実仮想設計

---

© T. Nuno  
Licensed under CC BY 4.0