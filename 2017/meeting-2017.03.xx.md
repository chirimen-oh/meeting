# アジェンダ

## [前回議事録](meeting-2017.02.15.md)

## ◆ CHIRIMEN の コミュニティ活動 について
### CHIRIMEN の github について
#### 完了 issue
* [replace boot logo(Tux) and recovery background(Android robot) with CHIRIMEN logo #114](https://github.com/chirimen-oh/any-issues/issues/114)
* [Web I2C API 品質改善版の本線への反映について #164](https://github.com/chirimen-oh/any-issues/issues/164)
  * releaseに-betaとかつけてimageをアップする。
    * [pre-release](https://github.com/chirimen-oh/release/releases) として配置。 2017.01.20 done
  * releaseレポジトリには、例えば差分のpatchを置いたbranchを作っておくなど、差がわかるようにしておく
  * [CMN2015-1_B2GOS-20170120](https://github.com/chirimen-oh/release/releases/tag/CMN2015-1_B2GOS-20170120)
  * 正式リリース化の検討
  * ブートサニメーションの採択
    * [@kazygumi](https://github.com/kazygumi) さんに作成して頂いたデモを見て採択 => OK
  * 下記手順で 2/24までに終わらせる予定。ご協力よろしくおねがいします！
    * https://github.com/chirimen-oh/any-issues/issues/167 => 2017.03.01 releases!!
* [3/1 release #167](https://github.com/chirimen-oh/any-issues/issues/167)

###  議論 issue
* プロモーションムービ制作
  * インタビュー収録後は、連絡待ち 2016.12.22時点
  * その後、不明　[@dadaa](https://github.com/dadaa) さんに確認
    * HAKUTOさんの扱いは確認中（画像も見てもらっている）。
    * 冒頭の"Mozilla"、(CHIRIMENに関係のない）緑の板が映りこんでいるなどは映像制作会社にコメント済み
    * 冒頭に「このコミュニティは」とあったときにそれが何を差すの変わらないので１クッション欲しい。
    * 出演者の性別・年齢層を幅広く出来たらいいな。
* [Create CHIRIMEN cording style standard #138](https://github.com/chirimen-oh/any-issues/issues/138)
  * js に関しては、mozilla の eslint を使用する
  * 上記 eslint は、CHIRIMEN用カスタマイズ出来る様に空継承をしておく。
    * eslintの使い方がわからない→ドキュメントが必要
    * examplesを書くためのスケルトンを用意すべき→templateというレポジトリを作る
      * 特にindex.htmlは共通化できるんじゃない？
      * 書き方統一の案
        * 単純なサンプルはPromiseで書く
        * 応用的な（複数センサーをつなぐ時など）内容の例としてtask.jsを使用した例を入れて、こんな例もあるよと紹介する。
        * 複数センサーを扱うような場合に課題があるという説明も加えて。
* [Polyfill に関する情報について #125](https://github.com/chirimen-oh/any-issues/issues/125)
  * I2CとGPIOの両方をインクルードするとonChangeが2回発生しちゃう問題→まだ解消していない
  * 別々のワーカーでGPIOとI2Cをやる方向でISSUEを作る [@dadaa](https://github.com/dadaa)
    * https://github.com/club-wot/WebGPIO/issues/22
    * 上記issueで対応していく。（手元でちょっと試した限りは問題なかった [@naokisekiguchi](https://github.com/naokisekiguchi) さん談）
  * クローズの条件をIssueに追記する（[@naokisekiguchi](https://github.com/naokisekiguchi) さん）→追記しました。
* [Hello Real Worldを作る #116](https://github.com/chirimen-oh/any-issues/issues/116)
  * examplesサイトへジャンプできるサイトを。参考：https://tadfmac.github.io/live-examples/
  * 継続中
* [ファームイメージを焼く手順書（mac版） #149](https://github.com/chirimen-oh/any-issues/issues/149)
  * VM経由で焼く方法を手順にまとめる
    * [作成途中](https://github.com/chirimen-oh/chirimen-oh.github.io/issues/70)
  * VirtualBoxのイメージ [@gurezo](https://github.com/gurezo) さん
    * 配布可能状態、リンク公開可能です。
  * Vagrant → Issueにした方が良さそう
    * 手が開いてる人お願いします
  * Macについては仮想環境で対応する
  * 仮想環境とは別に https://github.com/chirimen-oh/CHIRIMEN-tools/issues/1 を実施したので、別途マニュアルを作る。
    * mergeする（上記issueのPR） => 2016.11.19 done
* [B2G/rockdev/ is not for CMN2015-1 #112](https://github.com/chirimen-oh/any-issues/issues/112)
  * [@naobsd](https://github.com/naobsd) さん、よろしくお願いします
* [電子情報通信学会の東京支部教育イベントの公募](https://github.com/chirimen-oh/any-issues/issues/153)
  * フィードバック共有
  * 締め切り 11/11に申し込み済み。
  * ゲームパッド（ハードとソフト）をカリキュラム内容にする
  * 調整中 => 採択された。
    * [@naokisekiguchi](https://github.com/naokisekiguchi) さんがまとめて事務手続きします。
    * 8月頃開催予定
* [Web I2C APIの仕様で定義されているAPIが足りない #156](https://github.com/chirimen-oh/any-issues/issues/156)
  * PRに解説の図を追記する[@MSakamaki](https://github.com/MSakamaki)
* [Proposal for alliance #157](https://github.com/chirimen-oh/any-issues/issues/157)
  * 2017.1.4 回答 反応なし
  * 2017.2.16 close後、コメントあり
  * 2017.3.10 reopen
* [CHIRIMENの次期量産販売について #160](https://github.com/chirimen-oh/any-issues/issues/160)
* Web X IoT ハッカソン
  * [サイト公開](https://browserobo.github.io/hackathon2017/)
* [GitHubやSlackの国際化 #162](https://github.com/chirimen-oh/any-issues/issues/162)
  * issueのタイトルだけ英語で書くくらいから始めてみる
* [WebGPIO/WebI2C Polyfillの chirimen-ohへのforkについて #165](https://github.com/chirimen-oh/any-issues/issues/165)
  * [@MSakamaki](https://github.com/MSakamaki)さんのご意見を聞かないと => コメント頂いた。
  * リリース版には対応したPolyfillを含める

### CHIRIMEN の 主体のイベント活動 について
* 現状保留
  * [ 企業を含む各種団体からの後援・賛同・貢献について #47  ](https://is.gd/y9GQVO)
  * [ イベントなどに対するプレス対応について #48  ](https://is.gd/03PdBo)
  * 金銭情報管理
* [replacement for CMN2015-1 OS #147](https://github.com/chirimen-oh/any-issues/issues/147 )
  * 各自知見を得たものをこのissueに追記する。
  * [radxaさんのイメージダウンロードリンク](http://wiki.radxa.com/Rock/prebuilt_images )
  * 優先度低 & 継続
  * 現状保留
* [セルフ開発環境の構築 #140](https://github.com/chirimen-oh/any-issues/issues/140)
  * ソフトウェアキーボードが課題
  * [marsf](https://github.com/marsf) さん [のソース(ソフトウェアキーボード非表示)を活用](https://github.com/marsf/Phantom-keyboard)
  * 他教育機関で使えるように調整中
  * 優先度低 & 継続
  * 現状保留
* [CHIRIMENの販売に関してOPENで情報共有するチャンネルのリンク、誘導をホームページに置く #151](https://github.com/chirimen-oh/any-issues/issues/151)
  * 定期チャンネル案内のGoogle Action Scriptをgithubで管理する
    * 自動連携（Google Action Scriptのソース管理をgithubで、連携する）
    * リポジトリを作ってREADMEを置く[@gurezo](https://github.com/gurezo) done.
* [GPIOの入力をキーボード（のキー）にバインドする機能 #130](https://github.com/chirimen-oh/any-issues/issues/130)
  * 優先度低 & 継続
  * 現状保留

## コミュニティ・イベント活動のマイルストーン（暫定）
### 2017年
* 1 月
  * 28日：[CHIRIMEN タッチ ＆ トライ イベント](https://chirimen-oh.connpass.com/event/47706/)事前準備-済
* 2 月
  * 04日：[CHIRIMEN タッチ ＆ トライ イベント](https://chirimen-oh.connpass.com/event/47706/)-済
  * 18日：NTT ICCでのトークイベント-済
* 3月
  * 02日：[学生向け Web X IoT ハッカソン 事前イベント](https://connpass.com/event/49593/)-済
  * 03日：[学生向け Web X IoT ハッカソン 事前イベント](https://connpass.com/event/49593/)-ト-済
  * 11日：[学生向け Web X IoT ハッカソン 事前イベント](https://connpass.com/event/49593/)-ト-済
  * 18日：[Web X IoT ハッカソン](https://browserobo.github.io/hackathon2017/)
  * 19日：[Web X IoT ハッカソン](https://browserobo.github.io/hackathon2017/)
* 8月
  * 05日：Maker Faire Tokyo 2017(初日)
  * 06日：Maker Faire Tokyo 2017(最終日)


## その他
* [議論メモ 01/19](https://public.etherpad-mozilla.org/p/chirimen-20170119)
* [議論メモ 02/15](https://public.etherpad-mozilla.org/p/chirimen-20170215)
