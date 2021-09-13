# CHIRIMEN meeting 202109

## 開催日と場所
2021年09月13日 Zoom

## タイムスケジュール
|時間|種別|テーマ|担当者|
|:----:|:----:|:----|:----|
|19:30~19:35|議論|挨拶|-|
|19:55~20:15|議論|[#3](https://github.com/chirimen-oh/meeting/issues/3) +pizero tutorialの件|-|
|20:15~20:35|議論|[#4](https://github.com/chirimen-oh/meeting/issues/4)|-|
|20:35~20:55|議論|[#5](https://github.com/chirimen-oh/meeting/issues/5)|-|
|20:35~20:55|議論|[#7](https://github.com/chirimen-oh/meeting/issues/7)|-|
|20:35~20:55|議論|[2021-08 リリース作業 chirimen#109 報告](https://github.com/chirimen-oh/chirimen/issues/109)|-|

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
- [#3](https://github.com/chirimen-oh/meeting/issues/3) 
    - https://tutorial.chirimen.org/pizero/ たたき台
    - いずれ　https://tutorial.chirimen.org/pizero/pizeronodejs へ移行
    - micro:bit 版, raspi版, pizero (nodejs) 版と増えてきたので、効率化を図りたい
        - 例：抵抗の読み方等
    - 別issueを作成
        - 章立てを検討・議論
        - https://github.com/chirimen-oh/chirimen.org/issues/104
- 名称
    - CHIRIMEN (with?|for?) Node.js on? Rspberry Pi Zero (W)
        - with: 別の PC などの開発＆プログラム実行環境と一緒 (with) にというイメージ
        - for: CHIRIMEN 環境があるよというイメージ
        - だったが今回はどうするか悩ましい...
            - 今回は開発環境としては別だが動作自体は単体動作する形になっているので microbit と同じかというとまたちょっと違う
        - microbit 含めて全部 for で良いんじゃないか
            - 使う人、説明する人からしても分かり易い
        - 単に CHRIMEN といってれば、for/with xxxx なんて名称は付けなければ良いんじゃないのか
        - 利用デバイス毎の説明があるだけで、呼称としては CHIRIMEN というだけで良いのではないか
        - マーケティング的には CHIRIMEN、x,y,z で使えます、それぞれの場合の説明ページはこちらくらいの流れが分かり易い
        - ゲームが対象機器ごとに名称を分けてないのと同じ
    - summary:
        - 単純に「CHIRIMEN」として統一しましょう
        - 何を使うかという説明「for <ボード名>」「<ボード名> 向け」「<ボード名> 版」(表記は特に統一に拘らない) などと書くことがあるが、プロダクト？名称としては分けない(常にfoxなどを付記しなくて良い)ことにしよう
        - browser / node についても特に名称を分けたものを用意しない 
- 対象環境毎のページ構成分けについて
    - 初心者目線で分かり易いことを優先して構成する
        - 実行環境 (browser/node) などより対象ボード毎
    - node 向けのコードの説明は raspi/pizero 
        - raspi ボード種別毎の違い
            - 0/4 は OTG 対応で同じ手順で済む
            - 2/3 は OTG 非対応で手順が変わる
            - USB Serial 使った編集の所も手順が違うのは一緒
            - node 向けの説明は zero (と 4) メインというスタンスで、違いは必要があれば分けて書いてあげる
            - 別ページに分けるかアコーディオン的に少し補足するかは任意、古いボード全てのメンテも必須とはしない
        - raspi 
- ワークショップ向けの Raspi 確保状況
    - WebDINO 新品 WH x 25+
    - WebDINO 中古 WH x 15, W x3
    - グンマー新品 WH x2, W x 2
- Pi 400
    - 取りあえず最小必要な 2 台 (+ 長期貸し出し用 1 台) 確保して検証できるときにする
- 定期投稿ボットどうするの問題
    - twitter, slack #events への定期投稿について
    - URL リンク集だけが繰り返し流れるのは情報が埋もれるのでは
    - URL 集としての定期投稿は止めてみる
    - URL 集よりは Tips / News 的な投稿にしたい？
        - CHIRIMEN が Raspberry Pi Zero にも対応しました！チュートリアル絶賛拡充中です！ https://tutorial.chirimen.org/pizero/
        - CHIRIMEN が XXXX (デバイス名) に対応しました！ https://link/to/device/sample/page
    - 新しいイメージリリースに対する Github Actions (？) での自動投稿などはできると良いかも

- [PRチャンネルの充実 #4](https://github.com/chirimen-oh/meeting/issues/4)
- [チュートリアルのリンクの修正  #5](https://github.com/chirimen-oh/meeting/issues/5)
    - gc/contribディレクトリを廃止して統合
        - example ページの統廃合をするというよりは [chrimen-drivers](https://github.com/chirimen-oh/chirimen-drivers/) 配下をメインとするようにしていく中で contrib という区分を無くす方向で
- [#7](https://github.com/chirimen-oh/meeting/issues/7)
- [2021-08 リリース作業 chirimen#109 報告](https://github.com/chirimen-oh/chirimen/issues/109)
- Lite 版について
    - https://github.com/kou029w/chirimen-os
    - 名称は、CHIRIMEN Lite版とする
    - リポジトリは別にする
    - リポジトリイメージ： https://github.com/chirimen/chirimen-lite @kou029w 
- カスタムイメージの登録
    - フォーラムにポストしてのその後の確認
- スターターキットのパッケージング
    - RasPi 向けのイメージは 8 月の最新版で
    - PiZero ユーザ向けのものは保留しておき必要になったタイミングにて

closing...

### HackMD
https://hackmd.io/YHoQxwQeR4CF-NaEgVdO5w
