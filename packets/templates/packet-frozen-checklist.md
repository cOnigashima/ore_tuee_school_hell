# packet frozen 前チェックリスト

> **template**: `packets/frozen/` に入れる直前に通すチェック。
> **source**: `learning/craft/craft-methodology-story-os.md` 第8節 + `CLAUDE.md` 「Arc / Packet / Scene の基準」

## 既存の frozen 条件

- [ ] `purpose` が埋まっている
- [ ] `episode_roles` が埋まっている
- [ ] `end_hooks` が埋まっている
- [ ] `disclose` が埋まっている
- [ ] `withhold` が埋まっている
- [ ] `guardrails` が埋まっている

## craft methodology による追加チェック

- [ ] この packet の「問い」（主題の一部）が 1 文で書ける
- [ ] packet 内の主要 Scene-Sequel 連鎖が、Goal→Conflict→Disaster→Reaction→Dilemma→Decision で説明できる
- [ ] 冒頭 scene に「読者の問い」を提示する仕掛けがある
- [ ] 伏線台帳（`story/foreshadowing-ledger.md`）に、この packet で置く／回収する伏線が登録されている
- [ ] 視点人物の知識状態が append-only で設計されている（drafter-preflight と整合）
- [ ] 世界ルールの例外を新しく追加していない（追加する場合は `story/design-debt.yaml` と `story/canon-patch-proposals/`）
- [ ] スコープ4因子（人物数／視点数／時間軸／ルール例外数）が前 packet と比べて暴走していない

## ボトルネック観点の事前宣言

- この packet で主に改善を狙う観点（craft 9 観点から 1〜2 つ）:
- 次の typed review で測る予定の指標:
