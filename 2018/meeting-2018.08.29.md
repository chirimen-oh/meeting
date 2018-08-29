## 開催日と場所
2018年8月29日　WebDINO Japan

 ## タイムスケジュール
|時間|種別|テーマ|
|:----:|:----:|:----|
|19:00~19:20|others|自己紹介||
|19:20~19:35|報告 |Maker Faire Tokyo 2018振り返り|hiyohiyo|
|19:35~19:50|報告 |人感センサーのサンプル追加について|tadfmac|
|19:50~20:05|報告 |テストボードについて|satakagi|
|20:05~20:10|報告 |CHIRIMEN for Raspberry Pi 3 を使った中央大学集中講義について|dynamis|
|20:10~22:00|議論 |CHIRIMEN for Raspberry Pi 3 リリース方法のディスカッション||

## 参加者
* sizuhiko
* kazy
* okuda
* t.mitamoto
* satakagi
* kotakagi
* gunmaer
* dynamis
* tadfmac
* forte916
* krunaru
* tisaku
* hiyohiyo

## 議事録
- リポジトリのファイル配置
  - tutorial にはチュートリアル専用コードだけ
  - デバイスを動かすサンプル系は chrimen-raspi3 配下の gc に入れていく
- バージョン管理
  - polyfill はバージョン番号付けたファイルを同じディレクトリに入れていく
  - polyfill ディレクトリだけ polyfil.chirimen.org にホストする？
  - polyfill.js ファイル名？ chirimen-raspi3.js で sleep() 入れておく
    - chirimen-raspi3-latest.js
    - chirimen-raspi3-1.0.2.js
- リリースの仕方
  - まずテストする時点で tag をつけて issue を立てる
  - リリース作業チェックリストを wiki のテンプレートからコピーして issue にはる
  - チェックリストをみんなで埋めていく
  - 適当な段階で beta or test リリースとかのイメージも作ってアップロード
  - フルテストのチェックリストが埋まったら正式リリース
  - 正式リリース前イメージは別のディレクトリに置く
- リダイレクトサービス作る
  - r.chirimen.org
    - rebrandly か urls.js を自前サーバに適当にホストとして管理アカウントを共有する
    - chirimen slack とかでスタッフグループ的なところで共有する

- チュートリアルをホストする
  - NO: chirimen.org/docs/tutorial/
    - 既存の chirimen.org.githubio に tutorial リポジトリを統合する？
  - THIS! tutorial.chirimen.org
    - netlify 使える(笑)
    - raspi3-tutorial.chirimen.org
    - examples.chirimen.org ?
    - 本当は wiki てきなもので簡単に contribute しやすいものにしたい
    - 
  - NOT chirimen.org/tutorial/
- web サイト chirimen.org のアップデート
  - 赤いちりめんはサポート終了宣言をしていく
    - スイッチサイエンスに一言のお詫び by @stakagi
  - 編集環境は docker でやりやすくなるとのこと
  - tutorial へのリンクを目立つようにいれる
- 土曜日の体験会
  - いつからか未定義だが体験会を WebDINO で実施していく
  - chirimen connpass で告知する
  - 告知手順書が欲しいところ。何処かに書いておこうかな。
    - twitter アカウントの管理パスワードは必要な人は知ってる人に聞きましょう
- Web x IoT Maker Challenge
  - 協力表記は許可する。
    - イベントのお手伝いなど相談することもあるかも知れないが勿論任意
  - スターターキット？パッケージにして利用する地方には必要数買ってもらえるように WebDINO で作成して販売する
    - sd image 入れるとすれば raspbian のライセンスとか表記については確認が必要かも知れない
    - raspi の名前じゃなくて chirimen の名前であれば良いのか？
    - そのあたりの確認はする by eri
- 大阪のあれ
  - 昨年度 3 月に実施した大阪工業大学と開催報告やアウトラインの報告書を書いている
  - システム情報制御学会？ の学会誌に投稿するので許可が欲しい。謝辞は入れるかも知れない。少なくとも CHIRIMEN Community の名称が出る。
    - OK!
