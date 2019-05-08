# ES6常用例子

### 1.const

定义一个变量或者常量，不可变

### 2.let

块级作用域的"var"

### 3.箭头函数

```
const fn = (a, b) => a + b;
```

相当于

```
var fn = function(a, b) {
    return a + b;
}
```

### 4.模板字符串

使用 `` 将整个字符串包裹起来，而在其中使用 ${} 来包裹一个变量或者一个表达式。

```
// es5
var a = 20;
var b = 30;
var string = a + "+" + b + "=" + (a + b);

// es6
const a = 20;
const b = 30;
const string = `${a}+${b}=${a+b}`;
```



### 5.展开字符串

用`...`来表示展开运算符，它可以将数组方法或者对象进行展开。

```
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 10, 20, 30];

// 这样，arr2 就变成了[1, 2, 3, 10, 20, 30];
```



### 6.新的数据类型Symbol

**Symbol**是用来定义对象的唯一属性名的不二之选