# 伏線台帳（foreshadowing ledger）

> **template**: コピーして `story/foreshadowing-ledger.md` として運用する（作品正本）。
> **source**: `learning/craft/craft-methodology-story-os.md` 第4節
> **rule**: 伏線は必ず ID を振り、置く／回収／代替回収の 3 列を常に書く。未回収の伏線が3件を超えたら `story/design-debt.yaml` に警告を立てる。

## 運用ルール

- 置いた瞬間に必ず ID を振る（F-001, F-002, ...）。
- 代替回収案は「その伏線を回収できないまま終わる場合、何を差し替えるか」。
- ステータスは `open / queued / resolved / dropped` のいずれか。
- `dropped` にしたものは必ず typed review に「なぜ落としたか」を書く。

## 台帳

| 伏線ID | 置いた場所（packet/scene） | 何として見せたか | 回収予定（packet/scene） | 回収条件 | 代替回収案 | status |
|---|---|---|---|---|---|---|
| F-001 | | | | | | open |
| F-002 | | | | | | open |

## 未回収カウント

- open:
- queued:
- resolved:
- dropped:
- 警告閾値: open + queued > 3 → design-debt 化を検討
