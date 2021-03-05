# 基本ルール

コードを記述する際の基本的なルールについて説明します。

## 文

プログラムは、何らかの処理を行う為に記述されたコードである「 **文** 」の集まりです。

```ts
// 何らかの処理 = 文
let value: number = 1;
```

文の中で空白やタブなどの空白文字と改行は自由に挿入できます。

文と文の区切り文字として、セミコロン(;)をつけます。

> セミコロンを省略した場合も自動で付与してくれますが、思わぬ動作をする場合があるので **必ずつける** ようにしましょう。

```ts
// パターン① スペースなし OK
let value:number=1;

// パターン② 半角スペースあり OK
let value: number = 1;

// パターン③ 全角スペースあり OK
let value:　number　=　1;

// パターン④ 途中で改行あり OK
let value: number
    = 1;

// パターン⑤ 1つの文に複数の文をセミコロンで区切り記述 OK
let numValue: number = 1; let strValue: string = 'value is string';
```

> 現場毎のルールにもよると思いますが、基本的には1つの文の中は1つの処理で、半角スペースを利用して下さい(パターン②)

## ブロック

ブロックとは、「 **{}** 」で囲まれたコードです。文をグループ化するのに使います。
if や for 等を記載する際の「 **{}** 」の中身がブロックです。

```ts
// if
if (value === 1) {
  // 何かの処理 この中身がブロック
}

// for
for (const item of list) {
  // 何かの処理 この中身がブロック
}
```

## if文

条件分岐をさせたい場合は、if文を利用します。

```ts
// 値に1を設定
const value: number = 1;

// if (条件式) {}
if (value === 1) {
  // valueが1の場合はブロック内が実行される
  console.log('value is 1'); // ★
}

// if (条件式) {} else {}
if (value === 2) {
  // valueが1の為このブロックは実行されない
  console.log('value is 2');
} else {
  // valueが1の為elseブロック内が実行される
  console.log('value is 1'); // ★
}

// if (条件式) {} else if {} else {}
if (value === 2) {
  // valueが1の為このブロックは実行されない
  console.log('value is 2');
} else if (value === 1) {
  // valueが1の為else ifブロック内が実行される
  console.log('value is 1'); // ★
} else {
  // valueが1の為このブロックは実行されない
  console.log('value is 1');
}
```

## for文

処理を繰り返したい場合はfor文を利用します。

後述する配列の中身を繰り返し実行するような場合によく利用します。

配列の取り扱いについては後述するので、こんな書き方があるんだという理解までで大丈夫です。

```ts
// 配列を定義
const list: number[] = [1, 2, 3];

// 配列の長さでループ
for (const i = 0; i < list.length; i++) {
  console.log(list[i]);
}

// for...ofでループ
for (const item of list) {
  console.log(item);
}
```

## 大文字と小文字の区別

コードを記述する際に、変数名等は大文字と小文字が区別されます。

```ts
// 1. 数字を設定
let value: number = 1;
 
// 2. valueの値を更新
Value = 10;  // エラー
```

上記のコードを実行した場合、変数名「value」の値を更新したいのに誤って「Value」と記述してしまっている為、エラーとなります。

## 予約語

以下の予約語は特別な意味を持つ名前として登録済みの為、変数名や関数名としては利用できません。詳しくは[11.6.2 Keywords and Reserved Words](https://www.ecma-international.org/publications-and-standards/standards/ecma-262/#sec-keywords-and-reserved-words)を参照。

- await
- break
- case
- catch
- class
- const
- continue
- debugger
- default
- delete
- do
- else
- enum
- export
- extends
- false
- finally
- for
- function
- if
- import
- in
- instanceof
- new
- null
- return
- super
- switch
- this
- throw
- true
- try
- typeof
- var
- void
- while
- with
- yield
