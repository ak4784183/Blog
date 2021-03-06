## arguments 对象

arguments 是一个伪数组对象. 它表示在函数调用的过程中传入的所有参数的集合.
在函数调用过程中没有规定参数的个数与类型, 因此函数调用就具有灵活的特性, 那么为了方便使用,
在 每一个函数调用的过程中, 函数代码体内有一个默认的对象 arguments, 它存储着实际传入的所有参数.

js 中函数并没有规定必须如何传参

1. 定义函数的时候不写参数, 一样可以调用时传递参数
2. 定义的时候写了参数, 调用的时候可以不传参
3. 定义的时候写了一参数, 调用的时候可以随意的传递多个而参数

在代码设计中, 如果需要函数带有任意个参数的时候, 一般就不带任何参数, 所有的 参数利用 arguments 来获取.
一般的函数定义语法, 可以写成:

```
    function foo ( /* ... */ ) {
    }
```

##### 利用 Function 创建一个函数, 要求允许函数调用时传入任意个数参数, 并且函数返回这些数字中最大的数字.

```
    function foo ( ) {
        // 所有的参数都在 arguments 中. 将其当做数组使用
        // 问题而已转换成在有一个数组中求最大值
        var args = arguments;
        var max = args[ 0 ];
        for ( var i = 1; i < args.length; i++ ) {
            if ( max < args[ i ] ) {
                max = args[ i ];
            }
        }
        return max;
    }
```