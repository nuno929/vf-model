# 価値場理論 — 背景と整理の経緯

> この文書は理論コアではなく、価値場理論が現在の K / K_i / P / A / field 構造へ至るまでの整理経緯を保存する履歴ノートである。現行定義は README / Core / Measurement / Projections を優先する。

## 1. 初期構造

初期には P / K / X / A や独立した価値場変数 V を置いたが、選好 X や独立 scalar V は廃止した。

現行の field は独立変数ではなく、K / K_i / P_i / relations / constraints が A を条件づけ、誘発し、再生産する配置構造を指す。

---

## 2. K / K_i の再整理

途中では K を広い external world state、K_i を actor-relative access / usability view として扱う案を採った。

しかし、この定義では resource / capital と契約・制度・権利等の境界が崩れたため撤回した。

現行では、

- `K`：physical / real-resource state
- `K_i`：actor-specific exchange-value / capital representation

と分ける。

`K_i` は K の subset / partition ではない。

一時期 `K_i ≡ B/S` に近い表現を採ったが、B/S は assets / liabilities / equity 等を持つ制度的 accounting representation であり型が異なるため撤回した。formal accounting projection では K_i を B/S / ledger 上の monetary positions として形式化できるが、両者を同一視しない。

---

## 3. use-value / exchange-value

同一 resource は use-value / exchange-value の二重表現を持ちうる。

VFT における use-value quantity は、resource stock 自体や technical service potential ではなく、期間内の利用・消費・充足を通じて実現する効用量とする。

physical stock / capability は K として時点観測できる一方、限界効用逓減等により realized utility は stock 量だけから一意に決まらない。

exchange-value は resource 間を比較可能な尺度へ写像する representation であり、point-in-time position にも interval transaction valuation にも現れうる。

したがって「use-value = flow / exchange-value = stock」という完全な一対一対応は撤回した。ただし use-value quantity は期間利用から計量し、異質な stock を共通交換尺度で比較した評価は exchange-value representation に属するという区別は維持する。

複式簿記は use / exchange の二重表現を説明するアナロジーに留める。

---

## 4. P

P は structured subjective state とする。

belief / expectation、preference / valuation、trust / reputation、norm recognition 等を内部 component として持ちうるが、Core primitive は分割しない。

`E_i[ΔK | a,I_i]` は P_i の belief / expectation component から導出される action-contingent forecast と整理した。

また、A による加工・変換結果が resource の利用可能性・実現 use-value を変え、その結果が P_i を更新する経路を明示した。

---

## 5. A / ΔK

途中では ΔK records を gross activity / generalized bookkeeping のように使ったが、activity と endpoint state change が混同されるため撤回した。

現行では、

```text
A history = interval gross activity / events
ΔK_[t0,t1] = K_t1 - K_t0
```

と分ける。

独立した gross-flow primitive は Core に置かない。

ΔK は accounting entry でもない。

---

## 6. accounting の位置づけ

一時期、physical flow → P/L → B/S を Core の主要因果経路として表現したが、P/L には financial / contractual / valuation-only events も入りうるため、literal accounting model としては狭すぎた。

現行では P/L・B/S・複式簿記を **formal accounting projection** とする。

```text
physical/resource events ─────┐
contract/financial events ────┼→ recognition / valuation → accounting entries
valuation-only events ────────┘
```

帳簿そのものは actor-specific であり、財務報告・連結・統計は別 representation とする。

---

## 7. surplus

surplus は physical primitive ではない。

physical / use-value activity の input / output 等を exchange-value の比較可能尺度へ写像し、その差分を recognition / accounting boundary 内で比較・集計したときに成立する。

したがって余剰は「物理的に増えた量」そのものではない。

同じ物理対象でも、利用方法・交換可能性を認識できる主体とできない主体では value representation が異なりうる。機械が利用法を知らない主体には単なる箱・物体にしか見えないという例は、この非物理性を示す。

---

## 8. institutional / legal state

契約・制度・法的権利関係それ自体は physical K に置かない。

一方で、それらの客観状態を必要とする projection があることは認め、`C_t` 等の institutional / legal state を projection-local に追加できるとした。

Core の普遍 primitive にはしない。

---

## 9. field / business

「価値場」の field は、A を誘発する配置構造として再定義した。

事業体を profit maximization から定義すると、営利企業の既存事業運営は説明しやすい一方、NPO、公共事業、国家・自治体の事業、そして起業・新規事業 formation が例外化されやすい。

そこで事業体を、**一定の目的・機能に向けた A を継続的に誘発・再生産する局所 field structure** として扱う。

```text
起業           = 新しい action-generating field の形成
新規事業開発   = 既存 field から新しい field を形成・分岐
既存事業運営   = 成立済み field の維持・再生産・改善
```

profit / surplus は business existence の定義条件ではなく、exchange-value 側の重要 metric とする。

---

## 10. 3つの管理合理性

resource-realization / activity-flow / P-downside の3則は constitutive rationality assumptions とする。

activity-flow は既存 activity の継続だけでなく、必要に応じた field formation / renewal を含みうる。

profit / utility は3則の特殊化ではなく、具体的 decision problem の metric / objective / proxy とする。

---

## 11. Marxian categories

VFT が一般化して保持するのは、use-value / labor / exchange-value / surplus / accumulation の区別である。

Marx 固有の labor-value theory / surplus-value theory は socially necessary labor time 等の追加条件を持つ projection-specific specialization とする。

---

## 12. 現行最小構造

```text
field_t
= configuration of K_t, (K_i,t)_i, (P_i,t)_i, relations / constraints
          ↓
        (A_i)_i
          ↓
resource activity / transformation / exchange / learning
          ↓
ΔK, realized use-value, exchange-value changes
          ↓
P_i update / K_i update / field reproduction or formation
```

---

© T. Nuno  
Licensed under CC BY 4.0