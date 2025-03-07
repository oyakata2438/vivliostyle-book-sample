---
class: chapter
---

# 【保存版】　入稿までの手順

大体、執筆者というのは極道入稿をぶちかまして、泣きながら全部をギリギリでやってしまう生き物だ。間違いない。

というわけで、入稿までの手順を残しておく。これは筆者が自分で参照するために書かれている。



## 初期時点でやっておくべきこと

* まずPDFの作成ができることを確認する
* 印刷所受付可能なPDFが作成できることを確認する
* CIでも同じPDFを作成できることを確認する
* 締め切りの設定

## 早めにやっておくべきこと

* 目次の設定
* 技術調査
* サンプルコードの作成
* 刷る部数をおおよそ考える
* ページ数のめどを立てる

## 大体原稿ができたらやるべきこと

* コンビニプリントか、レーザープリンタを使って実際に印刷しての校正
* 執筆モードと、校正モードの脳の切り替え
* よく寝る
* 宣伝ブログ、宣伝ツイート
* 当日用のポスターなどの作成

### 魔法の呪文

毎回検索しているのでここに記す。

|項目|値|解説|
|---|--|----|
|判型|`A4`, `B5`|技術同人誌の場合、A4かB5が一般的。ただし日本のB5は特殊なので Vivliostyleの設定ファイルでは `JIS-B5` という設定が必要。印刷所は大体日本規格のはず|
|閉じ|`左とじ`|技術同人誌は左とじ。漫画や縦書き小説は右とじ|
|製本|`無線綴じ`|ページ数がある程度を越えるとこれしかなくなる。ページ数が凄く少ない場合は `中とじ` もあり|
|印刷方式|`オンデマンド`, `オフセット`|少部数ならオンデマンドの方が安い。部数が多いならオフセット印刷の方が安い|
|本文|`モノクロ` or ???| 基本的には本文はモノクロ|
|表紙|`フルカラー` or ???| 基本的には表紙はフルカラー。こだわりがあるならモノクロでもいいけど、フルカラーかつ手に取ってもらいやすい表紙じゃないと売れない|
|ページ数|偶数|ページ数は偶数である必要があります。中とじだと4の倍数縛りあり|

## チェックリスト

|項目|内容|目安|チェック|
|---|----|----|---------|
|方向性|本の方向性をどうするのか？|思い立ったが吉日|　|
|目次|目次ができれば本の半分はできたようなもの|思い立ったが吉日|　|
|参加の確定|同人誌即売会に申し込む必要があります。自分のサークルで参加しない場合は、知り合いのサークルに委託する、あるいは同人誌即売会に参加せずにオンラインサイト(Boothなど)で販売するなどを考える必要があります|思い立ったが吉日|　|
|執筆|長い戦い|締め切り日を決めましょう（入稿日の一週間前までには執筆を終えるのが理想型です）|　|
|技術調査|技術書なので技術調査が必要です。初期のうちに完了するのが最善です。|締め切り日を決めましょう|　|
|サンプルコード作成|技術書の場合、サンプルコードは意外と苦戦します。早めにめどを付けた方がいいです|締め切り日を決めましょう（執筆のかなり早めに終わらせましょう）|　|
|校正|誤字・脱字、構成の悪さなど、あら探しはいくらでもできます。最近だと生成AIを使って校正をするという手法も一般的になってきています。意外と時間がかかります。早めに校正しましょう。|締め切り日を決めましょう|　|
|印刷所申し込み|入稿日ギリギリにせず早めに申し込みをしましょう|入稿日より一週間以上前|　|
|入稿|印刷所に入稿できるPDFを作成しアップロードをしましょう|入稿日|　|
|当日準備|当日に必要なものを準備しましょう|余裕を持って|　|
|両替|いきなり一万円を使ってくる人は希によくいるため、千円札をある程度多めに用意しておきましょう。|余裕を持って|　|

## 表紙を作る

タイトルを決めたら、いい感じに表紙を作ろう。

* 解像度の高めの画像を使うことで、印刷したときにガビガビしない。
* 内容を説明しつつ、人にフックするタイトルを頑張ってつける。
* レイアウト、フォント：がんばる。いくつか作ってみてしっくりくるものを選ぶ。人に見てもらうとよい。
* GoogleSlideやKeynote、PowerPointでも作れる。

PDFでよいが、表の表紙と裏の表紙がある。B5サイズの本を作る場合、B5の2枚分+背表紙分のサイズで作る必要がある。

背幅は、「背幅計算」などで検索すればいくつかヒットする。

例：https://www.printpac.co.jp/contents/musen_outline.html

使用する紙やページ数で計算できる。例えば100ページの本なら5.2mm程度になる。

表紙と本文は、印刷工程も別だから、別ファイルで作る。

印刷・丁合・製本によって多少の誤差は出るので、あまり厳密なデザインにしない方がよい。

背だけ塗る、といったデザインにすると、背に表紙の色がはみ出したり、背の色が表紙にはみ出したり、と、ちょっと残念な気持ちになることがあるため。

また、背にタイトルを入れると、見分けがつきやすくなるのでオススメ。文字は小さくてもよいので、タイトルとサークル名が入ると嬉しい。

表紙と本文は、印刷工程も別だから、別ファイルで作る。


## 印刷所に出す
本を作ったら、物理本として印刷したくなりますよね。

そんな時は、出力されたPDFを同人誌印刷所に送って、本にしてもらいましょう。

同人誌を印刷してくれる会社(印刷所)は、日本には星の数ほどあります。それぞれに特色はありますが、いくつか、筆者の独断と偏見により挙げておきます。
予算と、締切日程とから適宜選択してください。

* ねこのしっぽ　https://www.shippo.co.jp/neko/
* 栄光　https://www.eikou.com/
* ポプルス　https://www2.popls.co.jp/pop/
* しまや出版　https://www.shimaya.net/

基本的に、PDFが出力されていれば、本になります。細かいノウハウはいろいろありますが、おおよそ今PDFが出力されていれば問題なく印刷されます。

印刷所のページには「見積り」といったボタンがあります。ここにページ数や判型、表紙の仕様を入力すると費用見積もりができます。

発注ボタンを押したら、決済手続きに移行しますので、見積額の決済を行います。

決済が完了したら、入稿用のアップロードページが開きますので、ここに出力されたPDFを登録しましょう。

基本的にはこれだけです。


### 印刷時の備忘録

* 紙の厚み(表紙)

表紙は、一般的には、135kg～180kg(ハガキくらいの厚み)の紙を使います。PP加工を入れると良いです。

クリアPPは、表紙がよく見えるツヤツヤしたコート、マットPPはさらさらして少し落ち着いた印象になるでしょう。

* 紙の厚み(本文)

本文の紙は、70kg～90kgが適当です。

なお、A5版でページ数が多い場合、90kgの紙を使うと紙が硬いため開きづらい・読みづらいと感じることがあります。
100ページ程度より多くなる場合は、70kの紙にするとよいでしょう。70kgは一般的なコピー用紙の厚さです。

* 綴じ方向

綴じ方向は、横書きの技術同人誌ならば左綴じが原則、縦書きの文学系やマンガは右綴じです。

* 遊び紙

表紙をめくったところに入れる色紙など。

本のイメージカラーに合わせた色紙を選んだり、クラフト紙やトレーシングペーパーを入れたりすると雰囲気が変わります。


その他、同人誌印刷に関する細かいノウハウは、「技術同人誌を書こう-アウトプットのススメ-」という書籍があるので、ぜひそちらを参照してください。ネタ出しから本の作成、サークル参加のノウハウ、お金回りまでを網羅した本です。

https://www.amazon.co.jp/dp/B07BY9YWCN/