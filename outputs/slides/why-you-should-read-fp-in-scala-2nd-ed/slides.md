---
theme: default
colorSchema: light
transition: none
fonts:
  sans: 'Inter, Noto Sans JP'
  serif: 'Domine, Noto Serif JP'
  mono: 'JetBrains Mono'

layout: image
image: /fpinscala2_title.png
---

<!--
Functional Programming in Scala第2版 読書のすすめというタイトルで発表いたします、かすてらふぃと申します。
-->

---
layout: default
---

# `whoami`

- **かすてらふぃ** / jiftechnify
- <twemoji-man-technologist-medium-light-skin-tone /> Full-stack™ SWE
- <twemoji-heart-hands-medium-light-skin-tone /> 自分の意図を**過不足なく素直に**書き下せるプログラミング言語が好き
- 最近の趣味
  - <twemoji-radio /> 海外の技術系Podcast視聴
    - イチオシ: [Developer Voices](https://www.developervoices.com)
  - <twemoji-man-walking /> 散歩
  - <twemoji-musical-keyboard /> 音ゲー
- <logos-github-icon /> [jiftechnify](https://github.com/jiftechnify), <twemoji-globe-with-meridians /> [c-stellar.net](https://c-stellar.net)

<v-drag pos="488,220,174,_">
  <img class="mx-auto w-48 object-contain rounded-full" src="/blackleaf.png" alt="jiftechnify's icon" />
</v-drag>

<!--
何でも屋をやっています。
自分の意図を過不足なく素直に書き下せる言語が好きです。
最近は海外の技術系ポッドキャストを聴くのにハマってます。
-->

---

# 赤い本

<img class="mx-auto w-60 object-contain" src="/redbooks.jpg" alt="red books" />

<v-drag pos="613,499,111,_">
  <div class="text-sm">
    @洗足池図書館
  </div>
</v-drag>

<!--
まず余談から。
最近、行きつけの図書館で赤い本特集みたいなのをやっていて、壮観だなぁとなったのですが、同時に、ぜひここにある本を一冊加えたいなぁと思ったのです。その本というのが…
-->

---

# 赤い本 in Scala

<img class="mx-auto w-90 object-contain" src="/fpinscala2.jpg" alt="FP in Scala 2nd Ed." />

<!--
この本です。
-->

---
layout: two-cols
---

<style>
.grid-cols-2 {
  column-gap: 2rem;
}
p.no-margin {
  margin-top: 0;
  margin-bottom: 0;
}
</style>

# Functional Programming in Scala

- Scala関数型プログラマーの「聖書」
  - "The Red Book"

<p></p>

> 関数型の色々な型クラスやパターンが「なぜそういう仕組になっているのか？」という根本的な考え方が分かる(略)

> 細かいScala自体の言語仕様や (略) 既存の実在するライブラリの使い方は一切説明せず、とにかく「考え方や概念」のみを重点的に説明しているので、この本を読んで身につけた知識は古くなりにくいという点でおすすめできる一冊です

<div class="w-full text-right text-sm mt-2">
  <a href="https://scala-text.github.io/scala_text/">Scala研修テキスト「はじめに」</a>より
</div>

<v-drag pos="65,436,416,_">
  <div class="flex items-end">
    <span class="text-sm mr-1">邦訳:『Scala関数型デザイン＆プログラミング』→</span>
    <img class="w-20 object-contain" src="/fpinscala_ja.jpg" alt="Scala関数型デザイン＆プログラミング" />
  </div>
</v-drag>

::right::

<img class="object-contain" src="/fpinscala2.jpg" alt="FP in Scala 2nd Ed." />

<!--
FP in Scala。
言わずと知れたScala関数型プログラマーの「バイブル」で、界隈では”The Red Book”と呼ばれて親しまれています。

初版は日本語訳も出ていて、表紙のデザインが原書と結構違うので、「赤い本」と言われてピンとこなかった方もいるかも。

ちなみに、この本読んだことがあるよという方？手をあげてみてください。

(読んだことない人が多かった場合)
「Scala研修テキスト」の最初のページにこの本がどんな本なのかを端的に言い表した文章が載っていたので引用しました。

TODO: クリックで「Second Edition」に集中線
-->

---

# FP in Scala 第2版
- [Manningの書籍ページ](https://www.manning.com/books/functional-programming-in-scala-second-edition)
- 2023年5月刊行
- メイン著者: Michael Pilquist氏
  - [fs2](https://fs2.io/#/)のコアメンテナ
- 現状、邦訳なし<twemoji-crying-face />

<!--
で、実は、FP in Scalaの第2版・Second Editionが2年半ほど前に出ていたんですが、みなさんご存知でしたか？

知ってるよ、読んだことあるよという方は挙手。

メインの著者は関数型ストリーム処理ライブラリ「fs2」のメンテナである マイケル・ピルクイストさんに交代しています。

残念ながら現状日本語訳は出ていないようです。
-->

---
layout: center
---

# Q. なぜ第2版を読むべきなのか？

<style>
h1 {
  font-size: 3rem;
}
</style>

<!--
さて、この発表のタイトルは
「FP in Scala「第2版」読書のすすめ」なわけですが、
どうして第2版を読むべきなのでしょうか。
-->

---
layout: center
---

# A. アップグレードが盛りだくさんだから！

<style>
h1 {
  font-size: 2.75rem;
}
</style>

<!--
それは、初版と比べて、いろいろな面でアップグレードしているからです。

というわけで、アップグレードの内容について紹介していきたいと思うのですが…
-->

---
layout: two-cols-header
---

# 変わっていないもの: 章立て

::left::

- Part 1: **関数型プログラミングの基礎**
  - 1 関数型プログラミングとは
  - 2 Scala関数型プログラミングの準備
  - 3 関数型プログラミングのデータ構造
  - 4 例外を使わないエラー処理
  - 5 正格と遅延
  - 6 純粋関数型の状態
- Part 2: **関数型設計とコンビネータライブラリ**
  - 7 純粋関数型の並列処理
  - 8 プロパティベーステスト
  - 9 パーサコンビネータ 

::right::

- Part 3: **関数型設計に共通する構造**
  - 10 モノイド
  - 11 モナド
  - 12 Applicative & Traversable
- Part 4: **作用とI/O**
  - 13 外部作用とI/O
  - 14 局所作用と可変状態
  - 15 ストリーム処理とインクリメンタルI/O

<style>
li li {
  font-size: 0.9rem;
}
</style>

<!--
その前に、変わっていないものについて。

この 4部・15章 構成は全く変わっていません！不変です。
-->

---

# 初版と第2版の差分: 概要

- Scala 3対応
- 第15章(ストリーム処理)の内容一新
- 全演習問題の解答・解説を収録

<!--
じゃあ、何が変わっているのか。

変更点は大きく分けて3つあります。
-->

---
layout: two-cols-header
---

# Scala 3対応: 新構文でコード例のノイズを削減

::left::

- Optional Braces
- New ("quiet") Control Syntax
- `enum`

etc.

::right::
例: List型の定義

```scala
// 1st Ed.
sealed trait List[+A]
case object Nil extends List[Nothing]
case class Cons[+A](head: A, tail: List[A]) extends List[A]

object List {
  def apply[A](as: A*): List[A] =
    if (as.isEmpty) Nil
    else Cons(as.head, apply(as.tail: _*))
}
```

```scala
//✨2nd Ed.
enum List[+A]:
  case Nil
  case Cons(head: A, tail: List[A])

object List:
  def apply[A](as: A*): List[A] =
    if as.isEmpty then Nil
    else Cons(as.head, apply(as.tail*))
```

<!--
まず、一番大きいのがScala 3の新機能の導入です。

例えば、Scala 3で入った
Optional Bracesなどの
括弧が少なく済む構文を積極的に取り入れたり、ADTをenumで書いたりによって、コード例がキュッとなりました。
-->

---
layout: default
---

# Scala 3対応: 型ラムダ

- やりたいこと: 型引数の部分適用
- 初版(Scala 2.x)では、ヤバい見た目の型を書いて無理やり実現していた
  - Structural Type + Type Projection<twemoji-exploding-head />
  - (すでにKind Projectorは存在していたようだが…)

```scala
// 1st Ed.
object IntStateMonad 
extends Monad[({type IntState[A] = State[Int, A]})#IntState] {
  // ...
}
```

- 第2版では、Scala 3の型ラムダ構文でスッキリ

```scala
//✨2nd Ed.
given IntStateMonad: Monad[[x] =>> State[Int, x]] with 
  // ...
```

<!--
そして、型ラムダ。

複数の型引数をとる型コンストラクタをモナドにしたいとき。
一部の型引数を固定したい、つまり型引数の部分適用をしたいとなるわけですが、

初版では、こんな、なんというかヤバい見た目の型を書いて無理やりやってたんですね。

第2版ではScala 3で入った型ラムダの構文でスッキリしています。
-->

---

# Scala 3対応: その他

- 第10章(モノイド)に型クラスの解説追加
  - 実は初版には「型クラス」という言葉が出てこない！
- Opaque Typeと拡張メソッドの活用
- 遅延評価コレクション: `Stream` → `LazyList`
  - (正確にはScala 2.13対応)

<!--
他にも、
型クラスについての解説が追加されてたり、
Opaque Typeとかがいい感じに活用されてたり、
細かいところでは最初の方に出てくるStreamがLazyListに変わったりしてます。
-->

---
layout: two-cols-header
---

# 第15章(ストリーム処理)の内容一新

::left::

- fs2の簡略版をイチから実装して学ぶ
  - エフェクト非対応版からスタート
  - エフェクト実行を挟めるように拡張
  - エラー処理とリソース管理機能を追加
  - <span class="text-gray-400">(Chunkや並行処理まわりは割愛)</span>
- Scala 3の新機能のおかげで本物のfs2のコードよりノイズが減っているので、「本質」に集中して学べる

::right::

```scala
// エフェクト非対応版Pull/Streamの雰囲気
enum Pull[+O, +R]:
  case Result[+R](result: R) extends Pull[Nothing, R]
  case Output[+O](value: O) extends Pull[O, Unit]
  case FlatMap[X, +O, +R](
    source: Pull[O, X],
    f: X => Pull[O, R]) extends Pull[O, R]

  def step: Either[R, (O, Pull[O, R])] = this match
    // ...

opaque type Stream[+O] = Pull[O, Unit]
```

<style>
.two-cols-header {
  column-gap: 2rem;
}
</style>

<!--
次に大きなポイントですが、この本の最後を飾る第15章、ストリーム処理の章 の内容が一新されました。

第2版では、あのfs2の簡略版を自分でイチから実装して学ぶ形になっています！
先ほど、第2版のメイン著者がfs2のコアメンテナだというがありましたが、伏線回収ですね。

まずエフェクトなしの純粋版からスタートし、少しずつ進化させていって、最後にはリソース管理機能がどうなっているかまで学べます。
-->

---

# 全演習問題の解答・解説を収録

- 初版では、演習問題の解答は[公式GitHubリポジトリ](https://github.com/fpinscala/fpinscala)に別途掲載
  - 解答やチャプターノートなどをまとめた[副読本](https://blog.higher-order.com/assets/fpiscompanion.pdf)もある
- 第2版では、全ての演習問題の解答が紙面上に掲載されている！
  - さらに、どこよりも丁寧な解説つき！
  - 詰まったときにチラ見してヒントにするもよし

> 議論の余地があるかもしれないが、解説つきの解答を含めることにした。これで、演習問題に詰まってやる気をなくしてしまった読者が、紙面上の解答を見て理解を深め、次へと読み進められるようになれば幸いである。

<div class="w-full text-right text-sm mt-2">
  「第2版へのまえがき」(preface to the second edition)より、拙訳
</div>

<!--
さらにもう一点。
FP in Scalaというと演習問題が難しいなんてイメージを持っている方も多いと思いますが、

なんと、第2版には全ての演習問題の解答に加え、どこよりも詳しい解説まで、全部紙面上に載っています！助かりますね。
-->

---

# FP in Scala「第2版」読書のすゝめ

- 初版・邦訳版を**読んだことがある**方へ
  - アップデートされた第15章を読み直すだけでも楽しめる
  - 開いたことはあるが演習が難しくて挫折してしまった方でも、解答が全部載っているので安心(?)
- FP in Scalaを**読んだことがない**方へ
  - **関数型プログラミングの「心」を知りたいなら、ぜひとも読むべき一冊**
    - (個人の感想)この本を読んではじめて、モナドのことを「わかった」と思えるようになった
  - 今から読むなら、ぜひ第2版を！
    - <span class="text-gray-400">(和訳が出ていれば、手放しで勧められるのだが…)</span>
  - 注意: FP in Scalaは何「ではない」か
    - **Scalaの入門書**ではない → [Scala研修テキスト](https://scala-text.github.io/)などからはじめよう
    - **関数型ライブラリ**<span class="text-sm">(Cats{, Effect}, ZIO, etc.)</span>**のガイドブック**ではない<br/>→ 公式ドキュメントの他、[なっとく！関数型プログラミング](https://www.shoeisha.co.jp/book/detail/9784798179803)・[Scala with Cats](https://scala-with-cats-ja.cohotech.co/dist/scala-with-cats.html)あたりを読むと幸せになれるかも

<!--
というわけで、第2版のアップグレード内容についてお話ししてきました。

これを踏まえて、FP in Scalaの第2版を読むべき理由をまとめてみました。

まず、邦訳版を含めた初版を読んだことがある方へ。
第15章がまるっきり書き変わっているので、そこを読むだけでも楽しめるはずです。
また、演習問題が難しくて読むのをやめてしまった方も、解答が全部載っているので、再チャレンジしてみてはいかがでしょうか。

次に、FP in Scalaをまだ読んだことがないという方へ。
もしあなたが、関数型プログラミングの本質、「心」を理解したいと思っているなら、この本が間違いなく助けになるはずです。ぜひ読みましょう。
個人的な体験ですが、自分はFP in Scalaを読んではじめて、自信を持ってモナドを「理解した」と思えるようになりました。
そして、今から読み始めるのであれば、8年の時を経て大幅にアップグレードした第2版をお勧めします。

ところで、FP in ScalaはScalaの入門書とか、Cats EffectやZIOなどのライブラリの使い方を教えてくれる本ではないので、そこのところはご注意を。
-->

---

# 入手方法

- [Manning Publicationsのオンラインストア](https://www.manning.com/books/functional-programming-in-scala-second-edition)にてお求めください
  - ちょうど今日(11/27)、Thanksgiving Dayセールで**50％OFF**！！！
  - 今日を逃しても、わりと頻繁にセールしてるので要チェック

<v-drag pos="317,193,409,_">
  <div class="flex items-end">
    <img class="object-contain" src="/manning_store_page.png" alt="Manning store" />
  </div>
</v-drag>

<!--
ここまでの話を聞いて、赤い本が欲しくなった方がいらっしゃれば、Manning Publicationsのオンラインストアからぜひお買い求めいただきたいのですが。

なんと、今日、アメリカのサンクス・ギビング・デイらしく、Manningの本がだいたい半額になっていて、FP in Scalaももちろん対象になってます！今がチャンス！
-->

---

# まとめ

- **FP in Scala 第2版を読もう！**

---
layout: center
---

# Thanks!

<style>
h1 {
  font-size: 4rem;
}
</style>
