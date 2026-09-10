# 価値場理論（Value-Field Theory）

**Theory refresh — Draft**  
Author: **T. Nuno**  
License: **CC BY 4.0**

---

## 1. 目的

価値場理論（Value-Field Theory; VFT）は、企業・国家・市場・通貨・資本といった既存の制度カテゴリーを出発点とせず、より基礎的な **資源 K、主体別資源状態 K_i、将来関係への信用 P_i、活動 A_i** から、経済活動とその発展を記述するための構造的フレームワークである。

現代では、国家・通貨・市場・プラットフォーム等の境界は必ずしも一対一に対応しない。

```text
state field
≠ necessarily currency field
≠ necessarily market field
≠ necessarily platform field
```

そのため VFT は、「国家」「企業」「通貨」等を primitive として固定するのではなく、より下位の構造からそれらがどう成立・維持・拡張されるかを記述する。

VFT の目的は、既存経済理論を一つの目的関数へ統合することでも、特定の制度形態だけを説明することでもない。

> 資源、信用、行為、関係から、経済形態を同一の構造上で連続的に再構成する。

---

## 2. 基本変数

### 2.1 K：resource state

`K` は対象となる系に存在する resource / capability の量を表す。

対象 resource は projection に応じて定める。物理資源だけでなく、設備、エネルギー、時間余力、技能、知識、労働能力等の capability を含めてもよい。

```text
K_t
= time t における resource state
```

K は制度、信用、期待そのものではない。

### 2.2 K_i：actor-specific resource state

`K_i` は、主体 `i` に帰属する resource state を表す。

```text
K_i(t)
= time t における actor i の resource position
```

基本的には stock として扱い、区間 `τ=(t0,t1]` を取ることで flow を表現する。

```text
ΔK_i(τ)
= K_i(t1) - K_i(t0)
```

生産、消費、交換、移転等の gross activity は `A_i,τ` と対応づける。したがって所有量、消費量、交換量等を別 primitive として固定する必要はない。

### 2.3 P_i：未実現関係への信用状態

`P_i` は、まだ実現していない関係や結果が将来成立すると主体 `i` が信用し、現在の意思決定で参照している非物理的な状態を表す。

例えば、

- 明日も同程度に生産できる
- 相手が次回も交換に応じる
- 預金を将来も引き出せる
- 契約が履行される
- 制度が継続する
- 商品を将来も販売できる

といった未実現関係への信用が P に属する。

P そのものは直接観測できず、主体は複数の proxy / reference `X_i,t` を参照して P を形成・更新する。

```text
X_i,t = {x_1, x_2, ..., x_n}

X_i,t
→ P_i,t
```

経済関係が複雑になるほど、P を支える proxy は増加しうる。

```text
X^(stage+1) ⊇ X^(stage)
```

### 2.4 A_i：activity / action

`A_i` は主体 `i` によって実行される活動を表す。

労働、生産、消費、使用、交換、投資、移転、契約、決済、探索、学習、政策、制度変更、情報伝達等を含みうる。

---

## 3. 基本循環

VFT の最小循環は、

```text
K_t
↓
P_t
↓
A_t
↓
ΔK_(t+1)
↓
P_(t+1)
```

として表せる。

観測側まで含めれば、

```text
realized ΔK
↓
observable proxies X
↓
P
↓
A
↓
next realized ΔK
```

となる。

過去に実現した resource change は直接または proxy を通じて P を支持する。P は未実現の将来関係を現在の判断で利用可能にし、その P に基づいて A が実行される。A の結果として新しい `ΔK` が生じ、その結果が再び P を更新する。

---

## 4. Field

VFT における field は独立した価値スカラーではない。

ある時点の K、各主体の K_i / P_i、および主体間・resource 間の関係・制約によって形成される **action-generating configuration** を指す。

```text
F_t
= configuration(
    K_t,
    (K_i,t)_i,
    (P_i,t)_i,
    relations,
    constraints
  )
```

必要な projection では、

```text
Γ_i^feas(F_t)
Γ_i^avail(F_t)
Γ_i^adm(F_t)
```

を用いて、物理・制度上可能な A、主体が認識可能な A、判断上採用可能な A を区別できる。これらの普遍的な choice rule は Core では固定しない。

---

## 5. 使用価値

resource は、保有されているだけでなく、使用・消費 A を通じて現実に利用される。

```text
resource K
↓
use / consumption A
↓
physical realization
```

VFT では、使用価値を異種 resource 間で単一の共通尺度へ還元することを前提としない。

使用価値の実現を観測する必要がある場合は、resource ごとに実際に使用・消費された物理量を記録する。

```text
food     → kg consumed
energy   → kWh used
machine  → operating time / output
land     → utilized area / period
```

