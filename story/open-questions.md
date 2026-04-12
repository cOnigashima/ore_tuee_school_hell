# Open Questions

- 未決定は放置せず、ここに残す
- 空欄は禁止。決めきれない場合も `未決定` と書く
- `blocker` は今書く packet / first episode を止める論点だけにする

## 決定ログ（過去のクロージング）

### decided-001: 「第二保健室」の廃止

- 2026-04-09 決定
- 判定: 破棄
- 理由: 象徴ではあるが機能が弱く、そこにしか起きない出来事がない。芯を立てるために捨てる
- 出典: `story/seeds/2026-04-09-moto-oretuee-gakuen.md`

### decided-002: タイトルの確定

- 2026-04-09 決定
- 採用: 『元オレつえー学園 ──かつて最強だった俺たちは、かませ犬として働きます』
- 理由: 長いが企画がそのまま入っていて、軽薄さと哀愁が両立する
- 代案（却下）: 「かませ犬として働く」語尾は乾きすぎで却下

### decided-003: 作品の芯

- 2026-04-09 決定
- 採用: 「俺つえー」を成立させるために大量消費されてきた"その他大勢"を、労働として可視化する話
- 却下: 「俺つえーを笑う話」（薄くなるため）

### decided-004: 学園はベースキャンプ構造

- 2026-04-09 決定
- 採用: 学園は矯正・訓練の拠点。本当の舞台は毎回の実習世界への派遣
- 理由: 「火花をやらされる」「女神役をやらされる」という配役の筋を通すために、少しだけ自然主義を捨てる必要がある

### decided-005: クラスは不良ではなく症状で分ける

- 2026-04-09 決定
- 採用: A 実務適応 / B 再発監視 / C 役割喪失 / 特別矯正組（世界観汚染）
- 却下: 学園マンガ的な「不良クラス」設定

### decided-006: 会話は和解で閉じない

- 2026-04-09 決定
- 採用: 本音に触れそうになったら「くそ」で切る。苦労話は反省ではなく禁断症状
- 判定: `bible/rules.md` の canon として固定

### decided-007: 処罰の設計基準

- 2026-04-09 決定
- 採用: 「その処罰は、その人物が昔に奪っていたものの側に落ちているか」を canon の判定軸とする
- 出典: `bible/world.md` の処罰体系

## Active Questions

### oq-001: 発散：処罰カタログ 20 個

- question: 背景勤務 / 演出勤務 / 神話勤務 / 使い捨て勤務の 4 カテゴリで、処罰カタログを 20 個まで出す
- why_pending: 現在 4 カテゴリ 20 件相当は出ているが、設計基準（奪っていたものの側に落ちているか）で篩にかけ直す必要がある
- impact: 第一話の配役決定に直結
- decide_by: packet-001 frozen の前
- blocker: blocker
- owner: plotter
- latest_note: 2026-04-09 seed で初期案あり

### oq-002: 発散：実習世界 5 個への絞り込み

- question: 実習世界候補 12 個から、第一クールで使う 5 個を選ぶ
- why_pending: 現行候補は網羅リストで、相性のよい組み合わせを選んでいない
- impact: 第一話と第二話の現場がここから出る
- decide_by: packet-001 frozen の前
- blocker: blocker
- owner: plotter
- latest_note: 掛け合わせ例は seed に 4 本ある（追放覚醒 × 元パーティ幹部 × 冒険者ギルド など）

### oq-003: 発散：無双エンジン 20 個と食われる役 20 個

- question: seed にある 15 個ずつを 20 個まで発散し、相性のいい組み合わせを 5 本選ぶ
- why_pending: 主人公類型と第一話の配役を決めるために必要
- impact: 主人公の元・無双エンジンが決まらないと char-001 が provisional のまま
- decide_by: packet-001 frozen の前
- blocker: blocker
- owner: plotter
- latest_note: seed に 15 個 + 15 個の初期リストあり

### oq-004: 主人公の類型決定

- question: char-001 の元・無双エンジンを 1 つ選ぶ
- why_pending: oq-003 の成果物を待つ
- impact: 主人公の禁断症状の具体形が決まらない
- decide_by: oq-003 直後
- blocker: blocker
- owner: plotter
- latest_note: B 組（再発監視）想定だけは固定

### oq-005: スコープ 4 因子の上限設定

- question: 登場人物数／視点数／時間軸／世界ルール例外数の上限を決める
- why_pending: 派遣先ごとに視点を切り替えたくなる誘惑が強く、暴走リスクが高い
- impact: packet 設計の安全弁
- decide_by: packet-001 frozen の前
- blocker: non-blocker
- owner: plotter
- latest_note: 現時点では三人称一元・POV 固定を暫定採用（`bible/rules.md`）

### oq-006: 派遣先との「現地主人公」衝突ルール

- question: 配役先の現地主人公を潰すのは禁忌として canon 化するか
- why_pending: 主人公の moral_line として仮置きしたが、canon には未昇格
- impact: 実習世界ごとの葛藤構造に効く
- decide_by: packet-002 の前
- blocker: non-blocker
- owner: plotter
- latest_note: 主人公の moral_line で暫定採用

### oq-007: 恋愛ラインの有無とペア

- question: 第一クールで恋愛ラインを走らせるか、どのペアで走らせるか
- why_pending: 原則（役から降りた後の恋愛）は決まったが、実装は未定
- impact: char-001 / char-002 の関係設計に効く
- decide_by: arc-01 scoped の前
- blocker: non-blocker
- owner: plotter
- latest_note: 勤務中の接触は原則制限（`bible/characters.md`）

### oq-008: 世界ルール例外の有無

- question: 世界ルールの例外を 1 つ作るか、例外なしで通すか
- why_pending: craft methodology は例外最大 1 つを推奨。設計自由度と理解負荷のトレードオフ
- impact: 世界観強度と design-debt 監視に効く
- decide_by: packet-001 frozen の前
- blocker: non-blocker
- owner: plotter
- latest_note: 現時点は「例外なし」で暫定運用
