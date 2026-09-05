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

期間所得そのものは通常 flow であり、K の stock/state と同一視しない。期間中に実現した所得受取は K の transition / `ΔK` 側で扱い、受取可能な請求権や earning capacity 等を K 側へ置く。

金融資源は、名目上の評価額そのものではなく、実際に行動可能性を増やす利用可能な資源・権利として K / `K_i` へ操作化する。

---

## 3. P の計測

`P_i` は主体 `i` の将来の見通し・評価・選好・信用・信念等を保持する多次元の subjective evaluation / expectation state である。

他主体 `a` について主体 `j` が保持する評価・信用・見通し等を区別する必要がある場合は、`P_j(a)` と書く。これは `a` 自身の P ではなく、評価者 `j` の主観状態である。

個々の `P_i` の全構造を直接観測できるとは仮定しない。

候補 proxy には、調査された期待・信念・選好・評価、発話、契約に対する信用、評判・ブランド評価、価格、金利、スプレッド、信用条件等がある。

価格・金利・信用条件等は P そのものではなく、P と K / A / 制度・市場過程等の相互作用から生じる observable として扱う。

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

## 5. A の観測可能性

A は各主体側で生じる actor-side process / event を表す。

外部に実現した action event は直接観測できる場合がある。取引、移動、発話、投資、労働、契約、政策変更等が該当する。

一方、内部の意思決定、観測、情報受容、解釈等は直接観測できない場合があり、proxy を要する。

観測・情報受容・解釈を A に含める場合も、それらが必ず能動的行為であることを意味しない。P 更新を記述する actor-side process として必要な範囲で含める。

---

## 6. ΔK / ΔP の観測

観測・会計仕様 `S` と時間区間 `τ=[t0,t1]` を明示した実資源変化を `ΔK(S, τ)` とする。

`S` は少なくとも以下を含む。

1. 対象資源・主体
2. resource coordinates
3. accounting boundary
4. transformation convention

例えば一つの消費行為が、在庫減少、現金移転、身体への摂取、別形態の資源への変換等を同時に生む場合、どの座標と会計境界で `ΔK` を測るかを `S` で固定する。

一般には、観測仕様に対応する状態表現と change operator を

```text
Y_S(t) = M_S(K_t)
ΔK(S, τ) = δ_S(Y_S(t0), Y_S(t1)) ∈ D_S
```

と考える。`M_S` と `δ_S` は measurement / projection 側で定める specification-local な写像・演算であり、Core の新しい原始変数ではない。

`ΔK` は必ずしも算術差分を意味しない。加法的な quantitative projection が適用できる場合にのみ、

```text
δ_S(y0, y1) = y1 - y0
```

と置ける。

`ΔP_i` も一般には算術差ではなく、主体 `i` の P に実現した change descriptor / state transition を表す。非加法的な場合は少なくとも

```text
P_i,t0 -> P_i,t1
```

として扱い、数量化が必要な場合だけ measurement mapping を追加する。

`ΔK` はミクロ用・マクロ用に数学的な同一型を要求しない。`S` に応じて `D_S`、座標、単位、集約規則等は異なりうるが、**S-indexed change schema** は共通に保つ。

---

## 7. P の変化と観測

A は P を変化させる主要な actor-side process である。

政策変更、価格提示、契約条件変更、情報伝達、観測・情報受容・解釈等による P の変化も、必要に応じて A を介する経路として記述できる。

記憶減衰等の微小・非主体的な P の変化の存在自体は否定しない。ただし、それが観測可能な A や P proxy に意味のある差を生じない限り、Core の主要変化経路として明示的に操作化しない。

---

## 8. E[ΔK] の位置づけ

主体 `i` が対象 `S`・区間 `τ` について形成する期待実資源変化を `E_i[ΔK(S, τ)]` とする。

`E[...]` は expectation operator として、対象となる `ΔK` が quantitative projection 上で表現され、期待値が定義可能な場合に用いる。

