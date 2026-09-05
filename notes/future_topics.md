# 価値場理論 — 拡張・再検討ノート

> この文書は Core 定義ではなく、今後の展望・具体化候補・再検討事項を保存するためのノートである。

## 1. 集約と分布化

Core では、K は共通の resource / capital state、`K_i` は主体ごとの ownership / attribution、`P_i` / `A_i` は主体ごとの state / process として扱う。

今後の検討候補：

- どの条件で分布化が有効か
- 平均・代表主体で失われる情報
- 多峰性・非対称性
- ネットワーク構造をどこまで残すか
- ownership distribution と resource distribution の違い
- shared P の推定と集約
- micro observable から macro observable を再構成する条件

---

## 2. K と K_i の表現粒度

K は resource / capital、`K_i` は主体 `i` に所有・保有・帰属する resource / capital とする。

`K_i` は actor-relative access / usability view ではない。また、K / K_i の完全な真値を主体本人や観測者が常に把握できるとは仮定しない。

今後の検討候補：

- K の標準次元を設けるか
- physical resource / capital / human capital / knowledge / money の分解
- ownership / possession / control / attribution の境界
- 共有資産・共同所有の表現
- liabilities / claims / financial capital の扱い
- stock / flow の境界
- K_i の測定誤差と未把握資産・債務
- Marxian capital concept や conventional accounting capital との対応

---

## 3. P と shared P

P は主体ごとの subjective evaluation / expectation state とする。

P はどれだけ共有されても主観状態である。shared P は、指定 actor set の P の共通性・整合性・分布を表す projection-local な構造として扱う。

今後の検討候補：

- P の標準次元を設けるか
- belief / valuation / preference / trust / norm-expectation の型区分
- shared P の定義：平均、重なり、支持率、consensus、common belief 等のどれを使うか
- P 最大化を使う場合の actor set / dimension / proxy
- P 真値が直接観測不可であることを前提にした measurement model
- 契約・制度・規範認識と P の関係
- `P_j(a)` の評価者・評価対象の識別
- market outcome を P proxy に使う際の endogeneity

---

## 4. 契約・制度・法的効力

契約・制度は resource / capital そのものとして K へ押し込まず、法的・制度的事実、主体の主観、実現 resource change を分けて扱う。

今後の検討候補：

- legal validity / enforceability をどの layer で記述するか
- contract event / legal record / institutional rule の observable representation
- 履行期待・執行期待を P へどう落とすか
- 契約履行・違反・制裁が ΔK に与える経路
- shared P と institution stability の関係

---

## 5. ΔK records と会計

Core では `H` を置かず、一つの A が生む複数の ΔK を record / history として保持する。

```text
A
├─ ΔK_1
├─ ΔK_2
└─ ...
```

これを accounting projection に写像すると、一般化された仕訳として利用できる。

今後の検討候補：

- ΔK record の標準的な identity / timestamp / actor / owner / resource coordinate
- gross activity と net state change の再構成
- double-entry accounting との対応
- stock-flow consistency
- recognition timing
- transfer と transformation の識別
- internal transfer の相殺規則
- resource destruction / depreciation / depletion の記帳

---

## 6. valuation / surplus / accumulation

surplus は物理的 primitive ではなく、実現した ΔK records を valuation / bookkeeping rule で共通尺度化して得る accounting residual とする。

今後の検討候補：

- unit of account の選択
- physical quantity と monetary valuation の関係
- historical cost / market value / replacement cost 等の差
- surplus / profit / income / wealth change の相互関係
- consumer / producer surplus との対応
- surplus attribution / distribution
- surplus distribution → K_i(t+1) → accumulation の動学
- nominal / real の射影

---

## 7. 使用価値・労働価値・交換価値

マルクス経済学の理論骨子を、規範・政治的結論を前提にせず VFT 上へ射影する。

### 使用価値

今後の検討候補：

