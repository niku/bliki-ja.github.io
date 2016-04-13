---
layout: pofeaa
title: ReadingPofEAA004.md
---


連絡用に[PofEAA読書会メーリングリスト](PofEAAReadingMailingList)を用意しています。読書会への参加を検討されている方は、メーリングリストにもご参加ください。

# 開催概要
- 日時：**2005/6/26(日) 13:00〜18:00頃**
- 場所：(株)オージス総研 東京オフィス会議室

## 内容

※第4章は飛ばします。

- ポジションペーパー（立場表明書）ベースの自己紹介
- Chapter5: Concurrency(第5章 並行性) (by id:ogijun)
- [『.NETエンタープライズWebアプリケーション開発技術大全 Vol.5　トランザクション 設計編』第3部 複雑なトランザクション制御](http://bpstore.nikkeibp.co.jp/nsp/book/04312/04312.html)、のサマリ (by WR)
- 関連して、もうちょっとネタがあるかも……

終了後、懇親会があると思います(参加はもちろん任意です)。

# 当日の内容

## Chapter5. Cuncurrency

## [『.NETエンタープライズWebアプリケーション開発技術大全 Vol.5　トランザクション 設計編』第3部 複雑なトランザクション制御](http://bpstore.nikkeibp.co.jp/nsp/book/04312/04312.html)のサマリ(by WR)をベースに議論 

- 8章. 対話型トランザクション処理の設計方法
  - 対話型トランザクション処理とは
  - 業務排他制御による対話型トランザクション処理の設計方法
  - 楽観同時実行制御による対話型トランザクション処理の設計方法
- 9章.  複雑なトランザクション制御
  - 複雑なトランザクション制御とは
  - ネットワーク障害時のメッセージロスト対策

第3部の残りは[次回](http://capsctrl.que.jp/kdmsnr/wiki/PofEAA/?ReadingPofEAA005)へ持ち越し。

論点いくつか。
- ロックの方式
  - 楽観的同時実行制御における「残念！」は、ユーザーに嫌がられる可能性アリ
  - 在庫引き当ての場合など厳密なモノの管理が求められるケースだと、ここで提示した方法＋αが求められるだろう。
  - 会員限定とか、在庫をクラス分けするとかもあり。
  - 楽観的同時実行制御の実現方式であるtimestamp方式は、サーバ時刻ズレなどの問題をはらむ。versionNoが一番ツブシが効く。
- 二重submit防止とロギング
  - (類似例として?)ビューに対するモデルを、サーバ側で永続化しておき、過去の画面（＝ビュー）を再現できることを求められたケースアリ
  - (類似例として?) モデルをXML化しておいたが、予想以上にサイズが大きくなりいろいろ苦労した。
  - (WebObjects屋的には) (ブラウザ戻る対策が主目的であるが)pageCacheとしてメモリ上にレンダリング後の画面データを持つ仕組みが存在している

## ふりかえり

### Keep

- ポジションペーパーの時間配分（初回の方3分、それ以外2分はイイ）
- 内容＋おまけの2部構成イイ
- 逐次議論（インタラクティブ）イイ → 専門知識を聞ける
- 机の配置（囲み）イイ → 顔を合わせての議論ができる
- 休み時間の取り方イイ（5分/1時間）

### Problem

- 時間の配分が難しい（インタラクティブだから仕方ない面も）
- 本をちゃんと読んでこよう

1. 机の移動に時間がかかる(約10分)
1. 遅れてくる人はポジションペーパーを受け取れない
1. 今後、人数が多くなるとどうしよう

### Try

- 教室形式はやってみる価値がある？（話し手と聞き手に分かれてしまわないか？）
  - やはり、顔を合わせての議論ができる今の形式のほうが良いだろう

1. 時間早めに入る（10分前）→ 開場を早めることが可能か？(オージス総研様)
1. ポジションペーパー置き場を事前に作っておく
  1. 置き場は、紙のポジションペーパーの置き場所を、会場で設置しておくということ(と認識したがどうか？)
  1. ポジションペーパの事前資料配布（本名載るからpublicには置けない...qwikwebに載せる？）
1. 人数制限をする？、大きい部屋の準備なども視野に(ただしインタラクティブ性に欠けそう)
  1. 制限するとしたら〜30人くらい?

# トラックバック
参加された方で、weblogをお持ちの方はご協力をお願いします。

- trackback : [[[PofEAA] PofEAA 読書会(第4回) - Concurrency (Aufheben - GLAD!! の日記)|http://d.hatena.ne.jp/aufheben/20050626/1119882531]] (2005-07-03 (日) 04:05:21)
> 遅ればせながら報告と感想をまとめておきます。(7/3)    場所の予約を担当した関係で少し早めに会場へ到着。 部屋の鍵を開けて冷房を入れて準備OK... のはずが人数が多かったため隣の部屋へ移動、冷房があまり効いていなくてゴメンなさい。 集合場所へ行ってみると角谷さんがなぜかマスクをしている。おや? と思いつつその場では聞かなかったが、やはり具合が悪かったんですね。ポジションペーパーの発表..


- trackback : [PoEAA 4th - Csus4.net](http://www.csus4.net/d/2005/06/26/poeaa-4th/) 
>行ってきた&発表してきた。

- trackback : [PofEAA読書会: 第4回 体調不良で早退という失態 (角谷HTML化計画)](http://kakutani.com/20050626.html#p01) (2005-06-27 (月) 22:04:34)
>金曜の夜から熱発。ひたすら寝て回復を図るも果せず。液体・錠剤・ビタミン剤などなどでドーピングしてオープニングとポジションペーパーの司会までどうにかこなしたものの、終盤は妙な汗をかいていたり。後を唐突に隣に座ってたKKDさんに押しつけて(ありがとうございます)、早退。参加されたみなさん、すみませんでした。そして、ありがとうございました。いろいろ話をしたいことも多かっんだけどな……。
>
>
>現..


- trackback : [[[dev]PofEAA読書会 第4回 (ちくわプログラマの作業履歴@はてな)|http://d.hatena.ne.jp/thata/20050627#1119870350]] (2005-06-27 (月) 20:06:06)
> 行ってきました。以下、箇条書きで。 [http://oden.air-nifty.com/position_paper.pdf:title=オレのポジションペーパー](PDF) 高橋さん、ポジションペーパーも高橋メソッド kdmsnrさんのポジションペーパーが『もんたメソッド』w 言語ワークベンチ期待age おー、koichikさんだ!! 7年くらい前から憧れの人なのです もっとお話を聞きた..


- trackback : [PofEAA:ReadingPofEAA004 (capsctrldays)](http://capsctrl.que.jp/kdmsnr/diary/20050626.html#p01) (2005-06-27 (月) 14:01:31)
>Concurrencyの章はRDBMSの章と捉えたほうがいいみたいですね。RDBMSにおけるビジネストランザクションの実装から始めて、例えばWebサービスがリソースとして加わった場合にどうしましょうとかいうふうに進めていくと分かりやすいのかも（Compensationの手段を考えるとイヤな感じになりますが）。