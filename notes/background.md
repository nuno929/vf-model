# 価値場理論 — 背景と整理の経緯

> この文書は理論コアではなく、価値場理論が現在の K / P / A 構造へ至るまでの整理経緯を保存する履歴ノートである。以下に登場する旧変数・旧定義は現行 Core では用いない。現行定義は README / Core / Measurement / Projections を優先する。

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

その後、中間変数の重複を減らし、K / P / A を中心に整理した。

---

## 2. K：自由度から資源・資本へ

初期の K は自由度・選択可能域に近い概念だった。

その後、行為可能性を説明する際に、自由度そのものより、実際に存在する資源・資本を基礎に置く方が経済理論として素直だと整理した。

現行 Core では、

- `K`：共通の resource / capital state
- `K_i`：そのうち主体 `i` に所有・保有・帰属する resource / capital

とする。

途中では `K_i` を actor-relative access / usability view として広く定義し、権利、資格、契約、制度状態等まで K に含める案を採った。しかし、この定義では K が resource / capital を超えて「外部 world state」全体へ膨張し、K / P の境界が崩れた。

現行ではこの拡張を撤回し、K を resource / capital に戻している。

また、`K_i` は主体が「利用可能だと認識している K」ではない。所有・保有・帰属する資源・資本を表し、その認識は P 側に属する。

K_i の真値を主体本人や観測者が完全に把握しているとも仮定しない。未把握資産・債務、評価差、帰属の複雑さは計測・会計上の問題として扱う。

---

## 3. P：背景構造から主観的評価・期待 state へ

P は最も意味が変化した概念である。

初期には制度・文化・環境等をまとめた背景構造だったが、議論を進める中で、信用、評価、選好、信念、将来見通し、規範認識等が、同じ資源条件でも行動を変える側として整理された。

現行では `P_i` を、**主体 i の subjective evaluation / expectation state** とする。

P は多数主体に共有されても主観状態である。shared P は複数主体の P の共通性・整合性・分布として扱い、客観的な社会価値の真値とはみなさない。

契約・制度についても、法的効力や外部 record の存在と、主体が履行・執行・継続をどう期待するかを区別する。経済行動を条件づける共有された契約・制度認識は P 側で扱う。

---

## 4. X：独立した選好変数から P への統合

初期モデルでは選好方向 X を独立変数として置いていた。

しかし、選好は P の evaluative / preference-like component として扱えるため、X を独立 primitive として置く必要性は薄れた。

現行 Core では X を置かない。

---

## 5. V：価値場変数の廃止

途中では K / P / X から価値場状態 V を生成する案も検討した。

しかし V を独立 state とすると中間変数が増えるため、現行 Core では V を置かない。

価値場は、**K / K_i と P_i の配置・関係が A_i を条件づける構造**として扱う。

---

## 6. ΔK：state descriptor から実現 resource change へ

ΔK をどこまで一般化するかについても整理が進んだ。

途中では、観測仕様 `S` に対する generic state-change descriptor として

```text
Y_S(t) = M_S(K_t)
ΔK(S, τ) = δ_S(Y_S(t0), Y_S(t1))
```

のように広く定義し、gross interval activity を `H_S` として分離する案を採った。

その後、経済理論として必要以上に形式化していることが分かった。

現行では、`ΔK` を **K の利用・移転・変換・消費・生成等の結果として実現した resource / capital change** とする。

一つの A が複数の資源変化を生む場合は、複数の ΔK record を保持する。

```text
A
├─ ΔK_1
├─ ΔK_2
└─ ...
```

区間活動量を表す独立変数 `H` は置かない。gross activity が必要なら A と ΔK records の event history から再構成する。

この意味で、複数の ΔK record は「一般化された仕訳」として読むことができる。

---

## 7. surplus：物理量ではなく会計的派生量

余剰を物理世界の primitive として扱う必要はない。

実現した ΔK records を valuation / bookkeeping rule で共通尺度へ写像し、同じ accounting boundary で差し引いた最終差分が surplus / deficit になる。

```text
realized ΔK records
        ↓ valuation / bookkeeping
accounting entries
        ↓ aggregation
surplus / deficit
```

したがって surplus は、物理的に直接観測される独立量ではなく、**resource / capital change を会計的に評価・集約した residual** として扱う。

貨幣についても、保有資産としての money は K に入りうる一方、unit of account / valuation scale としての money は accounting representation である。両者を役割で区別する。

---

## 8. E[ΔK]：期待と実現の分離

主体は K を利用する前に、その結果として生じる ΔK について期待を持ちうる。

```text
E_i[ΔK]
```

は expected realized resource / capital change であり、desire / preference / plan とは区別する。

望ましさ・選好は P、planned change は必要な economic projection で `x_i`、実現結果は ΔK として分離する。

---

## 9. 経済学への射影整理

VFT は独自の均衡則を作るのではなく、既存経済学へ K / K_i / P_i / A_i / ΔK / E_i[ΔK] を接続する。

### マルクス経済学の骨子

VFT が取り込みたいのは、特定の政治的・規範的結論ではなく、マルクス経済学が区別した、

- 使用価値
- 労働
- 交換価値
- 余剰
- 蓄積・分配

という経済現象の骨格である。

現行の方向では、

- 使用価値：K が特定の A / transformation を可能にする機能
- 労働価値：labor activity / labor time を価値記述の尺度として使う射影
- 交換価値・価格：market / accounting valuation
- 余剰：ΔK records の accounting residual

として分離する。

「労働だけが価値の唯一の源泉である」「余剰が存在すれば直ちに搾取である」といった規範・形而上学的主張は Core に置かない。

---

## 10. ミクロ／マクロ接続

現行 VFT ではミクロとマクロを別々の K として置かない。

```text
micro:
(K_i, P_i) -> A_i -> ΔK records

              ↓ same common K

macro:
ownership distribution
production / consumption
surplus distribution
capital accumulation
shared P
```

個別主体の A_i が同じ K の構成・所有分布を変え、マクロではその同じ K と ΔK records を異なる accounting / aggregation boundary から観測する。

surplus の帰属・分配が次期 K_i を変えることで、主体の意思決定と資本蓄積・所有分布を同じ系列で接続できる。

---

## 11. 3つの管理合理性

現行の3則は、

1. resource-realization
2. activity-flow
3. P-downside

である。

3則は actor type ではなく意思決定合理性の公理系として扱う。同一 actor が3則を同時に考慮し、文脈・制度・役割・時間 horizon に応じて比重・優先順位が変わる。

P-downside は、客観的 P の最大化ではなく、対象主体群の shared P / trust / expectation 等の大幅な毀損により将来 A が成立しなくなることを防ぐ合理性として扱う。

---

## 12. 現行 Core の最小構造

```text
common K_t
  └─ ownership / attribution -> (K_i,t)_i

(K_i,t)_i, (P_i,t)_i
        ↓ conditions
      (A_i,τ)_i
        ↓
realized ΔK records, ΔP_i
        ↓
valuation / bookkeeping if needed
        ↓
surplus / deficit / macro aggregates
```

独立した X / V / H、普遍的 deterministic choice function、P 更新関数、期待形成関数、独自の均衡式、普遍的 surplus 変換式は Core に置かない。

---

© T. Nuno  
Licensed under CC BY 4.0