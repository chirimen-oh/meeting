# CHIRIMEN meeting 2024.08.07

[![hackmd-github-sync-badge](https://hackmd.io/MSNWDYTpR8yFyOWZwKn5IQ/badge)](https://hackmd.io/MSNWDYTpR8yFyOWZwKn5IQ)

## 開催日と場所

2024 年 08 月 07 日 19:30~ Zoom

## タイムスケジュール

|    時間     | 種別 | テーマ                                                                                                            | 担当者 |
| :---------: | :--: | :---------------------------------------------------------------------------------------------------------------- | :----- |
| 19:30~19:35 | 議論 | 挨拶                                                                                                              | -      |
| 19:35~19:40 | 議論 | [技術書典 16 オンライン・オフラインイベント準備 #23](https://github.com/chirimen-oh/meeting/issues/23)            | -      |
| 19:40~19:50 | 議論 | [ Node v20.x or v22.x 対応 #121 ](https://github.com/chirimen-oh/chirimen/issues/121)                             | -      |
| 19:50~20:20 | 議論 | [チュートリアルサイトをコミュニティトップに差し替える #88](https://github.com/chirimen-oh/chirimen.org/issues/88) | -      |
| 20:20~20:35 | 議論 | [クラウドサービスを使う可能性があるサンプルについて #24](https://github.com/chirimen-oh/meeting/issues/24)        | -      |
| 20:35~20:50 | 議論 | [デバイスドライバの差異（Polyfill 版と Node 版）の解決 #25](https://github.com/chirimen-oh/meeting/issues/25)     | -      |
| 20:50~21:10 | 議論 | [CONTRIBUTING の整理 #26](https://github.com/chirimen-oh/meeting/issues/26)                                       | -      |
| 21:10~21:30 | 議論 | [CHIRIMEN コミュニティの今後の活動について #30](https://github.com/chirimen-oh/meeting/issues/30)                 | -      |
| 21:30~21:40 | 議論 | イベント                                                                                                          | -      |
| 21:40~21:50 | 議論 | 共有・フィードバック                                                                                              | -      |

## 参加者 (alphabetical order)

- @Aritaka-hub
- @eli-j
- @kou029w
- @satakagi
- @sizuhiko
- @tadfmac

## 議題

### [技術書典 16 オンライン・オフラインイベント準備 #23](https://github.com/chirimen-oh/meeting/issues/23)

- [売上等報告](https://github.com/chirimen-oh/meeting/issues/23#issuecomment-2143704732)
- ステッカー残200枚くらいなので、要追加印刷をする
- 新バージョンのチラシも同様
- @Aritaka-hub

### [ Node v20.x or v22.x 対応 #121 ](https://github.com/chirimen-oh/chirimen/issues/121)

- 現状確認
- CHIRIMEN Lite は、2024-07-04のイメージ版で作成したい @kou029w
    - https://nodejs.org/en/blog/release/v22.6.0#2024-08-06-version-2260-current-rafaelgss
    - TypeScript 最新版になると実装しやすくなると（v24.x で、本格的に議論しましょう
    - 型定義が充実できたらいいな（下記イメージ
        - @type/node-web-gpio
        - @type/node-web-i2c

### [チュートリアルサイトをコミュニティトップに差し替える #88](https://github.com/chirimen-oh/chirimen.org/issues/88)

<details>

<summary>前回メモ</summary>
    
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

#### 閉じる条件

- チュートリアルサイトの移管が完了次第、着手
  - [#3](https://github.com/chirimen-oh/meeting/issues/3)
  - [#5](https://github.com/chirimen-oh/meeting/issues/5)

</details>

### [CHIRIMEN コミュニティの今後の活動について #30](https://github.com/chirimen-oh/meeting/issues/30)

#### what is chirimen
- ユースケースを再認識したい。@tadfmac
- 1 ウェブアプリケーションからデバイス・ハードを動かしたい @sizuhiko
    - 1 つのURLで様々なアプリケーションでデバイスが動かせる
- JS の API の実装のひとつ @kou029w
    - 選択肢は多い方が良い
- ユースケースについて @Aritaka-hub
    - 先生が専門学校で教えている
    - 学校で、広がりつつある。
    - Pi Zero で、学校で採用しやすくなっている
- 素の javascript 、標準 javascript で、使える事に意味がある @satakagi
    - 標準からの差分が少ないところが利点
    - ライブラリ的な使い方ができる
- ２つ視点がある @eli-j
    - 参加する人
        - コミュニティとしての純粋な活動が減っているかも？
        - エンジニアが楽しい事を企画できないか？
    - Web DINO の視点
        - 教育の現場では重宝される
- Q：メーカーズチャレンジ以外で、chirimen を使われているのか？ @tadfmac
    - ユースケースを再定義してみては？ @tadfmac
    - プロトタイピングとしては、良い
    - どこに重点をおくか？
        - Web, JavaScript ?
    - どんなコミュニティ？
        - Web のコミュニティ
    - ブラウザの UI で、デバイスを動かしたい
    - Pi Zero版は、Node.js で使える事に利点がある
- ネクストアクション？
    - サポート・メンテナンス対象
        - デバイスドライバー
        - GPIO/I2C
    - Polyfill と Node 版の差異ををどうなくす？
        - 別テーマ？(issue, discussion)で
- 定義？
    - Web の技術で、ハードウェアを動かす
        - Web の標準技術を使う
        - JavaScript を使う
    - 上記の技術を使って、プロトタイピング環境を提供する
    - 


### イベント

- 報告：[Ogaki Mini Maker Faire 2024](https://makezine.jp/blog/2024/03/ommf2024_announce.html) に当選しました。
- 相談：[CHIRIMEN OSS 化 10 周年記念イベント準備 #31](https://github.com/chirimen-oh/meeting/issues/31)
- 共有：技術書典17 エントリーしました。

### 共有・フィードバック

#### 共有

- TBD

#### フィードバック

- TBD

#### まとめ

##### 共有については

- TBD

##### フィードバックについては

- TBD

###### issue

### 次回 MTG

- TBD

### HackMD

#### 前回

- https://hackmd.io/CsJ0RlSCTLmEfZKHx4y9WA

#### 今回

- https://hackmd.io/@HjCTpd66RpCNd7l1dtr5Xw/SJQz4ztYA/edit
