# アジェンダ

## [前回議事録](meeting-2016.10.11.md)

## ◆ CHIRIMEN の コミュニティ活動 について
### CHIRIMEN の github について
#### 完了 issue
* [B2GOS & Chirimen Collaboration](https://discourse.mozilla-community.org/t/b2gos-chirimen-collaboration/10749)
* [イベント用資材の管理・運用 #142](https://github.com/chirimen-oh/any-issues/issues/142)
* [chirimen-oh organization に contributor team とか作る？ #132](https://github.com/chirimen-oh/any-issues/issues/132)

###  議論 issue
* 発売記念収支報告
  * 金銭情報管理は、現状保留
* プロモーションムービ制作
  * 今年中につくるぞー
  * 専門学校の学生さんに聞いてみる
* CHIRIMEN のブランド利用について申請について（[kimono](https://github.com/chirimen-oh/Cases/tree/master/kimono)）
 * `CHIRIMEN` という名前を使うのに異論があるか？
  * 承認 === OK！
 * バージョンアップを予定している（ロゴ：コード名やピンアサインなど）
* [CHIRIIMENボードのOSについて #147](https://github.com/chirimen-oh/any-issues/issues/147)
  * 各自知見を得たものをこのissueに追記する。
  * [radxaさんのイメージダウンロードリンク](http://wiki.radxa.com/Rock/prebuilt_images)  
* [ライセンスに関する検証  #148](https://github.com/chirimen-oh/any-issues/issues/148)
  * CHIRIMEN Open Hardware利用規約 第一版より
    * 「MJから」の部分を変える必要がありそう
    * 「本コミュニティ」の部分を変える必要がありそう
    * 「本コミュニティ及びMJ」の部分を変える必要がありそう
    * 次のリンクを読んでおく http://certificate.oshwa.org/
    * 別途オンラインMTGで、ライセンスに関する議論をする場を設ける。
    * [@kudodo](https://github.com/kudodo) さん交えて、議論
      * [基本的に問題なしです
      * [「同じライセンスの下で」という翻訳は、原文だと「同じ条件の下で」の方が意味として正しく、問題ないだろうという解釈
      * http://www.oshwa.org/definition/japanese/
    * [oshwa へ申請](http://certificate.oshwa.org/get-certified/)
      * 担当：[@gurezo](https://github.com/gurezo)
* [[12/3-4] Ogaki Mini Maker Faire 2016 #146](https://github.com/chirimen-oh/any-issues/issues/146)
  1. チラシの確保（2-300枚程度。枚数確認）
    * 現在の在庫状況
    * チラシは300枚
    * シールは100枚強
  1. パネルも余ってたら貸してください。
    * インターロップのもの→破棄
    * 別途作ったもの ->確認 [@kotakagi](https://github.com/kohichi000000)
  1. 展示作品募集中です。MAX机半分使えます。
    * 11/18くらいまでに出展の意思表示をgithubの方にエントリー
  1. 当日説明員対応いただける方も募集中です。12/3 12/4 いずれかのみでも助かります。こちらは直前でも大丈夫ですが泊まりの場合、ホテル早目に予約した方が良いと思います。
    * [@gurezo](https://github.com/gurezo) : 12/3午後から12/4終日
    * [@dadaa](https://github.com/dadaa) : 12/3?
    * [@tadfmac](https://github.com/tadfmac) : 両日終日
    * [@WhiteHawk-taka](https://github.com/WhiteHawk-taka) : 参加予定 詳細は不明
    * まだまだ募集中。
  1. 出展社マニュアルまだ -> 11/18到着
    * slack [#ogaki_mini_maker_fair](https://chirimen-oh.slack.com/archives/ogaki_mini_maker_fair) 参照
* [セルフ開発環境の構築 #140](https://github.com/chirimen-oh/any-issues/issues/140)
  * ソフトウェアキーボードが課題
  * [marsf](https://github.com/marsf) さん [のソース(ソフトウェアキーボード非表示)を活用](https://github.com/marsf/Phantom-keyboard)
* [Create CHIRIMEN cording style standard #138](https://github.com/chirimen-oh/any-issues/issues/138)
* [専門学校東京テクニカルカレッジの授業協力 #136](https://github.com/chirimen-oh/any-issues/issues/136)
  * 開発中の受講システム環境が整ったら、協力者にトライアルのお願いをする。
* [GPIOの入力をキーボード（のキー）にバインドする機能 #130](https://github.com/chirimen-oh/any-issues/issues/130)
* [Polyfill に関する情報について #125](https://github.com/chirimen-oh/any-issues/issues/125)
  * ディレクトリ構成（bower_componentsの見直し）
  * url指定で、サイトを動くようにしたい。（index.htmlだけで動くようにしたい）
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
* [Ubuntu環境でイメージ生成に失敗する #144](https://github.com/chirimen-oh/any-issues/issues/144)
  * Ubuntu 14.04は推奨ビルド環境です。issueに記載の通り.shのバグです。
    * [@dadaa](https://github.com/dadaa) さんが修正、PR済み
* [B2G/rockdev/ is not for CMN2015-1 #112](https://github.com/chirimen-oh/any-issues/issues/112)
* [電子情報通信学会の東京支部教育イベントの公募](https://github.com/chirimen-oh/any-issues/issues/153)
  * 締め切り 11/11に申し込み済み。
* [Proposal #150](https://github.com/chirimen-oh/any-issues/issues/150)
* [CHIRIMENの販売に関してOPENで情報共有するチャンネルのリンク、誘導をホームページに置く #151](https://github.com/chirimen-oh/any-issues/issues/151)
  * 新しいチャンネルを作った場合に、どういう風に共有するか？→ #general で当該情報（何？）をピンうち
  * #general: 最初に入る場所じゃ！
  * 定期チャンネル案内のGoogle Action Scriptをgithubで管理する
    * 自動連携（Google Action Scriptのソース管理をgithubで、連携する）

### CHIRIMEN の 主体のイベント活動 について
* 現状保留
  * [ 企業を含む各種団体からの後援・賛同・貢献について #47  ](https://is.gd/y9GQVO)
  * [ イベントなどに対するプレス対応について #48  ](https://is.gd/03PdBo)

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
  * 05日：[OSC Tokyo 2016 Fall 初日 展示のみ？](www.ospn.jp/osc2016-fall/)
  * 06日：[OSC Tokyo 2016 Fall 最終日 展示のみ？](www.ospn.jp/osc2016-fall/)
  * 18日：[Open Research Forum 2016](http://orf.sfc.keio.ac.jp/2016/)
  * 19日：[Open Research Forum 2016](http://orf.sfc.keio.ac.jp/2016/)
  * xx日：B2G OS ビルドもくもく会
  * xx日：各種センサー味見会
* 12 月
  * 03日：[Ogaki Mini Maker Faire 2016](http://ommf.iamas.ac.jp/)
  * 04日：[Ogaki Mini Maker Faire 2016](http://ommf.iamas.ac.jp/)

## 出展可能性のあるイベント候補
* w/ fabcafe
* ICC (w/ 明治大渡辺先生）
* 東京テクニカルカレッジ授業(2016/11/4~12/9,毎週金13:00~16:00)

## その他
* [議論メモ 07/02](https://public.etherpad-mozilla.org/p/chirimen-20160702)
* [議論メモ 07/26](https://public.etherpad-mozilla.org/p/chirimen-20160726)
* [議論メモ 08/08](https://public.etherpad-mozilla.org/p/chirimen-20160808)
* [議論メモ 09/06](https://public.etherpad-mozilla.org/p/chirimen-20160906)
* [議論メモ 10/11](https://public.etherpad-mozilla.org/p/chirimen-20161011)
* [議論メモ 11/08](https://public.etherpad-mozilla.org/p/chirimen-20161108)
* 専門学校のオンラインチューター支援構想
  * 支援者のスケジュールを決めていきたい => [専門学校東京テクニカルカレッジの授業協力 #136](https://github.com/chirimen-oh/any-issues/issues/136)
