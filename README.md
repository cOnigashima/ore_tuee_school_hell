# Story Template

この template は、創作の会話ログをそのまま本文にしないための Story OS です。
正本は会話ではなく repo の各ファイルに置きます。

この template が目指している接続は次の通りです。

- `Promise -> Arc -> Packet -> Scene -> Draft`
- `Review -> Canon reverse flow`

つまり、

- 作品の核が固定されている
- 今書く単位まで分解されている
- 本文が上流へトレースできる
- レビュー結果を上流へ返せる

この 4 点が揃えば機能します。

## どのアシスタントを使うか

どれでも構いません。重要なのは「会話」ではなく「ファイル」を正本にすることです。

- ChatGPT / Claude の Web UI を使う場合:
  `prompts/` の prompt を順番に使い、出力を対象ファイルへ貼る
- Codex / Claude Code のように repo に入れる場合:
  `README.md`, `CLAUDE.md`, 各 starter を読ませて直接ファイルを埋める
- どのツールでも共通:
  `CLAUDE.md` はファイル名が歴史的にそうなっているだけで、実質は repo の制作契約

## まず何をどこまで決めればいいか

先に固めるのは「次の 1〜2 packet の因果に効くもの」だけで十分です。

今決めるべきもの:

- 主人公の欲望と欠落
- 敵対圧
- 世界のハードルール
- 禁忌
- この Arc の終点
- 直近 Packet の `disclose / withhold`
- 文体ルール

まだ決めなくてよいもの:

- 3 Arc 先の細部
- 現在出ない地名一覧
- 今出ない脇役の全履歴
- 世界史の完全年表
- 将来使うかも不明な設定

判断基準はこれです。

- その情報がないと、キャラの選択が決まらないか
- その情報がないと、世界の因果が破綻するか
- 後で変えると、既存 Draft を壊すか

どれにも当たらないなら、`story/open-questions.md` に逃がします。

## ディレクトリの見方

### 契約層

- `CLAUDE.md`
- `template.manifest.json`

制作ルールと runtime contract。

### Canon / Macro 層

- `story/promises.md`
- `story/open-questions.md`
- `story/design-debt.yaml`
- `story/seeds/`
- `story/canon-patch-proposals/`
- `bible/world.md`
- `bible/characters.md`
- `bible/rules.md`
- `arcs/`

作品の核と安定設定。

### Planning / Meso 層

- `packets/`

Arc を数話単位の実装可能な粒度に落とす場所。

### Execution / Micro 層

- `scenes/`
- `drafts/`

局所衝突と本文。

### Feedback / Release 層

- `reviews/`
- `learning/`
- `approved/`
- `published/`

評価し、戻し、公開する場所。

### 運用オプション層

- `actions/`
- `community/`
- `campaigns/`
- `metrics/`
- `queue/`

必須コアではありません。`queue/` は legacy projection です。

## 推奨フロー

1. `story/seeds/` で発散する
2. `story/promises.md`, `bible/world.md`, `bible/characters.md`, `bible/rules.md` で収束する
3. `arcs/series-overview.md` で長期変化を切る
4. `arcs/arc-01.md` で今の変化線を scoped にする
5. `packets/exploring/` か `packets/scoped/` で packet を作る
6. `packets/frozen/` に上げる
7. `scenes/` に first episode を書ける scene 群を作る
8. `drafts/` で本文化する
9. `reviews/` で批評し、必要なら `story/design-debt.yaml` と `story/canon-patch-proposals/` に返す

## どのファイルが何を担うか

- `story/promises.md`
  作品の約束。何を絶対に壊してはいけないか
- `bible/world.md`
  物語の因果に効く世界制約
- `bible/characters.md`
  主要キャラのドラマ圧
- `bible/rules.md`
  文体、視点、禁則
- `arcs/series-overview.md`
  長期変化の見取り図
- `arcs/arc-01.md`
  今の Arc の骨
- `packets/*.yaml`
  数話単位の実装仕様
- `scenes/*.md`
  scene card。本文ではない
- `drafts/*.md`
  本文
- `reviews/*.md`
  typed review
- `story/canon-patch-proposals/*.yaml`
  Canon 修正案

## Packet の使い分け

- `packets/exploring/`
  まだ論点が荒い段階。entry / exit や disclose / withhold の仮説を立てる
- `packets/scoped/`
  役割、入口、出口、依存関係が見えている段階
- `packets/frozen/`
  scene 担当に渡しても「この話は何のためにあるのか」と聞かれない段階

原則:

- Arc は `scoped` で Packet 開始
- Packet は `frozen` で Scene 開始

## 執筆開始ライン

少なくともここまで揃っていれば本文を書き始めてよいです。

- `CLAUDE.md` がある
- `story/promises.md` に作品約束がある
- `bible/world.md` に現行 Arc に必要な制約がある
- `bible/characters.md` に主要キャラのドラマ情報がある
- `bible/rules.md` に文体ルールがある
- `arcs/arc-01.md` がある
- `packets/frozen/` に 1 本ある
- `scenes/` にその Packet の scene 群がある
- 今書く packet / first episode を止める blocker が `story/open-questions.md` に残っていない

注意:
template を配った瞬間には、ここまでは埋まっていません。starter を埋めて初めて開始ラインに乗ります。

## 完了ライン

- `drafts/` に公開対象の draft がある
- `reviews/` に typed review がある
- 必要な Canon 修正が `bible/` に反映されている
- 未反映のものが `story/canon-patch-proposals/` にある
- 長期課題が `story/design-debt.yaml` にある
- `approved/` に承認済み成果物がある
- `published/` に公開物がある

## 具体的な入り方

### ChatGPT / Claude Web で進める

1. `prompts/common-preamble.md` を先頭に付ける
2. `prompts/promises.md` から順番に使う
3. 出力を対象ファイルへそのまま貼る
4. `packet-scoped.md` で packet を作り、`packet-freeze-check.md` で frozen 判定をかける
5. `scene-batch.md` で first episode の scene 群を作る

### Codex / Claude Code で進める

1. この `README.md` と `CLAUDE.md` を読ませる
2. 対象 starter を直接埋めさせる
3. 必要なら `prompts/` を素材として流用する
4. `.claude/skills/` が使える環境では `/pitch`, `/draft`, `/critic`, `/review-meeting` を補助に使う

## 関連ファイル

- 制作契約: `CLAUDE.md`
- prompt 集: `prompts/README.md`
- review 運用: `reviews/README.md`
