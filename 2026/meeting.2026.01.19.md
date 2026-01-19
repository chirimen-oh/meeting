# CHIRIMEN meeting 2026.01.19 meeting vol 40

## 開催日と場所

2026 年 01 月 19 日 19:30~ オンライン

## タイムスケジュール

|    時間     | 種別 | テーマ                                                                                                       | 担当者 |
| :---------: | :--: | :----------------------------------------------------------------------------------------------------------- | :----- |
| 19:30~19:35 | 議論 | 挨拶                                                                                                         | -      |
| 19:35~19:50 | 議論 | [チュートリアルのリンクの修正 #5](https://github.com/orgs/chirimen-oh/discussions/5)                         | -      |
| 19:50~20:05 | 議論 | [example 用新規リポジトリ作成 #73](https://github.com/orgs/chirimen-oh/discussions/73)                       | -      |
| 20:05~20:20 | 議論 | [デバイスリストのカラム削除での影響調査 #76](https://github.com/orgs/chirimen-oh/discussions/76)             | -      |
| 20:20~20:35 | 議論 | [技術書典 20 オンライン・オフラインイベント準備 #90](https://github.com/orgs/chirimen-oh/discussions/90)     | -      |
| 20:35~20:50 | 議論 | [CHIRIMEN コミュニティ 10 周年イベント準備 #101](https://github.com/orgs/chirimen-oh/discussions/101)        | -      |
| 21:05~21:20 | 議論 | [ちりめん対応でばいすれしぴ集 第二版制作 #105](https://github.com/orgs/chirimen-oh/discussions/105)          | -      |
| 21:20~21:35 | 議論 | [ちりめんぱいぜろちゅーとりある用リポジトリの作成 #110](https://github.com/orgs/chirimen-oh/discussions/110) | -      |

## 参加者 (alphabetical order)

- @gurezo
- @kou029w
- @satakagi
- @sizuhiko

<!--
- @eli-j
- @hiyohiyo
- @tadfmac
-->

https://github.com/orgs/chirimen-oh/discussions/70

### [チュートリアルのリンクの修正 #5](https://github.com/orgs/chirimen-oh/discussions/5)

- [example 用新規リポジトリ作成 #73](https://github.com/orgs/chirimen-oh/discussions/73)が片付いたら、close 

### [example 用新規リポジトリ作成 #73](https://github.com/orgs/chirimen-oh/discussions/73)

- https://github.com/chirimen-oh/examples
- https://github.com/chirimen-oh/examples/pull/2
    - レビューお願いします
- デバイス情報の一元管理
    - [デバイスリスト CSV](https://github.com/chirimen-oh/chirimen.org/blob/master/_data/partslist.csv)
- [デバイス情報の一元管理 #3](https://github.com/chirimen-oh/examples/issues/3)
- [Example（サンプルコード）のガーデニング #70](https://github.com/orgs/chirimen-oh/discussions/70)
- どれかに集約できない（互いに独立した）リストの一覧
  - デバイスドライバのリスト
  - サンプルコードのリスト (複数のデバイスを使ったサンプル、(デバイスドライバがない)GPIOを使ったサンプルなどがあるので、デバイスドライバと一対一対応しない)
  - デバイスのリスト (同じサンプルでも別のデバイスを使うケース(異なるサーボモータとかLEDとか）があるので、exmapleと一対一対応しない)


|デバイス型番|デバイスドライバリスト|サンプルコードリスト|デバイスリスト|備考|
|:----|:----:|:----:|:----:|:----|
|赤いLED|-|◯|◯|-|
|青いLED|-|-|◯|違う型番|
|モータードライバ|-|◯|◯|-|
|VL53L1x (I2Cデバイス)|〇|◯|◯|-|
|スイッチ＋ＬＥＤ|-|◯|-*1|-|
|SHTx0 (I2Cデバイス)|〇|◯|◯|-|
|SHTx0(I2C温度センサ)＋モータ|-*2|◯|-|-|

- *nのノート
  - *1:スイッチもLEDもデバイスリストにあるので不要
  - *2:SHTx0はI2CデバイスだがデバイスドライバはSHTx0専用のデバイスドライバがあれば不要

- 現在のを元に新規にデータを作成し、移行が完了したら消す
    - CSV
        - デバイスリスト (I2Cにしかドライバの概念がないのでドライバではない)
            - I2C(SHTx0温度センサとか) 
            - GPIO(人感センサとかスイッチとか)、アナログデバイス(アナログ温度センサとか) 
            - タグ
                - GPIO
                - I2C
            - 項目
                - 部品型番/カテゴリ
                - デバイス画像
                - 説明
                - サンプルコード
                - 各種リンク
        - サンプルコードリスト
        - デバイスリスト
    - デバイスリストの Web ページ
        - 型番（をクリックしたら、各ページへ遷移）
            - 説明
            - サンプルコード
            - 回路図
            - スペックシート
            - 販売サイト
- CSV は、一旦下記ディレクトリに配置する運用をためす
    - https://github.com/chirimen-oh/examples/device-list
- 管理イメージ
    - examples/device-list/partslist.csv/json を chirimen.org/_data/partslist.csv


### [デバイスリストのカラム削除での影響調査 #76](https://github.com/orgs/chirimen-oh/discussions/76)

- 上記の対応になったので、この issue は閉じる

### [技術書典 20 オンライン・オフラインイベント準備 #90](https://github.com/orgs/chirimen-oh/discussions/90)

- エントリーしました 1/15

### [CHIRIMEN コミュニティ 10 周年イベント準備 #101](https://github.com/orgs/chirimen-oh/discussions/101)

- @eli-j にメンションつけて相談
    - 予算
    - 人数
    - 場所
        - オフィス or １F のお店？（場所
- 3 月中に決める

### [ちりめん対応でばいすれしぴ集 第二版制作 #105](https://github.com/orgs/chirimen-oh/discussions/105)

- 新規リポジトリを作成
    - ぱいぜろちゅーとりある
    - デバイスレシピ集 <= 第二版は、ここで管理します。

### [ちりめんぱいぜろちゅーとりある用リポジトリの作成 #110](https://github.com/orgs/chirimen-oh/discussions/110)

- 上記通りです。

### 追加議題
#### npm publish（公開）の手順が変わった
- 上記影響で、CI が失敗するようになった
- https://github.com/chirimen-oh/chirimen-drivers/actions/runs/21126884645/job/60749754667

#### 解決案
- CI の publish を修正する @gurezo
- 暫定運用のシェルと手順を作成する
- CI が解決しない場合
    - @chirimen/* を全て一つにまとめる？
        - デメリット：パスの変更が必要？

```diff
// @chirimen/* を全て一つにまとめた場合を変更
// Before
import { ADT7410 } from "@chirimen/ADT7410";

// After
import { ADT7410 } from "chirimen";

できれば、最後の手段
```

### chirimen-drivers/CONTRIBUTING.md 課題
- 手順が分かり難い
    - https://qiita.com/suin/items/c9c342f557bd885dbe06
- 簡単なシェルを作成するか？
- 資料
    - 新規追加された時に 404 になる
    - 自動化出来る
        - https://zenn.dev/rdlabo/articles/0b5364331e0bf6
    - モノレポなら `trusted publish（provenance）` が使えそうですけどね

### HackMD

#### 前回

- https://hackmd.io/@HjCTpd66RpCNd7l1dtr5Xw/SJxZgToojex

#### 今回

- https://hackmd.io/@HjCTpd66RpCNd7l1dtr5Xw/H1SwZO8B-x/edit