ここで扱うのは、主体の満足度そのものではなく、resource が use / consumption A を通じて現実にどの程度利用されたかである。

---

## 6. 余剰

主体が再生産・生存・維持等に必要な resource を超えて K を持つ場合、余剰が成立する。

単純には、

```text
surplus
= available K
- required K
```

と表現できる。

重要なのは余剰が一度発生することではなく、**必要量を超える K が反復的に生成されること**である。

```text
A
→ K
→ required K を満たす
→ surplus
→ next A
```

反復的な余剰が成立すると、次期の A をすべて再生産のために拘束する必要がなくなる。

余剰は備蓄、交換、贈与、投資、生産能力拡張、労働時間削減、新しい活動等へ振り向けることができる。

したがって反復的な余剰は、単なる残余 resource ではなく、

> 次期の resource allocation や A を選択できる抽象的な自由度

として機能する。

---

## 7. 分業・相互依存・交換

主体ごとに A / capability が分化すると、分業と相互依存が成立する。

```text
actor i
→ specialized A_i
→ output K_i

actor j
→ specialized A_j
→ output K_j
```

余剰があり、異なる主体が互いの resource を必要とすると交換 A が成立する。

```text
actor i : surplus r_a
actor j : surplus r_b

r_a ↔ r_b
```

交換実績は次回の交換可能性を支える proxy となる。交換が反復されると、「この条件なら次回も交換できる」という shared P が形成される。

一回限りの利得を増やしても、相手の再生産条件を破壊すれば次期の交換 A は縮小する。この段階ですでに、現在の成果だけでなく `A_(t+1)` の維持が重要になる。

---

## 8. 貨幣

貨幣は、交換によって生まれた余剰の自由度をさらに抽象化する。

物々交換では余剰は特定 resource と具体的な交換相手に拘束される。貨幣が成立すると、

```text
specific resource surplus
↓
money
↓
many possible future resources / activities
```

となり、余剰から生まれた交換可能性をより一般的な形で保存できる。

貨幣は、

> 余剰交換可能性の保存と、shared P の共通計量

として扱える。

価格、残高、交換レート等は P そのものではなく、P を形成・支持する observable proxy である。

---

## 9. 銀行と信用

貨幣の保管・決済・移転が増えると、それらを媒介する銀行等の主体が成立する。

預金残高は observable な記録であり、

> その残高が将来も引出し・決済に利用できる

という信用は P に属する。

```text
deposit balance
→ observable proxy

future availability of deposit
→ P
```

銀行は保管、決済、為替、信用供与等を通じて主体間で成立可能な A を拡張する。一方、貸倒れ、流動性不足、決済不能等は、個別の resource loss に加えて将来関係への P を大きく毀損しうる。

---

## 10. 機械資本と大量生産

machine resource を利用すると、同じ labor A からより多くの output K を生成できる。

```text
A^labor + K^machine
→ expanded K^output
```

生産 capability が拡張すると、生産された K を利用・消費する A も必要になる。

```text
A^production
↔
A^consumption
```

価格調整、販路拡大、広告、商品改良、決済手段の拡張等は、現在利益のためだけでなく、次期にもより多くの A を成立させるための活動として読むことができる。

---

## 11. 資本

余剰そのものを capital とはしない。

反復的な余剰が生み出す自由度の一部を、将来の A を拡張する K へ再投入すると、次の循環が形成される。

```text
repeated surplus
↓
abstract degree of freedom
↓
reinvestment
↓
K / capability expansion
↓
broader A_(t+1)
↓
new surplus
```

VFT では capital を、単なる asset stock ではなく、

> 余剰によって得られた自由度を将来の A の拡張へ再投入する反復構造

として記述する。

---

## 12. 国家・制度圏・プラットフォーム

主体間関係が拡張すると、それを安定化する制度が形成される。

所有権、契約、裁判、制裁、貨幣制度、商慣行等は主体間 P を安定させ、より広い A を成立させる。

国家も新しい primitive を必要とする存在ではない。法律、政策、安全保障、外交、資源アクセス、インフラ、決済制度等を通じて、自らの field 上で成立する A を維持・拡張する主体として記述できる。

また、国家、宗教、大規模プラットフォーマー等は、自身の A によって他主体の P へ直接作用する能力を強く持つ。

```text
A_F
→ ΔP_i
```

例えば法律、政策発表、保証、制裁、認証、推薦、ランキング、アカウント停止、決済保証等は、対応する physical `ΔK` がまだ実現していなくても他主体の期待や信用を変化させる。

```text
A_F
→ P_i
→ A_i
```

ただし、このように先行して形成された P が長期的に維持されるためには、その後の realized `ΔK` と一定の整合性を持つ必要がある。制度的 A は信用の先行形成、realized `ΔK` はその事後検証として区別できる。

---

## 13. 3つの管理合理性

