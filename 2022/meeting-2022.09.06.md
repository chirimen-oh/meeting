# CHIRIMEN meeting 2022.09.06

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
| 20:45~20:55 | 議論 | [#12](https://github.com/chirimen-oh/meeting/issues/12)                                                   | -      |
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
- PiZero版の開発環境(USBOTG直結する)のコンソールが、最近のChromeで文字消えする
    - CHIRIMEN PiZeroのコンソールについて、MacOSのChromeで文字化け（文字消え）が起きるとの報告が複数来ています。
    - https://webiotmakerschallenge.slack.com/archives/C031RJPCEBW/p1644718373320289
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

### [Raspberry Pi OS 2022.01.28 64bit 版 setup.sh](https://github.com/chirimen-oh/chirimen/issues/118) 
- 進捗ありません。ごめんなさい。
- 落ち着いて作成します。

### HackMD
#### 前回
- https://hackmd.io/aEObXEtuRDq23cdeS6AwaA

#### 今回
* https://hackmd.io/SZ-BQ-bHQnOXUkVBUI3PNA