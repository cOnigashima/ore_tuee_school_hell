# craft methodology — Story OS 運用版

> **status**: working / translated
> **source**: `learning/craft/2026-04-09-craft-methodology-source.md`（原典、改変禁止）
> **role**: 原典の知見を Story OS の語彙（seed / promises / bible / arc / packet / scene / draft / typed review / canon patch / learning）に翻訳し、この repo の制作フローに接続する。原典の主張と衝突したときは、`story-os-boundaries.md` と `CLAUDE.md` を正本とする。

本ファイルは参照ドキュメントであり、作品の正本ではない。学習ログ（`learning/`）として運用し、反証が出れば上書きしてよい。

---

## 1. 設計思想の Story OS 翻訳

原典は創作を「閃き」ではなく「反復可能な作業」とみなす。Story OS 用語に置き換えると次のようになる。

- 「最小限の設計→書く→矛盾を直す」= `seed → promises + bible + arcs → packets → scenes → drafts → typed review → (reverse flow or canon patch proposal)` を小さく何周も回すこと。
- 「スコープ暴走」の4因子（人物数／視点数／時間軸／ルール例外数）は、`story/design-debt.yaml` の監視対象として明示する。暴走は packet で発見されやすいので、`packets/frozen/` に入れる前に4因子の数を数える。
- 「後工程の確保」= drafting より typed review と approval review に時間を残す。`learning/` は後工程で拾ったパターンを蓄積する場所。
- If-Then 計画（Implementation Intention）は、プロジェクト横断の運用メモとして `actions/` に置くか、ここで「標準 If-Then」を提示する（第8節）。

## 2. プロット / 起承転結 / Scene-Sequel を OS に接続する

原典の「起承転結の入れ子」は、Story OS では次の粒度に対応する。

- series-overview（作品全体の起承転結）
- arc（`arcs/arc-01.md` の変化線）
- packet（`章束` 単位の起承転結）
- scene（scene card 単位の局所衝突）

Scene-Sequel は scene card と draft の両方に効く。scene card の必須項目 `purpose / desire / obstacle / turn / reveal / emotional_turn` は、Scene 側の Goal/Conflict/Disaster にほぼ対応する。Sequel（Reaction/Dilemma/Decision）は、scene card に現在明示欄がないので、以下の拡張を推奨する。

- scene card に `sequel:` ブロックを追加し、`reaction / dilemma / decision` の3項を埋める
- 既存 `emotional_turn` は Sequel の reaction と重なるが、decision は別物として必ず書く

この拡張は canon ではなく方法論レイヤなので、`bible/` ではなく本ファイルと `packets/templates/` で提示する。

## 3. 視点と語り口を「知識状態の単調性」と接続する

原典の「視点人物が当然気づくはずを気づかない問題」は、`.claude/rules/drafter-preflight.md` の 知識状態台帳 と直結する。したがって、

- 視点設計は packet の `purpose / disclose / withhold` に属する意思決定とみなす。
- draft 執筆時は drafter-preflight を必ず通す。視点人物 = focal character。
- フェアプレイ（嘘を書かない／省略はOK）は、台帳の `予感レイヤ` と「正式な既知」の区別として運用する。叙述の操作は「嘘」ではなく「情報の順序」で行う。

## 4. 描写・対話・伏線

- 描写の原則「情報価値 ÷ 文字量」は、typed review のチェック項目に加える。reviewer は「読者が飛ばす部分」を指摘してよい。
- 対話は「①情報伝達 ②関係性の変化 ③欲望の衝突」のいずれかを担うことを scene card の `purpose` と紐づけて確認する。どれも担っていない台詞は reverse flow で scene card に戻す。
- 伏線は「台帳化」する。Story OS では `story/seeds/` に seed の形で置くのが初期段階、packet 以降は後述の `story/foreshadowing-ledger.md`（第6節で提案）で管理する。

## 5. 世界観・ルール設計を bible に接続する

