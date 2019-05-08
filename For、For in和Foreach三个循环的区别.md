# For、For in、Foreach以及For of循环的区别

### 1.for遍历

一般用于数组，若是遍历对象则不行

语法：略

### 2.for in遍历

一般用于遍历对象

语法很简单

for( x in 数组或者对象){

操作的代码

}

### 3.foreach遍历

这个方法对数组的每个元素执行一次提供的函数。

```
array.forEach(function(currentValue, index, arr), thisValue)
```

什么意思呢，就是给arr数组的index索引的currentValue项，进行函数的操作，换句话说就是给每个项调用函数操作

### 4.for of遍历

```
for (variable of iterable) {
    //statements
}
```

和for in很像，但是for of无法遍历对象，前者输出索引，后者输出数组的值