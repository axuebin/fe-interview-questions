## 大搜车实习生笔试

#### 已经有padding如何让它的实际宽度减去padding

只要将盒子模型转换一下，让padding给计算到content里就好了，`box-sizing` 设为 `padding-box` 或者 `border-box` 即可。

#### 字符串中提取数字

这题不会。

- 比如 `我有100.11元`，要输出`100.11`。
- 如果有多个数组，要输出一个数组。

#### 2进制转10进制然后相加

```javascript
const add = function(num1, num2) {
  return parseInt(num1, 2) + parseInt(num2, 2);
}
```

#### 递归对象

这个无非就是需要对每次的值进行判断，是否是数组，大概的意思如下：

```javascript
const result = [];
function test(arr){
  for(let i = 0;i < arr.length;i += 1){
    if(Array.isArray(arr[i])){
      // 递归调用
    }else{
      result.push(arr[i]);
    }
  }
}
```

#### http状态码

可以先说一下分类吧：

- 1字头：表示临时响应，请求被接受了。
- 2字头：这类状态代码表明服务器成功地接受了客户端请求。
- 3字头：客户端浏览器必须采取更多操作来实现请求，比如重定向之类的。
- 4字头：发生错误，比如一些资源不存在或者权限不够的问题。
- 5字头：服务器由于遇到错误而不能完成该请求。

然后举几个常用的状态码：

- 200：请求成功。
- 302：临时重定向。
- 304：使用缓存。
- 400：请求出现语法错误。
- 403：由于服务器上文件或目录的权限设置导致。
- 404：无法找到指定位置的资源。
- 500：服务器出现错误。

#### PC端优化
#### 两个div并排方式，一个百分40宽，一个60宽

- float
- flex

#### call bind apply区别

[JavaScript call apply bind](https://github.com/axuebin/articles/issues/7)

#### localStorage sessionStorage cookies区别和场景

- localStorage:HTML5新增的本地存储。除非被清除，否则永久保存。不参与和服务器的通信。
- sessionStorage:仅在当前会话下有效，关闭页面或浏览器后被清除。不参与和服务器的通信。
- cookies: cookie由服务端生成，用于标识用户身份。可以设置失效时间。cookie在与服务器端通信每次都会携带在HTTP头中。

## 大搜车实习生技术面

#### babel如何将es6变成es5的

1. 解析：将代码字符串解析成抽象语法树
  1. 分词：将整个代码字符串分割成 语法单元 数组
  2. 语义分析：在分词结果的基础之上分析 语法单元之间的关系
2. 变换：对抽象语法树进行变换操作
3. 再建：根据变换后的抽象语法树再生成代码字符串

- [Babel将ES6代码转换成什么样了？（还没写好）](https://github.com/axuebin/articles/issues/14)
- [Babel是如何读懂JS代码的](https://zhuanlan.zhihu.com/p/27289600)
- [Babel 基础及代码转换简单探究](http://www.qcyoung.com/2017/02/06/Babel%20%E5%9F%BA%E7%A1%80%E5%8F%8A%E4%BB%A3%E7%A0%81%E8%BD%AC%E6%8D%A2%E7%AE%80%E5%8D%95%E6%8E%A2%E7%A9%B6/)

#### 单页面应用服务端渲染怎么做

这一块因为只是了解还没自己做过，所以不好回答。

- [精读前后端渲染之争](https://github.com/camsong/blog/issues/8)
- [单页面应用后台渲染的三次实践](https://github.com/phodal/articles/issues/20)
- [从单页应用(SPA)到服务器渲染(SSR)](https://zhuanlan.zhihu.com/p/24286605)

#### 单页面的SEO怎么优化，你有什么想法

- [单页面应用后台渲染的三次实践](https://github.com/phodal/articles/issues/20)

#### webpack看过文档吗，知道哪些配置

四个核心概念：入口(entry)、输出(output)、loader、插件(plugins)。

这一块不太了解，不敢给自己挖坑，所有没怎么说。

#### npm依赖包区别

- dependencies：生成环境中用到的依赖包
- devDependencies ：开发环境中用到的依赖包

#### 在哪学习前端

- Github，SegmentFault等了解开源技术以及最近流行的技术。
- MDN和ECMAScript规范学习JavaScript/HTML/CSS等。
- 看书，高程、深入理解ES6等。
- 遇到问题查书或者谷歌搜索。

#### 遇到问题怎么办

先分析一下问题可能出处，但是不要瞎猜，要不然会怀疑人生。。有条理的进行一步步地分析然后进行debug，遇到解决不了的问题就查一查Google上是否有标准的解法。

#### 有用代码规范检查吗

用的是 `ESLint` 来检查代码规范，其中用的是 `airbnb` 的规范。

#### es6了解哪些

`const `、箭头函数、字符串模板、`Promise`。

貌似面试官都比较喜欢问对于 `Promise` 了解多少。 

#### 测试有了解吗，测试的作用主要是什么

了解过单元测试但是没写过。

在JavaScript中，一般是以类或者模块作为一个单元。

单元测试是独立的。给单元测试一个输入，让它自动执行，将输出结果和预期结果做对比看其是否正确（输入可以是一个函数参数，输出就是函数的返回值）。

在写单元测试的时候，尽量将你的单元测试独立出来，不要几个单元互相引用。

#### node有了解吗
#### 平时是在Windows还是Linux下开发

如实回答。如果说在 `Linux` 下开发，但是命令一个都不会还是白扯。

#### 知道哪些常用linux命令吗

[Linux 常用命令](https://github.com/slowlog/slowlog.github.io/issues/5)

## 大搜车实习生HR面

#### 什么时候可以实习
#### 平时怎么学习前端的
#### 在哪了解到我们的，觉得我们哪里好
#### 你想去的一个公司应该是个怎么样的公司
#### 除了前端你还学习些什么
#### 对于自己的职业规划是什么，有想过吗
#### 除了导师的项目还有自己做一些东西吗
#### 有什么问题想问我