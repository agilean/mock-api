# mock-api(模客)
[mock-api](http://mock-api.com/?from=Agilean)(模客)是一个线上restful api的模拟平台。前端开发人员可以使用该平台建立虚拟的后端api，从而在开发测试阶段脱离对后端开发进度的依赖。后端开发人员同样可以使用该平台建立虚拟的外部系统的api，从而在开发测试阶段隔离外部真实系统的依赖。

# 注册
第一步在注册页面输入有效的邮箱和密码之后，您会收到一封带有注册码的邮件，在第二步的页面输入该注册码就注册成功了，以后就可以使用之前填写的邮箱和密码登录了。

# 开始使用
1. 登录系统之后，首先要建立`模拟系统`，`模拟系统`可以代表某一个后端服务，也可以是一组相关的api集合。
2. 进入建立好的`模拟系统`后就可以创建`规则`，规则由一组`http request(请求)`和`http response(响应)`组成，请求和响应的具体编写方式可以查看规则编辑页面的[帮助文档](http://mock-api.com/rule-help.html)。规则创建时可以指定属于哪一个api以及tag(分类标签)，后续可以通过api和tag来查找和过滤规则。
3. 建立完需要的规则后可以进入`模拟`界面，该界面有 `启动`／`暂停`／`结束` 按钮，点击启动按钮表示开始模拟，这时之前编辑的规则都会生效，当有规则里定义的`请求`被触发时模拟系统会返回预先定义好的`响应`。
4. 模拟系统启动之后，系统会给出改系统的一个`url地址前缀`，前端或者真实系统可以通过这个虚拟的url地址加上后续的api地址来访问自定义的虚拟api, (比如:系统给出的模拟url为***http://mock-api.com/wjzpy8gX.mock***, api为***/users***, 则使用***http://mock-api.com/wjzpy8gX.mock/users***就可以访问到虚拟的api了)。如果要切换回真实环境，把api的地址改回原来的真实环境即可。
5. 模拟系统会记录对虚拟api的访问历史(请求与响应)以及一些简单的统计，后续会逐步开放更详细的统计。

### [新手图文教程](https://github.com/agilean/mock-api/wiki/新手教程)

# 特性
* 支持text/xml/json/form等多种格式的请求
* 支持参数化和表达式的响应
* 支持响应返回多种异常http status code(非200)
* 支持响应返回自定义的http header
* 支持基于soap协议模拟，[参考例子](https://github.com/agilean/mock-api/wiki/%E5%B0%8F%E4%BE%8B%E5%AD%90:-%E6%A8%A1%E6%8B%9Fsoap%E5%8D%8F%E8%AE%AE%E7%9A%84api)
* 支持基于jsonp的跨域请求模拟，[参考例子](https://github.com/agilean/mock-api/wiki/%E5%B0%8F%E4%BE%8B%E5%AD%90:-%E6%A8%A1%E6%8B%9Fjsonp%E7%9A%84%E8%B7%A8%E5%9F%9F%E8%AF%B7%E6%B1%82)

# 案例
### 模拟微信支付api
改案例通过模拟模拟微信支付api，可以在开发调试阶段模拟微信支付接口返回支付结果，不用实际支付，这样可以模拟任何金额的交易甚至异常或者交易失败的情况。进入下面的公众号后点击支付可以看到实际例子。
<br/>
<img src="https://github.com/agilean/mock-api/blob/master/wiki-content/WechatIMG.jpeg" width="200">

# 联系方式
* QQ交流群：555715964
* 邮箱：support@agilean.cn
