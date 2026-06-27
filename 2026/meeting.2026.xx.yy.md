# CHIRIMEN meeting 2026.xx.yy meeting vol 44

## 開催日と場所

2026 年 xx 月 yy 日 19:30~ オンライン

## 今回の主な目的

今回のミーティングでは、まず **PiZeroSerialConsole の現状課題と改善方針について認識合わせ**を行う。

時間があれば、**Examples / Device List の役割整理**について議論する。
Examples / Device List については、まず Examples を今後どう位置付けていくかから確認する。

今回の議論では、すぐに実装方針を確定することよりも、以下を揃えることを優先する。

- 現在の実装・既存資産に対する課題認識
- どの部分を改善対象とするか
- 既存資産との連続性・移行性をどう扱うか
- コミュニティとして長期保守できる形にするための方向性

## タイムスケジュール

|    時間     | 種別 | テーマ                                              | 担当者   |
| :---------: | :--: | :-------------------------------------------------- | :------- |
| 19:30~19:35 | 議論 | 挨拶・今回の進め方確認                              | satakagi |
| 19:35~20:15 | 議論 | PiZeroSerialConsole: 現状課題と改善方針の認識合わせ | satakagi |
| 20:15~20:35 | 議論 | Examples / Device List の役割整理                   | satakagi |
| 20:35~20:50 | 議論 | 決定事項・次回までのアクション確認                  | satakagi |

> 時間が不足する場合は、PiZeroSerialConsole の議論を優先する。Examples / Device List の詳細は次回以降に回す。

## 参加者

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

## 議題 1: PiZeroSerialConsole

### 背景

PiZeroSerialConsole について、現状課題の整理と改善方針を議論したいという開催要請があった。

PiZeroSerialConsole は、CHIRIMEN Raspberry Pi Zero 版 (CHIRIMEN Lite) の重要な利用導線であり、以前から改善提案もあるため、まずはコミュニティとして方向性を確認する。

今回は、PiZeroSerialConsole の現状課題と改善方針に集中する。
Raspberry Pi 3A+、Docker、Node.js バージョン、KTEC インターン題材などは重要な話題だが、それぞれ単独で議論可能なため、必要に応じて次回以降の議題として整理する。

### 今回話したいこと

#### 1. 現状課題の整理

- 現在の実装について、どのような課題があると考えているか
- どの部分を改善したいのか

#### 2. 改善方針

- 課題に対して、どのような方向性で改善するのがよいか
- 既存資産との連続性や移行性も含めて考えたい
- 現行実装・改良実装・関連する再実装案の関係をどう整理するか

#### 3. 保守体制・実装方針

- コミュニティとして長期的に保守していくために、どのような体制・技術選択が適切か
- 新しい実装や改善を取り込む場合、担当者・検証方法・ドキュメント更新範囲をどう決めるか

### 参考リンク

- 現行実装
  - https://chirimen.org/PiZeroWebSerialConsole/PiZeroWebSerialConsole.html
  - https://github.com/chirimen-oh/PiZeroWebSerialConsole

- 改良実装
  - https://github.com/satakagi/PiZeroWebSerialConsole
  - https://satakagi.github.io/PiZeroWebSerialConsole/

- 関連する再実装案・参考情報
  - https://github.com/gurezo/chirimen-lite-console

### この議題で確認したいこと

- PiZeroSerialConsole の主な課題認識
- 次に深掘りする改善対象
- 現行実装・改良実装・関連する再実装案の扱い
- 次回までに確認すること・作業すること

## 議題 2: Examples / Device List

### 背景

Examples / Device List については、今後どう位置付けるかを整理したい。

まずは Examples の位置付けから議論し、Device List との役割分担を確認する。

### 今回話したいこと

#### 1. 現在進められている改善案の方向性確認

#### 2. Examples と Device List の役割整理

- Examples: ユースケース軸
- Device List: デバイス軸
- それぞれが担っている役割の確認

| 軸          | 役割           | 利用者の入口         |
| :---------- | :------------- | :------------------- |
| Examples    | ユースケース軸 | 何をしたいか         |
| Device List | デバイス軸     | どのデバイスを使うか |

#### 3. ユースケース軸とデバイス軸の両立方法

- 学習者や利用者にとってどのような導線が望ましいか

#### 4. データ構造やメタデータの扱い（次回以降）

- 今後の拡張や保守も見据えた整理

### 参考リンク

- コミュニティ議論
  - https://github.com/orgs/chirimen-oh/discussions/73
  - https://github.com/orgs/chirimen-oh/discussions/76

- 個人試作・参考情報
  - https://github.com/gurezo/chirimen-device-dashboard
  - https://chirimen-device-dashboard.web.app/
  - https://github.com/gurezo/chirimen-example-catalog

### この議題で確認したいこと

- Examples の主な役割
- Device List の主な役割
- Examples と Device List の役割分担
- データ構造・メタデータ設計を次回以降の議題にするか

## 今回決めないこと

以下は重要だが、今回のミーティングでは結論を急がない。

- Raspberry Pi 3A+ の正式サポート追加
- 軽量インストーラ方式と Docker 方式の採用可否
- Node.js バージョン移行の具体方針
- KTEC インターン題材の正式決定
- Examples / Device List の詳細なデータ構造
- 既存リポジトリの統廃合・archive 判断

## 次回以降の候補議題

- Raspberry Pi Zero 2W / Zero 2 WH の入手性への対応
- Raspberry Pi 3A+ の USB OTG / serial console 検証
- 軽量インストーラ方式と Docker 方式の比較
- Node.js バージョン移行方針
- KTEC インターン題材として扱う場合の範囲整理
- PiZeroSerialConsole の具体的な改善・移行計画
- Examples の現役 / deprecated / historical の整理
- Device List の正本データ形式
- Examples / Device List のメタデータ設計
- chirimen.org / chirimen-drivers / device-dashboard の責務分担
- CI によるデータ検証・生成・公開フロー
- Ogaki Mini Maker Faire 2026 エントリー（おそらく9月頃エントリー開始なので予告）

### 技術書典 21

- CHIRIMEN コミュニティとしては、次回のエントリーはオンラインのみ申し込む想定

## その他・継続議題

時間があれば触れる。詳細は前回までの議事を参照。

### HackMD

#### 前回

- https://hackmd.io/@HjCTpd66RpCNd7l1dtr5Xw/SJN-kUoPbg/edit

#### 今回

- （未作成）
