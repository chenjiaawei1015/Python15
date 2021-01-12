# Python汇总

## Python基础

### day001

- Python 介绍
- Python 语言
  - 编译器与解释器
  - 编译型与解释型
  - 优缺点
- 变量
- 常量
- 注释
- 数据类型
  - 数字型
  - 字符串
  - 布尔型
- input
- if

### day002

- while循环
- break 与 continue
- 格式化输出
- 基本运算符
- 编码
- 计算机的单位换算
- in 与 not in

### day003

- int型
- bool型
  - 其他类型与 bool 型转换
  - bool型为 false 的情况
- 字符串
  - 索引与切片
  - 常用方法
- for循环

### day004

- 列表
  - 索引与切片
  - 增删改查
  - 常用方法
  - 嵌套列表
- 元组
  - 空元组与只有一个元素的元组
  - 查询
  - 二级元素的增删改查
  - 常用方法
- range

### day005

- 字典
- 字典的增删改查
- 字典的遍历
- 解构(拆包)

### day006

- is 与 == 与 id
- 小数据池
- 编码与解码

### day007

- 字符串的 join 方法
- 列表, 字典删除的注意点
- 集合
  - 增删改查
  - 交集, 并集, 差集, 反交集, 子集, 超集
  - forzenset 不可变集合
- 浅拷贝与深拷贝
  - = 没有进行拷贝操作
  - copy 方法, 浅拷贝
  - copy 模块的 deepcopy 方法, 深拷贝

### day008

- 冒泡排序
- 绝对路径与相对路径
- 文件操作
  - 操作模式
  - 文本文件的读写追加
  - 字节型文件的读写追加
  - \+ 模式
  - read
  - seek
  - tell
  - truncate 截断
- with 关键字
- 文件的更新

### day010

- 函数
- 实参与形参
- 函数返回值
  - 不写 return
  - 只写 return
  - return 1个值
  - return 多个值
- 函数参数
  - 实参角度
    - 位置参数
    - 关键字参数
    - 混合参数
  - 形参角度
    - 位置参数
    - 默认值参数
    - 动态参数

### day011

- 函数的动态参数

  - 位置参数的动态参数

  - 默认值参数的动态参数
- 函数形参的定义顺序
- 万能函数
- 函数的注释
- 命名空间
  - 内置命名空间
  - 全局命名空间
  - 局部命名空间
- 作用域
  - 全局作用域
  - 局部作用域
  - globals 与 locals
  - global 与 nonlocal
- 函数的嵌套
- 知识补充
  - 对于形参为默认值参数的注意点

### day012

- 三元表达式
- 函数名的作用
  - 函数名就是一个变量
  - 可以进行赋值
  - 可以作为函数的参数
  - 可以作为函数的返回值
- 闭包
- 闭包的优点
- 迭代器
  - 可迭代对象
  - 迭代器
  - for循环的原理
  - 可迭代对象与迭代器的鉴别方法

### day013

- 生成器
  - 定义
  - 生成器函数
  - 生成器函数的特点
  - send 与 \_\_next\_\_ 的区别
- 推导式
  - 列表推导式
  - 字典推导式
  - 集合推导式
- 生成器表达式
- 生成器取值的几种方式
  - \_\_next\_\_
  - send
  - 转换为列表
  - for 循环
- 生成器面试题

### day014

- 内置函数

### day015

- lambda表达式
- 匿名函数
- sorted()
- filter()
- map()
- 递归
- 二分查找

### day016

- 正则表达式
- re模块

### day017

- re模块及其常用方法
  - 查找
    - findall
    - search
    - match
  - 字符串处理 切割/替换
    - split
    - sub
    - subn
  - 进阶方法
    - compile 节省时间
    - finditer 节省空间
- re模块使用分组
  - search的分组
  - finditer的分组
- 命名分组
- 爬虫示例

### day018

- random模块
- time模块
- datetime模块
- os模块

### day019

- os模块补充
- 序列化模块
  - json
  - pickle

### day20

- 异常
- 异常处理
- 自定义异常

### day021

- 模块
- 包
- 绝对引入与相对引入

