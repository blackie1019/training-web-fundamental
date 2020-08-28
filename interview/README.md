# Interview 題目
https://stoner609.github.io/2017/12/04/20171204_javascript_testA/

## 問題一：作用域(Scope)

console出來的值是多少?

```js
(function() {
    var a = b = 3;
})();

console.log(b);
```

## 問題二：創建原生方法

在String對象上創建一個repeatify函數，接收的這個參數，代表要重複幾次。

console.log('hello'.repeatify(5));

## 問題三：在JavaScript中，this是如何工作的?

console出來的結果?
能的話順便說出原因

```js
var fullname = 'John Doe';
var obj = {
   fullname: 'Colin Ihrig',
   prop: {
      fullname: 'Aurelio De Rosa',
      getFullname: function() {
         return this.fullname;
      }
   }
};
console.log(obj.prop.getFullname());
 
var test = obj.prop.getFullname;
console.log(test());
```
