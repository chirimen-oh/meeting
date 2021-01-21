# CHIRIMEN meeting 202012

## 開催日と場所
2020年12月11日 Zoom

## タイムスケジュール
|時間|種別|テーマ|担当者|
|:----:|:----:|:----|:----|
|19:30~19:35|議論|挨拶|-|
|19:35~20:05|議論|RPi SDイメージ更新リリース|-|
|19:35~20:05|議論|chirimen-drivers|-|
|19:35~20:05|議論|microbit|-|
|20:05~20:35|議論|技術書典|-|
|20:35~21:00|議論|BOOTHオンラインショップ|-|
|21:00~21:30|議論|公式サイト|-|
|21:00~21:30|議論|オンラインイベント|-|


## 参加者 (alphabetical order)


## 議題
### RPi SDイメージ更新リリース

- RasPi 4 のロットによっては？古い OS Image と互換性が無い
- raspbian latest であれば問題無い
    - ref: https://www.raspberrypi.org/forums/viewtopic.php?t=282250
- RasPi 4 公式サポートを謳うには OS Image の更新が必要。
- ターゲットとしては WIMC 鳥取 1/10~ の開始までにリリースできることが望ましい。
- 年末年始に宮本さんが更新を試してみる。
    - 可否の判断は一旦 1/1 くらいに
- ターゲット OS:
    - Raspberry Pi OS がメインターゲット (仮)
    - ダメだったら Rasbian OS (片方だけで良い)
- リリース後テスト
    - OS イメージ頂いたら浅井もテスト予定
    - ぐんまーさんなどもテストに参加予定
- サードパティイイメージ問い合わせ中（ぐんまー）

### chirimen-drivers
* ES Module 
* Examples引っ越し
* 行動規範
  * drivers には仮に入れてあった。コード貢献向けのもの
  * https://chirimen.org/chirimen-drivers/CONTRIBUTING#%E6%8E%A8%E5%A5%A8%E3%81%99%E3%82%8B%E3%83%A2%E3%82%B8%E3%83%A5%E3%83%BC%E3%83%AB%E3%81%AE%E6%A7%8B%E6%88%90
  * 今後はコミュニティ行動規範とコード貢献行動規範を設定
  * コミュニティ: chirimen.org サイト上にページ作成・掲載する
      * http://www.association.droidkaigi.jp/code-of-conduct.html ベースに
  * コード貢献
    * https://docs.github.com/ja/free-pro-team@latest/github/building-a-strong-community/adding-a-code-of-conduct-to-your-project
    * 専用リポジトリに入れる
- メンテナンスを Git Action **先々したい**
- driver をオンライン => オフライン化しうシェルを実装したい
- 新イメージ作成時にリポジトリから最新の drivers をシェルで持ってくる実装を **先々したい**
- 上記の自動化を先々したい
- 現時点では、最新のOSイメージありきですすめる

driver/example 新構成
- master: https://github.com/chirimen-oh/chirimen-drivers/tree/master/examples
    - リポジトリ名
        - GPIO サンプルも含めるなら chirimen-drivers を chirimen-packages? devices? 等にリポジトリ名を変える？
    - Tier1 環境の example は入れる: raspi, microbit, node 
        - driver 更新時に example の更新を同時にし易くするため
    - 単一 example からの生成・統一化は今後の検討
- ディレクトリ構成
    - ひとまず現状コードのままでまとめる
    - /raspi-examples (← examples から改名 (DONE))
        - gpioled
            - GPIO なども全部こちらに移してくる
        - sht30
        - ...
    - /microbit-examples
    - /node-examples (変更無し)
- contrib の区別は無くす
    - https://github.com/chirimen-oh/chirimen/tree/master/gc/contrib
    - 配下の者も区別なく raspi-examples 配下に入れる



メモ:

* CJS -> ejs/umd変換のCLIあるけど、使ったことはない
* https://github.com/getify/moduloze


### microbit
  * V2　公式サポート
      * V1 サポート継続
  * PWM API

### アーカイブにしたほうが良いリポジトリ
- [x] [device-rockchip-rksdk](https://github.com/chirimen-oh/device-rockchip-rksdk)
- [x] [gaia](https://github.com/chirimen-oh/gaia)
- [x] [b2g-manifest](https://github.com/chirimen-oh/b2g-manifest)
- [x] [platform_build](https://github.com/chirimen-oh/platform_build)
- [x] [release](https://github.com/chirimen-oh/release) ⇒  chirimen-oh/echigo-release
- [x] [linux-rockchip](https://github.com/chirimen-oh/linux-rockchip)
- [x] [examples](https://github.com/chirimen-oh/examples) => echigo-exmaples
- [x] [device-chirimen](https://github.com/chirimen-oh/device-chirimen)
- [x] [CHIRIMEN-tools](https://github.com/chirimen-oh/CHIRIMEN-tools)
- [x] [gecko-dev](https://github.com/chirimen-oh/gecko-dev)
- [x] [b2g-rockdev](https://github.com/chirimen-oh/b2g-rockdev)
- [x] [B2G](https://github.com/chirimen-oh/B2G)
- [x] [platform_system_core](https://github.com/chirimen-oh/platform_system_core)
- [x] [b2g-patches](https://github.com/chirimen-oh/b2g-patches)

### 継続利用 (アーカイブしないことにした) repo
- [ ] [any-issues](https://github.com/chirimen-oh/any-issues)
    - 技術書典的なのも chirimen repo で扱う (chirmen repo が any-issues の役割を引き継ぐ)？いや、取りあえずこのままで


### 技術書典
- https://techbookfest.org/
- 2020.12.26-2021.01.06
- 既刊本のみになります。
- 作成まで出来ないです。

### BOOTH オンラインショップ
- 公開準備可能状態です
- DONE
- https://chirimen-oh.booth.pm/

### 公式サイト
- ドメイン切替 https://github.com/chirimen-oh/chirimen.org/issues/88
- 旧サイトは archive.chirimen.org に
    - https://archive-chirimen-org.netlify.app/ にデプロイ済みのものに archive.chirimen.org でアクセス可能に
- 中身はドメイン切替前後気にせずこのまま順次進める

### オンラインイベント
- もくもく会 on 1/23 (土)
- イベントページ準備中 https://connpass.com/event/163004/
    - 始めてさん枠向けの貸し出し申し込みフォーム
    - 下書きの見直し
        - スターターキットについてのアンケート等々を考える
    - 貸し出し
        - WebDINO から貸し出しは可能
        - 何を貸し出すのかを定義して決める
    - 対象を IoT マーカーズのチューター対象にするアリ
- WIMC slack #general などに案内を流す

### WIMC
- 岡山の成果発表会 12/20 15:00 くらいのオンライン見学も可能
- 希望があれば井上さんにリクエスト
    - 木暮希望
- Zoom で参加可能

### サポートデバイス

- micro:bit v2 サポート！
- RasPi 400 は動作確認予定
    - 鳥取の景品に提供予定
        - 発売予定は 2021 春だが目録か何かで後日送付？
        - https://raspberry-pi.ksyic.com/news/page/nwp.id/99
    - 多分動くと信じて、販売・入手したらテストする


### Next

- 来年 1 月中頃くらいで調整さん

## HackMD
- https://hackmd.io/@ukzioj9rSYutR9JNZjaZAg/SJrziae3P
