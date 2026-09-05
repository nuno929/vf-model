# 価値場理論 — 計測

## 1. 目的

本書は、価値場理論の Core を実証・観測へ落とす際の境界を整理する。

Core では、K は共通の実資源世界、`K_i` はそのうち主体 `i` がアクセス・利用・行使・参照可能な actor-relative view、`P_i` は主体ごとの subjective evaluation / expectation state として扱う。

計測上の課題は、K / P / A を一つのスカラーへ還元することではなく、**どの資源、主体、時間窓、resource coordinates、accounting boundary、transformation convention、proxy、集約規則を観測対象にするかを明示すること**である。

---

## 2. K と K_i の計測

K は共通の実資源世界を参照する。

`K_i` は、その K のうち主体 `i` が実際にアクセス・利用・行使・参照可能な actor-relative view である。

`K_i` は集合論的な部分集合を必ずしも意味しない。共有情報、インフラ、権利、信用枠、制度上利用可能な手段等では、主体ごとの access / usability relation を通じて操作化する。

したがって、同じ設備、情報、インフラ、信用制度等が複数主体の `K_i` に関係しうるが、資源自体が主体ごとに複製されたことを意味しない。

K の候補指標には、利用可能な現金残高、行使可能な金融請求権、受取可能額、earning capacity、設備・在庫・インフラ、時間、人員、技能、知識、情報、利用可能な信用枠、権限・アクセス可能な手段等がある。

期間所得そのものは通常 flow であり、K の stock/state と同一視しない。期間中に実現した所得受取は state transition または interval activity として扱い、受取可能な請求権や earning capacity 等を K 側へ置く。

金融資源は、名目上の評価額そのものではなく、実際に行動可能性を増やす利用可能な資源・権利として K / `K_i` へ操作化する。

---

## 3. P の計測

`P_i` は主体 `i` の将来の見通し・評価・選好・信用・信念等を保持する多次元の subjective evaluation / expectation state である。

他主体 `a` について主体 `j` が保持する評価・信用・見通し等を区別する必要がある場合は、`P_j(a)` と書く。これは `a` 自身の P ではなく、評価者 `j` の主観状態である。

個々の `P_i` の全構造を直接観測できるとは仮定しない。

候補 proxy には、調査された期待・信念・選好・評価、発話、契約に対する信用、評判・ブランド評価、価格、金利、スプレッド、信用条件等がある。

価格・金利・スプレッド・信用条件等は P そのものではなく、P と K / A / 制度・市場過程等の相互作用から生じる observable でありうる。

### P proxy admissibility

market outcome 等を P の proxy として用いる場合は、同時決定・post-treatment・outcome leakage を避けるため、少なくとも以下を確認する。

1. proxy が target `A` / `ΔK` より前に観測されたものか
2. 同時決定の場合、joint structural / measurement model を明示しているか
3. target outcome を使って latent P を事後的に構成していないか
4. proxy validity を別データ、独立測定、または追加制約で検証できるか

`P_t -> A_t -> price_t` のような構造が想定されるのに、同じ `price_t` から `P_t` を復元して `A_t` を説明する、といった循環を避ける。

### 理論変数と observable の分離

`P_i` / `ΔP_i` は理論上の subjective state とその変化であり、直接観測できることを Core の要件とはしない。価格、金利、調査値、信用条件、発話等は、それらと K / A / 制度・市場過程等の相互作用から生じる observable / proxy として扱う。

したがって、**理論変数と observable の対応は応用・計測ごとに定める measurement mapping であり、Core が普遍的な観測式を固定するものではない。**

---

## 4. K / P の識別原則

K / P は対象物の種類だけで分類しない。

- **K**：実際に存在し、主体が利用・行使・参照できる資源・能力・権利・情報等
- **P**：それらを含む環境について主体が保持する見通し・評価・選好・信用・信念等

例：

- 契約上行使可能な権利 → K
- 契約が履行される見込み → P
- 参照可能な情報 → K
- その情報から形成された将来見通し → P
- 公開レビュー値 → K 上の accessible information
- そのレビューを読んだ `j` が `a` をどう信用するか → `P_j(a)`

