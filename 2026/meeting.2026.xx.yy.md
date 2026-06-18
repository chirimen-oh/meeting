# CHIRIMEN meeting 2026.xx.yy meeting vol 44

## 開催日と場所

2026 年 xx 月 yy 日 19:30~ オンライン

## 今回の主な目的

次回ミーティングでは、まず **(1) PiZeroSerialConsole の現状課題と改善方針について認識合わせ**を行う。
時間があれば **(2) Examples / (3) Device List の役割整理**について議論する。  
(2)(3) については、まず **Examples を今後どう位置付けていくか**から議論できればとする。

今回の議論では、すぐに実装方針を確定することよりも、以下を揃えることを優先する。

- 現在の実装・既存資産に対する課題認識
- どの部分を改善対象とするか
- 既存資産との連続性・移行性をどう扱うか
- コミュニティとして長期保守できる形にするための方向性

## コミュニティの本質的課題

1. **資産整理の問題**: 何が現役で、何が歴史資料で、何を捨てる・残す・移すのかが未整理。
2. **意思決定の問題**: 議論はあるが、決定・担当・完了条件・close まで流れる仕組みが弱い。
3. **保守体制の問題**: 少人数・属人化に対して、保守対象と導線が広すぎる。

## タイムスケジュール

|    時間     | 種別 | テーマ                                                                                                                                      | 担当者 |
| :---------: | :--: | :------------------------------------------------------------------------------------------------------------------------------------------ | :----- |
| 19:30~19:35 | 議論 | 挨拶・今回の進め方確認                                                                                                                      | -      |
| 19:35~20:15 | 議論 | PiZeroSerialConsole: 現状課題と改善方針の認識合わせ                                                                                         | -      |
| 20:15~20:35 | 議論 | Examples / Device List の役割整理 — [#73](https://github.com/orgs/chirimen-oh/discussions/73) / [#76](https://github.com/orgs/chirimen-oh/discussions/76) | -      |
| 20:35~20:50 | 議論 | 決定事項・次回までのアクション確認                                                                                                          | -      |

> 時間が不足する場合は、(1) PiZeroSerialConsole の議論を優先する。(2)(3) の詳細は次回以降に回す。

## 参加者 (alphabetical order)

- TBD

<!--
- @gurezo
- @kou029w
- @eli-j
- @tadfmac
- @satakagi
- @sizuhiko
- @hiyohiyo
-->

### 議題 1: PiZeroSerialConsole

#### 背景

PiZeroSerialConsole について、現状課題の整理と改善方針を議論したいという開催要請があった。

#### 今回話したいこと

##### 1. 現状課題の整理

- 現在の実装について、どのような課題があると考えているか
- どの部分を改善したいのか

##### 2. 改善方針

- 課題に対して、どのような方向性で改善するのがよいか
- 既存資産との連続性や移行性も含めて考えたい

##### 3. 保守体制・実装方針

- コミュニティとして長期的に保守していくために、どのような体制・技術選択が適切か

#### 参考リンク

- 現行実装
  - https://chirimen.org/PiZeroWebSerialConsole/PiZeroWebSerialConsole.html
  - https://github.com/chirimen-oh/PiZeroWebSerialConsole
- 新規実装
  - https://github.com/gurezo/chirimen-lite-console

#### この議題で決めたいこと

- PiZeroSerialConsole の主な課題認識
- 次に深掘りする改善対象
- chirimen-lite-console を議論・検証対象として扱うか
- 次回までに確認すること・作業すること

### 議題 2: Examples / Device List

#### 背景

[example 用新規リポジトリ作成 #73](https://github.com/orgs/chirimen-oh/discussions/73)、[デバイスリストのカラム削除での影響調査 #76](https://github.com/orgs/chirimen-oh/discussions/76) などで議論はあるが、Examples / Device List を今後どう位置付けるかは未整理。
まずは Examples の位置付けから議論し、Device List との役割分担を確認する。

#### 今回話したいこと

##### 1. 現在進められている改善案の方向性確認

##### 2. Examples と Device List の役割整理

- Examples（ユースケース軸）
- Device List（デバイス軸）
- それぞれが担っている役割の確認

| 軸          | 役割           | 利用者の入口         |
| :---------- | :------------- | :------------------- |
| Examples    | ユースケース軸 | 何をしたいか         |
| Device List | デバイス軸     | どのデバイスを使うか |

##### 3. ユースケース軸とデバイス軸の両立方法

- 学習者や利用者にとってどのような導線が望ましいか

##### 4. データ構造やメタデータの扱い（次回以降）

- 今後の拡張や保守も見据えた整理

#### 参考リンク

- コミュニティ議論
  - [example 用新規リポジトリ作成 #73](https://github.com/orgs/chirimen-oh/discussions/73)
  - [デバイスリストのカラム削除での影響調査 #76](https://github.com/orgs/chirimen-oh/discussions/76)
  - https://github.com/chirimen-oh/examples — リポジトリ案はボツ
- 既存 Example の所在
  - [chirimen-drivers](https://github.com/chirimen-oh/chirimen-drivers) を基準とする方針
  - chirimen.org/pizero/src/esm-examples（`index_examples.csv`, `index.html` でページ生成）
- 既存デバイスリスト（コミュニティ現行）
  - [デバイスリスト CSV](https://github.com/chirimen-oh/chirimen.org/blob/master/_data/partslist.csv)
- 個人試作（@gurezo が開発・公開。コミュニティとしての合意・採用は未）
  - https://github.com/gurezo/chirimen-device-dashboard
  - https://chirimen-device-dashboard.web.app/
  - https://github.com/gurezo/chirimen-example-catalog（試作 → 上記に統合、アーカイブ済み）

#### この議題で決めたいこと

- Examples の主な役割
- Device List の主な役割
- Examples と Device List の役割分担
- データ構造・メタデータ設計を次回以降の議題にするか

### 次回以降の候補議題

- PiZeroSerialConsole / chirimen-lite-console の具体的な移行計画
- Examples の現役 / deprecated / historical の整理
- Device List の正本データ形式
- Examples / Device List のメタデータ設計
- chirimen.org / chirimen-drivers / device-dashboard（個人試作）の責務分担
- CI によるデータ検証・生成・公開フロー

### その他・継続議題

時間があれば触れる。詳細は前回までの議事を参照。

#### 技術書典 21 について

- 次回のエントリーについて

### メモ（@gurezo）

- chirimen-lite-console 実装中。画面移植より、接続・コンソール・設定・Examples 導線を保守しやすい構成に整理したい
- example-catalog は試作後、個人リポジトリ device-dashboard に統合。#73 は議論がすすんでいない認識
- device-dashboard は個人で公開中。コミュニティとして採用するかは未合意
- Device List の正本は CSV / Google スプレッドシート運用は避けたい

### HackMD

#### 前回

- https://hackmd.io/@HjCTpd66RpCNd7l1dtr5Xw/SJN-kUoPbg/edit

#### 今回

- （未作成）