- K が特定 A / transformation を可能にする「機能」をどう表現するか
- physical productivity / capability と subjective utility の分離
- use-value の多目的性
- scarcity と use-value の分離

### 労働価値

今後の検討候補：

- labor activity / labor time の標準表現
- skill / intensity / productivity 補正
- socially necessary labor time の benchmark 定義
- direct / indirect labor の追跡
- labor-value と monetary valuation の関係
- labor-value を「唯一の価値源泉」とする必要があるかの理論分離

### 交換価値

今後の検討候補：

- price / exchange ratio / accounting valuation の区別
- use-value / labor input / exchange value の相互変換を普遍式にしない条件
- market institution / bargaining / monopoly power 等の影響

---

## 8. 期待変化 E[ΔK]

`E_i[ΔK]` は expected realized resource / capital change として扱う。

今後の検討候補：

- 多次元 ΔK に対する expectation representation
- probability / scenario / qualitative forecast の接続
- action-contingent forecast の conditioning
- planned change と expected realized change の乖離
- P 内の belief / outlook から forecast をどう生成するか
- forecast error と learning

---

## 9. 3つの管理合理性公理

現行 VFT は、

1. resource-realization
2. activity-flow
3. P-downside

を意思決定合理性の公理系として採用する。

今後の検討候補：

- 3則の独立性・完備性・最小性
- 第4の独立合理性が必要になる条件
- context-dependent priority / weight / constraint
- actor / institution / hierarchy 間の機能分担
- same action が複数則へ寄与するときの識別
- resource-realization と long-run accumulation の関係
- activity-flow と going-concern / growth / contraction の関係
- P-downside と shared P / system viability の関係

### P-downside

P の客観的真値は置かない。今後の具体化では、

- 誰の P を対象にするか
- どの P 次元を対象にするか
- shared P をどう推定するか
- downside / unacceptable region / threshold をどう定義するか
- rights / minimum guarantee / satisficing 等とどう接続するか

を扱う。

---

## 10. 自給自足・制度的分業・組織階層

自給自足では単一 actor が3則すべてを担える。

国家レベルの資本主義社会を粗視化すると、典型的には

```text
individuals -> resource-realization heavy
firms       -> activity-flow heavy
state       -> P-downside heavy
```

と見える。

今後の検討候補：

- 資本主義以外での分業パターン
- household / cooperative / family business / commune の比較
- crisis / growth / contraction での priority shift
- operational / managerial / governance の階層差
- state weakness 時に R3 を誰が担うか

---

## 11. ミクロ／マクロ接続

VFT は同じ common K 上でミクロとマクロを接続する。

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

今後の検討候補：

- micro ΔK records から macro accounting aggregate を再構成する方法
- ownership distribution と capital accumulation の接続
- shared P と macro demand / investment / credit conditions の接続
- distributional accounting
- macro observable から micro structure をどこまで逆推定できるか
- policy A → P_i → A_i → ΔK → macro aggregate の識別

---

## 12. 既存経済学との接続

utility / profit は3則の特殊化ではなく、decision evaluation の指標・関数として扱う。

今後の検討候補：

- utility と use-value の明示的分離
- profit と surplus の分離
- budget constraint / compatibility / market equilibrium の射影
- supply / demand と planned resource change の関係
- mainstream micro / macro と Marxian accounting structure の共通表現
- real / nominal / physical / accounting のレイヤー分離

---

## 13. 実証・計量化

今後の具体化候補：

- K / K_i の partial observability
- ownership / attribution measurement
- P / shared P の proxy design
- A / ΔK record の event log
- valuation / bookkeeping mapping
- surplus / accumulation measurement
- labor activity / labor-time measurement
- use-value capability measurement
- planned / expected / realized change の分離
- actor/context ごとの3則 priority 推定
- micro / macro accounting consistency
- ケーススタディ
- パネルデータ
- structural estimation / simulation

---

© T. Nuno  
Licensed under CC BY 4.0