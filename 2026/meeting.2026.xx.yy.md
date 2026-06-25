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

## タイムスケジュール

|    時間     | 種別 | テーマ                                              | 担当者   |
| :---------: | :--: | :-------------------------------------------------- | :------- |
| 19:30~19:35 | 議論 | 挨拶・今回の進め方確認                              | satakagi |
| 19:35~20:25 | 議論 | PiZeroSerialConsole: 現状課題と改善方針の認識合わせ | satakagi |
| 20:25~20:40 | 議論 | Examples の今後の位置付け確認                       | satakagi |
| 20:40~20:50 | 議論 | Device List との役割分担・今後の論点整理            | satakagi |
| 20:50~21:00 | 議論 | 決定事項・次回までのアクション確認                  | satakagi |

> 時間が不足する場合は、PiZeroSerialConsole の議論を優先し、Examples / Device List の詳細は次回以降に回す。

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

## 議論を進める上での前提

今回の議論では、以下を分けて扱う。

- **技術的に動作する可能性があること**
- **コミュニティとして正式に保守対象にすること**
- **参考情報・検証候補として記録すること**
- **今回のミーティングで決めること**
- **次回以降の検討課題にすること**

特に、Raspberry Pi 3A+、Docker、軽量インストーラ、Node.js バージョン、KTEC インターン題材は関連するが、それぞれ別の論点である。
今回の主議題は、あくまで **PiZeroSerialConsole を中心とした既存 CHIRIMEN 環境の今後の改善・開発の方向性** とする。

## 議題 1: PiZeroSerialConsole

### 背景

この議題は、CHIRIMEN Raspberry Pi Zero 版 (CHIRIMEN Lite) 用の PiZeroSerialConsole をはじめとした、既存の CHIRIMEN 環境について、今後の改善・開発の方向性をコミュニティで相談するためのものです。

事前の Slack スレッドでは、検討の優先順位として以下が挙がっています。

1. PiZeroSerialConsole
2. CHIRIMEN with Node.js / RPi Zero Examples
3. CHIRIMEN 対応デバイスリスト

特に PiZeroSerialConsole は、以前から改善提案があり、CHIRIMEN Lite の利用導線としても重要な位置にあるため、まずは現状課題と改善方針について認識合わせを行います。

また、Raspberry Pi Zero 2W / Zero 2 WH の入手性が悪くなっていることから、Raspberry Pi 3A+ などの代替候補や、セットアップ方式についても話題に出ています。

ただし、このあたりは話題が広がりやすいため、今回の中心はあくまで PiZeroSerialConsole の現状課題と改善方針に置きます。
代替ハードウェア、Docker、軽量インストーラ、Node.js バージョンなどの話は、必要に応じて派生論点として整理します。

### 今回話したいこと

#### 1. 現状課題の整理

現在の実装について、どのような課題があると考えているかを整理する。

確認したい観点:

- 現在の PiZeroSerialConsole / 関連実装で、保守しづらい箇所はどこか
- 利用者がつまずきやすい箇所はどこか
- 既存コード・既存ドキュメント・既存チュートリアルとの整合性に問題はあるか
- 現在の実装をそのまま延命する場合のリスクは何か
- 改善する場合、どこまでを対象範囲とするのが現実的か

#### 2. 改善したい範囲の確認

改善対象を広げすぎると議論が発散するため、まず今回どの範囲までを扱うか確認する。

大きくは、以下の観点で整理したい。

- **利用者導線**
  - 利用者が Pi Zero / CHIRIMEN 環境を使い始めるまでの流れをどう整理するか
  - 既存の PiZeroSerialConsole の導線を維持するのか、見直すのか
- 現行実装
  - https://chirimen.org/PiZeroWebSerialConsole/PiZeroWebSerialConsole.html
  - https://github.com/chirimen-oh/PiZeroWebSerialConsole
