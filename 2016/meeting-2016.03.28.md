# ◆ アジェンダ

## 現在の状況
- オープンソース化の進捗状況の報告 工藤 紀篤氏
  1. オープンソース化に課題があり、ブランディングの調整中(03/28 時点)
  1. オープンソース化についてのアップデートがありました。(04/01 時点)
     - Mozilla Corporationのリーガル担当から回答は、以下の条件を満たせば問題ないだろうとの事です。
       1. プロジェクトのURLを変更し、mozillafactory.org以外の場所とする。その際MozやMozillaを含まない事
       1. コミュニティの関係者がプロジェクトの成果物（ソフトウェア/ハードウェア）紹介する際には、Mozilla Factoryから生まれたプロジェクトであると言ってよい。
       1. 販売する際には、販売者はMozilla Factoryも含めてMozillaについて言及することはできない。
       1. プロジェクトの成果を公開する際には、新たなプロジェクト名において公開し、Mozilla Factoryとしては公開しない。

## 各種フィードバック
- [前回議事録](http://is.gd/ppnhCM)

## 議題
- ドキュメント・情報整理ついて
  - タカギ・サトルさんが、現在進行形で整備中 [(クイックスタートガイドホームページ)](https://developer.mozilla.org/ja/Firefox_OS/Board_guide)
  - ブランディングの問題がクリアにならないと、ドキュメント置き場所が決められない
  - ブランディングが決まるまでの作業
    - 現在の状態でドキュメント編集を続行する。
    - [サイト](http://is.gd/5hzvBf) 公開を継続
  - 情報をまとめる
    - CHIRIMEN調べたいときに、全体が見えるサイトが見つからなくてわかりにくい　梶井さん
    - [tumblr：mozOpenHard](http://is.gd/5hzvBf)
    - [Fabble - ChirimenEdu](http://fabble.cc/chirimenedu)　　
      1. B2G ver 2.6 で、再動作検証が必要　　関口さん
      1. サイトにある記事の原型は、関口さんがワードドキュメントで所有との事
        * ハンズオン時のzip 配布対応準備で、確認
    - サイトに掲載したい情報
      1. ドメインは、確保済み　担当：赤塚さん
      1. 本体ハード仕様
      1. 接続機器のノウハウ集
      1. API
      1. 教育関連情報
      1. NEWS
      1. 構成の参考サイトは、[arduino - Home](http://www.arduino.cc/)
      1. CHIRIMEN-org で取る作業 => 酒巻さん done 3/28
        - [chirimen-org](http://chirimen-org.github.io/)
        - markdown で記述する為、Jekyll を使用
  - 提案：やることチケット化したい 酒巻さん
- イベントの実施内容について
  - おさわり会2 (Open)
    - 位置付け：ハンズオンのチュータースタッフ公募と養成
    - 内容：[Fabble - ChirimenEdu](http://fabble.cc/chirimenedu)
    - 人数：20人程度
    - 次回期日：下記利用する機材調達の確認が取れたら、調整さんで公募 => 04/07 公募開始
      - [CHIRIMENおさわり会2 (Open) の出欠確認](http://is.gd/gXObPB)
  - ハンズオン (Open)
    - [CHIRIMEN入門インデックス案](http://is.gd/m5o0th)
    - 上記ドキュメントのセンサー項目を一通り網羅する事が当面の目標
    - 最初は５名程度を公募して小規模で行い、徐々に人数を増やしていく
    - CHIRIMENをネットに繋がないコンテンツであれば、イベント開催は可能
    - 会場は、mixi さんにご協力をお願いする？
    - 利用する機材の調達はどうするのか？ => 関口さんの確認待ち
      - 4/1回答：[Available devices for Events](https://github.com/chirimen-org/meeting/wiki/Available-devices-for-Events)
    - 課題
      - モニター準備問題
        - 対策：スリープしないように設定しておけばいい
      - wi-fi 関連の接続設定問題
      - ネット回線利用不能時のリカバリ案
        - 紙媒体とかUSB メディアとか
        - お持ち帰りセットの用意は必要
- スターターキットに関して
    - 保留
- スクラッチソフトに関して
    - 保留：スターターキットがメドが付くまで

##　Facebookグループページにやる事
1. 説明ピンを創る -> 3/11済
    - ※MozOpenHardのページだけ、未作成

## 保留事項
- 保留事項：今後の関連ドキュメントの整備は、どうするのか？
  - 誰がやるか？
  - どこに何を置くか？
  - ブランディングが決まるまで、何ができるのか？
- スクラッチソフト候補（スターターキットがメドが付くまで）
  - 公開されているので、Forkして開発可能
      - [App Maker](https://apps.webmaker.org/designer)
      - [Framin](http://framin.kddi.com/pc/)
  - [MameBlock](http://ycatch.github.io/mameblock.js/)
     - ycatchさんがリリースした？（未確認）
