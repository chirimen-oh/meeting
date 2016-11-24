# アジェンダ（実施前）

## [前回議事録](meeting-2016.11.08.md)

## ◆ CHIRIMEN の コミュニティ活動 について
### CHIRIMEN の github について
#### 完了 issue
* CHIRIMEN のブランド利用について申請について（[kimono](https://github.com/chirimen-oh/Cases/tree/master/kimono)）
* [Ubuntu環境でイメージ生成に失敗する #144](https://github.com/chirimen-oh/any-issues/issues/144)
* [fixed chirimen-oh/any-issues#144 #3](https://github.com/chirimen-oh/CHIRIMEN-tools/pull/3)
* [Mac OSX用バイナリ #2](https://github.com/chirimen-oh/CHIRIMEN-tools/pull/2)
* [Prepare a youtube channel for sharing CHIRIMEN demo #155](https://github.com/chirimen-oh/any-issues/issues/155)
  * [youtube チャンネル](https://www.youtube.com/channel/UCd7PtdviaJeHfMMFeszx06A)
* [Proposal #150](https://github.com/chirimen-oh/any-issues/issues/150)

###  議論 issue
* プロモーションムービ制作
  * 今年中につくるぞー
  * 専門学校の学生さんに聞いてみる
* [CHIRIIMENボードのOSについて #147](https://github.com/chirimen-oh/any-issues/issues/147)
  * 各自知見を得たものをこのissueに追記する。
  * [radxaさんのイメージダウンロードリンク](http://wiki.radxa.com/Rock/prebuilt_images)
* [ライセンスに関する検証  #148](https://github.com/chirimen-oh/any-issues/issues/148)
  * CHIRIMEN Open Hardware利用規約 第一版より
    * [基本的に問題なし
    * http://www.oshwa.org/definition/japanese/
    * [oshwa へ申請](http://certificate.oshwa.org/get-certified/)
      * 担当：[@gurezo](https://github.com/gurezo)
* [[12/3-4] Ogaki Mini Maker Faire 2016 #146](https://github.com/chirimen-oh/any-issues/issues/146)
* [セルフ開発環境の構築 #140](https://github.com/chirimen-oh/any-issues/issues/140)
  * ソフトウェアキーボードが課題
  * [marsf](https://github.com/marsf) さん [のソース(ソフトウェアキーボード非表示)を活用](https://github.com/marsf/Phantom-keyboard)
* [Create CHIRIMEN cording style standard #138](https://github.com/chirimen-oh/any-issues/issues/138)
  * js に関しては、mozilla の eslint を使用する
  * 上記 eslint は、CHIRIMEN用カスタマイズ出来る様に空継承をしておく。
* [専門学校東京テクニカルカレッジの授業協力 #136](https://github.com/chirimen-oh/any-issues/issues/136)
* [GPIOの入力をキーボード（のキー）にバインドする機能 #130](https://github.com/chirimen-oh/any-issues/issues/130)
* [Polyfill に関する情報について #125](https://github.com/chirimen-oh/any-issues/issues/125)
  * I2CとGPIOの両方をインクルードするとonChangeが2回発生しちゃう問題→まだ解消していない
  * 別々のワーカーでGPIOとI2Cをやる方向でISSUEを作る [@dadaa](https://github.com/dadaa)
    * https://github.com/club-wot/WebGPIO/issues/22
* [Hello Real Worldを作る #116](https://github.com/chirimen-oh/any-issues/issues/116)
  * 継続
* [replace boot logo(Tux) and recovery background(Android robot) with CHIRIMEN logo #114](https://github.com/chirimen-oh/any-issues/issues/114)
* [ファームイメージを焼く手順書（mac版） #149](https://github.com/chirimen-oh/any-issues/issues/149)
  * vm経由で焼く方がスマートでないか（macのバージョン毎に対応するのは非常に手間がかかるので）
  * VM経由で焼く方法を手順にまとめる
  * VirtualBoxのイメージ [@gurezo](https://github.com/gurezo) さん
  * Vagrant → Issueにした方が良さそう
  * Macについては仮想環境で対応する
  * 仮想環境とは別に https://github.com/chirimen-oh/CHIRIMEN-tools/issues/1 を実施したので、別途マニュアルを作る。
    * mergeする（上記issueのPR）。
* [B2G/rockdev/ is not for CMN2015-1 #112](https://github.com/chirimen-oh/any-issues/issues/112)
* [電子情報通信学会の東京支部教育イベントの公募](https://github.com/chirimen-oh/any-issues/issues/153)
  * 締め切り 11/11に申し込み済み。
  * ゲームパッド（ハードとソフト）をカリキュラム内容にする
* [CHIRIMENの販売に関してOPENで情報共有するチャンネルのリンク、誘導をホームページに置く #151](https://github.com/chirimen-oh/any-issues/issues/151)
  * 新しいチャンネルを作った場合に、どういう風に共有するか？
    * 告知場所
      * #general
      * ピン留する
      * 告知期間：１週間
  * 定期チャンネル案内のGoogle Action Scriptをgithubで管理する
    * 自動連携（Google Action Scriptのソース管理をgithubで、連携する）
* [Web I2C APIの仕様で定義されているAPIが足りない #156](https://github.com/chirimen-oh/any-issues/issues/156)
* [Proposal for alliance #157](https://github.com/chirimen-oh/any-issues/issues/157)

### CHIRIMEN の 主体のイベント活動 について
* 現状保留
  * [ 企業を含む各種団体からの後援・賛同・貢献について #47  ](https://is.gd/y9GQVO)
  * [ イベントなどに対するプレス対応について #48  ](https://is.gd/03PdBo)
  * 金銭情報管理

## コミュニティ・イベント活動のマイルストーン（暫定）
* 04 月
 * 30日：済-CHIRIMEN Open Hardware Open Source化
* 06 月
 * 08日：済-Interop Tokyo 2016(初日)
 * 09日：済-Interop Tokyo 2016(二日目)
 * 10日：済-Interop Tokyo 2016(最終日)
* 07 月
 * 30日：済-NodeBots Day 2016 for Tokyo
* 08 月
 * 06日：済-Maker Faire Tokyo 2016(初日)
 * 07日：済-Maker Faire Tokyo 2016(最終日)
 * 26日：済-takram brew 展示
* 09 月
  * 03日：済-中央大学生向け、集中オープンプロジェクト演習
  * 10日：済-中央大学生向け、集中オープンプロジェクト演習
  * 17日：済-中央大学生向け、集中オープンプロジェクト演習
  * 17日：済-CHRIMEN Board 発売記念イベント
* 10 月
* 11 月
  * 04日：[専門学校東京テクニカルカレッジの授業協力 #136](https://github.com/chirimen-oh/any-issues/issues/136)
  * 05日：[OSC Tokyo 2016 Fall 初日 展示のみ？](www.ospn.jp/osc2016-fall/)
  * 06日：[OSC Tokyo 2016 Fall 最終日 展示のみ？](www.ospn.jp/osc2016-fall/)
  * 11日：[専門学校東京テクニカルカレッジの授業協力 #136](https://github.com/chirimen-oh/any-issues/issues/136)
  * 18日：[Open Research Forum 2016](http://orf.sfc.keio.ac.jp/2016/)
  * 18日：[専門学校東京テクニカルカレッジの授業協力 #136](https://github.com/chirimen-oh/any-issues/issues/136)
  * 19日：[Open Research Forum 2016](http://orf.sfc.keio.ac.jp/2016/)
  * 25日：[専門学校東京テクニカルカレッジの授業協力 #136](https://github.com/chirimen-oh/any-issues/issues/136)
* 12 月
  * 02日：[専門学校東京テクニカルカレッジの授業協力 #136](https://github.com/chirimen-oh/any-issues/issues/136)
  * 03日：[Ogaki Mini Maker Faire 2016](http://ommf.iamas.ac.jp/)
  * 04日：[Ogaki Mini Maker Faire 2016](http://ommf.iamas.ac.jp/)
  * 09日：[専門学校東京テクニカルカレッジの授業協力 #136](https://github.com/chirimen-oh/any-issues/issues/136)
  * xx日：B2G OS ビルドもくもく会
  * xx日：各種センサー味見会

## 出展可能性のあるイベント候補
* w/ fabcafe
* ICC (w/ 明治大渡辺先生）

## その他
* [議論メモ 07/02](https://public.etherpad-mozilla.org/p/chirimen-20160702)
* [議論メモ 07/26](https://public.etherpad-mozilla.org/p/chirimen-20160726)
* [議論メモ 08/08](https://public.etherpad-mozilla.org/p/chirimen-20160808)
* [議論メモ 09/06](https://public.etherpad-mozilla.org/p/chirimen-20160906)
* [議論メモ 10/11](https://public.etherpad-mozilla.org/p/chirimen-20161011)
* [議論メモ 11/08](https://public.etherpad-mozilla.org/p/chirimen-20161108)
* [議論メモ 12/xx](https://public.etherpad-mozilla.org/p/chirimen-201612xx)
