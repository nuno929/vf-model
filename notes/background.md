# 価値場理論 — 背景と整理の経緯

> この文書は理論コアではなく、価値場理論が現在の K / K_i / P / A 構造へ至るまでの整理経緯を保存する履歴ノートである。現行定義は README / Core / Measurement / Projections を優先する。

## 1. 初期構造

初期には P / K / X / A を置いたが、選好 X や独立した価値場変数 V は P と A に統合・廃止した。

---

## 2. K の再整理

途中では K を広い external world state、`K_i` を actor-relative access / usability view として扱う案を採った。

しかし、この定義では resource / capital と契約・制度・権利等の境界が崩れたため撤回した。

現行では、

- `K`：physical / real-resource state
- `K_i`：B/S 上の actor-indexed book-value capital position

と分ける。

`K_i` は K の subset / partition ではなく、ownership / holding / attribution と monetary valuation / bookkeeping を通じて形成される通貨的表現である。

---

## 3. P

P は主体ごとの subjective evaluation / expectation state とする。

P はどれだけ共有されても主観状態であり、shared P は複数主体の P の共通性・整合性・分布として扱う。

契約・制度についても、法的 event / record、主体の履行・執行期待 P、実現した economic effect を分離する。

---

## 4. ΔK と会計の分離

途中では ΔK records 自体を「一般化された仕訳」と表現したが、これは physical change と accounting representation を混同しうるため撤回した。

現行では、

```text
physical K
   ↓ A
physical flow / ΔK
   ↓ monetary measurement
P/L entries
   ↓ closing / attribution / distribution
B/S K_i
```

と分ける。

`ΔK` は physical K に実現した resource change であり、会計仕訳そのものではない。

---

## 5. P/L / B/S / surplus

P/L が表現する対象は期間中の physical / economic flow、B/S が表現する対象は actor-specific monetary capital stock / position である。

両者は同じ abstract monetary unit によって接続する。

surplus は physical primitive ではなく、指定 accounting boundary で P/L monetary amounts を aggregation / consolidation した period increment / residual とする。

surplus の attribution / retention / distribution は次期 B/S の `K_i` を変える。

---

## 6. 金融資産

預金、債券、売掛債権等は、それを成立させる契約・法的権利関係そのものを K とせず、会計上認識・評価された financial asset position として B/S 上の `K_i` に置く。

---

## 7. 3つの管理合理性

resource-realization / activity-flow / P-downside の3則は、経験的普遍法則ではなく VFT の constitutive rationality assumptions とする。

経験的仮説は projection 側で具体化する。

---

## 8. Marxian categories

VFT が一般化して保持するのは、use-value / labor / exchange-value / surplus / accumulation の区別である。

Marx 固有の labor-value theory や surplus-value theory は socially necessary labor time 等の追加条件を持つ projection-specific specialization とする。

---

## 9. 現行最小構造

```text
K_t, (K_i,t)_i, (P_i,t)_i
          ↓
        (A_i)_i
          ↓
physical activity / ΔK
          ↓ monetary measurement
        P/L
          ↓ aggregation / closing / attribution
surplus / deficit, (K_i,t+1)_i

realized outcomes
          ↓
       P_i update
          ↓
       next A_i
```

---

© T. Nuno  
Licensed under CC BY 4.0