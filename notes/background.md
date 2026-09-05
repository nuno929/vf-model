# 価値場理論 — 背景と整理の経緯

> この文書は理論コアではなく、価値場理論が現在の K / K_i / P / A / field 構造へ至るまでの整理経緯を保存する履歴ノートである。現行定義は README / Core / Measurement / Projections を優先する。

## 1. 初期構造

初期には P / K / X / A や独立した価値場変数 V を置いたが、選好 X や独立 scalar V は廃止した。

現行の field は独立変数ではなく、K / K_i / P_i と projection-specified relations / constraints から導かれる action-generating configuration を指す。

必要に応じて、

```text
F_t := configuration(...)
Γ_i(F_t) := feasible / inducible action correspondence
```

という derived notation を使うが、これらは universal state primitive や deterministic choice function ではない。

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

P_i の valuation は subjective appraisal、K_i の valuation は specified recognition / comparison / unit-of-account rules の下で作る exchange-value representation として区別する。

---

## 3. use-value / exchange-value

同一 resource について、physical capability / realized use experience / exchange-value representation を区別する。

VFT における use-value quantity は、resource stock 自体や technical service potential ではなく、**主体が interval 内に resource を実際に利用・消費し、その経験に帰属される形で ex post に realized した主観的効用量**とする。

physical stock / capability は K として時点観測できる一方、それは use-value quantity そのものではない。

同じ主体・同じ resource・同じ利用量でも、充足状態、順序、文脈、他の経験等によって realized outcome は変わりうる。限界効用逓減はその一例である。そのため use-value quantity に一般的な再現性や interval 間の加法性を仮定しない。

この整理により use-value quantity は interval-indexed outcome として扱う。

```text
actual use over previous interval
        ↓
subjective experience
        ↓
realized use-value
        ↓
P_i update
        ↓
expectation about future use
```

時点 `t` で参照できる use-value は前区間までの realized outcome であり、将来区間の use-value は P_i 上の expectation として表現される。

瞬間的な use-value rate が必要な projection では interval quantity の極限・微分的表現として導入できるが、point-in-time stock valuation とは扱わない。

この時間形式を P/L-like と呼ぶ。ただし会計上の P/L entry と同一視しない。

exchange-value は resource 間を比較可能な尺度へ写像する representation であり、point-in-time position にも interval transaction valuation にも現れうる。

したがって「use-value = flow / exchange-value = stock」という完全な一対一対応は採らない。ただし **VFT-specific use-value quantity は interval realization に限定し、exchange-value representation は stock / flow の双方を取りうる**という非対称性を維持する。

以前の「利用可能性と交換可能性を複式に保持する」という表現は、利用可能性が K capability 側であり realized use-value と異なるため撤回した。現在は複式簿記との対応を Core には置かず、多面的記述という弱い会計アナロジーに留める。

---

## 4. P / forecast

P は structured subjective state とする。

belief / expectation、preference / valuation、trust / reputation、norm recognition 等を内部 component として持ちうるが、Core primitive は分割しない。

一時期 `E_i[ΔK | a,I_i]` を Core の forecast 記法として使ったが、probability measure / causal semantics を固定しているように読めるため撤回した。

現行では、

```text
ΔK̂_i(a;I_i)
```

を generic action-contingent forecast とし、確率・因果構造を持つ projection だけ条件付き期待値等へ specialize する。

また、A による加工・変換は resource の利用可能性を変えるが、加工後 use-value quantity は加工時点で確定しない。後続 interval の実利用体験で realized し、その前区間までの realized value が P_i を更新する経路を明示した。

---

## 5. A / ΔK

途中では ΔK records を gross activity / generalized bookkeeping のように使ったが、activity と endpoint state difference が混同されるため撤回した。

さらに `K_t1-K_t0` を universal Core 式とすると heterogeneous K coordinates に subtraction を要求するため、一般形を projection-defined difference operator に変更した。

```text
A history = interval gross activity / events
ΔK_τ := δ_K(K_t0,K_t1)
```

additive vector projection では `δ_K(K_t0,K_t1)=K_t1-K_t0` を特殊形として使える。

独立した gross-flow primitive は Core に置かない。

また A は actor-side に限定し、自然劣化・災害・偶発故障等の actor-side でない変化は、必要な projection で `Ω_τ` 等の exogenous / environmental process として追加できる。

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

当初は physical / use-value activity の input / output を exchange-value へ写像する経路を中心に説明したが、accounting projection では contract / financial / valuation-only events も存在する。

そこで現行 Core では、**specified economic changes を exchange-value の比較可能尺度へ写像し、specified comparison boundary の下で取る差分 / residual** とする。

```text
specified economic changes
        ↓ exchange-value representation
comparable values
        ↓ comparison under specified boundary
surplus / deficit
```

production surplus / accounting profit / income / valuation gain / wealth change は Core で同一視しない。

余剰は「物理的に増えた量」そのものではない。同じ物理対象でも、利用方法・交換可能性を認識できる主体とできない主体では value representation が異なりうる。機械が利用法を知らない主体には単なる箱・物体にしか見えないという例は、この非物理性を示す。

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
起業           = business-oriented field formation の一類型
新規事業開発   = 既存 field から business-oriented field を形成・分岐
既存事業運営   = 成立済み business field の維持・再生産・改善
```

profit / surplus は business existence の定義条件ではなく、exchange-value 側の重要 metric とする。

---

## 10. 3つの管理合理性

resource-realization / activity-flow / P-downside の3則は constitutive rationality assumptions とする。

use-value を realized experience として明示したことで、resource-realization は resource / capital outcome だけでなく、resource の利用による desired realized-use outcome も含むように整理した。

activity-flow は既存 activity の継続だけでなく、必要に応じた field formation / renewal を含みうる。

P-downside は P 全体の universal ordering を意味しない。projection-specific な P component と threshold / loss / viability criterion によって、将来の action-generating viability の重大な劣化を定義する。

profit / utility は3則の特殊化ではなく、具体的 decision problem の metric / objective / proxy とする。

---

## 11. Marxian categories

VFT が一般化して保持するのは、use-value / labor / exchange-value / surplus / accumulation の区別である。

ただし VFT-specific use-value quantity は subjective interval realization として定義し、Marxian use-value と自動的に同一視しない。

Marx 固有の labor-value theory / surplus-value theory は socially necessary labor time 等の追加条件を持つ projection-specific specialization とする。

---

## 12. 現行最小構造

```text
F_t
= configuration of K_t, (K_i,t)_i, (P_i,t)_i,
  projection-specified relations / constraints
          ↓
        Γ_i(F_t)
          ↓
        (A_i)_i
          ↓
resource activity / transformation / exchange / learning
          ↓
δ_K endpoint difference / subjective use experience / exchange-value changes
          ↓
realized use-value over interval
          ↓
P_i update / K_i update / field reproduction or formation
```

A を通らない K change が必要な projection では、別途 `Ω_τ` 等を加える。

---

© T. Nuno  
Licensed under CC BY 4.0