VFT では、経済発展の各段階を通じて、管理・意思決定に少なくとも3つの異なる合理性が反復して現れると考える。

### 13.1 resource-realization

主体は candidate A に対して resource outcome を期待する。

```text
candidate A
↓
preference / expectation
↓
expected ΔK
↓
execution
↓
realized ΔK
```

第1の合理性は、期待した resource outcome と実際の resource outcome の乖離を抑えることにある。

```text
expected ΔK
≈
realized ΔK
```

これは単純な K 最大化ではなく、期待した結果を現実に成立させる予実一致の合理性である。

### 13.2 activity-flow

第2の合理性は、現在の A の量そのものではなく、次期にも A が成立可能である状態を維持・拡張することにある。

```text
maximize / maintain A_(t+1)
```

個人であれば生存、体力、技能、関係、選択肢等、企業であれば顧客、販路、資金、人材、技術、市場等、国家であれば資源アクセス、安全保障、外交関係、制度参加等が次期 A を支える。

市場シェア、利用者数、取引量、標準採用等は、特定 projection における `A_(t+1)` の proxy となりうる。

### 13.3 P-downside

第3の合理性は、将来の A を支えている P に重大な毀損が生じることを避けることである。

```text
minimize ΔP^-
```

貸倒れ、流動性不足、契約未達、信用毀損、顧客離脱、制度への信頼喪失、将来 A を成立させる関係の破壊等が対象になる。

これは P を最大化することではなく、future activity viability を破壊する重大な downside を避けることを意味する。

### 13.4 3合理性の競合

3つの合理性は一つの目的関数へ還元しない。

```text
1. expected ΔK と realized ΔK の一致
2. A_(t+1) の維持・拡張
3. P downside の抑制
```

A の拡張を優先しすぎれば予実差や P downside が増える。P を守りすぎれば A が縮小する。予実一致を優先しすぎれば既存の活動へ固定され、新しい A の形成を阻害する。

したがって A の選別は第4の独立合理性ではなく、3合理性の競合結果として生じる。

危機、停滞、失敗は、主体が単に非合理だから生じるだけではなく、**3つの合理性を同時に満たせなくなる構造**としても説明できる。

---

## 14. 組織における機能分化

3合理性は、大規模組織で繰り返し見られる機能分化とも大きく外れていない。

```text
A_(t+1) の維持・拡張
→ strategy / direction / domain expansion

P downside の抑制
→ management control / protection / allocation

予実一致
→ execution / operation / plan realization
```

これは組織階層が必ず3段になるという意味ではない。異なる合理性が同時に存在し相互に衝突するため、組織が大規模化すると別責務へ分化しやすいという構造的対応として扱う。

---

## 15. 企業・国家・通貨を同じ構造で見る

企業、国家、通貨は制度的には異なる。

一方、

```text
field を形成・維持する
↓
P を通じて A を成立させる
↓
A_(t+1) を維持・拡張する
```

という抽象構造では比較できる。

企業の市場シェア拡大、国家の活動圏・制度圏維持、通貨の利用圏拡大は、それぞれ別 projection ではあるが、どの field 上でどの程度の A が継続的に成立するかという共通構造へ配置できる。

```text
currency field
≠ necessarily state field
```

profit maximization は企業行動を説明する有力な projection ではあるが、VFT の universal rule とはしない。

---

## 16. 既存理論との関係

VFT は既存理論を単純に合成するものではない。

既存理論が捉えてきた部分構造を、K / K_i / P / A / field 上へ再配置する。

Marxian categories からは use-value、labor、exchange-value、surplus、accumulation の区別を参照する。ただし labor-value theory / surplus-value theory 等の固有仮定は Core の universal rule とはしない。

Capability Approach、bounded rationality / behavioral theory of the firm、managerial theories of the firm、management control、institutional economics、expectation theory、financial instability、control theory / system dynamics、accounting ontology 等との接続は、Core と分離して整理する。

---

## 17. Core で固定しないもの

VFT Core では、以下を universal rule として固定しない。

- utility maximization
- profit maximization
- general equilibrium
- deterministic choice function
- preference の普遍的関数形
- P の単一 proxy
- `A_(t+1)` の単一計測法
- 3合理性の weighting function
- Marxian labor-value theory / surplus-value theory
- B/S・P/L・複式簿記
- 特定の市場・制度・契約形態

必要な具体形は projection / measurement 側で定義する。

---

## 18. ドキュメント

- [モデルノート](docs/01_model_notes.md)
- [計測](docs/02_measurement.md)
- [背景・整理経緯](notes/background.md)
- [既存概念・応用への射影](notes/projections.md)
- [既存理論との接続](notes/theoretical_connections.md)
- [拡張・再検討ノート](notes/future_topics.md)

---

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)  
© T. Nuno
