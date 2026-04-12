# 元オレつえー学園 ──かつて最強だった俺たちは、かませ犬として働きます

この作品 repo の制作OS契約。別セッションの ChatGPT / Claude が入っても、
`promises -> arc -> packet -> scene -> draft -> review -> canon reverse flow`
の接続が切れないようにする。

## 作品概要

- title: 元オレつえー学園 ──かつて最強だった俺たちは、かませ犬として働きます
- slug: moto-oretuee-gakuen
- 一行要約: かつて"俺つえー"をやっていた元・最強主人公たちが、矯正学園に再配属され、他人の物語を成立させるためのかませ犬・背景役・演出素材として労働させられる、笑いと哀愁の更生未満学園劇。
- 芯（一文）: 俺つえーを成立させるために大量消費されてきた"その他大勢"を、労働として可視化する話
- 現在のフォーカス Arc: `arc-01`
- 現在のフォーカス Packet: `packet-001-first-assignment`（frozen）
- 現在のフェーズ: バイブル v1.0 + パケット 000–003 frozen 完了。次は packet-001 の scene card 作成 → draft

## 制作優先順位

1. `story/promises.md` の約束を壊さない
2. 次の 1〜2 packet の因果に効くものだけ先に固める
3. 空欄は禁止。未確定は必ず `未決定` と書く
4. Review は感想で終わらせず、必要なら上流へ戻す
5. 「最小限の設計 → 書く → 矛盾を直す」を回す。全部決め切ってから書くことを禁じる（詳細: `.claude/rules/craft-methodology.md`）
6. 締切直前の時間は drafting ではなく構造改稿と文章推敲に残す

## 文体指針

- 視点: 三人称一元（scene ごとに focal character を固定）
- 時制: 過去形基調
- 文体: 乾いていて少し皮肉。笑えるのに胸が痛い温度
- 一文の長さ: 短めを基調、哀愁では時々長めに
- 地の文の温度: 薄め〜中。内面は身体反応で出す
- 会話の核: 和解で閉じない。本音に触れると「くそ」で切る（1 scene 1 回を上限）
- 詳細: `bible/rules.md`

## 禁則

- 絶対NG:
  - 役割語テンプレの貼り付けで声を作ること
  - 元主人公をただの愚か者として嘲笑うだけの書き方
  - 和解・反省・改心で会話を閉じること
  - 処罰を「奪っていたものの側」以外の因果で配ること
  - 俺つえー批判を説教として書くこと
- 避ける: 過剰な情景描写、説明セリフの連発、恋愛を"救い"として描く、「くそ」の乱発

## 執筆開始ライン

- `CLAUDE.md` が埋まっている
- `story/promises.md` に作品約束がある（1行ログライン／読者体験の約束／主題の問い＝craft methodology の企画 3 点）
- `bible/world.md` に現行 Arc に必要な制約がある（できないこと・代償・例外 1 つまで）
- `bible/characters.md` に主要キャラのドラマ情報がある（Want / Need / Misbelief / Decision）
- `bible/rules.md` に文体ルールがある（視点・時制・文体・地の文温度のいずれも `未決定` ではない）
- `arcs/arc-01.md` がある（主要転換点 3〜5 点が書かれている）
- `packets/frozen/` に 1 本ある（`packets/templates/packet-frozen-checklist.md` を通っている）
- `scenes/` にその Packet の scene 群がある（Scene-Sequel 両方埋めた拡張カードを推奨）
- `story/foreshadowing-ledger.md` が作成されている（open + queued が 4 件未満）
- 今書く packet / first episode を止める blocker が `story/open-questions.md` に残っていない
- スコープ 4 因子（人物数／視点数／時間軸／ルール例外数）が暴走していない

## 参照ファイル

- 運用ガイド: `README.md`
- 作品約束: `story/promises.md`
- 未解決論点: `story/open-questions.md`
- 設計負債: `story/design-debt.yaml`
- canon patch proposal: `story/canon-patch-proposals/`
- 種 inbox: `story/seeds/`
- 世界観: `bible/world.md`
- キャラクター: `bible/characters.md`
- 文体・禁則: `bible/rules.md`
- シリーズバイブル 1枚版 v1.0: `bible/series-bible-v1.md`
- 制度バイブル 1枚版 v1.0: `bible/system-bible-v1.md`
- キャラフルシート v1.0: `bible/character-sheets-v1.md`
- 7世界レギュラー顔フルシート v1.0: `bible/world-regulars-v1.md`
- 会話バイブル v1.0: `bible/dialogue-bible-v1.md`
- 100話章立て一覧: `arcs/100ep-chapter-list.md`
- シリーズ概観: `arcs/series-overview.md`
- 現行 Arc: `arcs/arc-01.md`
- 次 Arc: `arcs/arc-02.md`
- 最終 Arc: `arcs/arc-03.md`
- 30話チェックポイント: `arcs/arc-01-checkpoint-ep30.md`
- 企画書: `企画書v0.9.md`
- 制作ロードマップ: `actions/roadmap.md`
- 設計監査: `actions/design-audit.md`
- 章束: `packets/`
- シーン: `scenes/`
- 本文: `drafts/`
- レビュー: `reviews/`
- 学習ログ: `learning/`
- 公開準備: `approved/`
- 公開済み: `published/`
- ChatGPT prompt 集: `prompts/`
- 参考ノート: `community/`
- アクションパケット: `actions/`
- craft 方法論原典: `learning/craft/2026-04-09-craft-methodology-source.md`
- craft 方法論 Story OS 運用版: `learning/craft/craft-methodology-story-os.md`
- 制作フロー図: `learning/craft/creation-flow.md`
- craft 運用ルール: `.claude/rules/craft-methodology.md`
- 伏線台帳（雛形）: `story/templates/foreshadowing-ledger.md`
- 雛形: `story/templates/`, `bible/templates/`, `packets/templates/`, `scenes/templates/`, `reviews/templates/`
- `queue/` は legacy projection。実行キューの正本ではない

