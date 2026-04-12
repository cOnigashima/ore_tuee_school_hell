# /draft

frozen packet と scene 群から draft を起こす。

## 入力

- `packets/frozen/*.yaml`
- `scenes/drafted/`, `scenes/slotted/`, `scenes/merged/`
- 必要に応じて `story/promises.md`, `bible/`, `approved/`, `published/`

## 手順

1. 対象の frozen packet を読み、`purpose / episode_roles / disclose / withhold / guardrails` を確認する
2. 対象 episode の scene 群を読み、scene の loss / gain / emotional turn を把握する
3. `bible/rules.md` と直近の `approved/`, `published/` を読み、文体と handoff を合わせる
4. `drafts/` に episode 単位の draft を書く
5. draft から packet / scene へのトレースが残るようにする

## 執筆ルール

- `bible/rules.md` の文体・禁則に従う
- `withhold` にある情報は前倒しで明かさない
- 冒頭は `hook_in` を受け、末尾は `cliffhanger` を返す
- scene 群の役割が消えないように、各 scene の turn を本文に反映する

## 出力フォーマット

```markdown
# [タイトル]

[本文]

---

## メタ情報

- packet: packet-001-<slug>
- episode: ep01
- source scenes:
  - scenes/drafted/scene-ep01-01-<slug>.md
  - scenes/drafted/scene-ep01-02-<slug>.md
- draft status: drafted
- unresolved notes:
  - 
```

## 保存先

`drafts/draft_epXX_YYYYMMDD_HHMMSS.md`
