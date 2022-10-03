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
    -rpiネイティブカメラのgistは[こちら](https://gist.github.com/satakagi/1b5adc8dff8236421a593b93fa152222)に ⇒ chirimen ghに移行させました
    - PiZeroのnodeサンプルは登録完了しました！[ここから](https://tutorial.chirimen.org/pizero/esm-examples/)
        - [スタンドアロン](https://tutorial.chirimen.org/pizero/esm-examples/gpio-camera/index.html)
        - [リモート](https://tutorial.chirimen.org/pizero/esm-examples/remote_camera/index.html)
    - node版とブラウザ版の互換のAPI化はできない？
        - ブラウザ版の方は別の仕組みが必要(USBカメラとPiネイティブカメラでも違うのでいろいろ考える必要ありそう)
    - カメラのサンプルを作るのはノード版だけで良い？
        - [ カメラのサンプルを作る #1 ](https://github.com/chirimen-oh/tutorial.chirimen.org/issues/1)
            - PiZero: DONE
            - Pi4: postpone
- PiZero版の開発環境(USBOTG直結する)のコンソールが、最近のChromeで文字消えする
    - ~~CHIRIMEN PiZeroのコンソールについて、MacOSのChromeで文字化け（文字消え）が起きるとの報告が複数来ています。~~
    - https://webiotmakerschallenge.slack.com/archives/C031RJPCEBW/p1644718373320289
    - ~~=> mac OS でなければ、問題が出ない~~
    - ~~=> mac ユーザが検証する~~
        - ~~このスレッドの中に記載していますが、XTerm.jsをただ最新リリースにしても文字消えはなおらないようなのですが、さらにXTerm.jsの設定で影響が出そうなところをいろいろいじったものを置いてあります。~~
            - ~~オリジナルで同じ症状が出るかどうか~~
                - https://chirimen.org/PiZeroWebSerialConsole/PiZeroWebSerialConsole.html
            - ~~いろいろいじったものではどうか~~
                - https://chirimen.org/PiZeroWebSerialConsole/PiZeroWebSerialConsole_xtLatest.html
    - Chrome バージョン: 106.0.5249.91（Official Build arm64）では発生しない
    - Chrome の問題の可能性大
    - Pi Zero 2W で、LED検証出来た。  :smiley: 

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
        - 年明けにもくもく会イベント開く？ :cow: :monkey_face::8ball::meat_on_bone: :panda_face: :cake: :tropical_drink: 
        - 2023.01後半？ :two: :zero: :two: :three:  / :zero: :one:
    - Rasbian OS アップデート(2022.09.26版):two: :zero: :two: :two:  / :zero: :nine: :zero:/:two: :six:
        - https://downloads.raspberrypi.org/raspios_arm64/images/raspios_arm64-2022-09-26/
        - https://downloads.raspberrypi.org/raspios_full_armhf/images/raspios_full_armhf-2022-09-26/
        - [Raspberry Pi OS 2022.09.26 64bit 版 setup.sh #122](https://github.com/chirimen-oh/chirimen/issues/122)

### [#13](https://github.com/chirimen-oh/meeting/issues/13)
- 売上合計：22,500円
- 内訳

|	品名	|	オフライン会場	|	オンライン会場	|	総数	|	単価	|	売上	|
|	:----	|	----:	|	----:	|	----:	|	----:	|	----:	|
|	電子＋紙セット	|	6	|	1	|	7	|	1000	|	7000	|
|	電子本	|	1	|		|	1	|	1000	|	1000	|
|	フルテストボード部品セット	|	3	|		|	3	|	2000	|	6000	|
|	フルテストボード基盤のみ	|	1	|		|	1	|	500	|	500	|
|	スターターキット	|	2	|		|	2	|	4000	|	8000	|

### [Raspberry Pi OS 2022.09.26 64bit 版 setup.sh #122](https://github.com/chirimen-oh/chirimen/issues/122)
- 進捗ありません。ごめんなさい。
- 落ち着いて作成します。

### Web IoT Makers Challenge
- 壁紙を変えたい
- ~~CHIRIMEN のみにしたい。~~
    - ~~2021.01.?? に直っている~~
    - ~~イメージ reelase 2021.08.21 に直っている~~
    - ~~apt-get upgarde しなければ大丈夫？~~
- 2022-09-26が最新でイメージを作りたい
    - https://downloads.raspberrypi.org/raspios_full_armhf/images/raspios_full_armhf-2022-09-26/
    - https://downloads.raspberrypi.org/raspios_arm64/images/raspios_arm64-2022-09-26/
- Node 問題
    - サポート期限：2023-04-30まで
    - 該当ライブラリの調査
    - https://github.com/chirimen-oh/chirimen/issues/121
    - v16.x or v18.x を調査
    - node-web-gpio/i2cからバックポートする？
        - Node.jsをv16.x系にアップデートして動けば、一旦大丈夫
        - 当時の issue https://github.com/chirimen-oh/chirimen/pull/98
            - 該当 issue https://github.com/EnotionZ/gpio/issues/62
            - pr https://github.com/EnotionZ/gpio/pull/63
            - => v16.x 以上でテストしてみる
- オフラインミーティングをやりたい（状況次第）
    - 企画考えます @gurezo 

- さくらインターネットが群馬で実施するイベントで、CHIRIMENの宣伝をします 10月 @guzero
    - さくらの全国行脚オンラインイベント(10/26予定)
    - https://www.sakura.ad.jp/information/events/2022/08/16/1968210252/ これの群馬版

### 大垣 Mini Maker Faire 参加
- 2022 応募開始(2022.12)
    - https://makezine.jp/blog/2022/05/ommf2022.html
- 2024 応募開始(2024.12)
    - @tadfmac
    - @WhiteHawk-taka

### Node.jsバージョンアップやOS最新イメージの目標期限
- 2022.12 月中に全てクリアになっていると嬉しい
    - ※Pi4を使う場合

### 次回MTG
- 保留

### HackMD
#### 前回
* https://hackmd.io/SZ-BQ-bHQnOXUkVBUI3PNA

#### 今回
* https://hackmd.io/eH1zP0JoTSGxRykHQnKGpg
