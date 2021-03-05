# 関数

## 関数の種類

関数には大きく、functionキーワードを使って定義される関数 **function () {}** と、アロー関数 **() => {}** の2種類があります。

この場ではアロー関数についてのみ説明します。

書式は以下の通りです

> const [関数名] = ([引数]): [戻り値の型] => {[処理]}

```ts
// 引数が無く、戻り値もないアロー関数の定義
const voidFunction = (): void => {
  console.log('call void function');
  // return;  voidは戻り値が無いということを表す型の為、returnを省略可能
}

// 引数があって、戻り値もあるアロー関数の定義
const increment = (value: number): number => {
  return value++;  // 戻り値がある場合はreturnを記述する必要がある
}

// 関数を実行
const value = increment(10);

console.log(value);  // 11

// 引数があって、戻り値もあるアロー関数の定義
const increment = (value: number): number => {
  return value++;  // 戻り値がある場合はreturnを記述する必要がある
}

// 関数を実行
const value = increment(10);

console.log(value);  // 11
```
