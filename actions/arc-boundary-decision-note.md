# Arc Boundary Decision Note

> status: provisional
> owner: story-os
> created: 2026-04-12
> purpose: `packet-001`〜`packet-003` を仮正本として進めるため、arc 境界の扱いを一時決定する

## 背景

現在、正本同士で以下のズレがある。

- `story/promises.md`
  - arc-01 = ep01–35
  - arc-02 = ep36–70
  - arc-03 = ep71–100
- `packets/frozen/packet-003-festival.md`
  - ep30 の供養祭が、一年目の締めとして非常に強く機能している
- 現行設計レビュー
  - ep30 で
    - 「小さい話なら固定養分なしでも回る」
    - ただし「長い話はまだ無理」
    を出しており、読者体験上はここが一年目終点候補になっている

## いまの判断

### 仮採用

- `packet-001`〜`packet-003` は採用する
- ep30 を **一年目終点候補** として扱う
- ただし `story/promises.md` の arc 話数境界は **現時点では書き換えない**

### 理由

- 机上で arc 境界を確定しきるより、本文試し書き後に reverse flow で戻した方が安全
- `CLAUDE.md` の方針（全部決め切ってから書くことを禁じる）に合う
- packet 側の完成度は高く、まずは prose 検証を優先した方がよい

## 当面の working assumption

- 一年目の感情的・構造的な締めは ep30 を第一候補とする
- ep31 以降の二年目開始案は **有力だが未確定**
- arc-01 = ep01–35 は、いったん `promises.md` 側の旧境界として保持する

## 検証手順

以下の 4 本を優先して試し書き / 本文プロット化する。

1. ep01
2. ep12
3. ep23
4. ep30

### 検証観点

- ep30 が本当に「一年目の終点」として読後感を持つか
- ep31 で後輩導入 / 二年目開始した方が自然か
- 久瀬主人公が 30 話時点で十分に立っているか
- 供養祭の成功が「仮答え」として機能しているか
- 「でも長いやつはどうすんだよ」が次ブロックの強い引きになっているか

## patch の条件

以下が YES なら `story/promises.md` を patch する。

- ep30 が一年目終点として機能する
- ep31 を二年目開始にすると読者体験が良くなる
- packet-004 以降もその境界で無理なく接続できる

## patch 候補

### 候補A
- arc-01 = ep01–30
- arc-02 = ep31–70
- arc-03 = ep71–100

### 候補B
- `promises.md` の arc は維持
- block / packet 側だけ ep30 を一年目の実質締めとして扱う

現時点では **候補A を第一候補** とするが、未確定。

## 禁則

- このノートを根拠に `promises.md` を即時更新しない
- 試し書き前に arc 境界を canon 扱いしない
- packet-001〜003 の内容を arc 境界だけで巻き戻さない

## 次アクション

- ep01 / ep12 / ep23 / ep30 の本文プロットまたは試し書き
- その後、`story/promises.md` に対する canon patch proposal を作成する
