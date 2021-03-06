# Puread
Puread，中文名为纯阅读。
意在为开发者提供一个干净简洁的MVC框架，
同时希望开发者创造的站点能够为用户提供一个纯粹的阅读体验。
Puread提倡站点的设计以阅读为核心。

## 计划
实现一个IoC容器

## 特点
* 可视化模块

## Tips
* 是否内嵌web服务器

## 拓扑序列
* 阅读Spring源码
* 熟悉http协议
* tomcat服务器

## 主要包

我们可以有一个mvc.core项目，细分如下的包：
* common：公共的一组件，下面的各模块都会用到
* config：配置模块，解决框架的配置问题
* startup：启动模块，解决框架和Servlet如何进行整合的问题
* plugin：插件模块，插件机制的实现，提供IPlugin的抽象实现
* routing：路由模块，解决请求路径的解析问题，提供了IRoute的抽象实现和基本实现
* controller：控制器模块，解决的是如何产生控制器
* model：视图模型模块，解决的是如何绑定方法的参数
* action：action模块，解决的是如何调用方法以及方法返回的结果，提供了IActionResult的抽象实现和基本实现
* view：视图模块，解决的是各种视图引擎和框架的适配
* filter：过滤器模块，解决是执行Action，返回IActionResult前后的AOP功能，提供了IFilter的抽象实现以及基本实现


## 参考了哪些框架？

* sparkjava
* blade
* jFinal

* Laravel
* ThinkPHP

* Flask

## 怎么理解框架在Web开发中的地位？

- 如果你熟悉HTTP协议，那么任何Web框架上手应该很容易。Web框架的原理无外乎就是解析HTTP协议，然后给你Request，最后你按照Web框架规定的Response格式给出响应，至于中间，就是业务逻辑了，查询数据库，调用第三方 API之类，一般情况下，也就是需要写的代码了。所以只要是Web框架，都离不开HTTP协议然后就是语言层面了，就像Python的Tornado，这个框架是Python写的，如果你有Python基础，那么结合上面的HTTP协议就可以很快上手了。但是深入就不是那么简单了。
- 对于框架，我认为最重要的是为多人协作完成一件事情提供实现上的规范，其次是代码复用，减少工作量。

## 如何正确地使用框架？

Web框架的使用没什么难度，看官方网站文档照着打出来就能实现相应的demo， 难的是使用它需要具备的知识和经验，如熟悉Python语法、HTTP协议、一定的HTML/CSS/JS知识，并且知道前后端如何进行交互、数据库和ORM的使用、MVC、Request/Response/Middleware等等。作者在此不否认不同框架独有的设计哲学和杀手锏，比如Flask的Context和Django的Admin。无论是不是快速，只是学会框架的使用没什么用，单个框架不深入，多学另外几个也没有用。

## 为什么要写这个框架？

 Java Web诞生已久，从初始使用servlet或jsp技术开发，到日后Spring家族的框架产品在Java Web开发中占有了举足轻重的地位。虽然技术一直在发展进化，但Java Web开发中的“重”依然无法避免。Java语言编写的框架大都比较繁杂，搭建一个小型站点，仅是许多繁杂的配置文件就会让新手摸不清头脑。关键的是这些文件的配置对于我们理解web开发并没有太大意义。因此，作者萌生了编写一个简单易配置的Java Web框架的想法。但是，在开发大中型软件时，我们强烈建议使用Spring技术，其已经经过了历史的检验。 : )

## 开发过程

使用Servlet往往充当Controller的功能，

Controller中方法的返回

- 页面View
- 数据

