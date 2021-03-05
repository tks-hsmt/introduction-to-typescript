# 変数宣言

変数宣言は以下のように記述します。

```ts
// valueという変数をletで宣言という意味
let value: number;
```

変数宣言にはvar、let、constの3種類があります。

varはあまり使ってほしくないので、ここではletとconstのみ説明します。

## let

letで変数宣言した場合、 **値を更新できます。**

```ts
// 宣言のみ
let numValue: number;

// 宣言と共に値を設定
let strValue: string = 'string value';

// 値を更新
numValue = 0;

// 値を更新
strValue = 'update value';
```

## const

constで変数宣言した場合、 **値を更新できません。**

```ts
// 宣言と共に値を設定
const strValue: string = 'string value';

// 値を更新
strValue = 'update value';  // エラー
```

## let、constで共通していること

### 変数の有効範囲(スコープ)

宣言した変数はどこからでもアクセスできるわけではなく、使える範囲が決まっています。

let、constはブロックスコープ( **ifやfor等の{}の中身** )です。

ブロックの中で宣言した変数は、 **同じブロックの中でのみ使えます。**

また、違うブロックであれば、 **同じ名前の変数を再宣言できます。**

```ts
// グループIDリスト
const groupIds: number[] = [1, 2, 3];
// ユーザIDリスト
const userIds: number[] = [10, 20, 30];

// forブロック(グループIDリストをループ)
for (const id of groupIds) {
  console.log(id);  // 1, 2, 3
}

// forブロック(ユーザIDリストをループ)
for (const id of userIds) {
  // 上のforでも「id」という変数を宣言して利用しているが、違うブロックの為再宣言できる。
  console.log(id);  // 10, 20, 30
}

// forブロックの外側でidにアクセスしようとしても、ブロックの外側の為アクセスできない。
console.log(id);  // エラー
```
