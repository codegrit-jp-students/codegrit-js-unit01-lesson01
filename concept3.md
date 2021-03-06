## 演算子(Operator)

演算子と一言で言っても、異なる種類の演算子がいくつか存在します。
まずは一番簡単で、数学でも取り扱われるものも含む**算術演算子/四則演算**を見ていきましょう。
その他の演算子は、レッスン3で詳しく学びます。

### 算術演算子/四則演算

レッスン2にも少し関係のある内容ですが、JavaScriptでは計算もできます。
ただし、数学と少し異なる部分もあり、文字（文字列と言います。詳細はレッスン2で学びます。）や文章同士を連結させるのにも使用します。

文字や文章同士の連結は1つの例ですが、詳細はレッスン2でも学びますので、今の所は算術演算子は、算術で使用するものと同じか、似た用途で使うものと覚えておいてください。

一覧にした方がわかりやすいので、算術演算子の一覧をまずは見ていきましょう。

| 算術演算子 | 説明 | 実例 | 結果 |
| ------------- | ------------- | ------------- | -----:|
| + | 加算 | 3 + 1 | 4 |
| - | 減算 | 3 - 1 | 2 |
| / | 除算 | 3/2 | 1.5 |
| * | 乗算 | 3*4 | 12 |
| % | 除算の剰算 | 3%2 | 1 |
| - | 単項符号反転 | -y | yの負の値 |
| + | 単項プラス | +y | yが文字列である場合に数値に変えることができる |
| ++ | 前置インクリメント | ++y | yに1を足す。式の値は1を加えたあとの値になる |
| ++ | 後置インクリメント | y++ | yに1を足す。式の値は1を加える前の値になる |
| -- | 前置デクリメント | --y | yから1を引く。式の値は1をマイナスしたあとの値になる |
| -- | 後置デクリメント | y-- | yから1を引く。式の値は1をマイナスする前の値になる |

以下は、各演算子を利用した計算の例です。

```js
let y = 4;
let x = 3 - -y; // 7

x++ // 7
x // 7
x = x % 3 // 1
x = x * 3 // 3
```

上記の`var x = 3 - -y;`を詳しく見ていきましょう。これは**単項符号反転**を使用した計算ですが、減算の`-`よりも**単項符号反転**が優先されて評価されます。そのため、アウトプット（答え）として`7`が返ってきます。

**単項符号反転**はJavaScriptでよく使用する演算子ですので、**単項符号反転が減算よりも優先されて評価を受ける**ということを覚えておきましょう。
（単項プラスも同じことが言えますが、あまり使用頻度は高くありません。）

## 大文字小文字の区別

先ほど上記にも出てきた変数名ですが、変数名をつけるときに、大抵は変数自体に関連のあるわかりやすい変数名をつけることが良いとされています。

上記の例のように、人の名前を変数に入れたい場合は名前に関連のある、`name`のような変数名にするのが一般的です。

HTMLのクラス属性やid属性でも該当箇所に関連のある属性の名前にしますね。

ただし、JavaScriptでは大文字と小文字の書き方に留意すべき点があるので、以下に比較例を紹介します。

```js
fuzzylittleturtle // ×

FuzzyLittleTurtle // ×

fuzzy_little_turtle // 正解 非推奨

fuzzyLittleTurtle // 正解 推奨
```

1番上の例はまず単語の区切りが分かりづらく読みにくいですね。そのためJavaScriptではこの書き方はしません。

2番目の例は、一番先頭の`Fuzzy`の頭文字が大文字になっていますが、この書き方はJavaScriptでは基本的に行いません。（例外もありますが、ここでは触れません。）

3番目の例はアンダースコア「 _ 」が単語ごとに区切りで入れてあるので、どんな変数なのかわかりやすいですね。この書き方は、プログラミングでは**_スネークケース_**と呼ばれています。RubyやPythonのような言語ではこの書き方が標準なのですが、Javascriptでは非推奨となっています。

JavaScriptでもっとも推奨されているのは最後の例です。、一番先頭の**fuzzy**の頭文字を除いて、２つ目以降の単語は頭文字が大文字になっています。この書き方を、**_キャメルケース_**と呼びます。ラクダのコブのように大文字箇所を識別しているためです。

今後、CodeGritではJavaScriptの標準に従いこのキャメルケースを利用します。

## コメント

JavaScriptのコメントは、基本的には以下のように書くことができます。

```js
// これはjsのコメント
```

ただし複数行にわたるコメントは以下のように書きます。

```js
/*
これもJavaScriptのコメント。
ただし複数行の場合に書くコメント。
CSSのコメントに似ていますね。
*/
```

## 予約語（KeywordsとReserved Words）

JavaScriptには、あらかじめ用意されている**予約語**と言うものが存在します。
これは例えば変数を宣言するときに使われる`var`などがそれに当たります。
JavaScriptですでに用意されているキーワードの`var`を、関数として以下のように使用したとしましょう。

```js
const var = function() {
  console.log('not working!');
}

var(); // エラーとして"Uncaught SyntaxError: Unexpected token var"が返る
```

予約語`var`が関数のfunctionとして使用されていなければ、このコードの結果はdeveloper toolに "not working!" と文字列として表示されたはずです。

しかし、すでにJavaScriptで用意されている予約語である`var`を関数として使用したことによってエラーメッセージが返ってきました。
予約語は変数名でももちろん使用することができず、エラーになります。

※ ここでは詳細はまだ触れませんが、予約語は変数、関数の他にもメソッド、オブジェクトの識別子でも使用できません。

以下は予約語の一覧です。

```
break case catch class const continue debugger
default delete do else enum export extends false
finally for function if implements import in
instanceof interface let new null package private
protected public return static super switch this
throw true try typeof var void while with yield
```