原典の「できないこと・弱点・制約から決める」は、`bible/world.md` と `bible/rules.md` の書き方に直接反映できる。推奨スタイル:

- `bible/world.md` に `constraints` セクションを用意し、「何ができないか」「破る代償」「例外（最大1つ）」を書く。
- 「例外が増えると理解負荷が上がる」は design-debt の監視対象。例外が2つ以上になったら `story/design-debt.yaml` に記録する。
- 文化・地理は「価値観の衝突」「移動・通信・補給の遅延」という因果装置に変換してから bible に載せる。羅列は入れない。

## 6. キャラ・テーマ

- キャラ設計は「Want / Need / Misbelief / Decision」を主要4点として `bible/characters.md` に反映する。性格は形容詞ではなく「選好」と「ストレス時の破綻の仕方」で書く。
- テーマは「問い」として promises に置き、「仮説→反証→暫定結論」の往復を arc の変化線として設計する。テーマを説教にしないために、必ず「ジレンマ（どちらを選んでも傷が残る）」を scene 単位で作る。
- 役割語は金水の警告を踏まえ、`bible/rules.md` の文体指針に「役割語テンプレの貼り付けを禁じ、価値観・優先順位・禁句から台詞を設計する」と明記する（第9節で指針を提案）。

## 7. 評価ルーブリック（Story OS 運用版）

原典の9観点を Story OS の成果物と紐づけ、typed review と approval review で参照できる形に整える。

| 観点 | Story OS での測定点 | 上流差し戻し先（reverse flow） |
|---|---|---|
| 完成度 | 主要因果が途切れず、結末が必然 | `arcs/`（開示順・反転点）／`story/promises.md` |
| 読者体験 | 冒頭 3,000 字の問い提示、章ごとの山場 | `packets/`（hook / pacing） |
| 独創性 | 既存型との差分、視点の新しさ | `story/promises.md`／`story/seeds/` |
| 整合性 | 視点・情報・世界ルールの一貫性、フェア性 | `scenes/` or `drafts/`（知識状態台帳）／`bible/` |
| 感情的インパクト | 感情ピークの回数、Sequel の配分 | `scenes/`／`drafts/` |
| キャラ強度 | 決断シーン数、関係変化イベント数 | `bible/characters.md` |
| 世界観強度 | ルール例外数、ご都合解決の発生数 | `bible/world.md`／`bible/rules.md` |
| 文章技術 | 冗長箇所、台詞の目的不在数 | `drafts/` |
| 推敲耐性 | バージョン数、reverse flow の到達率 | `learning/`／`reviews/` |

運用ルール:

- typed review は「最下位の観点（ボトルネック）」を1つ特定し、reverse flow でどこに返すかを明示する。
- 長生きする構造問題は `story/design-debt.yaml` に、未確定の設定変更は `story/canon-patch-proposals/` に落とす。

## 8. 段階別チェックリスト（Story OS 成果物マッピング）

### 企画段階（seed → promises → bible 最小セット）

- [ ] 1行ログライン（主人公＋目的＋障害＋賭け）を `story/promises.md` に書く
- [ ] 読者体験の約束（ジャンル／後味／驚きの種類）を `story/promises.md` に書く
- [ ] 主題の問い（倫理ジレンマを含む）を `story/promises.md` に書く
- [ ] 主要キャラの Want / Need を `bible/characters.md` に書く
- [ ] 世界のルール（できないこと・代償）を `bible/world.md` に3条＋例外1条まで
- [ ] 主要転換点（始動／反転／最終決断）を `arcs/arc-01.md` に3〜5点で置く

### 執筆中（packet → scene → draft）

- [ ] 標準 If-Then（例: 「朝7時なら30分書く」）を `actions/` もしくは個人メモに明記
- [ ] 各 packet が `frozen` の条件（`purpose / episode_roles / end_hooks / disclose / withhold / guardrails`）を満たす
- [ ] scene card に Scene-Sequel 拡張（`sequel.reaction / dilemma / decision`）を埋める
- [ ] 伏線台帳（`story/foreshadowing-ledger.md` を雛形から作成）を更新している
- [ ] drafter-preflight の3項目（因果一段落 / 知識状態台帳 / 合理化語彙 self-check）を必ず埋める
- [ ] 冒頭 3,000 字で「問い」が読者に提示されている