Core は `E_i` に対応する確率測度・情報集合・期待形成式を普遍的に固定しない。具体的な expectation operator の定義は対象 projection / measurement model で与える。

`E[...]` は主体が形成する見込み値・期待値を表し、主体の望みそのものではない。選好・望ましさ・評価は P に保持され、期待形成や A に影響しうる。

---

## 9. 集約

VFT は、複数主体の `K_i` / `P_i` / `A_i` を自動的に一主体・一変数へ集約しない。

集約する場合は少なくとも以下を明示する。

1. 共通 K の対象範囲
2. 対象主体集合
3. 各主体の K へのアクセス・利用可能性
4. P に用いる proxy
5. A の観測単位とイベント順序
6. `τ`
7. `S` の resource coordinates / accounting boundary / transformation convention
8. `M_S` / `δ_S` または対応する change mapping
9. ΔK / ΔP の集約規則
10. 共有資源・重複アクセスの扱い
11. 情報損失

ミクロからマクロへの接続でも、新しい `ΔK_macro` の型を置く必要はなく、異なる `S` / `τ` / 集約規則を与えた同じ S-indexed change schema として扱う。

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

## 11. 主体間整合・market equilibrium・会計整合・定常状態

以下は別概念として扱う。

- **主体間整合 / compatibility**：各主体の予算・資源制約を満たした `x_i` が、価格・取引条件等のもとで相互に実行可能・両立可能であること
- **market equilibrium**：上記 compatibility に加え、射影先の理論が choice / optimality / best response / market-clearing 等の条件を与えた状態
- **会計整合**：同じ資源変化を同一会計境界・換算規則で記録した結果が収支上整合すること
- **定常状態**：対象 scope の K が区間を通じて実質的に増減しない等、別途定める状態条件

したがって、VFT 単独の compatibility を market equilibrium と同一視しない。

---

## 12. P の実証上の制約

P が観察後の residual state にならないよう、各 projection / empirical model では少なくとも以下を観測・推定前に固定する。

1. 採用する P の次元
2. 各次元の observable / proxy
3. P と A / E[ΔK] の mapping
4. 検証対象となる事前予測または識別条件
5. 代替説明と比較する基準

観察された A の差を説明するために事後的に任意の P 次元を追加することは避ける。

---

## 13. 評価・信用経済を扱う場合

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

この経路を使うことで、評価・信用側の変化が実資源アクセスや行動へどう波及するかを検証可能な projection として設計できる。

---

## 14. 実証上の原則

価値場理論を実証へ落とす際は、少なくとも以下を明示する。

1. 観測スケール
2. 共通 K の対象範囲
3. 各主体の K へのアクセス・利用可能性
4. P に用いる proxy と対象範囲
5. K / P の識別原則
6. A を直接観測する範囲
7. 内部 decision / observation の proxy
8. ΔK / ΔP を結果 proxy として使う範囲
9. 理論変数と observable の measurement mapping
10. `S` / `S_i`
11. `τ`
12. resource coordinates / accounting boundary / transformation convention
13. `M_S` / `δ_S` または対応する change mapping
14. 集約・会計・換算規則
15. 欠測・測定誤差
16. `E[ΔK]` を適用する quantitative projection
17. expectation operator / 推定方法
18. compatibility を扱う場合の予算制約・価格・取引条件
19. market equilibrium と呼ぶ場合の choice / optimality / clearing 条件
20. P の採用次元と事前固定した検証条件
21. 他者評価を扱う場合の評価者 `j` と評価対象 `a` の区別

目的は、**共通の実資源世界 K と、主体ごとのアクセス状態 K_i・主観的評価／期待状態 P_i・期待区間変化 E_i[ΔK(S, τ)] を混同せず、S-indexed change schema をミクロからマクロまで観測・会計仕様に応じて接続し、A / ΔP / proxy / compatibility / equilibrium と使い分けること**にある。