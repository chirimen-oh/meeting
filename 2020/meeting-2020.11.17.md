# CHIRIMEN meeting 202011

## 開催日と場所
2020年11月17日 Zoom

## タイムスケジュール
|時間|種別|テーマ|担当者|
|:----:|:----:|:----|:----|
|19:30~19:35|議論|挨拶|-|
|19:35~20:05|議論|デバイスについて|-|
|20:05~20:35|議論|技術書典|-|
|20:35~21:00|議論|BOOTHオンラインショップ|-|
|21:00~21:30|議論|公式サイト|-|

## 参加者 (alphabetical order)

- chibi
- eri
- dynamis
- kigure
- kodama
- miyamoto
- naoki
- stagaki
- sizuhiko
- watanabe

## 議題

### WIMC 2020
- 今年度は総務省主催で 6 地域 + 自立開催地域 2 地域 = 8 地域開催
- https://webiotmakers.github.io/2020/
- 緊急事態宣言あたりで、従来型の開催では密なイベントなので対応を議論
- オンラインを上手く活用して実施する方法を各地域毎に模索して実施
- 5 月頃は完全オンライン対応を可能にすることを想定して議論
- しかし RasPi とモニター等一式を各自自宅に配送するのは無理がある
- micro:bit 版のチュートリアルの充実化を目指し、それを利用することを検討
- satoru さん中心にチュートリアルの micro:bit 版を追加、一部地域で採用
- https://tutorial.chirimen.org/microbit/
- 主催する県ごとにコロナ対応の方針には差があり、各地域の運営委員会で方針決定
- 完全オンライン: 石川、徳島
    - 全員自宅から参加、講習会、ハッカソン共に自宅から参加
- 一部オンライン: 信州 etc...
    - 10 人前後までを広めの部屋に分散させ、遠隔で繋いで実施
    - 地域のスペースや学校などを利用して数名程度の最小限の現地
    - マスク、検温、体調チェックシート、飲食ゼロなどなどの対応
- CHIRIMEN 利用地域
    - micro:bit 徳島、信州...
    - RasPi: 岡山、鳥取？...

### 大学での利用
- 中央大学 (microbit)、慶応大学 (raspi) の講義にて利用

### デバイスについて
- micro:bit 版
    - 十分安定してイベントで利用できるようになってきた
- Raspberry Pi 3A
    - https://www.raspberrypi.org/products/raspberry-pi-3-model-a-plus/
    - 512MB しかないが一応動くハズ
    - サンプルボードを購入したけど誰もテストしてない
    - 検証担当者募集
    - ぐんまーさんが検証して Advent Calendar に書く！
        - WD から 1 台貸し出し
