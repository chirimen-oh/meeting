## 開催日と場所
2019年2月14日　WebDINO Japan

 ## タイムスケジュール
|時間|種別|テーマ|担当者|
|:----:|:----:|:----|:----|
|19:00~19:20|others|自己紹介||
|19:20~19:30|報告|Web×IoT メイカーズチャレンジの情報共有|hiyohiyo/satakagi|
|19:30~19:40|報告|CHIRIMEN for TY51822r3の紹介|hiyohiyo/tadfmac|
|19:40~19:50|報告|WebGPIO etc. via webBT / micro:bit |stakagi|
|19:50~21:30|議論|前回の振り返り方と今後の進め方|dynamis|

## 参加者
* sizuhiko
* t.mitamoto
* gunmaer
* dynamis
* tadfmac
* kohei
* na-sekiguchi
* NishinaTakumi
* hiyohiyo
* satakagi (skype)

## 議題
- Web×IoT メイカーズチャレンジ関連情報共有 (hiyohiyo/satakagi)
  - https://webiotmakers.github.io/
  - https://www.webdino.org/updates/blog/201901270144/
- CHIRIMEN for TY51822r3 の紹介 (hiyohiyo/tadfmac)
  - CHIRIMEN ファミリーとしての承認をいただきたい。
  - https://chirimen.org/chirimen-TY51822r3/
  - JSで制御するBluetoothと基板の勉強会でLT予定 https://html5j-robot.connpass.com/event/117812/
  - issues / WebGPIO, WebI2C (API競合, CHIRIMEN RPi3と共存難)
  - 本家スイッチサイエンスでは売り切れちゃったけど、[協立エレショップ](http://eleshop.jp/shop/g/gG31311/)に5こ在庫あり
- [WebGPIO, etc. sensors, AnalogPIN via WebBT / micro:bit](http://chirimen.org/webGPIO-etc-on-microbit-via-webBluetooth/) (satakagi)
  - issues / WebGPIO (Analog-IN、PWM-OUTが考慮されてないとか)
  - ToDo: Web I2C etc.
  - CHIRIMENファミリーとして承認するには？
  - [動画](https://chirimen-oh.slack.com/files/U0ABYSU2D/FFXBK8VNU/vid_20190205_103056c.mp4)
- 前回の振り返り方と今後の進め方 (dynamis)
  - 前回のミーティングで合意したことの進捗や未実施の内容について改めてどうすすめるか。
  - すでにSlackなどで話しながら随時行われてる、contribドライバやチュートリアルで高度すぎるとの声があるsectionの扱い
  - webの更新をみんなでしやすくするためのシステムなど
  - CHIRIMEN for Raspberry Pi 3のイメージに含めるデフォルトアプリについて
    - VSCodeなど入れたい。

## 議事録

* 自己紹介。
* CHIRIMEN for TY51822r3 について
  * WebGPIO/I2C からアクセスできるファームウェアとそのためのバックエンドを実装
  * チュートリアルも用意されている
  * driver ファイルが CHIRIMEN for Raspi3 と同じ
  * 差分
    * BLE 接続のペアリングはユーザアクションが必ず必要
      * 
    * Raspberry Pi 3 版と同居ができない
      * polifill が競合する
      * navigator.requestGPIOAccess などを別名で定義しておけばいいだけ
      * jQuery のようにデフォルト名以外に専用名を作って、それを個別に使えるようにすれば良い
      * local, ty51822r3, microbit などのオブジェクト毎に作れるようにメイン polyfill を変える
      * それにプラグインする形で各バックエンドを作れば良い
  * 量産方法
    * embed だから usb mass storage 認識しているドライブにファイルを入れるだけ
    * あとはピンヘッダを半田付けする
    * 以上終わり
* CHIRIMEN for micro:bit
  * 先ほどと同じくだけど GPIO だけが使える
  * BLE デバイスとしては唯一入手性が良い。長期的にも良い
  * 2000 円程度で安い
  * LED とかボタンのオンオフとか
  * 現状の実装
    * microBitBLE.requestGPIOAccess 等が生える
    * microBitBLE 配下に microbit 専用のユーティリティ
      * GPIO 以外については取りあえず専用ユーティリティ内の実装だけで放置
      * microbit のドライバー自体が onchange を持っている (advertise)
    * navigator 配下にない場合は navigator. 配下にもはやす
    * 次は requestI2CAccess やろうとしている
  * もう一点の課題
    * micro:bit も embed ベースに作られている
    * ファームウェアは microbit という USB storage デバイスに make code からダウンロードしたコンパイル済みファイルを置いたら動くようになる
  * ドライバーも makecode で作っている
    * [GitHub - chirimen-oh/webGPIO-etc-on-microbit-via-webBluetooth: webGPIO compatible driver for using micro:bit GPIO and other built-in devices via webBluetooth](https://github.com/chirimen-oh/webGPIO-etc-on-microbit-via-webBluetooth)
    * [BLE_t2b - Microsoft MakeCode](https://makecode.microbit.org/73833-86181-26357-25479)
      * 簡単に作っているが、サービスを一杯立ち上げるとメモリが足りない
    * このあたりの関数で地味に作る必要がある [i2c Write Number - Microsoft MakeCode](https://makecode.microbit.org/reference/pins/i2c-write-number) 
      * ついでに各 bluetooth service 類を全部自前で作りこんで軽量化しちゃおうとしている
      * 実際 I2C 以外の部分は完成している
    * makecode 自体も OSS でコンパイルしている方法とかはそこ見れば分かりそう [GitHub - Microsoft/pxt: Microsoft MakeCode (PXT - Programming eXperience Toolkit)](https://github.com/Microsoft/pxt)
      * [pxt/pxtcompiler at master · Microsoft/pxt · GitHub](https://github.com/Microsoft/pxt/tree/master/pxtcompiler) かな？
* makecode 連携
  * makecode の次に CHIRIMEN にアップグレードするように
* CHIRIMEN contrib デバイスのイメージ公開したい
  * contrib の配置を作る
* API v1.1 アップデート
  * navigator 配下に残す or そこからアクセスできる polifill を
  * navigator , microBitBLE, ty51822r3BLE あたり？ を親とした同じ API でどれでも読み込めるようにする
* API v2 アップデート
  * navigator の下よりも WebRTC のように IODevices とかを [MediaDevices - Web API \| MDN](https://developer.mozilla.org/ja/docs/Web/API/MediaDevices) のように作れば綺麗かも
  * permission
    * secure context 対応やユーザ許可については Audio などのものを参考にしていくことになるハズ
  * マルチデバイス対応と無線対応
    * 無線が切れたことを検知するイベント定義などが必要
    * ondevicechange とかを定義して復旧処理とかが作れる
    * 今後お具体的に議論を Web・Slack でしてスケジュールも考えていく
* Web
  * chirimen.org について
    * サイトは書き換えられる人が書き換える
    * 仕様の議論、教育チュートリアルその他全部含む、英語も必要というのは今後も同じ
    * 但し、初心者のチュートリアル求めてきた人が迷子にならないように
    * コミュニティの参加の仕方も迷子にならないように
    * 勝手に作って、こんな感じにしようとしてるって Slack に投げれば良い
    * 既存のソース、ページはアーカイブサイトに移すくらいの対応でも良い
