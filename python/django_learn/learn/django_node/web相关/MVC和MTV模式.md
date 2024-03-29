# MVC和MTV模式

著名的MVC模式：所谓MVC就是把web应用分为模型(M),控制器(C),视图(V)三层；他们之间以一种插件似的，松耦合的方式连接在一起。

模型负责业务对象与数据库的对象(ORM),视图负责与用户的交互(页面)，控制器(C)接受用户的输入调用模型和视图完成用户的请求。

![web_1](https://pic.amfc.ltd/learn/python/django/web_1.png)

Django的MTV模式本质上与MVC模式没有什么差别，也是各组件之间为了保持松耦合关系，只是定义上有些许不同，Django的MTV分别代表：

- Model(模型)：负责业务对象与数据库的对象(ORM)
- Template(模版)：负责如何把页面展示给用户
- View(视图)：负责业务逻辑，并在适当的时候调用Model和Template

此外，Django还有一个url分发器，它的作用是将一个个URL的页面请求分发给不同的view处理，view再调用相应的Model和Template

![web_2](https://pic.amfc.ltd/learn/python/django/web_2.png)