- 改良実装
  - https://github.com/satakagi/PiZeroWebSerialConsole
  - [Note](https://github.com/satakagi/PiZeroWebSerialConsole/blob/main/refactoringNote.md)
  - [Pages](https://satakagi.github.io/PiZeroWebSerialConsole/)
- 個人開発
  - https://github.com/gurezo/chirimen-lite-console

- **セットアップ方式**
  - 既存の Setup CHIRIMEN のような軽量インストーラ方式を継続・改善するのか
  - Docker など、別の環境構築方式を検討するのか
  - どの方式が、利用者にとって分かりやすく、コミュニティとして保守しやすいか

- **対象ハードウェア**
  - Raspberry Pi Zero 2W / Zero 2 WH を主対象とするのか
  - Raspberry Pi 3A+ などの代替候補をどう扱うのか
  - 技術的に動作することと、正式サポート対象にすることをどう分けるか

- **既存資産との関係**
  - PiZeroWebSerialConsole、関連実装、既存チュートリアル、examples との関係をどう整理するか
  - 現役として保守するもの、参考実装として残すもの、legacy として扱うものをどう分けるか

- **保守体制**
  - 今後もコミュニティとして保守できる範囲はどこまでか
  - 新しい対象や方式を増やす場合、担当者・検証方法・ドキュメント更新範囲をどう決めるか

#### 3. 改善方針

課題に対して、どのような方向性で改善するのがよいかを議論する。

論点:

- 既存資産を活かしつつ、どこまで作り直すべきか
- 現行の PiZeroSerialConsole と今後の改善実装の関係をどう整理するか
- 既存のチュートリアルや examples から見たとき、URL・操作手順・説明をどう移行するか
- 新しい実装をコミュニティ側に移管する場合、どの段階で何を確認すべきか
- 「動くものを維持する」ことと「保守しやすい構成へ整理する」ことのバランスをどう取るか

#### 4. 保守体制・実装方針

コミュニティとして長期的に保守していくために、どのような体制・技術選択が適切かを確認する。

確認したい観点:

- 現在の体制で保守できる範囲はどこまでか
- 新しい対応ボード・セットアップ方式・実装を増やす場合、誰が保守するのか
- 検証方法・ドキュメント更新範囲・不具合対応方針をどう決めるか
- 意見募集から決定、担当、完了条件、close までの流れをどう作るか

## 派生論点: Raspberry Pi Zero 2W / 3A+ / セットアップ方式

### 背景

Raspberry Pi Zero 2W / Zero 2 WH の入手性が悪化しており、実機を用意できないことで検証やコントリビュートの入口が狭くなる懸念がある。

代替候補として Raspberry Pi 3A+ が挙がっている。
また、セットアップ方式として、PiZeroWebSerialConsole の `Setup CHIRIMEN` ボタンに近い軽量インストーラ方式と、Docker による環境構築案が話題に出ている。

さらに、現在の仕組みで利用している Node.js バージョンについて、32bit バイナリ提供や EoS の観点から、今後の見直しが必要になる可能性がある。

### 議論が混ざりやすい論点

以下は関連しているが、別々に判断する必要がある。

- Raspberry Pi Zero 2W / Zero 2 WH の入手性
- Raspberry Pi 3A+ の代替可能性
- Raspberry Pi 3A+ で USB OTG / serial console が利用できるか
- Raspberry Pi 3A+ を正式サポート対象にするか
- 軽量インストーラ方式で CHIRIMEN 環境を構築する案
- Docker による環境構築案
- Node.js のバージョン・アーキテクチャ対応
- PiZeroWebSerialConsole の改良実装
- 関連する新実装・再設計案との関係
- KTEC インターン題材として扱えるか

### 今回の扱い

今回の主目的は、PiZeroSerialConsole の現状課題と改善方針の認識合わせである。
そのため、この派生論点については、以下の整理に留める。

- Raspberry Pi 3A+ は、現時点では正式サポート対象に追加するかどうかを決めない
- まずは検証候補・参考情報として扱う
- 正式サポート化する場合は、別 issue で判断する
- 軽量インストーラ方式と Docker 方式は、優劣を即決せず、比較観点を整理する
- Node.js バージョン問題は重要だが、別途技術調査・移行計画として扱う
- KTEC インターン題材として扱う場合も、正式サポート化とは分けて検討する

### 現時点の懸念

- 既存資産の整理が終わっていない状態で、新しい正式サポート対象を増やすと保守負荷が増える
- 「技術的に動作する可能性がある」ことと「コミュニティとして正式に保守する」ことは別で考える必要がある
- 軽量インストーラ方式も Docker 方式も、それぞれ保守コストがある
- PiZeroWebSerialConsole と関連実装の役割が重なる場合、今後どれを主導線にするか整理が必要
- インターン題材として扱う場合も、成果物・担当範囲・保守責任を明確にしたい

### 今回確認したいこと

- Raspberry Pi 3A+ を正式サポート対象として議論するのか、まずは検証候補・参考情報に留めるのか
- Raspberry Pi 3A+ を検証する場合、誰がどこまで検証するのか
- 軽量インストーラ方式と Docker 方式を、どの観点で比較するのか
- Node.js バージョン問題を、どの issue / 議題として扱うのか
- PiZeroWebSerialConsole の改良実装と関連する新実装・再設計案の関係をどう整理するのか

### 暫定方針案

- Raspberry Pi 3A+ は、現時点では正式サポート対象に追加しない
- ただし、動作検証や参考情報として記録することは歓迎する
- 正式サポート化する場合は、別 issue で以下を整理してから判断する
  - 検証担当者
  - 検証手順
  - 対象 OS / Node.js / 接続方式
  - ドキュメント更新範囲
  - Zero 2W / Zero 2 WH との差分
  - 不具合報告への対応方針

- セットアップ方式については、軽量インストーラ案と Docker 案を比較し、保守体制も含めて判断する
- Node.js バージョン問題は、PiZeroSerialConsole の改善方針と関連するが、別途技術調査として切り出す
- PiZeroWebSerialConsole と関連する新実装・再設計案は、現役導線・参考実装・legacy の位置付けを整理する

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

### この議題で決めたいこと

- Examples の主な役割
- Examples を Device List と分けて考えるか、統合的に扱うか
- 次回以降、Examples のデータ構造・メタデータ設計を議論するか

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

### この議題で決めたいこと

- Device List の主な役割
- Examples との役割分担
- 次回以降にデータ構造・メタデータを議論するか

## 今回決めたいこと

### PiZeroSerialConsole

- PiZeroSerialConsole の主な課題認識
- 今回の改善対象範囲
- 既存資産との連続性・移行性の考え方
- 今後の保守体制・実装方針の確認
- 次回までに確認すること・作業すること

### 派生論点

- Raspberry Pi 3A+ を正式サポート対象として扱うのか、検証候補・参考情報に留めるのか
- 軽量インストーラ方式と Docker 方式を比較するための観点
- Node.js バージョン問題を別 issue / 別議題として切り出すか
- KTEC インターン題材として扱う場合、どこまでを成果物とするか

### Examples / Device List

- Examples の主な役割
- Device List の主な役割
- ユースケース軸とデバイス軸の両立方法
- Device List は公開済みであり、Examples 試作内容は統合済み
- CSV / Google スプレッドシートを正本にする運用懸念をどう扱うか
- 関連 Discussion (#70 / #76) を踏まえた次回論点の整理
- 次回以降にデータ構造・メタデータを議論するか

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

- PiZeroSerialConsole の具体的な改善・移行計画
- PiZeroWebSerialConsole と関連実装の現役 / legacy / 参考実装の整理
- Raspberry Pi 3A+ の USB OTG / serial console 検証
- 軽量インストーラ方式と Docker 方式の比較
- Node.js バージョン移行方針
- KTEC インターン題材として扱う場合の範囲整理
- Examples の現役 / deprecated / historical の整理
- Device List の正本データ形式
- Examples / Device List のメタデータ設計
- chirimen.org / chirimen-drivers / device-dashboard の責務分担
- CI によるデータ検証・生成・公開フロー

## 参考リンク・参考情報

### PiZeroSerialConsole / 関連実装

- https://github.com/chirimen-oh/PiZeroWebSerialConsole
- https://github.com/gurezo/chirimen-lite-console
- `gurezo/chirimen-lite-console` は、PiZeroSerialConsole 周辺の再整理・再実装案として実装中
- 議論の中心は個別実装ではなく、PiZeroSerialConsole 周辺を今後どう保守・改善するかに置く

### Examples

- https://github.com/orgs/chirimen-oh/discussions/73
- https://github.com/gurezo/chirimen-example-catalog

#### 参考情報:

- `gurezo/chirimen-example-catalog` は試作後、Device List 側に統合
- #73 では Examples の位置付けについて十分に議論が進んでいない認識

### Device List

- https://github.com/gurezo/chirimen-device-dashboard
- https://chirimen-device-dashboard.web.app/

#### 参考情報:

- Device List は公開済み
- Examples の試作内容は Device List 側に統合済み
- CSV / Google スプレッドシートを正本にする運用には懸念がある
- https://github.com/orgs/chirimen-oh/discussions/70
- https://github.com/orgs/chirimen-oh/discussions/76

### PiZeroが市場に無くて困った課題？ ( @tadfmac )

- Raspberry Pi 3 Model A+ Chirimen Liteでつかえるの？
  - https://forums.raspberrypi.com/viewtopic.php?t=228267
  - https://chatgpt.com/share/6a3a81b6-6858-83e8-83af-356ef63da953
- CHIRIMEN環境入りOSの配布の課題
  - [dockerつくる案](https://github.com/gurezo/chirimen-raspi-docker/wiki/01.Development-Concept)
  - インストーラ (PiZeroSerialConsoleのSetup CHIRIMENボタン：　[該当コード](https://github.com/chirimen-oh/PiZeroWebSerialConsole/blob/e6f40e0d8b909c16df01dc7d21ca8a29662e648a/chirimenPanel.html#L27))

### 技術書典 21

- CHIRIMEN コミュニティとしては、次回のエントリーはオンラインのみ申し込む想定
