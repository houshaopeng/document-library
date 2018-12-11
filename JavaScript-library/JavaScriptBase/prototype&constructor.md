JavaScript 之 构造函数与原型对象
===

> Create by **jsliang** on **2018-12-11 09:27:44**  
> Recently revised in **2018-12-11 13:06:06**

<br>

> “每个构造函数都有一个原型对象，  
> 原型对象都包含一个指向构造函数的指针，  
> 实例都包含一个指向原型对象的内部指针。”   
> —— 《JavaScript 高级程序设计》

<br>

# <a name="chapter-one" id="chapter-one">一 目录</a>

&emsp;**不折腾的前端，和咸鱼有什么区别**

| 目录 |                                                                             
| --- | 
| [一 目录](#chapter-one) | 
| <a name="catalog-chapter-two" id="catalog-chapter-two"></a>[二 前言](#chapter-two) |
| <a name="catalog-chapter-three" id="catalog-chapter-three"></a>[三 正文](#chapter-three) |
| &emsp;<a name="catalog-chapter-three-one" id="catalog-chapter-three-one"></a>[3.1 基础配置](#chapter-three-one) |
| <a name="catalog-chapter-four" id="catalog-chapter-four"></a>[四 总结](#chapter-four) |

<br>

# <a name="chapter-two" id="chapter-two">二 前言</a>

> [返回目录](#catalog-chapter-two)

<br>

&emsp;在编写学习 [Node 基础](https://github.com/LiangJunrong/document-library/blob/master/other-library/Node/NodeBase.md) 中，写到 Node 仿 Express 的时候，我写了这么一段代码：

```
let Application = () => {
  // ...
}

Application.prototype.get = (path, handle) => {
  // ...
}
```

<br>

&emsp;然后代码死活跑不起来，于是我就去问大佬，大佬默默回了句：

* **“构造函数不能用箭头函数呀”**

&emsp;我一愣：

* 为什么不能用构造函数？
* 什么时候我不能使用构造函数？
* 箭头函数的解释是什么咯？
* 什么是构造函数？
* ……

&emsp;所以，在下面，咱一一分析这些问题。

<br>

# <a name="chapter-three" id="chapter-three">三 正文</a>

> [返回目录](#catalog-chapter-three)

<br>

&emsp;参考文献：

1. [箭头函数 | 廖雪峰的官网](https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/001438565969057627e5435793645b7acaee3b6869d1374000)
2. [什么时候你不能使用箭头函数？ | 简书 - 王仕军](https://www.jianshu.com/p/1357112985ef)
3. [js深入理解构造函数和原型对象 | 博客园 - 快饿死的鱼](https://www.cnblogs.com/thonrt/p/5900510.html)
4. [一句话总结JS构造函数、原型和实例的关系 | CSDN - 夜色芜染](https://blog.csdn.net/u012443286/article/details/78823955)

<br>

# <a name="chapter-three-one" id="chapter-three-one">3.1 箭头函数</a>

> [返回目录](#catalog-chapter-three-one)

<br>

&emsp;ES6 标准新增了一种新的函数：Arrow Function(箭头函数)。  
&emsp;为什么叫箭头函数？

```
x => x * x;
```

&emsp;因为它的定义用的就是一个箭头。上面代码相当于：

```
function(x) {
  return x * x;
}
```

<br>

# <a name="chapter-four" id="chapter-four">四 总结</a>

> [返回目录](#catalog-chapter-four)

<br>

&emsp;

<br>

> <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br /><a xmlns:dct="http://purl.org/dc/terms/" property="dct:title">**jsliang** 的文档库</a> 由 <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/LiangJunrong/document-library" property="cc:attributionName" rel="cc:attributionURL">梁峻荣</a> 采用 <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">知识共享 署名-非商业性使用-相同方式共享 4.0 国际 许可协议</a>进行许可。<br />基于<a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/LiangJunrong/document-library" rel="dct:source">https://github.om/LiangJunrong/document-library</a>上的作品创作。<br />本许可协议授权之外的使用权限可以从 <a xmlns:cc="http://creativecommons.org/ns#" href="https://creativecommons.org/licenses/by-nc-sa/2.5/cn/" rel="cc:morePermissions">https://creativecommons.org/licenses/by-nc-sa/2.5/cn/</a> 处获得。