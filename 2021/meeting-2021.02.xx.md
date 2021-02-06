# CHIRIMEN meeting 202101

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
  - https://github.com/chirimen-oh/chirimen/releases/tag/20210106
  - MVP 宮本君に感謝！
      - コミュニティ全員からの熱い賛辞が送られた！
  - 64bit OS Image には Node 非互換がある。これは今後の課題 (今のところ対応・リリースを決めてはいない)
  - あるセンサーだけ未検証
  - フルテストボードのお披露目の機会を考える

* chirimen-drivers
  * ES Module
      * https://chirimen.org/chirimen-drivers/CONTRIBUTING
      * 変換後 JS は取り除き自動ビルドになった
      * リポジトリには EMS の .js ファイルのみとなっている (.mjs から .js に拡張子は変更した)
          * .mjs では content-type 問題などもありがちだったため、過渡期的の拡張子は止めて .js に
      * 変換後のファイルの利用は自動 publish されているものを使えば良い
  * Examples引っ越し
      * 環境毎のディレクトリに引っ越しを行った:
          * https://github.com/chirimen-oh/chirimen-drivers/tree/master/raspi-examples
          * https://github.com/chirimen-oh/chirimen-drivers/tree/master/node-examples
          * https://github.com/chirimen-oh/chirimen-drivers/tree/master/microbit-examples/ccs811
  * 行動規範
      * [前回のミーティングで決めたもの](https://hackmd.io/@ukzioj9rSYutR9JNZjaZAg/SJrziae3P) を掲載する
      * コミュニティ: chirimen.org サイト上にページ作成・掲載する
         * http://www.association.droidkaigi.jp/code-of-conduct.html ベースに
     * コード貢献: 専用リポジトリに入れる
         * https://docs.github.com/ja/free-pro-team@latest/github/building-a-strong-community/adding-a-code-of-conduct-to-your-project
* microbit
  * V2　公式サポート
      * V1 (v1.5) サポート継続
      * MVP: 本家 MakeCode の対応も即時されて問題解決。無事 V2 サポートが可能になった
      * V2 ではヒープが大きくなったのでメモリの心配もない
  * PWM API
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



### BOOTH オンラインショップ
- 公開しました。
- https://chirimen-oh.booth.pm/

### オンラインイベント
- もくもく会 on 02/xx (土)
    - で想定していたが 2/6 (土) に開催に
- イベントページ準備中
  - https://chirimen-oh.connpass.com/event/198924/preview/
    - 始めてさん枠向けの貸し出し申し込みフォーム
- WIMC slack #general などに案内を流す
    - by ぐんまーさん

### サポートデバイス
- Pi 400 はリリース待ち
- Pi 3A+ はぐんま—さんに送って確認して貰う
- PiZeroW
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
- Twitter 埋め込みウィジェット
    - 公式のを埋め込めば良いハズ
    - タイムライン埋め込みか何かを入れましょう

### Next

- TBD

## HackMD
- https://hackmd.io/1ZlW0GasS5CrbEaMux3VHQ

