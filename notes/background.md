# 価値場理論 — 背景と整理の経緯

> この文書は理論コアではなく、価値場理論が現在の K / K_i / P / A / field 構造へ至るまでの整理経緯を保存する履歴ノートである。現行定義は README / Core / Measurement / Projections を優先する。

## 1. 初期構造

初期には P / K / X / A や独立した価値場変数 V を置いたが、選好 X や独立 scalar V は廃止した。

現行の field は独立変数ではなく、K / K_i / P_i と projection-specified relations / constraints から導かれる action-generating configuration を指す。

当初は、

```text
Γ_i(F_t) := feasible / inducible action correspondence
```

と一つにまとめたが、physical / institutional feasibility と behavioral inducibility が別概念であるため、

```text
Γ_i^feas(F_t) := feasible action set
Γ_i^ind(F_t)  := inducible / behaviorally available action set
Γ_i^ind(F_t) ⊆ Γ_i^feas(F_t)
```

へ分離した。

---

## 2. K / K_i の再整理

途中では K を広い external world state、K_i を actor-relative access / usability view として扱う案を採ったが、resource / capital と契約・制度・権利等の境界が崩れるため撤回した。

現行では、

- `K`：physical / real-resource state
- `K_i`：actor-specific exchange-value / capital representation

と分ける。

`K_i` は K の subset / partition ではない。

一時期 `K_i ≡ B/S` に近い表現を採ったが、B/S は制度的 accounting representation であり型が異なるため撤回した。formal accounting projection では K_i を B/S / ledger 上の monetary positions として形式化できるが、両者を同一視しない。

P_i の valuation は subjective appraisal、K_i の valuation は specified recognition / comparison / unit-of-account rules の下で作る exchange-value representation として区別する。

---

## 3. use-value / exchange-value

同一 resource について、physical capability / realized use experience / exchange-value representation を区別する。

VFT における use-value quantity は、resource stock 自体や technical service potential ではなく、**主体が interval 内に resource を実際に利用・消費し、その経験に帰属される形で ex post に realized した主観的効用量**とする。

physical stock / capability は K として時点観測できる一方、それは use-value quantity そのものではない。

同じ主体・同じ resource・同じ利用量でも、充足状態、順序、文脈、他の経験等によって realized outcome は変わりうるため、一般的な再現性や interval 間の加法性を仮定しない。

use-value quantity は interval-indexed outcome として扱う。瞬間的な use-value rate が必要な projection では interval quantity の極限・微分的表現として導入できるが、point-in-time stock valuation とは扱わない。

この時間形式を P/L-like と呼ぶが、会計上の P/L entry と同一視しない。

以前の「利用可能性と交換可能性を複式に保持する」という表現は、利用可能性が K capability 側であり realized use-value と異なるため撤回した。

---

## 4. P / forecast

P は structured subjective state とする。

一時期 `E_i[ΔK | a,I_i]`、その後 `ΔK̂_i(a;I_i)` を Core forecast としたが、decision model が K_i、realized use、P viability、activity continuity 等も評価するため、physical ΔK の forecast だけでは型が狭いと判断した。

現行では、

```text
Y_i^proj(τ) := projection-selected outcome bundle
Ŷ_i(a;I_i)  := forecast of Y_i^proj under candidate action a
```

とする。

`ΔK̂_i(a;I_i)` は必要な projection で `Ŷ_i` の physical-resource component として使える。

---

## 5. A / shared event / ΔK

途中では ΔK records を gross activity / generalized bookkeeping のように使ったが、activity と endpoint state difference が混同されるため撤回した。

また actor-side A records のみでは、交換・移転・契約等の multi-actor event を macro aggregation した際に同一 event の二重計上が起こりうる。

そのため、対応する actor records に shared `event_id` と participant / role relation を持たせる。

```text
event_id(A_i) = event_id(A_j) = e
participants(e) = {i,j,...}
```

