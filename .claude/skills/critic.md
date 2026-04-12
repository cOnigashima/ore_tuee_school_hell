# /critic

draft を typed review として批評し、必要なら上流へ返す。

## 入力

- `drafts/` にある原稿ファイル
- 関連する `packets/`, `scenes/`, `story/promises.md`, `bible/`, `approved/`, `published/`

## 手順

1. 指定された原稿または最新の原稿を読む
2. 対応する packet / scene / promises / rules を照合する
3. `reviews/` に typed review を出す
4. Canon 問題や長生きする構造問題があれば、`story/canon-patch-proposals/` または `story/design-debt.yaml` に返す候補を明記する

## 批評観点

### 構成
- 冒頭のつかみ
- 中盤の展開
- 末尾の引き

### 文体
- 視点のブレ
- 口調の一貫性
- 禁則違反

### キャラクター
- キャラクターの一貫性
- 会話の自然さ

### 読みやすさ
- 一文の長さ
- 情景描写と会話のバランス

## 出力フォーマット

```markdown
# Prose Review: [draft title]

## 対象
- draft:
- packet:
- episode:
- source scenes:

## 守れた約束
- 

## 破った約束
- 

## Canon 問題
- none | 

## 構成問題
- 

## 感情線の問題
- 

## 文体問題
- 

## 修正優先度
- 高:
- 中:
- 低:

## 上流へ返すべき項目
- return target:
- design debt:
- canon patch:
```

## 保存先

`reviews/prose-review-YYYYMMDD-HHMMSS.md`
