# CHIRIMEN meeting 202102

## 開催日と場所
2021年02月xx日 Zoom

## タイムスケジュール
|時間|種別|テーマ|担当者|
|:----:|:----:|:----|:----|
|19:30~19:35|議論|挨拶|-|
|19:35~20:20|議論|RPi SDイメージ更新リリース|-|
|20:20~20:45|議論|chirimen-drivers|-|
|20:45~20:50|議論|microbit|-|
|20:50~20:55|議論|技術書典|-|
|20:55~21:00|議論|BOOTHオンラインショップ|-|
|21:10~21:20|議論|公式サイト|-|
|21:20~21:30|議論|オンラインイベント|-|

## 参加者 (alphabetical order)


## 議題
* RPi SDイメージ更新リリース
  - WIMC鳥取では、問題なし
  - MVP 宮本君に感謝！+1
      - コミュニティ全員からの熱い賛辞が送られた！
  - 64bit OS Image には Node 非互換がある。これは今後の課題 (今のところ対応・リリースを決めてはいない)
      - aruduino => インストールしただけ（未検証32bit含む）
      - 64bit sourcelist を確認
      - apache
  - あるセンサーだけ未検証 => TBD
  - フルテストボードのお披露目の機会を考える => TBD

* chirimen-drivers
  * ES Module => done
  * Examples引っ越し => done
  * 行動規範 => done
  * チュートリアルのリンクの修正 @kou029w @dynamis @satakagi @gurezo
      * example のリンクの参照の仕方(microbit)
      * スタンドアロン用にリポジトリのコードをイメージにコピー
          * driversに加えてexamplesも
      * driversのコピー
      * gc/contribディレクトリを廃止して統合
* issue 管理やり直す
    * any-issue は、archive
    * https://github.com/chirimen-oh/meeting/issues/2
    * [issue移譲のやりかたがある?](https://docs.github.com/ja/github/managing-your-work-on-github/transferring-an-issue-to-another-repository)
    * 古いissueは置いておく
    * 新しいissue => meeting リポジトリ
        * 議論・確定後 => 各リポジトリにissueを移譲
* microbit
  * V2　公式サポート => done
      * V1 (v1.5) サポート継続
      * MVP: 本家 MakeCode の対応も即時されて問題解決。無事 V2 サポートが可能になった
      * V2 ではヒープが大きくなったのでメモリの心配もない
  * microbit I2C Examplesをchirimen driversのexampleへのリンクに切り替える @satakagi
  * PWM API => TBD
      * Analog Out が PWM として動いていたので、周波数などの調整機能を追加して API を決めていけば出来そう
      * WebGPIO/I2C と並ぶ形で WebPWM
          * 実際のボードでは周波数が全ポート固定の可能性あり、それを考えた仕様にしていくのが
      * RasPi は？
          * https://blog.boochow.com/article/raspberry-pi-hw-pwm-driver-2.html
          * GPIO 40,45 が使える？
          * 公式配置図 https://www.raspberrypi.org/documentation/usage/gpio/
              * Hardware PWM available on GPIO12, GPIO13, GPIO18, GPIO19
          * GPIO 12, 13
          * Pi0 も 18,19 or 12,13 辺りが使える？
          * Alternate Function 設定して使えと
              * 対応したらそういうイメージを作っていきましょう。サンプルコードへの影響などもあるかもですが、その時には頑張りましょう。
* スマートIoT推進フォーラム　人材育成分科会 で CHIRIMENを紹介することになりました。
    - パーツリストの自動生成の仕組みを共有 => @dynamis or @kou029w
* PRチャンネルの充実
    - パーツリストページを qiita に陳腐化する前提で記載 bot化？（週1アップデート）
        - ちなみに、実体配線図用のfritzingパーツもかな～り充実してるよ～
    - twitter bot 
        - パーツリストページへのリンク誘導 @gurezo
        - チュートリアルページへのリンク誘導 @gurezo
        - 実体配線図用のfritzingパーツポスト
        - 逆引きリスト情報
            - arudino逆引き本は売れている
    - zenn 掲載は、次回アジェンダにする。
    - SEO対策したほうが、早い？

### BOOTH オンラインショップ
- 公開しました。
- https://chirimen-oh.booth.pm/
- 既刊本後日販売開始

### オンラインイベント
- もくもく会 on 02/06 (土)　=> done
- 03/13以外で検討

### サポートデバイス
- Pi 400 はリリース待ち
- Pi 3A+ はぐんま—さんに送って確認して貰う
- PiZeroW　=> 公式サイトにも記載
    - モノは動く
    - Node 版は公式サポートしてスタートガイド 1-2 ページ書くのはありではないか
- 新規にやるとしたら Jetson Nano あたりから
    - 既に多少試していたし安価なバージョンがでている
- M5Stack も面白いのかも知れないが...

### 公式サイト

- もくもく会でチュートリアルサイトが公式サイトトップになっても良いようにガシガシ更新していきたい
- DNS 切替は赤塚さんにお願い
    - dynamis から適当なタイミングでお願い、切替
- 全部のせボードの紹介もしたい
    - スターターキットや Tinkering Sensoor Box だけでなくそれもページを作ると良い
    -  https://github.com/chirimen-oh/chirimen.org/issues/89
- Twitter 埋め込みウィジェット => done
- CHIRIMEN with node? のスタートアップガイド
    - Headless 省電力SBCとしての RPi Zero W　でつかう　スタートアップガイド
    - https://zenn.dev/kou029w/articles/node-web-gpio
    のZeroW版と、CHIRIMEN RPi用Examplesの簡単移植ガイド

### Next

- TBD

## HackMD
- https://hackmd.io/1ZlW0GasS5CrbEaMux3VHQ