必要な場合、

```text
E_τ^shared := deduplicate( ⋃_i A_i,τ , by = event_id )
```

を derived event view とする。独立した universal event-state primitive は追加しない。

`ΔK` は、

```text
ΔK_τ := δ_K(K_t0,K_t1)
```

という projection-defined endpoint difference とする。additive vector projection では `K_t1-K_t0` を特殊形として使える。

A は actor-side に限定し、自然劣化・災害・偶発故障等は必要な projection で `Ω_τ` 等へ分ける。

---

## 6. accounting の位置づけ

一時期、physical flow → P/L → B/S を Core の主要因果経路として表現したが、P/L には financial / contractual / valuation-only events も入りうるため撤回した。

現行では P/L・B/S・複式簿記を **formal accounting projection** とする。

帳簿そのものは actor-specific であり、財務報告・連結・統計は別 representation とする。

---

## 7. exchange-value residual / surplus

surplus は physical primitive ではない。

当初は physical / use-value activity の input / output を exchange-value へ写像する経路を中心に説明したが、accounting projection では contract / financial / valuation-only events も存在する。

そこで、より中立的な Core-level 型として **exchange-value residual** を置けると整理した。

```text
specified economic changes
        ↓ exchange-value representation
comparable values
        ↓ comparison under specified boundary
exchange-value residual
```

surplus / deficit、production surplus、profit、income、valuation gain 等は projection-specific な解釈とする。

---

## 8. institutional / legal state

契約・制度・法的権利関係それ自体は physical K に置かない。

それらの客観状態を必要とする projection では institutional / legal state を projection-local に追加できる。Core の普遍 primitive にはしない。

---

## 9. field / business

「価値場」の field は、A を誘発する配置構造として再定義した。

事業体を profit maximization から定義すると、NPO、公共事業、国家・自治体の事業、起業・新規事業 formation が例外化されやすい。

そこで事業体を、**一定の目的・機能に向けた A を継続的に誘発・再生産する局所 field structure** として扱う。

```text
起業           = business-oriented field formation の一類型
新規事業開発   = 既存 field から business-oriented field を形成・分岐
既存事業運営   = 成立済み business field の維持・再生産・改善
```

profit / surplus は business existence の定義条件ではない。

---

## 10. 3つの管理合理性

resource-realization / activity-flow / P-downside の3則は constitutive rationality assumptions とする。

use-value を realized experience として明示したことで、resource-realization は resource / capital outcome だけでなく desired realized-use outcome も含むように整理した。

P-downside は P 全体の universal ordering を意味せず、projection-specific な P component と threshold / loss / viability criterion によって定義する。

さらに、3則を事後説明ラベルにしないため、VFT decision projection では採用した dimension ごとに admissibility / exclusion condition または比較規則を事前に明示することとした。

3則は `Ŷ_i(a;I_i)` の outcome components を介して `Γ_i^ind` に接続する。

---

## 11. Marxian categories

VFT が一般化して保持するのは、use-value / labor / exchange-value / surplus / accumulation の区別である。

VFT-specific use-value quantity は subjective interval realization として定義し、Marxian use-value と自動的に同一視しない。

Marx 固有の labor-value theory / surplus-value theory は socially necessary labor time 等の追加条件を持つ projection-specific specialization とする。

---

## 12. 現行最小構造

```text
F_t
= configuration of K_t, (K_i,t)_i, (P_i,t)_i,
  projection-specified relations / constraints
          ↓
Γ_i^feas(F_t)
          ↓
Γ_i^ind(F_t)
          ↓
A_i actor-side records
          ↓ shared event identity where needed
E_τ^shared (derived)
          ↓
ΔK / realized-use outcomes / exchange-value changes
          ↓
P_i update / K_i update / field reproduction or formation
```

A を通らない K change が必要な projection では、別途 `Ω_τ` 等を加える。

---

© T. Nuno  
Licensed under CC BY 4.0