# /retro-meeting

Agent Team を起動して、週次の振り返りと戦略調整を行う。

## 概要

週1回実行する戦略会議。3人のチームメイトが今週のデータを分析し、来週の方針を決める。

## チーム構成

| Teammate | 役割 |
|----------|------|
| analyst | メトリクスを分析して傾向を出す |
| strategist | 分析結果から来週の方針を提案 |
| experimenter | 試してみるべき実験を1つ提案 |

## 実行手順

1. analyst が `metrics/publish_log.csv` を読み、今週の反応を分析
2. strategist が分析結果を受けて来週の方針を提案
3. experimenter が試してみるべき実験を1つ提案
4. 3人で議論し、最終的な方針を決定

## 出力

`metrics/retro_YYYYMMDD.md` に以下を保存:

```markdown
# Retro Meeting YYYY-MM-DD

## 今週の分析（by analyst）

[analyst の分析結果]

## 来週の戦略（by strategist）

[strategist の提案]

## 今週の実験（by experimenter）

[experimenter の提案]

## 決定事項

### 来週の重点施策
1. ...
2. ...

### スコアリング重み調整
- 変更なし / [変更内容]

### 実験採用
- 実施する / 見送る
- [理由]

## 議論メモ

[議論の要点]
```

## 起動コマンド例

```
週次振り返りのため Agent Team を作って。
3人にして:
- analyst: metrics/publish_log.csv を分析して傾向を出す
- strategist: 分析結果から来週の方針を提案
- experimenter: 試してみるべき実験を1つ提案

議論して、最終方針を metrics/retro_YYYYMMDD.md にまとめて。
```

## メトリクスファイル

### publish_log.csv
```csv
date,episode_id,title,pv,follows,stars,comments,score
2024-01-01,ep001,第1話,1234,12,5,3,85
```

### experiment_log.csv
```csv
date,experiment_id,hypothesis,group,metric,value,conclusion
2024-01-01,exp001,冒頭を短くするとPVが上がる,A,pv,1000,
2024-01-01,exp001,冒頭を短くするとPVが上がる,B,pv,1200,成功
```