- Raspberry Pi 400
    - https://www.elektormagazine.com/news/raspberry-pi-400-review
      ![](https://www.elektormagazine.com/assets/upload/images/28/20201102173325_RPI-400-TOP-DOWN-REAR-WHITE-s.jpg)
      ![](https://www.elektormagazine.com/assets/upload/images/28/20201102174003_raspberry-pi-400-insides.jpg)
    - 技適通過・日本語キーボードがでたら購入、検証したい
- [CrowPi2 - Raspberry Pi Laptop & STEM Education Platform](https://www.kickstarter.com/projects/elecrow/crowpi2-steam-education-platformand-raspberry-pi-laptop)
    - ぐんまーさんの手元に届いたらどの程度使えるか試してみる
- [CutiePi Tablet - Raspberry Pi, Untethered](https://www.kickstarter.com/projects/745629624/cutiepi-raspberry-pi-untethered)

### Node 版
- https://github.com/chirimen-oh/node-web-gpio
- https://github.com/chirimen-oh/node-web-i2c
- ちゃんと使える、紹介ページを作りたい、作って欲しい、いや、既にある
- https://tutorial.chirimen.org/raspi/nodejs
- Advent Calendar に書くと良いのでは！
    - [CHIRIMEN Open Hardware Advent Calendar 2020](https://qiita.com/advent-calendar/2020/chirimen_oh?fbclid=IwAR15IoMF7xLMILdGWleiKfHBYMA0U5dwQRsoq6x0J4VPTJITxtKj3TL-IMc)


### やりたいこと
- OS update 版を作りたい
    - 最新イメージでセットアップスクリプト実行 & フルテストボードで一通り検証
    - https://www.raspberrypi.org/software/
    - Raspberry Pi OS ? Ubuntu ?
    - 宮本さんの既存スクリプトを修正しつつ PiOS 対応、その後 Ubuntu もやるか
        - やる気、やる人募集中
    - 既存の手順 https://github.com/chirimen-oh/chirimen/wiki/Release
    - https://github.com/chirimen-oh/chirimen/wiki/Release-Checklist
- RasPi 公式サイトに OS イメージを載せて貰いたい
    - 再度問い合わせ（グンマー）

### スターターキット
- raspi3 向けから chirimen 一般の名称に変えて使ってる
    - スターターキット + microsd はオプション 500円
- ADT7410 から SHT30 に変更
- 在庫は多くはないが少しある

### オンラインイベント

- todo リストを消化する日を作ろう
    - OS update
    - ドキュメント更新
    - web site
- スターターキットで講習会
    - booth なりスイッチサイエンスなりで買って貰って参加して貰えば良いのでは
    - スターターキットじゃ無くとも同様のモノを用意して参加して貰う
- 今年に計画して年明けくらい？
    - イベントページドラフト書いてまた適当なタイミングで実施を検討
    - 参加に必要なものの手配をどうして貰うかなどもイベントページ書きつつ考える
    - ドラフトはぐんまーさんが書いてくれるのでそれをベースに議論
    - 1月中旬〜2 月くらいで実施？

### 技術書典

- 技術書典8報告 
- 技術書典9報告 
- 技術書典10相談
    - 既巻は出す
    - 新刊が出せるのかは調整

### BOOTH オンラインショップ

- 出店について
- Pixiv の BOOTH ショップ用意した！
    - 承認して！承認した！？
- 売上げ
    - 4 月に 8000 円の売上げ、11 月頭に技術書典 8 で売上げ発生
    - 1000 - 430 (技術書典手数料) = 570 / 冊
- 振込先
    - WebDINO で受ける口座を用意してそちらに設定したい
    - 技術書典同様に入ってくるという認識で WebDINO 側は了承済み
- 扱う商品
    - 書籍
- 検討中
    - 本だけじゃ無くてスターターキットなども売りたい？
        - 取りあえず 20 セットくらい入れられると良い気がする
        - 材料費を WebDINO のコミュニティ支援費で出すことも可能
    - その他
        - 全部のせボート！ (の基盤と部品セット)、neopixel driver?
        - 組立済みを 1 万くらいで売るの？(笑)いや...
    - イベント限定販売の保管くらいで、新規で作ってまで売るほどではない？
    - ハードウェアの売り先としては booth という感じでは無い？
- Status/Next
    - 在庫が数点はあるのでスターターキットや全部乗せセット数点なら出せる
    - イベントに合わせてまた作るときがあればその時に多めに作って販売開始すればよいのではないか
- リサーチ
    - 期間販売ができるかどうか？
        - スイッチサイエンス
        - Booth

### 公式サイト

- サイトデザイン
- サイト構築用のチャンネル: #webdev
- サイトの雰囲気
    - 日英併記はよろしくないね
    - 中華ハードウェア屋さんっぽい
    - WIMC のサイトくらいの、愉しくプロトタイピング感がある方が良い
- 既存の情報
    - 赤 CHIRIMEN
        - トップなどから辿れる必要は無い、アーカイブとしておけば良い
    - チュートリアルメインの導線に切り替えるだけからスタートで良い
    - chirimen.org のトップをチュートリアル誘導メインにするとか
    - DNS 設定で tutorial に、既存のをアーカイブサブドメインにして
        - 赤塚さんに設定切替をお願いする
    - いや、まずはチュートリアルサイト(https://tutorial.chirimen.org/)を chririmen.org にする
        - https://tutorial.chirimen.org/ => https://chirimen.org/
    - その上で対応していけば良い
    - 2019 チュートリアルアーカイブ: https://webiot-2019--tutorial-chirimen-org.netlify.app/raspi/
    - chirimen.org も netlify.app のサブドメインでアーカイブホストしよう
- チュートリアル
    - raspi/microbit 間の移動が分かりにくい
    - その他、チュートリアルをトップサイトとして大丈夫なようにしてみる？
- イラスト素材
    - イメージキャラクターは github にある
        - アクセントとして上手く使おう
        - https://github.com/chirimen-oh/technical-book8/tree/master/image
    - コミュニティ感の出る写真とかを素材に出来る
    - gdrive にある気がするので探して webdev チャンネルに貼る
    - 

### Next

- 12 月中頃くらいで調整さん
