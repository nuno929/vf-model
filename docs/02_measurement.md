# 価値場理論 — 計測

## 1. 目的

本書は VFT Core を実証・観測・会計へ落とす際の境界を整理する。

計測上は、physical K、actor-specific K_i、structured subjective state P_i、A の event history、endpoint change ΔK、use-value realization、exchange-value representation を区別する。

---

## 2. K の観測

K は physical / real-resource state である。

候補 observable には原材料量、製品量、設備、稼働、労働時間、エネルギー使用、土地、時間、技能・人的能力等がある。

K の完全観測は前提とせず、resource coordinates と観測単位は projection ごとに定める。

---

## 3. K_i の計測

`K_i` は actor-specific exchange-value / capital stock representation である。

計測には projection に応じて、

1. ownership / holding / attribution
2. recognition rule
3. valuation rule
4. unit of account / comparison scale

等が必要になる。

`K_i` は K の subset / partition ではない。

### accounting implementation

企業会計等では K_i を ledger / B/S 上の monetary positions として形式化できるが、`K_i ≡ B/S` とはしない。

正式な B/S projection では assets / liabilities / equity 等の account types と accounting identity を representation の定義条件として明示する。

帳簿は actor-specific であり、財務報告・連結・統計は別の external representation とする。

---

## 4. use-value の計測

VFT における use-value quantity は、resource stock 自体ではなく、期間内の利用・消費・充足を通じて実現した効用量である。

physical stock / capability 自体は K として時点観測できるが、限界効用逓減等により stock 量だけから実現効用量は一意に決まらない。

したがって use-value quantity の計測では少なくとも、

- interval
- actual use / consumption
- utility proxy
- 必要に応じて substitute / complement / use category

を指定する。

---

## 5. exchange-value の計測

exchange-value は resource を他の resource / money との比較関係から共通尺度へ写像した representation である。

exchange-value は point-in-time position にも interval event valuation にも現れうる。

```text
point-in-time valuation -> capital / asset position
interval valuation      -> transaction / revenue / expense etc.
```

したがって exchange-value を stock 専用とはしない。

異質な resource stock を共通交換尺度で比較・集計する評価は exchange-value representation として扱う。

複式簿記は use / exchange の二重表現を説明するアナロジーとしてのみ用い、普遍的認知構造とはしない。

---

## 6. P の計測

`P_i` は structured subjective state であり、belief / expectation、preference / valuation、trust / reputation、norm recognition 等を含みうる。

候補 proxy には期待調査、選好・評価調査、発話、信用・信頼指標、制度・契約への履行期待、将来見通し等がある。

shared P は actor set 上の共通性・整合性・分布として推定する。

`E_i[ΔK | a, I_i]` は P_i の belief / expectation component と情報集合から導出される forecast とする。

加工・変換後の実現 use-value が P_i 更新を引き起こす経路を観測する場合、期待時点・実現時点・更新時点を区別する。

---

## 7. A と ΔK

A は生産、消費、交換、投資、労働、移転、契約、政策、探索、学習等の actor-side action / process / event である。

区間中の gross activity は A の event history として記録する。

`ΔK` は endpoint state change とする。

```text
ΔK_[t0,t1] = K_t1 - K_t0
```

したがって gross activity と ΔK は別 observable である。

```text
+100 inflow
-100 outflow
=> gross activity exists
=> endpoint ΔK may be 0
```

`ΔK` は accounting entry ではない。

---

## 8. surplus の計測

surplus は physical primitive ではなく、exchange-value の比較可能尺度上で成立する差分 / residual である。

```text
physical / use-value activity
   ↓ valuation / recognition
comparable exchange values
   ↓ comparison / accounting
surplus / deficit
```

少なくとも、

1. actor set / scope
2. comparison / accounting boundary
3. unit of account
4. recognition timing
5. valuation rule
6. internal transaction treatment
7. attribution / distribution rule

を明示する。

---

## 9. accounting projection

formal accounting を用いる場合、physical flow だけでなく、contract / financial events、valuation-only events 等も recognition / valuation を経て accounting entries を形成しうる。

```text
physical/resource events ─────┐
contract/financial events ────┼→ recognition / valuation → accounting entries
valuation-only events ────────┘
```

P/L は recognized interval events、B/S は recognized point-in-time positions の monetary / exchange-value representation とする。

accounting identity は当該 projection の representation rule として検証する。

---

## 10. field / business の計測

field は、K / K_i / P_i / relations / constraints が A をどの程度誘発・再生産するかという配置構造として扱う。

直接1変数へ縮約することは Core では要求しない。

business / organization projection では、例えば、

- recurring action set
- activity continuity
- resource replenishment
- participant retention
- customer / beneficiary interaction
- learning / exploration activity
- field formation / dissolution

等を観測できる。

起業は新しい action-generating field の形成、新規事業開発は既存 field から新しい field を形成・分岐させる過程として測る。

profit はその一指標であり、business existence の定義変数とはしない。

---

## 11. 3つの管理合理性の計測

3則は constitutive rationality assumptions とする。

経験的には、projection-specific な objective / priority / weight / constraint / threshold / horizon が action / outcome をどの程度説明するかを検証する。

---

## 12. Marxian projection の計測

- use-value：期間内の realized utility / use
- labor measure：labor activity / labor time
- Marxian labor-value：socially necessary labor time 等の追加条件を伴う specialization
- exchange-value / price：resource 間の comparison / market / monetary valuation
- generic surplus：exchange-value 上の差分 / residual
- Marxian surplus value：Marx 固有条件を含む specialization

---

## 13. ミクロ／マクロ

ミクロとマクロは、同じ physical K と、actor-specific K_i / P_i / A histories を異なる scope で観測し、必要に応じて external reporting / statistical transformation で接続する。

主体ごとの帳簿自体が共通化されることは仮定しない。

---

## 14. 実証上の原則

少なくとも以下を明示する。

1. K の resource coordinates
2. A の event unit / ordering
3. ΔK の endpoint interval
4. use-value の utility proxy / interval
5. exchange-value / valuation rule
6. K_i の representation rule
7. P / shared P の proxy
8. E[ΔK] の推定法
9. surplus の comparison / accounting boundary
10. accounting projection を用いる場合の recognition / identity rule
11. field / business continuity の proxy
12. micro / macro reporting / aggregation rule
13. 欠測・測定誤差・情報損失

---

© T. Nuno  
Licensed under CC BY 4.0