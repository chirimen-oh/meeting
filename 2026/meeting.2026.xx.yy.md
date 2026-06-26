# CHIRIMEN meeting 2026.xx.yy meeting vol 44

## 開催日と場所

2026 年 xx 月 yy 日 19:30~ オンライン

## 今回の主な目的

今回のミーティングは、CHIRIMEN Raspberry Pi Zero 版 (CHIRIMEN Lite) 用の PiZeroSerialConsole をはじめとした、既存の CHIRIMEN 環境について、今後の改善・開発の方向性をコミュニティで相談するために開催する。

検討の優先順位は以下とする。

1. PiZeroSerialConsole
2. CHIRIMEN with Node.js / RPi Zero Examples
3. CHIRIMEN 対応デバイスリスト

今回は、まず **(1) PiZeroSerialConsole の現状課題と改善方針について認識合わせ**を行う。

時間があれば、**(2) Examples の今後の位置付け**、および **(3) Device List との役割分担**について確認する。

今回の議論では、すぐに実装方針を確定することよりも、以下を揃えることを優先する。

- 現在の実装・既存資産に対する課題認識
- どの部分を改善対象とするか
- 既存資産との連続性・移行性をどう扱うか
- コミュニティとして長期保守できる形にするための方向性
- 今回決めることと、次回以降に回すことの切り分け

## 今回決めたいこと

### PiZeroSerialConsole

- PiZeroSerialConsole の主な課題認識
- 今回の改善対象範囲
- 現行実装と改良実装の関係
- 既存資産との連続性・移行性の考え方
- 今後の保守体制・実装方針の確認
- 次回までに確認すること・作業すること

### Examples / Device List

- Examples の主な役割
- Device List の主な役割
- ユースケース軸とデバイス軸の両立方法
- 次回以降にデータ構造・メタデータを議論するか

## タイムスケジュール

|    時間     | 種別 | テーマ                                              | 担当者   |
| :---------: | :--: | :-------------------------------------------------- | :------- |
| 19:30~19:35 | 議論 | 挨拶・今回の進め方確認                              | satakagi |
| 19:35~20:25 | 議論 | PiZeroSerialConsole: 現状課題と改善方針の認識合わせ | satakagi |
| 20:25~20:40 | 議論 | Examples の今後の位置付け確認                       | satakagi |
| 20:40~20:50 | 議論 | Device List との役割分担・今後の論点整理            | satakagi |
| 20:50~21:00 | 議論 | 決定事項・次回までのアクション確認                  | satakagi |

> 時間が不足する場合は、PiZeroSerialConsole の議論を優先し、Examples / Device List の詳細は次回以降に回す。

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

## 議論を進める上での前提

今回の主議題は、**PiZeroSerialConsole の現状課題と改善方針の認識合わせ**とする。

Raspberry Pi 3A+、Docker、Node.js バージョン、KTEC インターン題材なども関連する重要な話題だが、それぞれ単独で議論可能なテーマであるため、今回の議題 1 では深掘りしない。

必要に応じて、次回以降の議題・別 issue として整理する。

今回の議論では、以下を分けて扱う。

- 技術的に動作する可能性があること
- コミュニティとして正式に保守対象にすること
- 参考情報・検証候補として記録すること
- 今回のミーティングで決めること
- 次回以降の検討課題にすること

## 議題 1: PiZeroSerialConsole

### 背景

PiZeroSerialConsole は、CHIRIMEN Lite を使い始めるための重要な導線の一つです。

以前から改善提案もあり、提案から少し時間も経っているため、まずは現在の実装について、どのような課題があるのか、どの部分を改善したいのかを整理したいです。

### 今回話したいこと

#### 1. 現状課題の整理

現在の PiZeroSerialConsole について、どのような課題があると考えているかを整理する。

確認したい観点:

- 現在の実装で、保守しづらい箇所はどこか
- 利用者がつまずきやすい箇所はどこか
- 既存コード・既存ドキュメント・既存チュートリアルとの整合性に問題はあるか
- 現在の実装をそのまま延命する場合のリスクは何か
- 改善する場合、どこまでを対象範囲とするのが現実的か

#### 2. 改善したい範囲の確認

改善対象を広げすぎると議論が発散するため、まず今回どの範囲までを扱うか確認する。

大きくは、以下の観点で整理したい。

- **利用者導線**
  - 利用者が CHIRIMEN Lite を使い始めるまでの流れをどう整理するか
  - 既存の PiZeroSerialConsole の導線を維持するのか、見直すのか

- **現行実装**
  - 現行の PiZeroSerialConsole をどこまで継続利用するか
  - 現行実装のうち、改善すべき箇所はどこか

- **改良実装**
  - 既存の改良実装をどのように評価するか
  - 現行実装との関係をどう整理するか

- **既存資産との関係**
  - 既存チュートリアル、examples、ドキュメントとの関係をどう整理するか
  - 現役として保守するもの、参考実装として残すもの、legacy として扱うものをどう分けるか

- **保守体制**
  - 今後もコミュニティとして保守できる範囲はどこまでか
  - 新しい実装や改善を取り込む場合、担当者・検証方法・ドキュメント更新範囲をどう決めるか

#### 3. 改善方針

課題に対して、どのような方向性で改善するのがよいかを議論する。

論点:

- 既存資産を活かしつつ、どこまで改善するべきか
- 現行の PiZeroSerialConsole と改良実装の関係をどう整理するか
- 既存のチュートリアルや examples から見たとき、URL・操作手順・説明をどう移行するか
- 新しい実装をコミュニティ側に取り込む場合、どの段階で何を確認すべきか
- 「動くものを維持する」ことと「保守しやすい構成へ整理する」ことのバランスをどう取るか

