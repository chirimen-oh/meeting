# CHIRIMEN meeting 2022.10.03

## 開催日と場所

2021 年 09 月 13 日 Zoom

## タイムスケジュール

|    時間     | 種別 | テーマ                                                                                                    | 担当者 |
| :---------: | :--: | :-------------------------------------------------------------------------------------------------------- | :----- |
| 19:30~19:35 | 議論 | 挨拶                                                                                                      | -      |
| 19:55~20:15 | 議論 | [#3](https://github.com/chirimen-oh/meeting/issues/3) +pizero tutorial の件                               | -      |
| 20:15~20:35 | 議論 | [#4](https://github.com/chirimen-oh/meeting/issues/4)                                                     | -      |
| 20:35~20:45 | 議論 | [#5](https://github.com/chirimen-oh/meeting/issues/5)                                                     | -      |
| 20:45~20:55 | 議論 | [#11](https://github.com/chirimen-oh/meeting/issues/11)                                                   | -      |
| 20:45~20:55 | 議論 | [#13](https://github.com/chirimen-oh/meeting/issues/13)                                                   | -      |
| 21:15~21:30 | 議論 | フリーテーマ :<br> スターターキットの商品化？<br>技術書典で同人誌＋組み立てキット<br>11でオフラインで物販した | -      |

## 参加者 (alphabetical order)

- @dynamis
- @kou029w
- @satakagi
- @sizuhiko
- @tadfmac
- @WhiteHawk-taka

## 議題
### [#3](https://github.com/chirimen-oh/meeting/issues/3)
- カメラ関係で、（ブラウザ版とnode版で）使い方が異なるので対応が必要
    - ユースケースも含めて検討
    -rpiネイティブカメラのgistはこちらに
        - https://gist.github.com/satakagi/1b5adc8dff8236421a593b93fa152222
    - node版とブラウザ版の互換のAPI化はできない？
    - カメラのサンプルを作るのはノード版だけで良い？
    - [ カメラのサンプルを作る #1 ](https://github.com/chirimen-oh/tutorial.chirimen.org/issues/1)
    - => サンプルを作るのみ（@satakagi）
- PiZero版の開発環境(USBOTG直結する)のコンソールが、最近のChromeで文字消えする
    - CHIRIMEN PiZeroのコンソールについて、MacOSのChromeで文字化け（文字消え）が起きるとの報告が複数来ています。
    - https://webiotmakerschallenge.slack.com/archives/C031RJPCEBW/p1644718373320289
    - => mac OS でなければ、問題が出ない
    - => mac ユーザが検証する
        - このスレッドの中に記載していますが、XTerm.jsをただ最新リリースにしても文字消えはなおらないようなのですが、さらにXTerm.jsの設定で影響が出そうなところをいろいろいじったものを置いてあります。
            - オリジナルで同じ症状が出るかどうか
                - https://chirimen.org/PiZeroWebSerialConsole/PiZeroWebSerialConsole.html
            - いろいろいじったものではどうか
                - https://chirimen.org/PiZeroWebSerialConsole/PiZeroWebSerialConsole_xtLatest.html

### [#4](https://github.com/chirimen-oh/meeting/issues/4)
- パーツリストを更新する
    - https://docs.google.com/spreadsheets/d/1iTIDHe9wqH_m_ck0TiM1JXA0OlGKVq1-VEkLnxdspz0/edit#gid=0
    - 元ネタ：https://github.com/chirimen-oh/chirimen.org/blob/master/_data/partslist.csv
    - pi zeroのリンクを追加する
    - github action を修正する
    - テンプレート: https://github.com/chirimen-oh/chirimen.org/blob/master/_includes/partslist.html
- 画像変換で、バグが有り？
    - github action 要確認
    - https://github.com/chirimen-oh/chirimen.org/commit/728a5ff60b104dff927b5294c98704707a66438d
        - この更新が反映されなかった感じでした(https://tutorial.chirimen.org/raspi/section1 の、３のbの実態配線図）
- [ チュートリアルサイトのパーツ画像変換バグ確認 #108 ](https://github.com/chirimen-oh/chirimen.org/issues/108)
    - => 画像をそのままで表示する処置で対応済み

### [#5](https://github.com/chirimen-oh/meeting/issues/5)
- 次回の Web IoT Makers Challenge までに やりたいこと
    - node-web-gpio/i2c
        - 202x.10月頃にLTSのタイミングで、最新リリース(v18.x系)したい
    - Raspberry Pi 3/4 系の Node v16.x or v18.x 系の検証を終わらせたい
    - Rasbian OS アップデート
    - ハード調達したい（切実

### [#11](https://github.com/chirimen-oh/meeting/issues/11)
- Web IoT Makers Challenge は、やらない
    - chrome 拡張機能で、ログを保存できる
- 現時点で、discussion 必要ない
- 過去ログが必要であれば、Github Discussion を使う
    - https://github.com/orgs/chirimen-oh/teams/chirimen-staff/discussions を活用する

### [#13](https://github.com/chirimen-oh/meeting/issues/13)
- 売上合計：24,500円
- 内訳

|	品名	|	オフライン会場	|	オンライン会場	|	総数	|	単価	|	売上	|
|	:----:	|	:----:	|	:----:	|	----:	|	----:	|	----:	|
|	電子＋紙セット	|	6	|	1	|	7	|	1000	|	7000	|
|	電子本	|	1	|		|	1	|	1000	|	1000	|
|	フルテストボード部品セット	|	3	|		|	3	|	2000	|	6000	|
|	フルテストボード単体	|	1	|		|	1	|	500	|	500	|
|	スターターキット	|	2	|		|	2	|	4000	|	8000	|
|	フルテストボード部品セット	|	1	|		|	1	|	2000	|	2000	|

### [Raspberry Pi OS 2022.01.28 64bit 版 setup.sh](https://github.com/chirimen-oh/chirimen/issues/118) 
- 進捗ありません。ごめんなさい。
- 落ち着いて作成します。

### Web IoT Makers Challenge
- 壁紙を変えたい
- CHIRIMEN のみにしたい。
    - 2021.01.?? に直っている
    - イメージ reelase 2021.08.21 に直っている
    - apt-get upgarde しなければ大丈夫？
- 2022-04-07が最新でイメージを作りたい
    - https://downloads.raspberrypi.org/raspios_arm64/images/raspios_arm64-2022-04-07/
- Node 問題
    - サポート期限：2023-04-30まで
    - 該当ライブラリの調査
    - https://github.com/chirimen-oh/chirimen/issues/121
    - v16.x or v18.x を調査
    - node-web-gpio/i2cからバックポートする？
        - 当時の issue https://github.com/chirimen-oh/chirimen/pull/98
            - 該当 issue https://github.com/EnotionZ/gpio/issues/62
            - pr https://github.com/EnotionZ/gpio/pull/63
            - => v16.x 以上でテストしてみる
- オフラインミーティングをやりたい（状況次第）

### 大垣 Mini Maker Faire 参加
- 2023 応募開始(2022.12)
- 2024 応募開始(2024.12)
    - @tadfmac
    - @WhiteHawk-taka

### バージョンアップや最新イメージの目標期限
- 2022.12 月中に全てクリアになっていると嬉しい

### 次回MTG
- 2022.09.26~2022.10.05の間で調整さん

### HackMD
#### 前回
* https://hackmd.io/SZ-BQ-bHQnOXUkVBUI3PNA

#### 今回
* https://hackmd.io/eH1zP0JoTSGxRykHQnKGpg
