
# php learn
一个开源的脚本语言 可以动态生成html内容，强大之处在于字符串及数据的处理，也支持面向对象的编程，有标准的可选择的扩展模块，
php可以与数据库进行交互例如mysql，oracle，画图，建立pdf文件和解析xml等。
# 基础
- 大小写的区分：用户定义的类名，方法名，内部函数×和关键字 例如echo，while等是不区分大小写的。相反的变量是区分大小写的
- 语句和分号：php使用分号来分割简单的语句。
- 空格和换行：像java一样，php不区分空格和换行，你可以随便写
- 变量的命名：变量名总是以$符号开始并且大小写敏感
- 方法的命名：方法名是不敏感的
- 类的命名：同方法名  
- 常量：常量是一个值的标识符，只有基本变量boolean，integer，double，和string可以为常量。常量一旦设置不能被改变。常量使用define方法定义，例如define('PUBLISHER','xiaofans')

# 数据类型
php提供8种数据类型。integers，floating-point numbers，strings哦booleans为基本类型。arrays和objects为数值类型，还有两种特殊类型resource和NULL。  
- Resources：大部分模块会提供与外部连接的方法。例如，一个数据库扩展模块至少提供一个连接的方法，一个查询的方法和一个关闭连接的方法。由于你会有很多数据库连接在同一时刻，这个连接的方法提供你一些东西识别是那个连接，这个识别的标示叫做resource。Resources表面上看是integers，在不再使用的时候会被回收。使用is_resource($res)可以判断是否为资源类型。
- NULL
NULL的类型只有一个值，NULL的大小写敏感。NULL说明一个变量没有值。使用is_null可以判断一个变量有没有值。
- notice 你可以使用一个变量的值作为另一个变量的名字例如：$foo='bar';$$foo='baz' = $bar='baz';
- 引用变量 使用=&可以引用一个变量的值，若这样做。他原有变量的值将会消失。例如 $white='w'; $black=&$white;echo $black;的值为'w'
- 变量作用域 有4种类型的变量作用域：local,global,static,和function paramters。local可以理解为方法内部定义的变量，只有在方法内可见，方法外访问不到。其实在方法外定义的变量也叫global变量，在方法内也不可以访问。若想方法内访问变量需要加上global关键字来引用。
- static变量 static只在方法内保留值，声明使用static关键字，例如static $counter = 0。
