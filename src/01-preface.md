---
class: preface
---

# まえがき

この本はできる限り労力を使わずにMarkdownで技術同人誌を作るためのノウハウと、その最小限を導くための知識についてまとめたものです。本の内容にのみ集中したい人に向けて書いています。

怠惰は美徳です。技術者たるもの怠惰を極めましょう。本を書くにしても原稿だけに集中してそれ以外は怠惰にやっていきたいものですね。この本は、そんな怠惰なあなたのためにあります。

まずこの本のリポジトリをforkするなり、設定をパクるなりして、新しい本のリポジトリを作るようにしましょう。

## 対象読者

対象読者は、技術同人誌もしくはそれに近い体裁の書籍を**簡単に**ハイクォリティで作りたい人。もっと言えば、原稿を書くことのみに集中したい人です。「寄り道したくない」人向けの本です。

ただし、この本を印刷までもっていくために必要なVivliostyleはJavaScriptで作られていて、技術者が使うことを前提としたツールであり、そういった技術を避けられません。ターミナルを使う必要があります。

原稿はすべてGitHubで管理し、VSCodeなどを使って執筆することを前提とします。多種多様な環境があり得るとは思いますが、この本では一番メジャーな方法論でシンプルを是とします。

そのため、ターミナルを使えること、JavaScriptが動いていること、GitHubやgitを使えることを前提とさせてください。

* 管理するための技術としてgitを使う
* GitHubというサービスで本を管理する
* VSCodeなどメジャーなテキストエディタを使って、Markdownという世界標準の記述方法で原稿を書く
* ローカルでPDFを作成する場合は、ターミナル上でコマンドを入力して作成する
* GitHub ActionsによってPDFが自動生成される

## この本を書いたモチベーション

筆者がVivliostyleを使って、Re:VIEW<span class="footnote">https://reviewml.org/ja/</span>と同じような技術同人誌をサクサク作れるようにするために書いた本です。

もともと親方Projectの合同誌をRe:VIEWからVivliostyleに移行できるか？の検証をするというのが主目的です<span class="footnote">親方Projectで記事を寄稿してくれる人のうち、元々技術同人誌をゴリゴリに書いてた人を除けば大体Markdownで原稿を書いています。それならいっそ最初からMarkdown前提のCSS国版に移行したいというモチベーションになりました。</span>。

Re:VIEWは技術同人誌を書く上で標準となっているソフトウェアです。Vivliostyleの強力なライバルといえますが、Vivilostyleでも同じような本が作れることを証明したくてこの本を書いています。

そのため、目指すレギュレーションは「Markdownで楽に原稿を書く」と「Re:VIEWで本を作ったときと同じこと・同じデザインをなるべく再現する」です。

* GitHub ActionsでPDFが自動生成されること
* ローカルでも同じようにPDFを作成できること
* クォリティもなるべくRe:VIEW Techbooster techbookスタイルに近づける
* できる限り特殊な記法を導入しない

この本は2部構成になっています。第1部はとにかく簡単に本を作るための説明のみに絞りました。第2部はVivliostyleで実現するためのノウハウと知見についてまとめました。そのため、本を書きたいだけの人は第1部だけを読めば大丈夫になっています。

## 既存組版のつらみ

皆さんは技術同人誌の組版をどうしてますか？多くの人はRe:VIEWを使っているでしょう。Re:VIEWはとても偉大なソフトウェアです。Re:VIEWによって技術同人誌ブームが発生し、世の中の様々な知見が同人誌として出回ることになりました。

ところがRe:VIEWにはいくつもの難関があります。

* Re:VIEW記法という独自記法を使っているため、ChatGPT/Claudeのような生成AIが全く学習しておらず、サポートを受けることができない<span class="footnote">頑張れば対応するためのプロンプトは作れるけど、それはそれで大変だし、そのプロンプトの分、生成AIの持つ知性を消費してしまう。</span>
* いい感じの本を作成しようとすると、結構色々頑張らないといけない。めちゃくちゃノウハウが必要
* Re:VIEWはあくまでLaTeXラッパーにすぎず、LaTeXのつらみを回避できない
* LaTeX環境を構築する必要がある。LaTeXはDockerを使わないと環境構築するだけでしんどすぎる
* Dockerを使うと楽はできるが、中身をいじろうとすると難易度が高い。たとえば現代的な任意のフォントを簡単には使えない
* LaTeXやRe:VIEWはアップデートし続けているため、それらに追従する必要がある
* LaTeXの吐き出すエラーが人類には意味不明すぎる
* 既存のテンプレートをカスタマイズするには、LaTeXと格闘する必要がある

Re:VIEWのバックエンドであるLaTeXは、日本のデジタル組版技術の知見が散々集まったものであり、クォリティがずば抜けています。ただ、LaTeXやTeXの思想としては、凝った組版をゴリゴリにやる前提なのと、Re:VIEW記法の独自性などが合わさって、結論としては僕らのような「原稿だけに集中したい」人にはハードルが高いです。

では、他の組版技術はどうか？残念ながらほぼ全滅です。日本の組版はかなり特殊なため、海外系の組版技術では日本の本を制作するのには不適切すぎてスタート地点にすら立てません。

今回選んだVivliostyleはその中でほぼ唯一、使い物になる選択肢で、これはCSS組版と呼ばれる手法をするためのソフトウェアです。LaTeXをいじるのとは違って、HTML+CSSの知識があれば自由自在に装飾できるという利点があります。

ただし、「自由自在に装飾できる」がくせ者で、僕らのような怠惰な人間にとっては、決して手放しで楽に、Re:VIEW並のハイクォリティで本が書けるというものではありません。

## リポジトリについて

この本のリポジトリは https://github.com/erukiti/vivliostyle-techbook-starter です。実際のソースコードがあるので、これを参考にして、皆さんも本を書いてみてください。

この本は著者であるerukitiと、親方Project有志によって作成されています。

TBD: 本のライセンスについて書く

## 謝意

TeX・LaTeXやRe:VIEWや、Vivliostyleなど、偉大なるソフトウェアを世に送り出した作者たちに最大限の感謝を述べます。あなた方の血と汗と涙の結晶がなければ、筆者は技術同人誌を世に送り出すことはできませんでした。

**本当に感謝しています**。

僕の試みで、さらに技術同人誌を書くハードルが下がることを願って本書を書いています。

## バージョンについて

本書で想定しているバージョンは次の通りです。

|ソフトウェア|バージョン|
|----------|---------|
|Node.js|v22.12.0|
|Vivliostyle|8.17.1|