同一 observable を根拠なく K / P の双方へ二重投入しない。

### event / persistent state / subjective representation

同じ観測対象が複数段階に現れる場合は、少なくとも

```text
actor-side event A
        ↓
persistent / accessible world state in K
        ↓ perception / interpretation
subjective representation in P
```

のどこを代理しているかを固定する。

例えば政策金利なら、変更 event は政策主体の A、変更後に持続する制度条件は必要に応じて K、それを主体がどう認識・予測するかは P として区別する。

---

## 5. A の観測可能性と時間型

A は各主体側で生じる actor-side process / event を表す。

外部に実現した action event は直接観測できる場合がある。取引、移動、発話、投資、労働、契約、政策変更等が該当する。

一方、内部の意思決定、観測、情報受容、解釈等は直接観測できない場合があり、proxy を要する。

観測・情報受容・解釈を A に含める場合も、それらが必ず能動的行為であることを意味しない。P 更新を記述する actor-side process として必要な範囲で含める。

時間順序は、選択則・更新則を固定せず、概念的には

```text
(K_t0, P_t0)
      ↓ conditions
A_(t0,t1]
      ↓ realized interval processes
(K_t1, P_t1)
```

とする。これは **actor-side channel の temporal typing** であり、普遍的な状態遷移関数を意味しない。減価償却・自然消耗・災害や記憶減衰等の A を介さない変化は、この図とは別に必要な projection で扱う。

P → A の時間的・因果的関係を検証する projection で、A 区間内の information reception / interpretation 等が途中で P を更新し、その後の decision / action に影響する場合は、**区間を分割するか event ordering を保持する**。途中更新後の P を初期 `P_t0` と同一視しない。

---

## 6. ΔK / ΔP と区間活動量の観測

観測・会計仕様 `S` と時間区間 `τ=[t0,t1]` を明示した K の state / resource change を `ΔK(S, τ)` とする。

`S` は少なくとも以下を含む。

1. 対象資源・主体
2. resource coordinates
3. accounting boundary
4. transformation convention

### state change `ΔK`

観測仕様に対応する state representation を

```text
Y_S(t) = M_S(K_t)
ΔK(S, τ) = δ_S(Y_S(t0), Y_S(t1)) ∈ D_S
```

とする。`M_S` と `δ_S` は measurement / projection 側で定める specification-local な写像・演算であり、Core の新しい原始変数ではない。

`ΔK` は必ずしも算術差分を意味しない。加法的な quantitative projection が適用できる場合にのみ、

```text
δ_S(y0, y1) = y1 - y0
Y_S(t1) = Y_S(t0) + ΔK(S, τ)
```

と置ける。`K_t1 = K_t0 + ΔK` は、さらに `M_S = id` で K 自体が同じ加法空間にある特殊ケースに限る。

一般形では `δ_S(y,y)` を no-change descriptor とみなす。**加法的な在庫 projection では**、生産 100・消費 100 で在庫が元に戻る場合 `ΔK(S,τ)=0` となる。

### interval activity `H_S`

gross production、gross consumption、transaction volume、resource transformation 等は state change そのものではないため、`ΔK` へ含めない。必要な measurement / projection では、

```text
H_S(τ) = h_S((K_t)_{t in τ}, A_τ)
```

のような derived path functional / interval activity descriptor として分離する。`A_τ` は区間内の actor-side event / process を保持し、必要なら event ordering を保持する。

`H_S` は Core の新しい primitive / state ではない。上の加法的在庫例でも、production / consumption を表す `H_S` はそれぞれ 100 と記録できる。

`ΔP_i` も一般には算術差ではなく、主体 `i` の P に実現した change descriptor / state transition を表す。非加法的な場合は少なくとも

```text
P_i,t0 -> P_i,t1
```

として扱い、数量化が必要な場合だけ measurement mapping を追加する。

`ΔK` はミクロ用・マクロ用に数学的な同一型を要求しない。`S` に応じて `D_S`、座標、単位、集約規則等は異なりうるが、**S-indexed state-change schema** は共通に保つ。区間活動量は必要に応じて別の `H_S` として定義する。

