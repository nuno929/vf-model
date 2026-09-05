# 価値場理論 — 既存概念・応用への射影ノート

> この文書は Core 定義ではなく、既存概念・応用領域への projection candidate を保存する。

## 1. 基本構造

VFT の経済射影では、

- `K`：physical / real-resource state
- `K_i`：actor-specific exchange-value / capital representation
- `P_i`：structured subjective state
- `A_i`：actor-side action / process / event
- `ΔK`：endpoint resource-state change

を区別する。

field は K / K_i / P_i と関係・制約がつくる action-generating configuration として扱う。

---

## 2. 使用価値 / 交換価値

同一 resource は use-value side と exchange-value side の二重表現を持ちうる。

### use-value

VFT の use-value quantity は resource stock 自体ではなく、期間内の利用・消費・充足を通じて実現した効用量とする。

physical stock / capability は K として時点観測できるが、限界効用逓減等により stock 量だけから realized utility は一意に決まらない。

### exchange-value

resource を他の resource / money との比較関係から共通尺度へ写像した representation とする。

exchange-value は point-in-time position にも interval transaction valuation にも現れうるため、stock 専用とはしない。

異質な resource stock を共通交換尺度で比較・集計した評価は exchange-value representation に属する。

### accounting analogy

use / exchange の二重表現は複式簿記を想起させるが、あくまで説明上のアナロジーである。

---

## 3. K_i / accounting projection

`K_i` は K の subset / partition ではなく、ownership / attribution / valuation 等を経た actor-specific exchange-value / capital representation である。

企業会計 projection では K_i を ledger / B/S 上の monetary positions として形式化できるが、`K_i ≡ B/S` とはしない。

formal accounting では、

```text
physical/resource events ─────┐
contract/financial events ────┼→ recognition / valuation → accounting entries
valuation-only events ────────┘
                                      ↓
                                   P/L / B/S
```

のように複数種の economic events を扱いうる。

帳簿そのものは actor-specific であり、財務報告・連結・統計は別の external representation とする。

---

## 4. 契約・制度・金融資産

契約・制度・法的権利関係それ自体は physical K としない。

一方、預金、債券、売掛債権等は recognized exchange-value / financial position として K_i / accounting projection 上に表現できる。

主体が契約・制度の履行・執行・継続をどう期待するかは P に属する。

客観的な institutional / legal state が必要な projection では `C_t` 等を projection-local に追加してよい。

---

## 5. P / forecast

P_i は belief / expectation、preference / valuation、trust / reputation、norm recognition 等を含む structured subjective state とする。

`E_i[ΔK | a, I_i]` は P_i の belief / expectation component と情報集合から導出される action-contingent forecast とする。

加工・変換後の changed use possibilities / realized use-value は P_i 更新を引き起こしうる。

---

## 6. A / ΔK

A は生産、消費、交換、投資、労働、移転、契約、政策、探索、学習等の event history を持つ。

`ΔK` は endpoint state change とする。

```text
ΔK_[t0,t1] = K_t1 - K_t0
```

したがって gross activity と ΔK は別概念であり、gross activity は A history から読む。

---

## 7. surplus / accumulation

surplus は physical primitive ではない。

physical / use-value activity の input / output 等を exchange-value の比較可能尺度へ写像し、その差分を recognition / accounting boundary の下で集計したときに成立する。

```text
physical / use-value activity
   ↓ exchange-value valuation
comparable values
   ↓ comparison / accounting
surplus / deficit
```

surplus の attribution / retention / distribution は次期 K_i を変える。

---

## 8. field / business projection

field は action-generating configuration とする。

business entity は **一定の目的・機能に向けた A を継続的に誘発・再生産する局所 field structure** として記述できる。

```text
起業           = 新しい field formation
新規事業開発   = 既存 field から新しい field を形成・分岐
既存事業運営   = 成立済み field の維持・再生産・改善
```

この定義では営利企業、NPO、協同組合、公共事業、国家・自治体の事業等を同じ型で扱える。

profit / surplus は business existence の定義条件ではなく、exchange-value 側の重要 metric の一つである。

---

## 9. 3つの管理合理性公理

1. resource-realization
2. activity-flow
3. P-downside

3則は constitutive rationality assumptions とする。

activity-flow は既存 activity の継続だけでなく、必要に応じた field formation / renewal を含みうる。

profit / utility は3則の特殊化ではなく、projection-specific metric / objective / proxy とする。

---

## 10. plan / forecast / equilibrium

```text
x_i              = planned / chosen resource change
E_i[ΔK | a,I_i]  = expected endpoint resource-state change
```

compatibility / market equilibrium / accounting consistency / steady state は別概念とする。

---

## 11. Marxian categories

VFT は use-value / labor / exchange-value / surplus / accumulation を一般化構造上で保持する。

- use-value：期間内に realized した utility / use
- labor measure：labor activity / labor time
- Marxian labor-value：socially necessary labor time 等の追加条件を持つ specialization
- exchange-value / price：resource 間の comparison / market / monetary valuation
- generic surplus：exchange-value 上の差分 / residual
- Marxian surplus value：Marx 固有条件を持つ specialization
- accumulation：surplus 等の帰属・留保・分配による K_i の変化

---

## 12. ミクロ／マクロ

```text
micro
field_i -> A_i -> resource activity
              -> ΔK
              -> realized use-value -> P_i update
              -> exchange valuation -> K_i update

                     ↓ external reporting / aggregation where needed

macro
physical production / consumption
exchange-value distribution / surplus
capital accumulation
shared P
field formation / dissolution
```

主体ごとの帳簿自体が共通化されることは仮定しない。

---

## 13. 射影時に明示するもの

1. K の resource coordinates
2. actor set
3. A の event unit / ordering
4. ΔK の endpoint interval
5. use-value の utility proxy / interval
6. exchange-value / valuation rule
7. K_i の representation rule
8. P / shared P の proxy
9. E[ΔK] の推定法
10. institutional state が必要な場合の追加定義
11. accounting projection の recognition / identity rule
12. surplus の comparison / attribution / distribution
13. field / business continuity の proxy
14. Marxian specialization の追加条件
15. micro / macro reporting / aggregation rule

---

© T. Nuno  
Licensed under CC BY 4.0