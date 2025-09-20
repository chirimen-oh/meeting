## 2025.09.20 meeting vol 39

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
    - node (esm-examples配下のコード)
        - pizero
    - (browser)
        - Pi 3/4

### パーツリスト
- [pizero/src/esm-examples/index_examples.csv](https://github.com/chirimen-oh/chirimen.org/blob/master/pizero/src/esm-examples/index_examples.csv)
  - Pi Zero 向けでカラムは少ない
- [chirimen.org/_data/partslist.csv](https://github.com/chirimen-oh/chirimen.org/blob/master/_data/partslist.csv)
  - カラムが罰ゲームのように多い => カラムを減らす
  - Google スプレッドシートなどで編集したい

### csv の分類

- デバイス観点
    - k
- 作例観点
    - Pi 3/4 用
    - Pi Zero

#### デバイス観点 csv 項目
- インターフェイス
- カテゴリー
- 型番
- 商品URL
- 説明
- 画像URL
- サンプルコードURL
    - 個別のREADME.mdでは良いのでは？
        - 回路図URL 
        - データシートURL
        - 製造元資料URL
        - アプリケーションノートURL
        - 仕様書URL
        - 説明書URL
        - ガイドURL
- microbitサンプルコードURL
- piZeroサンプルコードURL


#### 作例観点 csv 項目
- タイトル
- 概要
- ID(main-hoge.js)
- 回路図
- JSGet
- めも
    - 回路図と JSGET 以外のリンクは各デバイスの README に記載すれば良い

#### TODO
- 両方CSVのデバイスの付け合せ
- スプレッドシートの作成
    - デバイス観点
    - 作例観点
- 各デバイスに CSV統合・移行の目的で下記リンクを転記
    - 回路図URL 
    - データシートURL
    - 製造元資料URL
    - アプリケーションノートURL
    - 仕様書URL
    - 説明書URL
    - ガイドURL
    - code sandobox
    - CHIRIMEN ORIG参考リンク
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
- Web I2CとWeb GPIOのAPIスペックのアップデート
  - readByte()
  - readBytes(length)
  - writeByte(byte)
  - writeBytes(bytes)
  - https://browserobo.github.io/WebI2C/ に反映する?
  - ソースコード: https://github.com/browserobo/WebI2C
  - https://www.w3.org/community/browserobo/ W3C CG

## Slack Channel のガーデニングについて

- check したチャンネルをアーカイブ


## CHIRIMEN OSS 化 10 周年記念イベント
- 技術書典 20 にデバイスリスト ver.2 を作成
    - フォントサイズと書体を調整・フッターの冗長なURLを削る => ページを調整
    - 60ページを超えないよう、新しいexempleを増やした場合は、不要なものを削除して調整する。
    - ギアモーターのページは減らす

## CONTRIBUTING の整理
- Arduino を参考にしてみる
    - https://github.com/arduino/library-registry/blob/main/README.md
- コントリビュートのドキュメント整備
    - Chirimen ドライバーの追加する人対象のドキュメントがない
        - package-lock.json(CI) の説明
- slack 招待リンクの移行（sizuhikoさん）
    - 残り 5箇所
    - https://join.slack.com/t/chirimen-oh/shared_invite/zt-3dvgmnu1x-LxCW09XdSXYGoLVKfnXZww
- [チュートリアルサイトをコミュニティトップに差し替える #88](https://github.com/chirimen-oh/chirimen.org/issues/88)
    - こーへいさん