---

## 7. P の変化と観測

A は P を変化させる主要な actor-side process である。

政策変更、価格提示、契約条件変更、情報伝達、観測・情報受容・解釈等による P の変化も、必要に応じて A を介する経路として記述できる。

記憶減衰等の微小・非主体的な P の変化の存在自体は否定しない。ただし、それが観測可能な A や P proxy に意味のある差を生じない限り、Core の主要変化経路として明示的に操作化しない。

---

## 8. E[ΔK] の位置づけ

`ΔK(S, τ)` の値域 `D_S` は非数量・非加法でありうるため、期待値を取る場合は quantitative representation を明示する。

```text
q_S : D_S -> V_S
```

`V_S` は対象 projection で expectation が定義可能な quantitative value space とする。

記法上、

```text
E_i[ΔK(S, τ)] := E_i[q_S(ΔK(S, τ))]
```

と略記する。左辺は generic change descriptor 自体へ直接 expectation operator を掛ける意味ではない。

Core は `q_S` の具体形、`E_i` に対応する確率測度・情報集合・期待形成式を普遍的に固定しない。具体的な quantitative representation / expectation operator は対象 projection / measurement model で与える。

`E[...]` は主体が形成する見込み値・期待値を表し、主体の望みそのものではない。選好・望ましさ・評価は P に保持され、期待形成や A に影響しうる。

---

## 9. 集約と共通 K

VFT は、複数主体の `K_i` / `P_i` / `A_i` を自動的に一主体・一変数へ集約しない。

ただしミクロとマクロは別の資源世界ではなく、**同じ common K を異なる観測・会計仕様 `S` から見る**。micro observable から macro observable を再構成する場合にだけ、projection-local な aggregation / coarsening rule を明示する。

集約する場合は少なくとも以下を明示する。

1. 共通 K の対象範囲
2. 対象主体集合
3. 各主体の K へのアクセス・利用可能性
4. P に用いる proxy
5. A の観測単位とイベント順序
6. `τ`
7. `S` の resource coordinates / accounting boundary / transformation convention
8. `M_S` / `δ_S` または対応する state-change mapping
9. `H_S` を使う場合の path functional
10. `q_S` を使う場合の quantitative representation
11. ΔK / ΔP / H の集約規則
12. 共有資源・重複アクセスの扱い
13. 情報損失

---

## 10. 経済射影での会計的予算制約

経済射影では、主体 `i` の economic scope を `S_i` とする。

必要な projection では、A に含まれる planned / chosen net resource change を `x_i` と書く。取得を正、処分／供給を負とする符号規約を採用し、価格・会計換算ベクトルを `p` とする純粋交換の基本例では、

```text
p · x_i <= 0
```

として budget feasibility を操作化できる。`p · x_i = 0` は self-financing / budget exhaustion 等を追加仮定した特殊形である。

`E_i[ΔK(S_i, τ)]` は expected realized resource change であり、plan / choice である `x_i` と一致するとは限らない。

---

## 11. 3つの管理合理性を扱う計測

resource-realization / activity-flow / P-downside の3則は、VFT 上で管理合理性を記述するための基本前提として扱う。したがって、計測の目的は「3則そのものが存在するか」を毎回実証することではない。

経験的に扱うのは、各 projection / 組織 / 制度で、3則がどの actor によってどのように遂行・分担・重複され、その結果どのような A / K / P / H / ΔK が生じるかである。

quantitative model を置く場合は、3則そのものと、その具体的数理化を分離する。例えば `R_i` / `F_f` / `L_g^-` のような objective functional を導入する場合、それらの関数形・制約・時間 horizon は projection-specific であり、観測・比較の対象になる。

少なくとも以下を明示する。

1. 各管理合理性を担う actor / actor set
2. 具体的な objective / outcome proxy を置く場合の observable
3. feasible set / constraints
4. 対象時間窓
5. 予測・評価する A / K / P / H / ΔK の変化
6. 管理機能の分担・重複・conflict
7. 代替的な objective / organizational arrangement との比較条件

