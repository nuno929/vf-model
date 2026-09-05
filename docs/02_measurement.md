# 価値場理論 — 計測

## 1. 目的

本書は、VFT の Core を実証・観測・会計へ落とす際の境界を整理する。

計測上は、**物理・実物側 K、actor-specific subjective state P_i、期間 flow の P/L monetary representation、B/S 上の K_i** を区別する。

---

## 2. K の観測

K は実物・物理側の resource state である。

候補 observable には、原材料量、製品量、設備、稼働、労働時間、エネルギー使用、土地、時間、技能・人的能力等がある。

K の完全観測は前提としない。resource coordinates と観測単位は projection ごとに定める。

---

## 3. K_i の計測

`K_i` は B/S 上の actor-indexed book-value capital position である。

したがって `K_i` の計測には少なくとも、

1. ownership / holding / attribution
2. recognition rule
3. valuation rule
4. unit of account
5. bookkeeping / accounting standard

が必要になる。

`K_i` は K の subset / partition ではない。共同所有・重複帰属・連結対象等を含みうるため、actor-indexed monetary representation として扱う。

### financial assets

預金、債券、売掛債権等は、契約・権利関係そのものではなく、会計上認識・評価された financial asset position として `K_i` に現れる。

---

## 4. P の計測

`P_i` は subjective evaluation / expectation state である。

候補 proxy には、期待調査、選好・評価調査、発話、信用・信頼指標、制度・契約への履行期待、将来見通し等がある。

shared P は複数主体の P proxy の共通性・整合性・分布として推定する。客観的な社会価値の真値は仮定しない。

P proxy が price / market outcome と同時決定される場合は、endogeneity / post-treatment / outcome leakage を区別する。

---

## 5. A と ΔK の観測

A は生産、消費、交換、投資、労働、移転、契約、政策等の actor-side process / event である。

`ΔK` は K に実現した resource change であり、**会計仕訳そのものではない**。

```text
physical K
   ↓ A
physical flow / ΔK
```

`ΔK` は必ずしも `K(t1)-K(t0)` という単一の endpoint difference ではない。異質な resource coordinates ごとの変化を記録し、net endpoint change が必要な場合に projection 側で集約する。

---

## 6. P/L：physical flow の monetary measurement

P/L が表現する対象は期間中の physical / economic flow である。

```text
physical activity / ΔK
        ↓ monetary measurement μ
P/L entries
```

P/L statement 自体は通貨単位で記録されるが、対象は期間中の生産・消費・労働・減耗・交換等である。

計測では少なくとも、

- recognition timing
- monetary measurement / valuation
- revenue / expense classification
- internal transaction treatment
- accounting boundary

を固定する。

---

## 7. B/S：abstract monetary stock

B/S は actor-specific capital stock / position を通貨単位で表現する。

```text
B/S_i(t) ≡ K_i,t
```

P/L と B/S は同じ monetary unit により接続する。

```text
P/L period amounts
     ↓ closing / attribution / distribution
B/S K_i(t+1)
```

ただし P/L の期間損益と B/S の `ΔK_i` は、増資、配当、資本取引、評価差等により一般には一致しない。

---

## 8. surplus の計測

surplus は、指定 accounting boundary で P/L 上の monetary amounts を aggregation / consolidation / offset rule に従って合算した period increment / residual として測る。

```text
P/L books
  ↓ consolidation / aggregation
surplus / deficit
```

少なくとも、

1. actor set
2. accounting boundary
3. unit of account
4. recognition timing
5. internal transaction elimination
6. valuation rule
7. attribution / distribution rule

を明示する。

surplus の帰属・留保・分配は、次期 B/S 上の `K_i` へ接続する。

---

## 9. E[ΔK]

`E_i[ΔK]` は expected realized resource change であり、desire / preference / plan とは区別する。

candidate action ごとの forecast を

```text
E_i[ΔK(S,τ) | a, I_i]
```

と書く場合、`| a` は observational conditioning ではなく action-contingent forecast の略記である。

---

## 10. 3つの管理合理性の計測

3則は VFT の constitutive rationality assumptions とする。

経験的検証では、3則そのものの存在を毎回検証するのではなく、projection-specific に定めた objective / priority / weight / constraint / threshold / horizon が行動・結果をどの程度説明するかを検証する。

---

## 11. Marxian projection の計測

- use-value：K がどの A / transformation を可能にするか
- labor measure：labor activity / labor time
- Marxian labor-value：socially necessary labor time 等の追加条件を伴う specialization
- exchange-value / price：market / monetary valuation
- generic surplus：P/L aggregation による monetary increment
- Marxian surplus value：Marx 固有の追加制約を含む specialization

generic labor time と Marxian value、generic surplus と Marxian surplus valueを同一視しない。

---

## 12. ミクロ／マクロ集約

ミクロとマクロは、同じ physical K と、その activity を monetary measurement した P/L、および B/S 上の `K_i` を異なる scope で観測・集約することで接続する。

micro-to-macro reconstruction では、ownership / attribution、valuation、accounting boundary、consolidation、shared P aggregation の情報損失を明示する。

---

## 13. 実証上の原則

少なくとも以下を明示する。

1. K の resource coordinates
2. A の event unit / ordering
3. ΔK の観測単位
4. monetary measurement / valuation rule
5. P/L recognition / classification
6. B/S ownership / attribution / recognition
7. K_i の book-value rule
8. P / shared P の proxy
9. E[ΔK] の推定法
10. surplus の accounting boundary / consolidation rule
11. 3則の empirical specification
12. micro / macro aggregation rule
13. 欠測・測定誤差・情報損失

---

© T. Nuno  
Licensed under CC BY 4.0