## Story OS

- `seed = story/seeds`
- `macro = story/promises + bible + arcs`
- `meso = packets`
- `micro = scenes + drafts + episodes`
- `meta = reviews + learning + design debt + canon patch proposals`
- `release = approved + published`

### 制作フロー

1. `story/seeds/` で発散する（craft 7step の「企画」）
2. `story/promises.md`, `bible/` で収束する（「設計」: キャラ／世界／テーマの最小セット）
3. `arcs/` で変化線に変換する（「アウトライン」: 主要転換点と結末）
4. `packets/` で実装可能単位に分解する
5. `scenes/` で局所衝突に落とす（Scene-Sequel の両方を埋める）
6. `drafts/` で本文にする（「下書き」: まず最後まで到達）
7. `reviews/` で批評する（「構造改稿」→「文章推敲」を別工程で回す）
8. 必要なら `story/design-debt.yaml` と `story/canon-patch-proposals/` に返す

reverse flow は 2 本を常に開ける: 構造改稿 → `arcs/` / `packets/`、文章推敲 → `scenes/` / `drafts/`。図は `learning/craft/creation-flow.md`。

### Arc / Packet / Scene の基準

- Arc は `scoped` で Packet 開始:
  始点と終点、中核対立、主反転、読者フック、packet-001 / packet-002 の役割が見えていること
- Packet は `frozen` で Scene 開始:
  `purpose / episode_roles / end_hooks / disclose / withhold / guardrails` が埋まり、scene 担当に渡しても戦略質問が返らないこと
- Scene は draft-ready:
  `packet_id`, `target_episode`, `purpose`, `desire`, `obstacle`, `turn`, `reveal`, `emotional_turn`, `canon delta` があること

### ユビキタス言語

- 正式語は `章束`、実装語は `packet`
- `作品の核` の正式語は `作品約束`
- `review` を単独で使わない。`typed review` と `approval review` を分ける
- `backlog/` は legacy 資産。物語の入口正本は `story/seeds/`
- `Story Board`, `Loop Canvas`, `Run Ledger` は投影面であり、作品正本ではない

### Bible の役割

- `bible/world.md`, `bible/characters.md`, `bible/rules.md` は「安定設定の索引」
- 次の 1〜2 packet の意思決定に効かない情報は、無理に bible に入れない
- 差分案は bible に直接書かず、`story/canon-patch-proposals/`, `reviews/`, `story/design-debt.yaml` に置く
- bible への昇格は approval を通した canon patch で行う

### Reverse Flow

- prose 問題 -> `scenes/` または `drafts/`
- hook / pacing -> `packets/`
- 動機 / 関係性 -> `bible/characters.md`
- 開示順 / 反転点 -> `arcs/`
- 作品約束のズレ -> `story/promises.md`
- 長生きする構造問題 -> `story/design-debt.yaml`
- まだ確定していない設定変更 -> `story/canon-patch-proposals/`

### 評価ルーブリック（9 観点）

typed review はこの 9 観点でスコアを出し、最下位をボトルネックとして reverse flow 先を必ず明記する。詳細と雛形: `learning/craft/craft-methodology-story-os.md` 第 7 節 / `reviews/templates/typed-review.md`。

- 完成度 / 読者体験 / 独創性 / 整合性 / 感情的インパクト / キャラ強度 / 世界観強度 / 文章技術 / 推敲耐性

### 段階別チェックリスト（要約）

詳細は `learning/craft/craft-methodology-story-os.md` 第 8 節。

- 企画段階: ログライン／読者体験の約束／主題の問い／Want-Need／世界ルール 3 条＋例外 1／主要転換点 3〜5
- 執筆中: Scene-Sequel カード／伏線台帳／drafter-preflight 3 項目／冒頭 3,000 字に問い提示
- 推敲: 冷却 1 日以上／音読 1 回以上／ボトルネック観点 1 つ特定／フェア性点検
- 公開準備: あらすじ／最終校正／残す謎 3 つ／カクヨム AI タグ・投稿頻度の確認

## Story OS Docs

`factory-platform` が隣にある構成では、詳細は次を参照する。

- `../factory-platform/docs/story-os-ubiquitous-language.md`
- `../factory-platform/docs/story-os-domain-map.md`
- `../factory-platform/docs/story-os-sources-of-truth.md`
- `../factory-platform/docs/story-os-workflows.md`
- `../factory-platform/docs/story-os-implementation-map.md`
- `../factory-platform/docs/story-os-audit-checklist.md`

## Skills

- `/pitch` - seed / packet 材料を作る
- `/draft` - frozen packet と scene 群から本文を起こす
- `/critic` - typed review を作り、必要なら上流へ返す
- `/continuity` - 過去話との整合性チェック
- `/release` - 公開用に整形

## Agents

- `plotter` - promises / arc / packet 設計担当
- `drafter` - scene / draft 実装担当
- `critic` - typed review 担当
- `continuity-checker` - 連続性監視担当