企業型の activity-flow を扱う際、profit は outcome / objective proxy の一つであって activity-flow rule 自体と同一視しない。短期損失を伴う投資・採用・R&D・市場獲得等が将来 A-flow をどう変えるかを別途観測する。

国家・governance 型の P-downside を扱う際、異質な P proxy 間に普遍的な加法則を仮定しない。支持率・失業・犯罪・景況感・出生・健康・移住・市場指標等が何の P 次元を代理するかを固定し、downside 判定を事前定義する。

既存の管理階層と VFT 三則の関係を研究する場合は、三階層の存在そのものを検証対象にするのではなく、**各階層で3則がどう遂行・分担・重複し、その管理成果とどう関係するか**を比較する。

---

## 12. 主体間整合・market equilibrium・会計整合・定常状態

以下は別概念として扱う。

- **主体間整合 / compatibility**：economic projection が追加する条件として、各主体の予算・資源制約を満たした `x_i` が、価格・取引条件等のもとで相互に実行可能・両立可能であること
- **market equilibrium**：上記 compatibility に加え、射影先の理論が choice / optimality / best response / market-clearing 等の条件を与えた状態
- **会計整合**：同じ state change / interval activity を同一会計境界・換算規則で記録した結果が収支上整合すること
- **定常状態**：対象 scope の K が区間を通じて実質的に増減しない等、別途定める状態条件

compatibility 自体も VFT Core から自動導出されるものではなく、economic projection 側の追加条件である。

---

## 13. P の実証上の制約

P が観察後の residual state にならないよう、各 projection / empirical model では少なくとも以下を観測・推定前に固定する。

1. 採用する P の次元
2. 各次元の observable / proxy
3. proxy admissibility
4. P と A / E[ΔK] の mapping
5. 検証対象となる事前予測または識別条件
6. 代替説明と比較する基準

観察された A の差を説明するために事後的に任意の P 次元や proxy を追加することは避ける。

---

## 14. 評価・信用経済を扱う場合

評価対象 `a` と評価者 `j` を区別する。

- 公開レビュー値・rating 等 → K 上の accessible information / observable
- 主体 `j` が主体 `a` に対して形成する評価・信用・見通し → `P_j(a)`
- その結果として実際に `a` に付与された信用枠・請求権・契約上の権利・取引アクセス → K / `K_a`

実証では、少なくとも以下の経路を混同しない。

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

## 15. 実証上の原則

価値場理論を実証へ落とす際は、少なくとも以下を明示する。

1. 観測スケール
2. 共通 K の対象範囲
3. 各主体の K へのアクセス・利用可能性
4. P に用いる proxy と対象範囲
5. P proxy admissibility
6. K / P の識別原則
7. A を直接観測する範囲
8. 内部 decision / observation の proxy
9. temporal typing / event ordering
10. ΔK / ΔP を結果 proxy として使う範囲
11. interval activity `H_S` を使う範囲
12. 理論変数と observable の measurement mapping
13. `S` / `S_i`
14. `τ`
15. resource coordinates / accounting boundary / transformation convention
16. `M_S` / `δ_S` または対応する state-change mapping
17. `h_S` / `H_S` を使う場合の path functional
18. `q_S` / `V_S`
19. 集約・会計・換算規則
20. 欠測・測定誤差
21. expectation operator / 推定方法
22. 3則を quantitative model へ落とす場合の projection-specific objective / constraints / horizon
23. compatibility を扱う場合の予算制約・価格・取引条件
24. market equilibrium と呼ぶ場合の choice / optimality / clearing 条件
25. P の採用次元と事前固定した検証条件
26. 他者評価を扱う場合の評価者 `j` と評価対象 `a` の区別

目的は、**state change `ΔK`、interval activity `H_S`、subjective state `P_i`、planned change `x_i`、expected realized change `E_i[ΔK]`、3つの管理合理性、および各 projection が追加する具体的 objective を混同せず、観測・会計・因果上の位置を明示すること**にある。