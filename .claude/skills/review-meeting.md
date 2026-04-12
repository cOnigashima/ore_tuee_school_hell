# /review-meeting

Agent Team を起動して、複数視点の typed review をまとめる。

## 概要

3人のチームメイトが draft を批評し、`reviews/` に統合レビューを残す。
必要なら `story/design-debt.yaml` や `story/canon-patch-proposals/` に返す。

## チーム構成

| Teammate | 役割 |
|----------|------|
| critic | Promise を守れているかを見る |
| editor | 文体・テンポ・読みやすさの改善案 |
| continuity-guard | packet / scene / past canon との整合性を見る |

## 実行手順

1. 対象の `drafts/` と関連する `packets/`, `scenes/`, `story/promises.md`, `bible/`, `approved/`, `published/` を読む
2. critic が Promise / Arc / Packet とのズレを見る
3. editor が prose / pacing / readability の改善案を出す
4. continuity-guard が canon 矛盾と return target を特定する
5. 3人で議論し、統合 review を `reviews/` に出す

## 出力

`reviews/review-meeting-YYYYMMDD-HHMMSS.md` に以下を保存:

```markdown
# Review Meeting YYYY-MM-DD

## 対象
- draft:
- packet:
- episode:

## 総合スコア: [0-100]

### 内訳
- hook_strength（冒頭の引き）: [0-100]
- voice_consistency（口調の一貫性）: [0-100]
- continuity_safety（設定破綻なし）: [0-100]
- novelty（新鮮さ）: [0-100]
- readability（読みやすさ）: [0-100]
- pacing（テンポ）: [0-100]

## 改善点リスト

### 優先度: 高
1. [箇所]: [問題] → [提案]

### 優先度: 中
1. [箇所]: [問題] → [提案]

### 優先度: 低
1. [箇所]: [問題] → [提案]

## 議論メモ

[レビュー議論の要点]

## 上流へ返すべき項目
- design debt:
- canon patch:
- local rewrite:
```

## 起動コマンド例

```
drafts/draft_epXX_XXXXXXXX.md をレビューするため Agent Team を作って。
3人にして:
- critic: Promise と Arc のズレを指摘
- editor: 文体・テンポ・読みやすさの改善案
- continuity-guard: packet / scene / past canon との整合性チェック

議論して、スコアと改善リストを reviews/review-meeting-YYYYMMDD-HHMMSS.md にまとめて。
長生きする問題は story/design-debt.yaml や story/canon-patch-proposals/ に返す候補も書いて。
```
