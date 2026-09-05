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

## 3. 使用価値 / 交換価値の二重表現

同一 resource は、主体にとって use-value side と exchange-value side の二重表現を持ちうる。

- use-value：何に、どのように利用でき、期間内でどの程度効用を実現するか
- exchange-value：他の resource / money とどの程度交換可能かを比較尺度へ写像した量

使用可能な physical stock 自体は時点観測できるが、その stock 量だけから効用量は一意に決まらない。限界効用の逓減等により、使用価値の効用量は期間中の利用・消費・充足との関係で評価される。

一方、exchange-value は比較可能な共通尺度へ写像されることで stock / position として表現できる。

使用価値を時点 stock として共通尺度化・比較評価した場合、その表現は exchange-value 側へ移ったものとして扱う。

この二重性は複式簿記を想起させるが、複式簿記はあくまで説明上のアナロジーであり、借方・貸方や会計恒等式を全主体の認知構造として仮定しない。

---

## 4. P

P は主体ごとの subjective evaluation / expectation state とする。

P はどれだけ共有されても主観状態であり、shared P は複数主体の P の共通性・整合性・分布として扱う。

契約・制度についても、法的 event / record、主体の履行・執行期待 P、実現した economic effect を分離する。

また、同一由来の resource でも加工・変換結果により利用可能性・使用価値が変わる。この実現結果が、主体の「どの A がどの利用可能状態を生むか」という期待を更新し、P_i の変化につながる。

---

## 5. ΔK と会計の分離

途中では ΔK records 自体を「一般化された仕訳」と表現したが、これは physical change と accounting representation を混同しうるため撤回した。

現行では、

```text
physical K
   ↓ A
physical / use-value flow / ΔK
   ↓ exchange / monetary measurement
P/L entries
   ↓ closing / attribution / distribution
B/S K_i
```

と分ける。

`ΔK` は physical K に実現した resource change であり、会計仕訳そのものではない。

---

## 6. P/L / B/S / surplus

P/L が表現する対象は期間中の physical / economic flow、B/S が表現する対象は actor-specific monetary capital stock / position である。

この意味で、

- use-value realization は flow-oriented / P/L-like
- exchange-value position は stock-oriented / B/S-like

と整理できる。

帳簿そのものは actor-specific であり、主体ごとに recognition / valuation / bookkeeping が異なりうる。財務報告・統計は帳簿そのものではなく、そこから外部向けに構成される別 representation である。

surplus は physical primitive ではなく、physical / use-value flow を exchange-value の共通尺度へ写像し、input / output 等を比較したときに成立する period increment / residual とする。

したがって余剰は単なる物理的増加ではない。resource の物理的存在だけでは、use-value / exchange-value / surplus は一意に決まらない。

---

## 7. 金融資産

預金、債券、売掛債権等は、それを成立させる契約・法的権利関係そのものを K とせず、会計上認識・評価された financial asset position として B/S 上の `K_i` に置く。

---

## 8. 3つの管理合理性

resource-realization / activity-flow / P-downside の3則は、経験的普遍法則ではなく VFT の constitutive rationality assumptions とする。

経験的仮説は projection 側で具体化する。

---

## 9. Marxian categories

VFT が一般化して保持するのは、use-value / labor / exchange-value / surplus / accumulation の区別である。

Marx 固有の labor-value theory や surplus-value theory は socially necessary labor time 等の追加条件を持つ projection-specific specialization とする。

---

## 10. 現行最小構造

```text
K_t, (K_i,t)_i, (P_i,t)_i
          ↓
        (A_i)_i
          ↓
physical / use-value activity / ΔK
          ↓ realized use-value
       P_i update
          ↓ exchange / monetary measurement
        P/L
          ↓ comparison / closing / attribution
surplus / deficit, (K_i,t+1)_i
```

---

© T. Nuno  
Licensed under CC BY 4.0