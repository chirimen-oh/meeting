# CHIRIMEN meeting 2025.09.20 meeting vol 39

## 開催日と場所

2025 年 09 月 20 日 13:30~ Web DINO

## タイムスケジュール

|    時間     | 種別 | テーマ                                                                                            | 担当者 |
| :---------: | :--: | :------------------------------------------------------------------------------------------------ | :----- |
| 13:20~13:35 | 議論 | 挨拶                                                                                              | -      |
| 13:35~15:00 | 議論 | [Example（サンプルコード）のガーデニング #70](https://github.com/orgs/chirimen-oh/discussions/70) | -      |
| 15:00~16:00 | 議論 | [Slack Channel のガーデニングについて #65](https://github.com/orgs/chirimen-oh/discussions/65)    | -      |
| 16:00~17:00 | 議論 | [CHIRIMEN OSS 化 10 周年記念イベント準備 #33](https://github.com/orgs/chirimen-oh/discussions/33) | -      |
| 17:00~18:p0 | 議論 | [CONTRIBUTING の整理 #35](https://github.com/orgs/chirimen-oh/discussions/35)                     | -      |

## 参加者 (alphabetical order)

- @eli-j
- @gurezo
- @hiyohiyo
- @kou029w
- @satakagi
- @sizuhiko
- @tadfmac

https://github.com/orgs/chirimen-oh/discussions/70

### 新規リポジトリ作成

- examples - https://chirimen.org/examples/
  - REAMDE
    - [chirimen-drivers/microbit-examples](https://github.com/chirimen-oh/chirimen-drivers/tree/master/microbit-examples)
    - [chirimen-drivers/node-examples](https://github.com/chirimen-oh/chirimen-drivers/tree/master/node-examples)
    - [chirimen-drivers/raspi-examples](https://github.com/chirimen-oh/chirimen-drivers/tree/master/raspi-examples)
    - [chirimen/gc/gpio](https://github.com/chirimen-oh/chirimen/tree/master/gc/gpio)
    - [chirimen/gc/i2c](https://github.com/chirimen-oh/chirimen/tree/master/gc/i2c)
    - [pre-arrangement-contributions](https://github.com/chirimen-oh/pre-arrangement-contributions)
    - [remote-connection/examples](https://github.com/chirimen-oh/remote-connection/tree/master/examples)
    - [chirimen-micro-bit/examples](https://github.com/chirimen-oh/chirimen-micro-bit/tree/master/examples)
  - node (esm-examples 配下のコード)
    - pizero
  - (browser)
    - Pi 3/4

### パーツリスト

- [pizero/src/esm-examples/index_examples.csv](https://github.com/chirimen-oh/chirimen.org/blob/master/pizero/src/esm-examples/index_examples.csv)
  - Pi Zero 向けでカラムは少ない
- [chirimen.org/\_data/partslist.csv](https://github.com/chirimen-oh/chirimen.org/blob/master/_data/partslist.csv)
  - カラムが罰ゲームのように多い => カラムを減らす
  - Google スプレッドシートなどで編集したい

### csv の分類

- デバイス観点
  - Pi Zero
- 作例観点
  - Pi 3/4 用
  - Pi Zero

#### デバイス観点 csv 項目

- インターフェイス
- カテゴリー
- 型番
- 商品 URL
- 説明
- 画像 URL
- サンプルコード URL
  - 個別の README.md では良いのでは？
    - 回路図 URL
    - データシート URL
    - 製造元資料 URL
    - アプリケーションノート URL
    - 仕様書 URL
    - 説明書 URL
    - ガイド URL
- microbit サンプルコード URL
- piZero サンプルコード URL

#### 作例観点 csv 項目

- タイトル
- 概要
- ID(main-hoge.js)
- 回路図
- JSGet
- めも
  - 回路図と JSGET 以外のリンクは各デバイスの README に記載すれば良い

#### TODO

- 両方 CSV のデバイスの付け合せ
- スプレッドシートの作成
  - デバイス観点
  - 作例観点
- 各デバイスに CSV 統合・移行の目的で下記リンクを転記
  - 回路図 URL
  - データシート URL
  - 製造元資料 URL
  - アプリケーションノート URL
  - 仕様書 URL
  - 説明書 URL
  - ガイド URL
  - code sandobox
  - CHIRIMEN ORIG 参考リンク
- 作例で例えば：PCA9685 16 チャンネル PWM ドライバ + MX1508 モーターコントローラ
  - 以下のリンクを付ける
    - PCA9685
    - PWM ドライバ
    - MX1508 モーター
- コントリビュートガイド作成
  - CONTRIBUTE.md を作成
- テストブランチでカラムを減らした CSV を作成してみる

#### 課題

- Github Action で、Google スプレッドシートデータ取得
  - [スプレッドシートの内容を GitHub のリポジトリに自動的に同期する仕組みを作った](https://zenn.dev/odan/articles/11954a71ff0db3)
- README を転記するシェルを作成する
- 変更した場合、CI の影響範囲の調査
- Web I2C と Web GPIO の API スペックのアップデート(@tadfmac)
  - readByte()
  - readBytes(length)
  - writeByte(byte)
  - writeBytes(bytes)
  - https://browserobo.github.io/WebI2C/ に反映する?
  - ソースコード: https://github.com/browserobo/WebI2C
  - https://www.w3.org/community/browserobo/ W3C CG

## Slack Channel のガーデニングについて

- check したチャンネルをアーカイブ
  - @gurezo

## CHIRIMEN OSS 化 10 周年記念イベント

- 技術書典 20 にデバイスリスト ver.2 を作成(@gurezo)
  - フォントサイズと書体を調整・フッターの冗長な URL を削る => ページを調整
  - 60 ページを超えないよう、新しい exemple を増やした場合は、不要なものを削除して調整する。
  - ギアモーターのページは減らす

## CONTRIBUTING の整理

- Arduino を参考にしてみる
  - https://github.com/arduino/library-registry/blob/main/README.md
- コントリビュートのドキュメント整備
  - Chirimen ドライバーの追加する人対象のドキュメントがない
    - package-lock.json(CI) の説明
- slack 招待リンクの移行（sizuhiko さん）
  - 残り 5 箇所
  - https://join.slack.com/t/chirimen-oh/shared_invite/zt-3dvgmnu1x-LxCW09XdSXYGoLVKfnXZww
  - done
    - [ Slack の参加フォームを招待リンクに修正 #154 ](https://github.com/chirimen-oh/chirimen.org/pull/154)
- ## [チュートリアルサイトをコミュニティトップに差し替える #88](https://github.com/chirimen-oh/chirimen.org/issues/88)
  - @kou029w

### HackMD

#### 前回

- https://hackmd.io/@HjCTpd66RpCNd7l1dtr5Xw/SJQz4ztYA/edit

#### 今回

- https://hackmd.io/@HjCTpd66RpCNd7l1dtr5Xw/SJxZgToojex
