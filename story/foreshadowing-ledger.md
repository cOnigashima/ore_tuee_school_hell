# 伏線台帳（foreshadowing ledger）

> **正本**: このファイルが伏線管理の正本。
> **更新日**: 2026-04-12
> **source**: `learning/craft/craft-methodology-story-os.md` 第4節
> **rule**: 伏線は必ず ID を振り、置く／回収／代替回収の 3 列を常に書く。未回収の伏線が 3 件を超えたら `story/design-debt.yaml` に警告を立てる。
> **template**: `story/templates/foreshadowing-ledger.md`

## 運用ルール

- 置いた瞬間に必ず ID を振る（F-001, F-002, ...）。後から遡って振らない
- 代替回収案は「その伏線を回収できないまま終わる場合、何を差し替えるか」
- ステータスは `open / queued / resolved / dropped` のいずれか
- `dropped` にしたものは必ず typed review に「なぜ落としたか」を書く
- open + queued が 4 件以上になったら、packet 進行を停止して reverse flow する

## 台帳

| 伏線ID | 置いた場所 | 何として見せたか | 回収予定 | 回収条件 | 代替回収案 | status |
|--------|-----------|-----------------|---------|---------|-----------|--------|
| F-001 | ep08 scene card | 神代が固定敵席に向いているという嫌な空気 | arc-01 後半〜arc-02 | 固定敵席制度の正式開示時 | 神代が自ら固定席を志願する展開でも回収可 | queued |
| F-002 | ep10 scene card | 志摩「私を最初に"支える側"で見たでしょ」 | ep11〜（ローズ編） | 久瀬×志摩のペア実習内で展開 | 志摩 POV 回での内面開示でも回収可 | queued |

## 未回収カウント

- open: 0
- queued: 2
- resolved: 0
- dropped: 0
- **警告閾値**: open + queued > 3 → design-debt 化を検討
