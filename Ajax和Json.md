# Ajax和Json

### 1.Ajax是Asynchronous Javascript And XML的缩写

##### XMLHttpRequest()对象的属性

![](D:\H5new\Blog\异步\1.png)

![2](D:\H5new\Blog\异步\2.png)

![3](D:\H5new\Blog\异步\3.png)

---

### 第一步 判断支持对象与否

```
var xhr;	
if(window.XMLHttpRequest){
   xhr = new XMLHttpRequest();
}else{
   xhr = new ActiveXObjext('Microsoft.XMLHttp');
}
```

### 第二步 创建请求，get()或post()

```
open(method,url,bool)
```

method —— 请求类型 get / post
 url —— 请求地址
 bool —— 异步/同步请求
true：表示发送异步请求(当 Ajax 发送请求的时候，用户仍然可以对当前页面做其他操作)；
false：表示发送同步请求(当 Ajax 发送请求的时候，浏览器会锁定当前页面,用户不能对当前页面做其他操作)

### 第三步 发送请求，send()

若用get()，则填null，若用post()，里面填字符串

### 第四步 回调事件处理函数 onreadystatechange

```
![5](D:\H5new\Blog\异步\5.png)xhr.onreadystatechange = function(){
	if(xhr.readyState == 4 && xhr.status == 200){
		var txt = xhr.responseText;
               document.write(txt);
		   //DOM操作
	}
}
```

---

#### readyState状态

![](D:\H5new\Blog\异步\4.png)

#### status状态

![](D:\H5new\Blog\异步\5.png)



## 2.json

**在 JS 语言中，一切都是对象**。因此，任何支持的类型都可以通过 JSON 来表示，例如字符串、数字、对象、数组等。但是对象和数组是比较特殊且常用的两种类型。

对象：对象在 JS 中是使用花括号包裹 {} 起来的内容，数据结构为 {key1：value1, key2：value2, ...} 的键值对结构。在面向对象的语言中，key 为对象的属性，value 为对应的值。键名可以使用整数和字符串来表示。值的类型可以是任意类型。

数组：数组在 JS 中是方括号 [] 包裹起来的内容，数据结构为 ["java", "javascript", "vb", ...] 的索引结构。在 JS 中，数组是一种比较特殊的数据类型，它也可以像对象那样使用键值对，但还是索引使用得多。同样，值的类型可以是任意类型。

