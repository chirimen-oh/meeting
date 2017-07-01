# アジェンダ(実施前)

## [前回議事録](meeting-2017.05.25.md)

## ◆ CHIRIMEN の コミュニティ活動 について
### CHIRIMEN の github について
#### 完了 issue
- [Enrty of Android Bazaar and Conference 2017 Spring #185](https://github.com/chirimen-oh/any-issues/issues/185)

###  議論 issue
- [IEEE Tokyo Young Professionals hackathon (7/8-9) #187](https://github.com/chirimen-oh/any-issues/issues/187)
- [Enrtry of Maker Faire Tokyo 2017 #184](https://github.com/chirimen-oh/any-issues/issues/184)
- [Information of Web x IoT Hackthon Events is Sharing #171](https://github.com/chirimen-oh/any-issues/issues/171)
- [電子情報通信学会の東京支部教育イベントの公募](https://github.com/chirimen-oh/any-issues/issues/153)
- [CHIRIMEN Open Hardware Terms of Use For License #190](https://github.com/chirimen-oh/any-issues/issues/190)
- [CHIRIMENの次期量産販売について #160](https://github.com/chirimen-oh/any-issues/issues/160)
- [Create CHIRIMEN cording style standard #138](https://github.com/chirimen-oh/any-issues/issues/138)
  - js に関しては、mozilla の eslint を使用する
  - 上記 eslint は、CHIRIMEN用カスタマイズ出来る様に空継承をしておく。
    - eslintの使い方がわからない→ドキュメントが必要
    - examplesを書くためのスケルトンを用意すべき→templateというレポジトリを作る
      - 特にindex.htmlは共通化できるんじゃない？
      - 書き方統一の案
        - 単純なサンプルはPromiseで書く
        - 応用的な（複数センサーをつなぐ時など）内容の例としてtask.jsを使用した例を入れて、こんな例もあるよと紹介する。
        - 複数センサーを扱うような場合に課題があるという説明も加えて。
    - 適用範囲→examples, polyfill
- [WebGPIO/WebI2C Polyfillの chirimen-ohへのforkについて #165](https://github.com/chirimen-oh/any-issues/issues/165)
  - fork done at 30 March.
  - ドキュメントやexamples等のリンク修正が残
- [Web I2C APIの仕様で定義されているAPIが足りない #156](https://github.com/chirimen-oh/any-issues/issues/156)
  - PRに解説の図を追記する[@MSakamaki](https://github.com/MSakamaki)
- [Polyfill に関する情報について #125](https://github.com/chirimen-oh/any-issues/issues/125)
  - chirimenクイックスタートのリンクを修正して、close
- プロモーションムービ制作
  - 進捗なし
- [720Pなど、他の解像度への対応 #178](https://github.com/chirimen-oh/any-issues/issues/178)
  - chirimen-oh/linux-rockchip@f7c32cb frame bufferを1280x720にしました [@naobsd](https://github.com/naobsd)さん
- [security enhancement of Web GPIO API / Web I2C API #177](https://github.com/chirimen-oh/any-issues/issues/178)
- [ADCの例をexamplesにあげる。そして提供する部品と作例を一致させる (次のハッカソンに向けて) #174](https://github.com/chirimen-oh/any-issues/issues/174)
- [Arrangement of a document doesn't catch up. #173](https://github.com/chirimen-oh/any-issues/issues/173)
  - 起こったこと：
    1. fabbleの記事が古くて、古いPolyfillを入れちゃう問題が発生
    2. examplesが過去の全ての作例に対応できてなくて、古い MozOpenHardリポジトリの作例を引用する場面が
    3. もともとfabbleに集約していたものが、fabbleの障害によりQiitaやgistなどにドキュメントが発散したけど
       fabble側がその後復旧、しかし情報が複数の場所にコピーされた結果、もともとのfabble側の更新が追いつかない事態に。
    4. `bower install` で入るPolyfillが新しくなれば解決する部分はあるけど、そもそもドキュメントの
       メンテナンスどうやっていくか? という問題にも波及する話。
  - 提案
  　- 直近の作業は下記の通り
  　- fabbleで重複記事をQiitaやgistに移したものは消す (重複をなくす意味で)
    - MozOpenHard側のexamplesもChirimen-Ohに移して消す

### CHIRIMEN の 主体のイベント活動 について
- 現状保留
  - [ 企業を含む各種団体からの後援・賛同・貢献について #47  ](https://is.gd/y9GQVO)
  - [ イベントなどに対するプレス対応について #48  ](https://is.gd/03PdBo)
  - 金銭情報管理
- [replacement for CMN2015-1 OS #147](https://github.com/chirimen-oh/any-issues/issues/147 )
  - 各自知見を得たものをこのissueに追記する。
  - [radxaさんのイメージダウンロードリンク](http://wiki.radxa.com/Rock/prebuilt_images )
  - 優先度低 & 継続
  - 現状保留
- [セルフ開発環境の構築 #140](https://github.com/chirimen-oh/any-issues/issues/140)
  - ソフトウェアキーボードが課題
  - [marsf](https://github.com/marsf) さん [のソース(ソフトウェアキーボード非表示)を活用](https://github.com/marsf/Phantom-keyboard)
  - 他教育機関で使えるように調整中
  - 優先度低 & 継続
  - 現状保留
- [CHIRIMENの販売に関してOPENで情報共有するチャンネルのリンク、誘導をホームページに置く #151](https://github.com/chirimen-oh/any-issues/issues/151)
  - 定期チャンネル案内のGoogle Action Scriptをgithubで管理する
    - 自動連携（Google Action Scriptのソース管理をgithubで、連携する）
    - リポジトリを作ってREADMEを置く[@gurezo](https://github.com/gurezo) done.
- [GPIOの入力をキーボード（のキー）にバインドする機能 #130](https://github.com/chirimen-oh/any-issues/issues/130)
  - 優先度低 & 継続
  - 現状保留
- [Hello Real Worldを作る #116](https://github.com/chirimen-oh/any-issues/issues/116)
  - examplesサイトへジャンプできるサイトを。参考：https://tadfmac.github.io/live-examples/
  - 継続中
- [Proposal for alliance #157](https://github.com/chirimen-oh/any-issues/issues/157)
  - 進捗なし
- [firmware flashing guide for Mac OS X/macOS Using CHIRIMEN-tools(rkflashtool, rkunpack) #182](https://github.com/chirimen-oh/any-issues/issues/182)
- [firmware flashing guide for Mac OS X/macOS Using Vagrant #181](https://github.com/chirimen-oh/any-issues/issues/181)

## コミュニティ・イベント活動のマイルストーン（暫定）
### 2017年
- 1 月
  - 28日：[CHIRIMEN タッチ ＆ トライ イベント](https://chirimen-oh.connpass.com/event/47706/)事前準備-済
- 2 月
  - 04日：[CHIRIMEN タッチ ＆ トライ イベント](https://chirimen-oh.connpass.com/event/47706/)-済
  - 18日：NTT ICCでのトークイベント-済
- 3月
  - 02日：[学生向け Web X IoT ハッカソン 事前イベント](https://connpass.com/event/49593/)-済
  - 03日：[学生向け Web X IoT ハッカソン 事前イベント](https://connpass.com/event/49593/)-済
  - 11日：[学生向け Web X IoT ハッカソン 事前イベント](https://connpass.com/event/49593/)-済
  - 18日：[Web X IoT ハッカソン](https://browserobo.github.io/hackathon2017/)-済
  - 19日：[Web X IoT ハッカソン](https://browserobo.github.io/hackathon2017/)-済
- 5月
  - 15日：[CHIRIMENタッチアンドトライ＠大阪](https://connpass.com/event/56668/)-済
  - 28日：[Android Bazaar and Conference 2017 Spring](http://abc.android-group.jp/2017s/)-済
- 6月
  - 03日：IEEE スタッフ対象事前講習-済
- 7月
  - 08日：IEEE Tokyo Young Professionals hackathon(初日)
  - 09日：IEEE Tokyo Young Professionals hackathon(最終日)
- 8月
  - 05日：[Maker Faire Tokyo 2017(初日)](http://makezine.jp/event/mft2017/)
  - 06日：[Maker Faire Tokyo 2017(最終日)](http://makezine.jp/event/mft2017/)
  - 19日：電子情報通信学会の東京支部教育イベント？
- 10月
  - 14日：[Android Bazaar and Conference 2017 in KAWASAKI](http://abc.android-group.jp/2017a/) ?

## その他
- [議論メモ 01/19](https://public.etherpad-mozilla.org/p/chirimen-20170119)
- [議論メモ 02/15](https://public.etherpad-mozilla.org/p/chirimen-20170215)
- [議論メモ 03/30](https://public.etherpad-mozilla.org/p/chirimen-20170330)
- [議論メモ 04/26](https://public.etherpad-mozilla.org/p/chirimen-20170426)
- [議論メモ 05/25](https://public.etherpad-mozilla.org/p/chirimen-20170525)
