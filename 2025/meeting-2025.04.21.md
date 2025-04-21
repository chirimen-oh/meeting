# CHIRIMEN meeting 2025.04.21

[![hackmd-github-sync-badge](https://hackmd.io/yqToqi6dR5atVA6YRtvHxg/badge)](https://hackmd.io/yqToqi6dR5atVA6YRtvHxg)

## 開催日と場所

2025 年 04 月 21 日 19:30~ Google Meet

## タイムスケジュール

|    時間     | 種別 | テーマ                                                                                                            | 担当者 |
| :---------: | :--: | :---------------------------------------------------------------------------------------------------------------- | :----- |
| 19:30~19:35 | 議論 | 挨拶                                                                                                              | -      |
| 19:50~20:05 | 議論 | [チュートリアルサイトをコミュニティトップに差し替える #88](https://github.com/chirimen-oh/chirimen.org/issues/88) | -      |
| 20:05~20:20 | 議論 | [クラウドサービスを使う可能性があるサンプルについて #34](https://github.com/orgs/chirimen-oh/discussions/34)      | -      |
| 20:20~20:35 | 議論 | [デバイスドライバの差異（Polyfill 版と Node 版）の解決 #36](https://github.com/orgs/chirimen-oh/discussions/36)   | -      |
| 20:35~20:50 | 議論 | [Slack から Discord の移行について #41](https://github.com/orgs/chirimen-oh/discussions/41)                       | -      |
| 20:50~21:05 | 議論 | [技術書典 17 オンライン・オフラインイベント準備 #38](https://github.com/chirimen-oh/meeting/issues/38)            | -      |
| 21:05~21:20 | 議論 | [技術書典 18 オンライン・オフラインイベント準備 #42](https://github.com/chirimen-oh/meeting/issues/42)            | -      |
| 21:20~21:30 | 議論 | イベント                                                                                                          | -      |
| 21:30~21:40 | 議論 | 共有・フィードバック                                                                                              | -      |

## 参加者 (alphabetical order)

- @sizuhiko
- @tadfmac
- @satakagi
- @gurezo

## 議題

### [チュートリアルサイトをコミュニティトップに差し替える #88](https://github.com/chirimen-oh/chirimen.org/issues/88)
- @gurezo => @dyamis に確認

#### 課題
- 活動歴を気軽更新出来るようにしたい。
- メンテしない方針になったので、トップページは塩漬け状態
- X のアカウントのポストだけでも表示出来るようにできれば。
- トップページをどう変えるか
    - jekyll をそのまま使う
    - ニュース
    - 活動歴
    - SNS アカウント
    - チュートリアルのリンク
- プルリク作成して、プレビュー環境をレビュー

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

### [クラウドサービスを使う可能性があるサンプルについて #34](https://github.com/orgs/chirimen-oh/discussions/34)

- メーカーズチャレンジ参加者に情報を与える
    - https://groq.com/
    - 質問された時点で、参考・リンク情報を提供する

### [デバイスドライバの差異（Polyfill 版と Node 版）の解決 #36](https://github.com/orgs/chirimen-oh/discussions/36)

- モノレポコード
    - https://github.com/gurezo/chirimen-lib

#### 課題
- npm package の参照先
- Chirimen Desktop 版
    - メンテしていくかどうか
        - コミュニティのリソース問題
    - ニーズ調査する？
        - イベント後どんなデバイスをつかっているのか？
    - Pi Zero みたいにする？
        - リモート Chirimen
    - ブラウザ上の UI でやりたいケースもある

#### 問題の原点
- コミュニティのリソース問題
- ハードの入手が難しくなった。
- Node バージョンに対応できなくなった。

#### 方針
- Chirimen Desktop 版保留（塩漬け）
- Chirimen Desktop 版のニーズが出たら、相談する
- Chirimen Desktop 版を作り直す時に修正する

### [Slack から Discord の移行について #41](https://github.com/orgs/chirimen-oh/discussions/41)

- Discord だとアカウントの使い分け出来ない
- ビデオ会議は、遅延がある
- 音声の方は、遅延がない

#### 方針
- 必要性は無いので、一旦 Slack のままで

### [技術書典 17 オンライン・オフラインイベント #38](https://github.com/chirimen-oh/meeting/issues/38) 報告

- [売上等報告](https://github.com/chirimen-oh/meeting/issues/38#issuecomment-2543519865)
- 各残数

  | 品目       | 残数 |
  | :--------- | ---: |
  | ステッカー |   43 |
  | チラシ     |   44 |

### [技術書典 18 オンライン・オフラインイベント準備 #42](https://github.com/chirimen-oh/meeting/issues/42)
- オンライン・オフライン出展決まりました。
- スターターキットの販売の確認を瀧田さんに了承する。
- 売り子さん募集しています。


### イベント

- 相談：[CHIRIMEN OSS 化 10 周年記念イベント準備 #31](https://github.com/chirimen-oh/meeting/issues/31)
    - 同窓会的な内々のイベント？パーティ？を開く
    - コミュニティ関係者のみ
    - 新刊は未定
- [技術書同人誌博覧会](https://gishohaku.connpass.com/event/352601/)の参加の可否
  - 出展料が必要（Max 4,000 円）
  - => 不参加

### 雑談
- chirimen-drivers は、ts だったけ？
    - ejs で使える
    - Node の experimental mode 使えるかも
    - @type/chirimen/デバイス名みたいな型定義があると嬉しい？
        - デバイスドライバ毎に作る必要はないかも？
        - Uint8Array と boolean だけで良いはず
    - 無理に chirimen-drivers を ts 化するメリットは現時点でナシ
- コミュニティの呑み会を企画


### 共有・フィードバック

#### 共有

- TBD

#### フィードバック

- 今年も Pi Zero 版メーカーズチャレンジも使う模様
- 開催数も同程度になる見込み

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

- https://hackmd.io/@HjCTpd66RpCNd7l1dtr5Xw/SJQz4ztYA/edit

#### 今回

- https://hackmd.io/yqToqi6dR5atVA6YRtvHxg
