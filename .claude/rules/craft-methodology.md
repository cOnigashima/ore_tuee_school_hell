# craft methodology rule

> **role**: craft 方法論（原典: `learning/craft/2026-04-09-craft-methodology-source.md`）の運用ルール。日常の Story OS 作業でこのルールを守る。
> **source of truth**: 本ファイルは運用ルール。方法論の出典と詳細は `learning/craft/craft-methodology-story-os.md` を参照する。
> **境界**: `story-os-boundaries.md` と矛盾する場合は `story-os-boundaries.md` を優先する。

## 基本原則

1. 創作は「閃き」ではなく `seed → promises/bible/arc → packet → scene → draft → typed review → reverse flow` の反復として扱う。
2. 「最小限の設計 → 書く → 矛盾を直す」を小さく回す。設計を"全部決め切ってから書く"ことを禁じる。
3. スコープ暴走は 4 因子（登場人物数／視点数／時間軸／世界ルールの例外数）で検知する。閾値を超えたら `story/design-debt.yaml` に記録する。
4. 締切直前の時間は "書く" ではなく "構造改稿と文章推敲" に残す。drafting を締切ぎりぎりまで続けない。

## packet / scene / draft 段階のルール

### packet を frozen にするとき

- `packets/templates/packet-frozen-checklist.md` を通す。
- この packet で主に改善を狙う craft 観点（9 観点から 1〜2 つ）を宣言する。
- スコープ 4 因子を前 packet と比較する。暴走なら frozen を保留し、`story/design-debt.yaml` に記録する。

### scene card を書くとき

- Scene 側（Goal / Conflict / Disaster）と Sequel 側（Reaction / Dilemma / Decision）の両方を埋める。
- 埋められない場合は packet の `purpose / disclose / withhold` に戻って上流と相談する。
- 拡張版カードは `scenes/templates/scene-sequel-card.md`。

### draft を書くとき（drafter preflight との連動）

- `.claude/rules/drafter-preflight.md` の 3 項目（因果一段落／知識状態台帳／合理化語彙 self-check）を必ず通す。
- 視点設計＝「嘘は不可、省略は可」。情報操作は「順序」で行い、「嘘」で行わない。
- 冒頭 3,000 字の中に読者への「問い」を最低 1 つ提示する。提示がなければ draft を差し戻す。
- 対話は「情報伝達／関係変化／欲望衝突」のいずれかを必ず担う。担わない台詞は reverse flow で scene card に戻す。

## typed review のルール

- `reviews/templates/typed-review.md` を使う。
- 9 観点のうち、スコア未計測のものは `-` と書く（空欄禁止）。
- 最下位の観点を 1 つ特定し、reverse flow 先を必ず書く。
- 「良かった」「面白かった」だけで終わる感想型 review は typed review とみなさない。

## 伏線の管理

- 伏線は `story/foreshadowing-ledger.md` で管理する（雛形 `story/templates/foreshadowing-ledger.md`）。
- 置いた瞬間に ID を振る。後から遡って振らない。
- 未回収（open + queued）が 4 件以上になったら、packet 進行を停止して reverse flow する。

## 推敲のルール

- 構造改稿と文章推敲は別工程として実行する。同じ版で混ぜない。
- 冷却期間は最低 1 日。冷却なしで推敲を始めない。
- 音読または媒体変更（印刷、画面を変える等）による推敲を最低 1 回行う。

## 役割語・文体

- 役割語テンプレの貼り付けでキャラの声を作ることを禁じる。
- 台詞の個別化は「価値観／優先順位／禁句」から行う。これは `bible/characters.md` の当該人物欄に明記する。
- `bible/rules.md` の文体指針が `未決定` の場合、作品立ち上げ時に必ず最低限の方針（視点・時制・文体・地の文温度）を埋める。

## スケジュール

- 標準プランは 12 週（`learning/craft/craft-methodology-story-os.md` 第 10 節）。
- 日次ノルマは「文字数」より「座る／開始する」条件固定（If-Then）を優先する。

## カクヨム投稿との接続

- 最終的な公開判断は `.claude/rules/kakuyomu-policy.md` を通す。
- AI 本文利用タグの付与、投稿頻度制限、禁止コンテンツのチェックは craft methodology の「公開準備」段階と同時に行う。

## このルールの更新

- 実作品で反証が出たら `learning/` に反証ログを残し、本ファイルを更新する。
- 方法論と canon の衝突が発生した場合、canon（作品の正本）を優先する。方法論を canon に昇格させるときは `story/canon-patch-proposals/` を経由する。