#### 4. 保守体制・実装方針

コミュニティとして長期的に保守していくために、どのような体制・技術選択が適切かを確認する。

確認したい観点:

- 現在の体制で保守できる範囲はどこまでか
- 改善実装を取り込む場合、誰が保守するのか
- 検証方法・ドキュメント更新範囲・不具合対応方針をどう決めるか
- 意見募集から決定、担当、完了条件、close までの流れをどう作るか

> この議題で決めたいことは、冒頭「今回決めたいこと」に集約。

## 議題 2: Examples

### 背景

Examples については、以下の観点で方向性を確認したい。

- Examples はユースケース軸の導線として扱う
- Device List はデバイス軸の導線として扱う
- それぞれが担っている役割を整理する
- 学習者や利用者にとって、どのような導線が望ましいかを確認する

データ構造やメタデータの扱いは重要だが、次回以降の議題として扱う可能性がある。

### 今回話したいこと

まずは、Examples を **ユースケース軸の導線**としてどう扱うかを確認する。

確認したい観点:

- Examples は「何をしたいか」から探す入口にするのか
  - 例: LED を光らせたい
  - 例: 温度を測りたい
  - 例: I2C デバイスを試したい

- Examples は学習者向けの導線なのか、検証済みコードの置き場なのか
- chirimen.org / pizero / tutorial / console / device list のどこから Examples に導線を置くのが自然か
- 既存 examples のうち、どれを現役として扱い、どれを historical / deprecated とするか

> この議題で決めたいことは、冒頭「今回決めたいこと」に集約。

## 議題 3: Device List

### 背景

Device List については、デバイス軸の導線として位置付けられる。
Examples が「何をしたいか」から探す入口であるなら、Device List は「どのデバイスを使うか」から探す入口として整理できる。

### 今回話したいこと

Device List は、Examples と対になる **デバイス軸の導線**として扱う。

確認したい観点:

- Device List は「どのデバイスが使えるか」から探す入口にするのか
- デバイス詳細から Examples / Tutorial / Console へどう誘導するか
- Examples 側のユースケース軸と、Device List 側のデバイス軸をどう両立するか
- データの正本をどこに置くべきか

### 今回は深掘りしない可能性があること

以下は重要だが、PiZeroSerialConsole と Examples の位置付け確認後に、次回以降で議論した方がよい可能性がある。

- データ構造
- メタデータ設計
- スキーマ定義
- CI での検証・生成
- 既存 chirimen.org / chirimen-drivers との同期方法
- 登録・編集フロー

> この議題で決めたいことは、冒頭「今回決めたいこと」に集約。

## 今回決めないこと

以下は重要だが、今回のミーティングでは結論を急がない。

- Raspberry Pi 3A+ の正式サポート追加
- 軽量インストーラ方式と Docker 方式の採用可否
- Node.js バージョン移行の具体方針
- KTEC インターン題材の正式決定
- Examples / Device List の詳細なデータ構造
- CSV / Google スプレッドシート / JSON / Markdown / YAML / TypeScript などの正本データ形式
- 既存リポジトリの統廃合・archive 判断

## 整理したい構造的課題

今回の議論では、個別機能の追加だけでなく、以下の構造的課題も意識したい。

- 資産整理の問題
  - 何が現役で、何が歴史資料で、何を捨てる・残す・移すのかが未整理

- 意思決定の問題
  - 議論はあるが、決定・担当・完了条件・close まで流れる仕組みが弱い

- 保守体制の問題
  - 少人数・属人化に対して、保守対象と導線が広すぎる

## 次回以降の候補議題

- Raspberry Pi 3A+ の USB OTG / serial console 検証
- Raspberry Pi Zero 2W / Zero 2 WH の入手性への対応
- 軽量インストーラ方式と Docker 方式の比較
- Node.js バージョン移行方針
- KTEC インターン題材として扱う場合の範囲整理
- PiZeroSerialConsole の具体的な改善・移行計画
- PiZeroWebSerialConsole と関連実装の現役 / legacy / 参考実装の整理
- Examples の現役 / deprecated / historical の整理
- Device List の正本データ形式
- Examples / Device List のメタデータ設計
- chirimen.org / chirimen-drivers / device-dashboard の責務分担
- CI によるデータ検証・生成・公開フロー

## 参考リンク・参考情報

### PiZeroSerialConsole / 関連実装

- https://chirimen.org/PiZeroWebSerialConsole/PiZeroWebSerialConsole.html
- https://github.com/chirimen-oh/PiZeroWebSerialConsole
- https://github.com/satakagi/PiZeroWebSerialConsole
- https://satakagi.github.io/PiZeroWebSerialConsole/
- https://github.com/gurezo/chirimen-lite-console

参考情報:

- 議論の中心は個別実装ではなく、PiZeroSerialConsole 周辺を今後どう保守・改善するかに置く
- 関連する改良実装・再実装案は、比較対象・参考情報として扱う

### Examples

- https://github.com/orgs/chirimen-oh/discussions/73
- https://github.com/gurezo/chirimen-example-catalog

参考情報:

- `gurezo/chirimen-example-catalog` は試作後、Device List 側に統合
- #73 では Examples の位置付けについて十分に議論が進んでいない認識

### Device List

- https://github.com/gurezo/chirimen-device-dashboard
- https://chirimen-device-dashboard.web.app/

参考情報:

- Device List は公開済み
- Examples の試作内容は Device List 側に統合済み
- CSV / Google スプレッドシートを正本にする運用には懸念がある

### 関連議題

- https://github.com/orgs/chirimen-oh/discussions/70
- https://github.com/orgs/chirimen-oh/discussions/76
