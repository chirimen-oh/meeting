# CHIRIMEN meeting 2023.08.24

[![hackmd-github-sync-badge](https://hackmd.io/-O2Gu3BbQhOz8nF-AOk4Ng/badge)](https://hackmd.io/-O2Gu3BbQhOz8nF-AOk4Ng)

## 開催日と場所

2023 年 05 月 09 日 Zoom

## タイムスケジュール

|    時間     | 種別 | テーマ                                                                       | 担当者 |
| :---------: | :--: | :--------------------------------------------------------------------------- | :----- |
| 19:30~19:35 | 議論 | 挨拶                                                                         | -      |
| 19:55~20:15 | 議論 | [#3](https://github.com/chirimen-oh/meeting/issues/3) + pizero tutorial の件 | -      |
| 20:15~20:35 | 議論 | [#5](https://github.com/chirimen-oh/meeting/issues/5)                        | -      |
| 20:45~20:55 | 議論 | [#16](https://github.com/chirimen-oh/meeting/issues/16)                      | -      |
| 20:45~20:55 | 議論 | [#19](https://github.com/chirimen-oh/meeting/issues/19)                      | -      |
| 20:45~20:55 | 議論 | [#20](https://github.com/chirimen-oh/meeting/issues/20)                      | -      |

## 参加者 (alphabetical order)

- @Aritaka-hub
- @elie-j
- @kou029w
- @sizuhiko

## 議題

### [#3](https://github.com/chirimen-oh/meeting/issues/3)

手伝いできる方お願いします

### [#5](https://github.com/chirimen-oh/meeting/issues/5)

- https://github.com/chirimen-oh/chirimen/issues/125
- https://github.com/chirimen-oh/chirimen/issues/122
- chirimen lite も 2023.02.22 版出た
  - issue を建てる
  - カメラが動かないケースが有った（ただし、レアケース
  - bullseye で、カメラ周りが変わった模様
- やってい行きましょう！ご協力お願いします
- https://github.com/chirimen-oh/chirimen.org/issues/85
- https://github.com/chirimen-oh/chirimen.org/issues/88
- ドメイン管理の状況を赤塚さんと浅井さんに確認
- 閉じる条件
  - https://github.com/chirimen-oh/chirimen.org/issues/88 を終わらせる
  - https://github.com/chirimen-oh/chirimen.org/issues/88#issuecomment-1540000885

### [#16](https://github.com/chirimen-oh/meeting/issues/16)

- [売上等報告](https://github.com/chirimen-oh/meeting/issues/16#issuecomment-1565487663)
- 

### [#19](https://github.com/chirimen-oh/meeting/issues/19)
- チュートリアルを印刷をする案
    - 各イベントにも使える（配布物に使える
    - 配布物は、内部的に購入した建付け
    - 多少の差別化は考える
    - Pi Zero 
        - ~~ステップ３ (CHIRIMEN環境設定)~~
            - ~~コメントアウト~~ done
        - 最新イメージ作成中
            - https://github.com/chirimen-oh/chirimen-lite/issues/7
        - 目次が課題？
        - 表紙どうする？
        - https://github.com/chirimen-oh/chirimen.org/
            - 上記の md 活用する
            - ブランチを作成して作業する
        - リンクは PDF にする時に注釈する方法がある
            - https://pandoc.org/
            - https://qiita.com/sky_y/items/80bcd0f353ef5b8980ee
        - RE:VIEW を使ってみる？
            - https://reviewml.org/ja/
        - 追加ページや挿絵を考える
            - **お試しPDFを作って、アップデートする**
    - お手伝いの issue や 調整さんでリマインド
- 新刊：CHIRIMEN を支える技術 => 一旦後回し
    <details>
    
        1. **はじめに**
           - CHIRIMEN の概要と本書の目的についての説明。

        2. **CHIRIMEN の基本**
           - CHIRIMEN のアーキテクチャとサポートするハードウェアの紹介。
           - Web ブラウザを使ったプログラミングの基本概念。

        3. **Web シリアル通信**
           - Web シリアル通信の概要と利点の説明。
           - Web シリアルの設定方法と使用例の提供。

        4. **Web GPIO**
           - GPIO（汎用入出力）の基本と概要についての説明。
           - Web GPIO を使用してデジタル入出力を制御する手法と実際のプロジェクト例の提供。

        5. **Web I2C**
           - I2C プロトコルの説明と用途の紹介。
           - Web I2C を使ってセンサーやデバイスを制御する方法の解説。

        6. **Rasbian と CHIRIMEN**
           - Rasbian（ラズビアン）オペレーティングシステムの概要と CHIRIMEN との統合方法についての説明。
           - Rasbian 上での開発環境のセットアップ手順と注意点の提供。

        7. **実践プロジェクト**
           - 複数のプロジェクトを通じて、Web シリアル、Web GPIO、Web I2C を活用した具体的なアプリケーションの構築手法を示す。
           - 各プロジェクトでのコード例、配線図、画像などを提供。

        8. **応用と展望**
           - CHIRIMEN の技術を基にしたさらなる応用例や可能性についての洞察を提供。
           - ユーザーが独自のアイデアを開発する際のヒントやアドバイスを提供。

        9. **リソースと参考文献**
           - 書籍内で言及された資料やウェブリンク、コミュニティの情報へのアクセス方法を提供。    

    </details>
- スターターキット
    - 現時点で、在庫がない販売はない
    - 頒布する場合、オマケ頒布
- 全部乗せ基盤
    - 販売 OK
    - ※あまり人気ないかも？
- スケジュール
    - 執筆カレンダーを作る @gurezo
    - たたき台のリミット（9月中
    - みんなで、ブラッシュアップ（オフライン
        - 調整さん立てる
        - 平日か土日かをみんなで考える
    - DINO の状況：10月以降は、忙しい
    - 09/30(土)：satakagi さんが DINO に在所
    - 入稿は DINO にお願い
        - データを渡す

### [#20](https://github.com/chirimen-oh/meeting/issues/20)
- 見送り

### [チュートリアルサイトをコミュニティトップに差し替える #88](https://github.com/chirimen-oh/chirimen.org/issues/88)
- [@dynamis さんに確認中](https://github.com/chirimen-oh/chirimen.org/issues/88#issuecomment-1691532522)


### 確認中
- Pi Zero と M1 Mac で検証
    - Web Serial で接続後に無造作に外して、再接続して正しくつながるかどうか？
    - [M1 Mac で途中で接続を外すと認識できない現象が発生 #22 ](https://github.com/chirimen-oh/PiZeroWebSerialConsole/issues/22)
    - 2022-12-12-chirimen-lite 版

### 次回 MTG

- 調整さんを立てる
    - 新刊作業
        - 09/30(土)？＋α（別日設定？
            - 09/30(土)：satakagi さんが DINO に在所
            - みんなで、ブラッシュアップ（オフライン

### HackMD

#### 前回

- https://hackmd.io/@ICe-ErPVRmeEwSMsjoFUdA/HkHksOIN3

#### 今回

- https://hackmd.io/rQZfnzIPQ0Sg-v3aCAnmFw
