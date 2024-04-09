# プレイヤー名登録画面

## イメージ

![player-name-filling-form](/Users/dangthuyvy/Documents/Git/tic-tac-toe-screen-doc/player-name-filling-form.png)

## 項目一覧

| No. | 項目名 | 部品種類 | 表示/更新 | 必須 | 入力制限 | デフォルト | 文字数 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | ロゴ | image | 表示 | - | - | - | - |
| 2 | 案内文 | text | 表示 | - | - | - | - |
| 3 | プレイヤー１ | text | 更新 | ◯ | - | - | 50 |
| 4 | プレイヤー２ | text | 更新 | ◯ | - | - | 50 |
| 5 | スタートボタン | button | 表示 | - | - | - | - |

## 権限制限

なし

## イベント

### 初期表示

| No. | 項目名 | 処理概要 |
| --- | --- | --- |
| 1 | ロゴ | ゲームのロゴを表示 |
| 2 | 案内文 | 下記文言を表示<br/>「Please enter player’s name.<br/>　Player 1 will go first!」 |
| 3 | プレイヤー１ | ラベル：「Player 1 (O)」<br/>　※ただし、エラーメッセージ表示時、項目名を「Player 1's name」にしてください<br/>プレースホルダーテキスト：「Please enter player 1's name」 |
| 4 | プレイヤー２ | ラベル：「Player 2 (X)」<br/>　※ただし、エラーメッセージ表示時、項目名を「Player 2's name」にしてください<br/>プレースホルダーテキスト：「Please enter player 2's name」 |
| 5 | スタートボタン | ラベル：「START GAME!」 |

### 押下イベント

| No. | 項目名 | 処理概要 |
| --- | --- | --- |
| 5 | スタートボタン | 項目一覧を基にして、入力値に対してバリデーションチェックを行う（[共通設計](https://github.com/dangthuyvy94/tic-tac-toe-screen-doc/blob/main/common-spec.md)参照）<br/>エラーがない場合、入力されたプレイヤー名をstateに保存し、「プレイ画面」へ遷移<br/>引数：入力されたプレイヤー名 |