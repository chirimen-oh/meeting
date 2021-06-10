# CHIRIMEN meeting 202106

## 開催日と場所
2021年06月10日 Zoom

## タイムスケジュール
|時間|種別|テーマ|担当者|
|:----:|:----:|:----|:----|
|19:30~19:35|議論|挨拶|-|
|19:35~19:55|議論|[#2](https://github.com/chirimen-oh/meeting/issues/2)|-|
|19:55~20:15|議論|[#3](https://github.com/chirimen-oh/meeting/issues/3) +pizero tutorialの件|-|
|20:15~20:35|議論|[#4](https://github.com/chirimen-oh/meeting/issues/4)|-|
|20:35~20:55|議論|[#5](https://github.com/chirimen-oh/meeting/issues/5)|-|
|20:55~21:15|議論|webGPIO, webI2C / Node.js / Raspberry Pi Zero|-|
|21:15~21:35|議論|webGPIO, webI2C / Node.jsをCHIRIMENと名乗るのに必要な要件は？|-|
|21:35~21:55|議論|技術書典11|-|

## pizero tutorial
* https://tutorial.chirimen.org/pizero/pizeronodejs
* https://tutorial.chirimen.org/pizero/chirimen-nodejs-examples
* https://github.com/chirimen-oh/chirimen.org/tree/master/pizero


## 参加者 (alphabetical order)
- @dynamis 
- @kou029w 
- @satakagi 
- @sizuhiko 
- @tadfmac 
- @WhiteHawk-taka 

## 議題
- [#2](https://github.com/chirimen-oh/meeting/issues/2)
    - 賛同を得たので、close
- [#3](https://github.com/chirimen-oh/meeting/issues/3) 
    - stakagi: 折角だから実用的に CHIRIMEN を使いたいという声を聞くことが増えた
    - しかし Browser 起動する形だと IoT 的に自動起動・自動処理をするのには向かないことが多い
    - 学習キットそしては良いが実運用にはハードルがあるので Node Implementation されているものを CHIRIMEN 本流として使えるように整備していくと良いのではないか
    - gummar(gun): 試してみて思ったが window オブジェクトを使っているものだと使いにくい、node i でさっと使える形に倒していった方が良いかも
    - stagaki(st): 初心者向けには今の仕組みは捨てがたいところもある
    - node/browser の垣根を低くしていきたい。填まりポイントなくしたい
    - WIMC も今年度何らかの形で継続することになるとそこでも社会実験的にも使ってもらえるようになっていくと良いのではないか
    - 学習コストと実用性
    - node だけなら小型ボードでも動くものが増えてきて browser を要求しない環境で動かせるのはよい
    - gun: 今の polyfill で動くのはとても良い。node がないと js が動かない形にはしたくない
    - st: 環境を用意するのにスキルが必要なのはハードルが上がる
    - 今まで通り典型的な、安い SBC ですぐに本格 IoT 出来るのは保ちたい
    - m5stack 良いと思うが...
    - shizuhiko(shi): m5stack は js は動くかも知れないが node は動かない
    - node を動かすのは linux スタックが必要なので
    - st: OSS 整備されている node でできるのはロックインされずに良い
    - JS だけど node ではないのは縛られないなら良いが...
    - gun: node とか使えるのは raspi にどうしてもなる？
    - m5stack とかはサンプルとかを充実させる？
    - st: raspi os の中でやってる限り簡単
    - ...
    - kou029w: pizero ってボードとして古いけどどうなんだろう
    - st: pizero は polyfill 含めて共通なのはとても良い
    - dyna: OS image を別途作る必要があるのが Pi0 の面倒なところ
    - miyamoto(mi): リソース的にあちこち手を出せない
    - st: pi0 まで揃うと人おとり感もある...
- OS image の話
    - dyna: 自動化したいねー
    - st: setup スクリプトレベルまでなら出来る？
    - mi: できそうだがちゃんと動くもの作るのは手間掛かる
    - gun: 32/64 の分岐は？
    - mi: それは分けた方が良い
    - shi: 元の OS イメージも違うから一緒に出来ない
    - st: 0 で動くものは 2-4 でも同じものが動かせるだろうか
    - 0 は OTG が使えるところが他とは違う所だが
    - mi: 0 から上には出来そうな気がする
    - gun: rapis OS 最新版対応もしたいんね
        - chromium, などなどバージョンアップ
        - vs code も apt-get でさっと入るようになってて良いらしい
    - 64bit は 5/28 版で引き続き 32bit と揃えていこうとしてる
- 今後の話
    - Raspberry Pi OS Lite のイメージを用意できると良い
    - shi: node-gpio/i2c 以外に提供するメリット・意図は？
    - st: ブラウザのサンプルからシームレスに
    - import 周りは window オブジェクトあるけど
    - dyna: import して window 配下に置く形に polyfill?
    - kou: import 等はともかく他の所の使い方が...
    - st: console.log 以外全部違うよね
- サーバ経由で遠隔制御したい話
    - ... websocket 実装を pub/sub 的なものに作り直すコストは掛かる
    - os image とか driver などの整理が先か
- ts に書き換えてみる話
    - ...
    - node-webgpio とか作ったけど再発明的なところはある
    - polyfill の元々のコードは結構厳しい
    - メンテナンス性のあまりないコードにはなっている
- node-web-xxx と polyfill の実装が分かれてる話
    - 統合するなら node-web-xxx + 薄い browser 用 wrapper だろう
    - そうする場合は polyfill つかった example とか全部差し換えになる
    - CHIRIMEN 2.0 的になってしまい話が大きくなりすぎる
    - ...
- サンプルコードが分かれている話
    - console.log の代わりに何か使うだけでは解決できない
    - サーモとかバーの UI とか色々サンプルでもある
    - redux 的な仕組みを作るのもちょっと
    - 簡単にするために複雑な構造を入れるのはその非標準的実装に対する学習コストが高い
- ...けんけんがくがくほにゃらほにゃ...
- まとめ
    - node-web-gpio/i2c も CHIRIMEN ブランド
        - WebGPIO/I2C API で navigator と明記してるのは変えるのが望ましいがともかく CHIRIMEN の思想としては問題ない。OK
    - pizero 向けのドキュメントも含めて全面的に見せていこう
        - https://tutorial.chirimen.org/raspi/nodejs
        - https://tutorial.chirimen.org/pizero/pizeronodejs
        - ref: https://zenn.dev/kou029w/articles/node-web-gpio
    - remote example のサーバ側に node 版が欲しいね！
    - examples を browser/node/pizero 纏めて整理しても良いね
- rpi chirimenのjsdoc
    - https://github.com/chirimen-oh/chirimen/pull/107
    - merged!
    - node版も
- [#4](https://github.com/chirimen-oh/meeting/issues/4) 
- [#5](https://github.com/chirimen-oh/meeting/issues/5)
- webGPIO, webI2C / Node.js / Raspberry Pi Zero
- webGPIO, webI2C / Node.jsをCHIRIMENと名乗るのに必要な要件は？⇒#2であらかた話した？
- 技術書典11 オフライントライアル　サンシャイン
    - https://blog.techbookfest.org/2021/06/06/tbf11-trial/
- 教育利用事例
    - 中央大学オープンプロジェクト演習の集中講義で利用開始しています
    - 鳥取県の高校でも CHIRIMEN を利用しての IoT を体験する「探求」の特別授業を行うことを検討して頂いています
- Image Update について
    - 最新版がない事で困っていないか？
        - 色々アップデートして困る学生はいるが講師側でフォローしている
        - もちろんバージョンアップされると有り難いが Blocker ではない
- closing...

### HackMD
https://hackmd.io/AqANXtsOSl-C7U0w84F2sg?both