### 推敲・編集（typed review → reverse flow → approval review）

- [ ] 冷却期間（最低1日）を置いてから reviewer を回す
- [ ] 音読／媒体変更の推敲を少なくとも1回行う
- [ ] typed review でボトルネック観点を1つ特定し、reverse flow 先を書く
- [ ] フェア性点検（嘘 / 視点逸脱 / 後出し）を行い、不公平候補を列挙する
- [ ] 第三者フィードバック（具体質問付き）を `reviews/` に残す

### 公開準備（approved → published）

- [ ] あらすじ・見どころ文（約束の明文化）を `approved/` に置く
- [ ] 誤字脱字＋固有名詞＋時系列の最終校正を完了する
- [ ] 続編余地（"残す謎" 3つ）を `story/open-questions.md` に記録する
- [ ] `.claude/rules/kakuyomu-policy.md` の AI 利用タグ／投稿頻度ルールを満たす

## 9. 役割語と文体指針の補強提案

`bible/rules.md` の文体指針欄は現在 `未決定` だが、craft methodology を踏まえ次の標準文言を draft として提示する（採用は作品固有の判断）:

- 役割語は「便利さ」と「ステレオタイプ再生産」の二面性を持つことを前提にする。
- 台詞の個別化は、①価値観 ②優先順位 ③禁句の3点から行う。語尾テンプレの貼り付けで個性を作らない。
- 一人称／敬称／語尾の方針は `bible/characters.md` に人物ごとに書き、`bible/rules.md` では全体方針のみ記す。

## 10. 12週間プランの Story OS マッピング

| 週 | 原典プラン | Story OS 成果物 |
|---|---|---|
| 1 | 企画シート＋テーマの問い＋キャラ2〜4人＋ルール3条 | `story/promises.md`、`bible/characters.md`、`bible/world.md` 最小セット |
| 2 | 主要転換点＋章割り＋伏線台帳雛形 | `arcs/arc-01.md` の scoped 化、`packets/frozen/` の1本目、`story/foreshadowing-ledger.md` 作成 |
| 3-7 | 下書き完走 | `scenes/` と `drafts/` を週次で更新、drafter-preflight を毎回通す |
| 8 | 冷却＋通読メモ | `reviews/` に通読メモ、`learning/` に気づき |
| 9-10 | 構造改稿 | `packets/` と `arcs/` への reverse flow、`story/canon-patch-proposals/` 投入 |
| 11 | 文章推敲 | `drafts/` の文体パス、typed review を文章観点で回す |
| 12 | 第三者＋公開準備 | `approved/` への整形、`published/` への昇格 |

## 11. 既知の緊張と未決定

- scene card に Sequel 欄を追加するかは作品ごとに決める。本ファイルは拡張を推奨するだけで、canon ではない。
- 評価ルーブリックの「定量の例」は未検証。実作品で測ってから `learning/` に測定記録を残すこと。
- 原典の「3人称多元」言及は drafter-preflight と整合するが、視点切替の具体運用は作品ごとに decide する。

## 12. 参照

- 原典: `learning/craft/2026-04-09-craft-methodology-source.md`
- 制作フロー図: `learning/craft/creation-flow.md`
- drafter-preflight: `.claude/rules/drafter-preflight.md`
- story-os-boundaries: `.claude/rules/story-os-boundaries.md`
- kakuyomu-policy: `.claude/rules/kakuyomu-policy.md`
- 運用ルール: `.claude/rules/craft-methodology.md`
- 雛形テンプレ: `story/templates/`、`bible/templates/`、`packets/templates/`、`scenes/templates/`、`reviews/templates/`
