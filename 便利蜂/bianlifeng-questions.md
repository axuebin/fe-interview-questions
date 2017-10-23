## 便利蜂一面

- 说说项目
- AJAX是怎么实现的
- AJAX如何判断请求成功
- AJAX的contentType有哪些
- post请求的数据放在HTTP请求哪个地方
- HTTP状态码知道哪些
- jQuery链式操作时如何实现的
- JavaScript中this是什么
- JavaScript中prototype是什么
  - 不用prototype可不可以实现继承
  - 通过构造函数定义和原型定义对象有什么区别
  - 共有方法放在构造函数中有什么缺点
- 代码题
  - 会打印什么
  - 只能修改最后一句如何让它正确打印
  - 修改倒数第二句呢

```javascrpt
function Person(name){
  this.name=name;
  this.say=function(){
    console.log(this.name);
  }
}
var person1=new Person("axuebin");
var say1=person1.say;
say1()
```

- es6方法用过哪些
- Promise有几个方法