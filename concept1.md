## プログラムとは

プログラミング言語とは何か簡単に言うと、プログラムを書くための言語を指します。ではプログラムとは何でしょうか？これは、例えると料理のレシピに近いです。例えばカレーを作るためのレシピを想像してください。このレシピは日本語で書かれており、レシピには野菜や肉を切ることから始まって、切った肉や野菜を炒める、煮る、カレー粉を加える、と言った複数の指示が書かれています。これを順番に行っていくと最終的にカレーが出来上がりますよね。

プログラムというのは料理のレシピと同じで、コンピュータに対して、最終的にカレーのような成果物を作るための複数の指示の集合と言えます。例えばレシピでも日本語で書かれていても、英語で書かれていても最終的な成果物は同じかもしれません。同じようにプログラムも同じ成果のものを色々なプログラミング言語で書けます。しかし英語にはない日本語の表現だってあります。例えば英語ではわかめも昆布ももずくも全部"Sea weed"といいます。だから日本食を作るなら日本語が一番向いているといえるでしょう。同じようにプログラミングでも作りたいものによって向いている言語や向いていない言語があります。

実際には、もっと複雑なのですが、まずはプログラムは料理のレシピみたいなもので、プログラミング言語はレシピを書くための言語と認識して頂いて大丈夫です。

## JavaScriptとは？

JavaScriptは、インターネット黎明期の1995年、ネットスケープ(Firefoxの前身)ブラウザにプログラムを加えるために生まれました。その後他のブラウザにも採用されていき、現在ではブラウザ内だけではなく、サーバーやデータベースなど様々な用途で利用されています。

## JavaScriptの歴史

JavaScriptは現在でも進化をし続けています。元々JavaScriptはFirefoxの前身であるネットスケープといういブラウザのために開発されました。その後様々なブラウザに採用される中で標準的な言語仕様が固まりました。この標準的なものを*ECMAScript*と呼びます。現在のブラウザがサポートしているのは、このECMAScriptの5つ目のバージョン(ES5)です。

## ES6(ES2015)

上記の通り、現在のブラウザはES5までをサポートしていますが、2015年には次世代のES6(2015年に固まったのでES2015とも呼ばれる)の仕様が固まりました。 ES6ではES5にあった様々な欠点が改善されており、今後主要ブラウザでもサポートされていきます。またES6のコードをES5のコードへと変換する(トランスパイルと呼ぶ)ツールが多くあり、既に多くの企業がES6を当たり前のように使っています。このことから、CodeGritでもこのES6を基準にレッスンを行っていきます。今後レッスンの中でJavaScriptと書く時はES6のことを指します。

## JavaScriptとJavaは違う言語

よくJavaScriptのことをJavaと訳す方がいて、JavaScriptとJavaを一緒だと考える方がいますがこの2つは全く別の言語です。なぜ名前が似ているのかというと当時から広く使われていたJavaの人気に便乗しようというマーケティング目的だそうです。そのため、JavaScriptを略したい場合は"Java"ではなく"JS"と呼びます。

## フロントエンド開発におけるJavaScript

フロントエンドでの開発はHTML、CSS、JavaScriptの3つが互いを補う形で出来ています。HTMLはコンテンツの構造や内容を表現し、CSSはそのコンテンツのスタイルを定義するもの、そして最後にJavaScriptは表示されているコンテンツに動きを与えます。例えば、以下のような用途でJavascriptが使われています。

- Webサイト上のボタンをクリックしたときに別のコンテンツを表示させる。
- フォーム上でパスワードの長さの確認や、空白がないか確認する。
- Webサーバーにフォームのデータを送信する。

## 式(Expression)と文(Statement)

Javascriptのコードは式と文の組み合わせで出来ています。式とは最終的に何らかの値を返すコードの固まりのことをいいます。例えば、3 + 4 は7という値を返す式です。ここで「+」のことを演算子と呼びますが、

文とは簡単にいうと、何らかの処理を行うためのJavascriptコードの固まりを指します。

これだけでは分かりづらいかと思いますので、以下で詳しくみていきましょう。

## 式(Expression)

式は、分解すると**識別子**（変数名や関数名)と**リテラル値**（1, 'こんにちは'などの数値や文字列）、**演算子**(+,-など)の3つに分けることができます。

数値や文字列、変数名や関数名についてはレッスン2以降で詳しく解説しますが、少し理解しておくと後で理解しやすくなりますので、簡単に解説します。

```js
// nameという変数に"Julia"という値を代入しています。nameが変数名にあたります。
const name = 'Julia';

// 自分の名前を返すsayMyNameという関数。sayMyNameが関数名
function funcName() {
  document.write(name);
}
funcName(); // -> Julia
```

### 変数名

**_変数名_**とは、上記の例で言う「Julia」という文字を入れておく入れ物のことです。
数学の代入の考え方を思い出してみてください。

`name = "Julia"`を`x = 2`などの代入と同じ構成として見ることができますね。
今は `const` や Julia という文字を囲んでいる「''（シングルクォート）」に関して詳しく言及しませんが、レッスン2以降で学んでいきます。

### 関数名

**関数名**とは、上記の例でいうと、`funcName`がそれにあたります。
変数名と非常に似ていますが、関数名は単に入れ物の中身を指定するだけにとどまりません。
呼び出したい機能（関数）を収納することができ、呼び出すと、収納しておいた機能が使えると、ここでは覚えておいてください。

上記の例にある`function`や`document.write`など、その他の部分についても、今後のレッスンで学びます。

### 式の例

以下の例は全て式です。

```javascript
var x = 4; // xという変数に4を代入

x // 4という数値を返す
x + 1 // 5という数値を返す。
1 + 3 // 4という数値を返す
funcName() // 'Julia'という文字列を返す。
```

## 文(Statement)

文には例えば**if文**、**while文**のようなものがあります。先程のsayMyNameという関数も文です。例えば以下はif文を使った例です。

```js
const isTrue = true;

// isTrueという式がif文の中に出てくる
if (isTrue) {
  // 省略
}
```

`isTrue` は上記でも取り上げたように、変数名です。つまり、式と言うことになります。このように式は文の中に一部になることが出来ます。反対に、Javascriptでは文は式になることができません。

例えば、以下の文はJavascriptではエラーを返します。

```javascript
const isHuman = true
const myName = if (isHuman) { return "Julia" }
```

なぜかというと、式は値を返さないので変数myNameに値として格納出来ないためです。

### 文の例

以下の例は全て文です。

```javascript
if(式) { 処理 };
while(式) { 処理 };
for(式) { 処理 };
function(式) { 処理 };
```