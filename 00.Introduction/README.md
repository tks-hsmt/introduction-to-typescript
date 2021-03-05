# TypeScriptとは

TypeScriptとは「型定義のできるJavaScript」です！
まずはこれだけ覚えてください！
型を定義することでプログラムを実行する前にエラーを発見できるというメリットがあります。

## JavaScriptの場合
```js
// 1. 数字を設定
let value = 1;
 
// 2. 数字を入れた変数に文字列を設定
value = 'value is 1';
```
1.で変数valueに数字を設定した後、2.で文字列を設定していますが、JavaScriptの場合はエラーになりません。

## TypeScriptの場合
```ts
// 1. 数字を設定
let value: number = 1;
 
// 2. 数字を入れた変数に文字列を設定
value = 'value is 1';  // エラー
```
1.で変数valueをnumberで定義して数字を設定した後、2.で文字列を設定しようとしていますが、TypeScriptの場合はnumberに対してstringを設定している為、エラーとなります。

> let value<span style="color: red; ">: number</span> = 1;

の<span style="color: red; ">赤文字</span>の部分が型定義の書き方です。
