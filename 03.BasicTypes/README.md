# 基本型

## 真偽値(Boolean)

true か false を表します。

```ts
const isDone: boolean = false;
```

## 数値(Number)

10進数、16進数(0x〇〇〇)、8進数(0b〇〇〇)、2進数(0o〇〇〇)、bigint(〇〇〇n)を表します。

```ts
const decimal: number = 6;
const hex: number = 0xf00d;
const binary: number = 0b1010;
const octal: number = 0o744;
const big: bigint = 100n;
```

## 文字列(String)

文字列を表します。

シングルクォート( **'** )かダブルクォート( **"** )で囲みます。

```ts
const strValue: string = 'string value';
```

### テンプレート文字列

バッククォート( **`** )で囲み、埋め込み式( **${式}** )の形式で表現した形式です。

```ts
// ageに16を設定
const age: number = 16;

// 文中の「${age}」部分が「16」に置換される
const sentence: string = `Bob is ${age} years old.`;

console.log(sentence);  // Bob is 16 years old.
```

## 配列(Array)

データの入れ物を配列と言います。

参照する場合は0から始まる配列番号(インデックス)を指定します。

> 普段利用する場合は後述するfor文等で利用する場合が多いです。

```ts
// データ型[]での表現の仕方
const groupIds: number[] = [1, 2, 3];

// Array<データ型>での表現の仕方
const userIds: Array<number> = [10, 20, 30];

console.log(groupIds[0]);  // 1

console.log(userIds[1]);  // 20
```

### よく使う配列の機能

```ts
// 配列を宣言
const list: number[] = [10, 20, 30];

// 変数.length 配列の個数が取れる
console.log(list.length);  // 3

// 変数.push(追加したい値) 配列の最後に値を追加
list.push(40);

// 変数.lengthで配列の個数が増える
console.log(list.length);  // 4

// 新しいインデックスでアクセスすると増やした値が見える
console.log(list[3]);  // 40
```

## Tuple

複数のデータ型を持つことが出来る配列です。

1度定義した配列の数以上は追加できません。

```ts
// 1つ目は文字列、2つ目は数字の配列を定義
const tupleValue: [string, number] = ['string value', 10];

console.log(tupleValue[0]);  // string value

console.log(tupleValue[1]);  // 10
```

## Null と Undefined

色々な意見があるので難しいですが、以下のようなイメージで。

|型|説明|
|:--|:--|
|undefined|初期化されていないという状態を表す。|
|null|値が存在しないという状態を表す。|

## オブジェクト

任意の型のプロパティを持つ構造を表す型です。

```ts
// ageとnameというプロパティを持つhumanというオブジェクト
// ※ちなみに↓はブロック({})で記述しているが、代入している為セミコロン(;)が必要
const human = { age: 16, name: 'Bob' };

console.log(human.age);  // 16

console.log(human.name);  // Bob
```
