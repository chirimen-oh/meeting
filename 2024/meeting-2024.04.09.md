# CHIRIMEN meeting 2024.04.09

[![hackmd-github-sync-badge](https://hackmd.io/-O2Gu3BbQhOz8nF-AOk4Ng/badge)](https://hackmd.io/-O2Gu3BbQhOz8nF-AOk4Ng)

## 開催日と場所

2024 年 04 月 09 日 19:30~ Zoom

## タイムスケジュール

|    時間     | 種別 | テーマ                                                                                                            | 担当者 |
| :---------: | :--: | :---------------------------------------------------------------------------------------------------------------- | :----- |
| 19:30~19:35 | 議論 | 挨拶                                                                                                              | -      |
| 19:35~20:30 | 議論 | [チュートリアルサイトをコミュニティトップに差し替える #88](https://github.com/chirimen-oh/chirimen.org/issues/88) | -      |
| 20:30~20:35 | 議論 | [技術書典 15 オンライン・オフラインイベント準備 #19](https://github.com/chirimen-oh/meeting/issues/19)            | -      |
| 20:35~20:45 | 議論 | [技術書典 16 オンライン・オフラインイベント準備 #23](https://github.com/chirimen-oh/meeting/issues/23)            | -      |
| 20:45~21:00 | 議論 | [ Node v18.x or v20.x 対応 #121 ](https://github.com/chirimen-oh/chirimen/issues/121)                             | -      |
| 21:00~21:30 | 議論 | イベント                                                                                                          | -      |

## 参加者 (alphabetical order)

- @kou029w
- @satakagi
- @sizuhiko
- @eli-j

## 議題

### [チュートリアルサイトをコミュニティトップに差し替える #88](https://github.com/chirimen-oh/chirimen.org/issues/88)

- [@dynamis さんに確認中](https://github.com/chirimen-oh/chirimen.org/issues/88#issuecomment-1691532522)

  - tutorial サイトが未達
  - 他は移管完了
  - Cloudflare DNS/Cloudflare Pages に切り替え済み
  - r.chirimen.org はまだ Netlify のまま

- [node 版をよりアピールする#85](https://github.com/chirimen-oh/chirimen.org/issues/85)
  - いつやるか。
- https://github.com/chirimen-oh/meeting/issues/3#issuecomment-2044690936
- イベントでのフィードバックの連絡先をどうするか
  - チュートリアルは、[chirimen.org](https://github.com/chirimen-oh/chirimen.org) に issue を立てる
  - ドライバーは、[chirimen-drivers](https://github.com/chirimen-oh/chirimen-drivers) に issue を立てる
    - CONTRIBUTING.md を参照する
- chirimen-drivers リンク切れ
  - [Contributing Guidelines](https://chirimen.org/chirimen-drivers/CONTRIBUTING)
  - [CONTRIBUTING リンク切れ対応 #297](https://github.com/chirimen-oh/chirimen-drivers/issues/297)
- [pre-arrangement-contributions](https://github.com/chirimen-oh/pre-arrangement-contributions)
  - コントリビュート用手順リポジトリ
- JS GET 出来ない（ipv6 接続できない問題）
  - 塩尻会場で問題発生。
  - 愛媛でも起きた？
  - [Raspberry Pi で IPV6 を使う](https://qiita.com/ekzemplaro/items/6423d953ac4458719ca9)
  - [関連スレ](https://chirimen-oh.slack.com/archives/C048CQB7C/p1707809445954419)
  - tutorial に ipv6 問題を記載する（issue を立てる

### [#3](https://github.com/chirimen-oh/meeting/issues/3)

- 閉じる条件
  - チュートリアルサイトの移管が完了次第、着手

### [#5](https://github.com/chirimen-oh/meeting/issues/5)

- 閉じる条件
  - チュートリアルサイトの移管が完了次第、着手

### [技術書典 15 オンライン・オフラインイベント準備 #19](https://github.com/chirimen-oh/meeting/issues/19)

- [売上等報告](https://github.com/chirimen-oh/meeting/issues/19#issuecomment-1837069944)

### [技術書典 16 オンライン・オフラインイベント準備 #23](https://github.com/chirimen-oh/meeting/issues/23)

- 応募当選報告
- 在庫状況の確認
  - 100 部発注納品済み
  - 販促で 50 部買い取り
  - 技術書典 15 20 部販売
  - 献本 10 部くらい（コミュニティ 5 部？、イベント系 5 部？
  - 2024.04.09 時点で、70 部くらい（別途確認
  - WebDINO 内で在庫管理に関する意識合わせ
  -
- 事前準備
  - 新刊がなければ、イベントページの作業のみ
- 新刊
  - 見送り
  - ネタが思いつき次第教諭

### [ Node v20.x or v22.x 対応 #121 ](https://github.com/chirimen-oh/chirimen/issues/121)

- 現状確認
  - node-web-gpio
    - v20.x 対応済み
  - node-web-i2c
    - v20.x 対応済み
  - chirimen lite
    - v20.x 対応済み
    - 2024-03-15 版イメージ
  - chirimen
    - raspi 5 の入手次第で対応開始
    - 2024-03-15 版イメージ
  - v22.x 対応を考慮

### 確認中 => 解決

- Pi Zero と M1 Mac で検証

  - Web Serial で接続後に無造作に外して、再接続して正しくつながるかどうか？
  - [M1 Mac で途中で接続を外すと認識できない現象が発生 #22 ](https://github.com/chirimen-oh/PiZeroWebSerialConsole/issues/22)
  - 2022-12-12-chirimen-lite 版
  - => issue を close

- @sizuhiko さんに検証機用 Pi Zero セットを送る
  - 誰か検証できなかったら、送る
- @gurezo 自宅環境確認

### イベント

- メーカーズチャレンジは、 2024 も継続します。
- オフラインイベントも 2024.06 末までなら対応可能
- Maker Faire 2024 の参加について
  - 2024.04.19 から募集開始
  - コミュニティで参加するか、要相談
  - イベントはやみくもに出ない（リソースの問題
- もくもく会を定期的に開催する案もある

### @satahagi さんからの共有・フィードバック

#### 共有

- `新しいデバイスドライバ書いたけれどまだ本家のほうに投入できておらず、
どこかに紛失しないように、とりあえず適当なリポジトリをつくっておいてあります。`
  - https://github.com/chirimen-oh/pre-arrangement-contributions

#### フィードバック

- メイカーズチャレンジで、　スタッフや参加者の方々から、画像処理とか機械学習を利用するサンプルがあると良い
- 課題
  - webSocket（relayServer）と同様にこれらのケースではクラウドサービスを使うことになるケースが多い
  - 中立性とか透明性をどう考えるかの整理が必要

#### まとめ

##### 共有については

- GPS をつないでいるサンプルがあるのだけれど、これが node 版オンリーになってしまっている
- カメラも　 node 版とブラウザ版で差異が出る
- 今後こういったものが増えてくると残念なので、何か対策できないものか
  - 基本的にはシリアルが課題か？ブラウザ版でシリアルを使うには webSerial？

##### フィードバックについては

- クラウドサービスを使うようなサンプルが機械学習などで出てくるかもしれないが、中立性や透明性、持続可能性
- クラウドサービスの終了や仕様変更でサンプルが動かなくなるリスクが結構高そう）をどう考えるか？

### 次回 MTG

- TBD

### HackMD

#### 前回

- https://hackmd.io/rQZfnzIPQ0Sg-v3aCAnmFw

#### 今回

- https://hackmd.io/CsJ0RlSCTLmEfZKHx4y9WA