### day022

- 面向过程与面向对象
- 类
- 实例属性与类属性的访问与修改
- 嵌套函数模拟面向对象
- 类属性
- 继承与派生
- 多继承
  - 继承顺序
  - 广度优先与深度优先
- 继承原理
- super本质
- 多态
- 鸭子模型
- 封装
- 私有变量与私有方法
  - 自动变形

### day023

- 类的成员

  变量, 方法, 属性

- 私有与公有

- 类的组合

### day024

- 主动调用其他类的成员
  - 通过类直接调用
  - super
- 类的特殊成员
  - \_\_call\_\_
  - \_\_getitem\_\_ 与 \_\_setitem\_\_ 与 \_\_delitem\_\_
  - _\_add\_\_
  - \_\_enter\_\_ 与 \_\_exit\_\_
  - \_\_init\_\_ 与 \_\_new\_\_

### day025

- 类的特殊成员补充
  - \_\_iter\_\_
- 内置函数
  - issubclass
  - type
  - isinstance
- 函数与方法的区别
  - FunctionType 与 MethodType
- 反射
  - 模块的反射
  - 类的反射
  - 反射的四个方法 getattr hasattr setattr delattr
- 内置函数补充
  - callable

### day026

- 约束

  - 人为约束

  - 抽象类

- 自定义异常类

  - 捕获异常堆栈信息

- hashlib模块

- logging日志模块

  - 简单配置
  - 自定义配置

### day027

- 面向对象多继承
- 深度优先与广度优先
- C3算法
- 计算机网络
  - 发展史
  - ip协议, mac地址, arp协议, 路由器, 局域网, 子网掩码, tcp与udp
  - 三次握手与四次挥手
  - osi七层网络模型
- socket编程

### day028

- 黏包
- 黏包问题的解决
- 黏包案例分析
- subprocess模块
- struct模块

### day029

- socket实现文件上传
- hmac 模块
- socketserver 及其源码分析

### day030

- 线程
- 进程与线程的关系
- 全局解释器锁GIL
- 线程的创建

### day031

- socket 实现 FTP 客户端/服务端通信

### day032

- 操作系统知识
- 进程知识
- 串行, 并行, 同步, 异步, 阻塞, 非阻塞概念
- 进程的使用
- 线程与进程的关系
- 全局解释器锁GIL
- 线程的使用与其他方法

### day033

- 锁
- 同步锁/互斥锁
- 死锁
- 递归锁 RLock
- 信号量
- 事件
- 条件
- 定时器
- 线程队列与栈
- threadLocal
- 进程池, 线程池
- 生产者消费者模型

### day034

- 进程

- 进程操作

- 守护进程

- 锁

- 信号量

- 事件

- 条件

- 进程间通信

  - 管道

  - 队列
  - Manager

- 生产者消费者模型

- 进程池

- 爬虫案例

### day035

- 并行/并发 阻塞/非阻塞 同步/异步
- 协程
- greenlet
- gevent
- 五种IO模型
  - 阻塞IO
  - 非阻塞IO
  - IO多路复用
  - 信号驱动
  - 异步IO
- IO多路复用
  - select 模块
- selectors模块
  - select
  - pool
  - epool

### day036

- HTML
- 标签介绍

### day037

- CSS
- 导入
- 选择器
  - 基本选择器
  - 高级选择器
- CSS继承性和层叠性
- 盒模型
- 浮动

### day038

- CSS的padding
- 默认样式的清除
- 边框
- margin
- 标准文档流
- 块级元素和行内元素
- display
- 浮动
  - 元素脱标
  - 元素互相贴靠
  - 元素的字围效果
  - 收缩效果
- 清除浮动

### day040

- 浮动特性总结
- 盒子的居中显示
- 文字属性和字体属性
- 文本的居中显示
- background属性
- css脱离标准文档流的三种方式
- 定位
  - 静态定位
  - 相对定位
  - 绝对定位
  - 固定定位

### day042

- javascript基础
- DOM

### day043

- DOM
- 节点操作
- 属性操作
- innerHTML innerText value 三者的用法

