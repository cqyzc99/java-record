# Play-Java

# Java学习记录 

> 记录菜鸟Java的修仙之路~
> 💂 + 💻 = 👴🏽

## 第一阶段 🧱

### 概述 📕

- 计算机包括**硬件**和**软件**两部分组成



#### 硬件

```mermaid
 classDiagram
      总线 <|-- 中央处理器
      总线 <|-- 内存
      总线 <|-- 存储设备
      总线 <|-- 输入设备
      总线 <|-- 输出设备
      总线 <|-- 通信设备
      总线 : (bus)
      class 中央处理器{
      CPU
      }
      class 内存{
      主存
      }
      class 存储设备{
      如磁带、光盘、磁盘
      }
      class 输入设备{
      如键盘、鼠标
      }
      class 输出设备{
      如显示器、打印机
      }
      class 通信设备{
      如调制解调器、网卡
      }
```

#### 冯诺依曼体系结构

- ![查看源图像](https://gss0.baidu.com/-Po3dSag_xI4khGko9WTAnF6hhy/zhidao/wh%3D600%2C800/sign=a8ab5d01831001e94e691c09883e57d4/42166d224f4a20a44d44282f9e529822730ed0fb.jpg)

  > 冯·[诺伊曼](https://baike.baidu.com/item/诺伊曼)体系结构是现代计算机的基础，现在大多计算机仍是冯·诺伊曼计算机的组织结构，只是作了一些改进而已，并没有从根本上突破冯体系结构的束缚。冯·诺伊曼也因此被人们称为“计算机之父”。

- 如何选择该学习哪种程序设计语言？


> 没有“**最好**”的语言，**各有所长**

#### Java特点

1. 面向对象  ***(oop)***

2. 强类型机制、异常处理、垃圾自动收集

3. **跨平台性**

   >即一个编译好的class文件可以在多个系统下运行，这种特性称为跨平台性

   ```mermaid
   graph LR
    	A(Test.java) --> |编译 javac| B{Test.class}
    	B --> |运行 java| C[Windows的JVM]
    	B --> |运行 java| D[Linux的JVM]
    	B --> |运行 java| E[Mac的JVM]
   ```

4. 解释型语言

   - 不能直接被机器执行，需要**解释器**对class文件进行解释执行

   >解释性语言：JavaScript、PHP、**Java**、Python
   >
   >编译性语言：C / C++

#### Java的开发工具

- 先选择**文本编辑本**，到对Java有一定了解后，再使用IDEA 和 Eclipse等

- 为什么？

  >1. 更深刻的理解Java技术，培养代码感
  >2. 有利于公司面试 [需要手写代码]

#### Java运行机制

- 核心机制——Java虚拟机 [***JVM java virtual machine***] 

  >1. JVM是一个虚拟的计算机，具有指令集并使用不同的存储区域，负责执行指令，管理数据、内存、寄存器，包含在**JDK**中。
  >2. 对于不同的平台，有不同的虚拟机
  >3. Java虚拟机屏蔽了底层运行平台的差别，实现了"一次**编译**，到处**运行**"

- **什么叫做JDK,JRE？**

  - JDK介绍

    1. JDK全称 **Java Development Kit** ( Java 开发工具包 )

       >JDK = JRE + Java的开发工具[java, javac, javadoc, javap等]

    2. JDK是提供给开发人员使用的，其中包含了javac的开发工具，也**包括了JRE**。

  - JRE介绍

    1. JRE全称 **Java Runtime Environment** ( Java 运行环境 )

       > JRE = JVM + Java的核心类库[类]

    2. 如果想运行一个已经**开发好**的java程序（即`.class`文件）， 计算机**只需要安装JRE**即可

- **JDK**、**JRE** 和 **JVM**的包含关系

  1. JDK = JRE + 开发工具集
  2. JRE = JVM + Java SE标准类库

#### JDK的安装与配置

- 安装

  >⭐https://www.oracle.com/java/technologies/downloads/

- ***配置***  

  1. 复制根目录地址，右击我的电脑点击属性点击高级设置
  2. 点击环境变量，在上下两个变量区选择一个区新建
  3. 名字`JAVA_HOME` 下面一行将第一步复制的地址粘贴点击完成
  4. 选中`Path`点击编辑，新建，填入`%JAVA_HOME%\bin`,完成
  5. 在xx.java文件存储目录的地址栏输入`cmd`回车
  6. 输入"javac xx.java"编译，此时文件夹内多出一个`.class`文件，该文件为编译后的文件
  7. 接着在控制台输入"java xx.java",得到输出结果

#### 注意事项和细节说明

1. Java**源代码**以`.java`为扩展名，源文件的基本组成单位是**类**

2. Java应用程序的执行入口是**main()**方法。书写格式为：

   ```java
   public static void main(String[] args) {
       
   }
   ```

3. 严格区分大小写

4. Java方法由一条条语句构成，每个语句以"**；**"结束

5. 大括号**成对**

6. 一个源文件中最多**只能有一个**`public`类， 其他类的个数不限

7. 如果源文件包含一个`public`类，则文件名必须按该类名命名！

8. 可以将`main`方法写在**非**`public`类中， 然后指定运行非`public`类， 这样入口方法就是非`public`的`main`方法

#### 转义字符

1. **\t**	制表符

   ```java
   System.out.println("张三\t李四\t王五")
   ```

2. **\n**   换行符

   ```
   System.out.println("jack\nsmith\nmary")
   ```

3. **\\\\**    一个\

   ```
   System.out.println("D:\\Sublime Text\\Projests")
   ```

4. **\\"**   一个"

   ```
   System.out.println("老韩说：\"要好好学习java，有前途\"")
   ```

5. **\r**   回车符

   ```
   System.out.println("韩顺平教育\r北京")
   ```

#### 注释

1. 单行注释

   ```java
   //注释
   ```

2. 多行注释

   ```java
   /*
   
   */
   ```

   > 不允许有多行注释嵌套

3. 文本注释

   ```java
   /**
   *  @author	韩顺平
   *  @version	1.0
   */
   ```

   > 注释内容可以被JDK提供的工具`javadoc`所解析， 生成一套以网页文件形式体现的该程序的说明文档， 一般写在类

   - 如何生成对应的文档注释？

   - 应用实例

     >javadoc -d 文件夹名 -xx -yy Demo.java

   - `javadoc`标签

     | 标签 | 描述 | 示例 |
     | :--- | :--- | :--- |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |
     |      |      |      |

#### 代码规范(初学)

1. `类`、`方法`的注释， 要以`javadoc`的方式来写
2. 非`javadoc`的注释， 往往是给代码的维护者看的， 着重告诉读者为什么这样写， 如何修改， 注意什么问题等
3. 使用`Tab`操作，实现缩进， 默认整体向右移动， `shift + Tab`则相反
4. `运算符`和 `=` 两边习惯性各加一个空格
5. 源文件使用`utf-8`编码
6. 行宽度不要超过80字符
7. 代码编写`次行风格`和`行尾风格`

#### DOS [Disk Operating System]

- 基本原理

  ```mermaid
   graph LR
   A(DOS指令) --> B{DOS系统}
   B --> C(1.接收指令)
   C --> D(2.解析指令)
   D --> E(3.执行指令)
   E --> F(完成)
  ```

- **路径详解(重要)**

  > `相对路径`：从当前目录开始定位，形成的一个路径
  >
  > `绝对路径`：从顶级目录D， 开始定位， 形成的路径

  ```mermaid
   classDiagram
  	D盘 --> abc文件夹1
  	D盘 --> abc文件夹2
  	abc文件夹1 --> test100文件夹1
  	abc文件夹1 --> test200文件夹1
  	abc文件夹2 --> test100文件夹2
  	abc文件夹2 --> test200文件夹2
  ```

- 常用的`DOS`命令

  1. 查看当前目录

     ```
     dir d:\abc2\test200文件夹1
     ```

  2. 切换到其他目录下

     ```
     cd /D c:
     ```

  3. 切换到当前盘的其他目录下

     ```
     cd d:\abc文件夹2\test100文件夹2 cd ..\..\abc文件夹2\test200
     ```

  4. 切换到上一级

     ```
     cd ..
     ```

  5. 切换到根目录

     ```
     cd \
     ```

  6. 查看指定目录下所有的子级目录

     ```
     tree c:
     ```

  7. 清屏

     ```
     cls
     ```

  8. 退出DOS

     ```
     exit
     ```

  9. 说明：DOS在后面用得很少
     了解即可（在之后学习**Linux**需掌握指令）



------

###  变量 🔢

#### 概念

> `变量`相当于内存中一个数据存储空间的表示， 你可以把`变量`看作是一个房间的门牌号， 通过门牌号我们可以找到房间， 而通过`变量`名可以访问到`变量`（值）

#### 为什么需要变量？

- `变量`是程序的基本组成单位

  > 不论是使用哪种高级编程语言编写程序， 变量都是其程序的基本组成单位

#### 变量使用的基本步骤

1. 声明`变量`

   ```
   int a;
   ```

2. 赋值

   ```
   a = 60;
   ```

   [^ps]:通常一步到位， 即`变量`的使用 = 类型 + 名称 + 值

   ```
   int a = 60;
   ```

3. 使用输出

   ```
   System.out.println(a)
   ```

#### 尝试编写个人信息

```java
public static void main(String[] args) {
    //Record
    int age = 18;
    double score = 88.9;
    char gender = '男';
    String name = 'King';
    
    //Output
    System.out.println("本人信息如下：");
    System.out.println("age");
    System.out.println("score");
    System.out.println("gender");
    System.out.println("name")
}
```

#### 变量细节

1. `变量`表示内存中的一个存储区域[不同的`变量`， 类型不同， 占用的空间大小不同， 比如：int 4个字节；double 8个字节]
2. 变量必须先声明， 后使用
3. 该区域的数值可以在同一类型范围内不断变化
4. 变量在同一个`作用域`内不能重名

####  + 号的使用

1. 当左右两边都为数值型时， 做加法运算

2. 当左右两边有一方为字符串时， 做拼接运算

   ##### 尝试：

```java
System.out.println(100 + 98);//198
System.out.println("100" + 98);//10098
System.out.println(100 + 3 + "hello");//103hello
System.out.println("hello" + 100 + 3);//hello1003
```

#### 数据类型(必背)

##### 图示

```mermaid
 classDiagram
 	Java数据类型 --> 基本数据类型
  	Java数据类型 --> 引用数据类型
  	引用数据类型 --> 类
   	引用数据类型 --> 接口
  	引用数据类型 --> 数组
  	基本数据类型 --> 数值型
  	基本数据类型 --> 字符型
  	基本数据类型 --> 布尔型
  	数值型 --> 整数型
  	数值型 --> 浮点型
  	class 类{
  	class
  	}
  	class 接口{
  	interface
  	}
  	class 数组{
  	[]
  	}
  	class 字符型{
  	char[2]
  	}
  	class 布尔型{
  	boolean[1]
  	}
  	class 整数型{
  	byte[1]
  	short[2]
  	int[4]
  	long[8]
  	}
  	class 浮点型{
  	float[4]
  	double[8]
  	}
```

##### 整数类型

> 用于存放整数值

| 类型          | 占用存储空间 | 范围                                                 |
| :------------ | :----------- | :--------------------------------------------------- |
| byte[字节]    | **1字节**    | -2^7^ ~ 2^7^ - 1<br />为啥存放的范围是这个 => 二进制 |
| short[短整型] | **2字节**-   | -2^15^ ~ 2^15^ - 1                                   |
| int[整型]     | **4字节**    | -2^31^ ~ 2^31^ - 1                                   |
| long[长整型]  | **8字节**    | -2^63^ ~ 2^63^ - 1                                   |

```
byte n1 = 10;//1个字节
short n2 = 10;//2个字节
int n3 = 10;//4个字节
long n4 = 10;//8个字节
```

###### 使用细节

1. Java各整数类型有固定的范围和字段长度， 不受具体`OS`影响， 以保证`java`程序的可移植性

2. Java整型常量默认为`int`型， 声明`long`型常量须后加 '**l**' 或 '**L**'

3. Java程序中变量常声明为`int`型， 除非不足以表示大数， 才使用`long`

4. `bit`: 计算机中最小存储单位
   `byte`: 计算机中基本存储单位

   [^两者关系]: 1 byte = 8 bit

##### 浮点类型

> 表示一个小数

###### 分类

| 类型         | 占用存储空间 | 范围                   |
| ------------ | ------------ | ---------------------- |
| 单精度float  | **4字节**    | -3.403E38 ~ 3.40E38    |
| 双精度double | **8字节**    | -1.798E308 ~ 1.708E308 |

###### 说明

1. 关于浮点数在机器中存放形式的简单说明， `浮点数 = 符号位 + 指数位 + 尾数位`
2. 尾数部分可能丢失， 造成精度损失（小数都是近似值）

###### 使用细节

1. 与整数类型一样， Java各浮点类型有固定的范围和字段长度， 不受具体`OS`影响

2. Java的浮点型常量默认为`double`型， 声明`float`型常量， 须在后加 ‘**f**’ 或 ‘**F**’

   >double num1 = 2.1234567851;
   >
   >float num2 = 2.1234567851F;

3. 浮点型常量有两种表示形式

   > 十进制：如：5.12	512.0f	.512	(必须要有小数点)
   >
   > 科学计数法： 如： 5.12e2	5.12E2

4. 通常情况下， 应该使用double型， 因为它比float型更精准

5. 浮点数陷阱：2.7 和 8.1 / 3 比较

   ```java
   double num3 = 2.7;
   double num4 = 8.1/3;
   System.out.println(num3);//2.7
   System.out.println(num4);//接近2.7的一个小数
   ```

   

   > 因此当我们对运算结果是小数的进行相等判断时， 应该是以两个数的差值的绝对值， 在某个精度范围内判断

   ```java
   //错误
   if (num3 == num4) {
       System.out.println("相等")
   }
   //正确
   if (Math.abs(num3 - num4) < 0.0000000001) {
       System.out.println("差值非常小，到我规定的精度，认为相等……")
   }
   ```

##### 字符类型

> 表示单个字符（可以存放汉字）

```java
char c1 = 'a';
char c2 = '\t';
char c3 = '韩';
char c4 = 97;//字符 => 编码的概念
```

###### 使用细节

1. `char`常量时用单引号`‘’`括起来的单个字符
2. Java 中，char的本质是一个整数， 在输出时， 是unicode码对应的字符
3. `char`类型可以进行运算

###### 本质探讨

- [^存储]:'a' ==>  码值 ==>  二进制 ==> 存储

- [^读取]:二进制 ==> 97 ==> 'a' ==> 显示

###### 演示

```java
System.out.println('a' + 10);//107

char c5 = 'b' + 1;//98+1 ++> 99
System.out.println((int)c5);//99
System.out.println(c5);//字符
```

###### 字符编码表

- **ASCII**： 一个字节表示（实际一个字节能保存256个字符），共有128个字符
- **Unicod**： 字母汉字统一两个字节表示（占用空间），最多编码2^16^个字符，兼容ASCII
- **utf-8**： 字母一个字节，汉字3个字节，使用最广，可以使用1-6个字节表示一个符号
- **gbk**： 字母一个字节， 汉字两个字节
- **big5码**： 繁体中文，中国香港，中国台湾

##### 布尔类型

###### 介绍

1. 只允许取值`true`和`false`。无`null`
2. 占一个字节
3. 适用于逻辑运算

- while
- do-while
- for

###### 使用细节

> 不可以0或非0的整数代替false和true， 这点和C语言不同

#### 类型转换

##### 自动类型转换

###### 介绍

> 当java程序在进行赋值或者运算时， 精度小的类型自动转换成精度大的数据类型

###### 大小顺序

```mermaid
 graph LR
 	byte --> short
 	short --> int
 	char --> int
 	int --> long
 	long --> float
 	float --> double
```

###### 演示

```java
int a = 'a';//OK
double d = 80;//OK
```

###### 细节

1. 有多种类型的数据混合运算时， 系统首先自动将所有数据转换成精度最大的那种数据类型， 然后再计算

    ```java
    int n1 = 10;
    float d1 = n1 + 1.1;//false => 结果类型是double
    double d1 = n1 + 1.1;//true
    ```

2. 当我们把精度大的数据类型赋值给精度小的数据类型，会报错

    ```java
    int n2 = 1.1;//false => double精度>int精度
    ```

3. （`byte`, `short`）和 `char` 之间不会相互自动转换（当作规则理解）

4. 当把具体数值赋给 `byte` 时， 先判断该数是否在 `byte` 范围内， 如果是就可以

    ```java
    byte b1 = 10;//true  -128 - 127
    int n3 = 1;
    byte b2 = n3;//false 如果是变量赋值， 判断类型
    ```

5. `byte`, `short`, `cha`r 它们三者可以计算， 在计算时首先转换成 `int` 类型

    ```java
    byte b3 = 1;
    byte b4 =2;
    short s1 = 1;
    short s2 = s1 + b3;//false 结果类型为int
    int s2 = b2 + s1;//true
    byte b5 = b3 + b4;//false
    ```

6.  `boolean` 不参与转换

    ```java
    boolean pass = true;
    int num100 = pass;//false
    ```

7. 自动提升原则： 表达式结果的类型自动提升为操作数中最大的类型

    ```java
    byte b6 = 1;
    short s3 = 100;
    int num200 = 1;
    double num300 = 1.1;
    
    float = num300 + num200 + s3 + b6;//false 结果类型为double
    ```

##### 强制类型转换

###### 介绍

> 自动类型转换的逆过程， 将精度大的数据类型转换成精度小的数据类型

###### 格式

```java
int i = (int)1.9;
```

###### 演示

```java
int n2 = 2000;
int n1 = (int)1.9;//1	精度损失
byte b1 = (byte) n2;//数据溢出
```

###### 细节

1. 当大 --> 小时，就需要使用强制类型转换

2. 强转符号只对最近的操作数有效，往往使用小括号提升优先级

    ```java
    int x =(int)(10 * 3.5 + 6 * 1.5);
    ```

3. `char`类型可以保存`int`的常量值， 但不能保存`int`的变量值， 需要强转

    ```java
    char c1 = 100;//OK
    int m = 100;
    char c2 = m;//false
    char c3 = (char)m;//true
    ```

4. `byte`, `short`, `cha`r 它们三者可以计算， 在计算时首先转换成 `int` 类型

##### 练习

```java
1.  short s = 12;
	s = s - 9;
2.	byte b =10;
	b = b + 11;
	b = (byte)(b + 11);
3.	char c = 'a';
	int i = 16;
	float d = .314F;
	double result = c + i + d;
4.	byte b = 16;
	short s = 14;
	short t = s + b;
```

> 1.
>
> true
>
> false
>
> 2.
>
> true
>
> false
>
> true
>
> 3.
>
> true
>
> true
>
> true
>
> true
>
> 4.
>
> true
>
> true
>
> false

##### 基本数据类型和String类型的转换

###### 基本数据类型转String类型

> 语法： 将基本类型的值 + “” 即可

```java
int n1 = 100;
String str1 = n1 + ""
```

###### String类型转基本数据类型

> 通过基本类型的包装类调用parseXX方法即可

```java
Integar.parseInt("123");
Double.parseDouble("123.1");
Boolean.parseBoolean("true");
```

###### 注意事项

1. 在将String类型转成基本数据类型时，要确保有效数据， 例如不能把“hello”转成一个整数
2. 如果格式不正确程序将终止， 这个问题在后续异常处理章节， 会处理

#### Java API 文档

1. **API** [*Application Programming Interface*, *应用程序编程接口*]

   [^中文在线文档]:http://www.matools.com

2. Java 类的组织形式

   ```mermaid
    graph LR
    	A(JDK8,11) --> B(包1)
    	A(JDK8,11) --> C(包2)
    	A(JDK8,11) --> D(包...)
    	C(包2) --> E(接口)
    	C(包2) --> F(类...)
    	C(包2) --> G(异常)
    	F(类...) --> H(字段...)
    	F(类...) --> I(构造器)
    	F(类...) --> J(成员方法)
    	Java类的组织形式
   ```




------

### 运算符

#### 介绍

> 是一种特殊的符号， 用以表示数据的运算、赋值和比较等

1. 算术
2. 赋值
3. 关系
4. 逻辑
5. 位
6. 三元

#### 算术运算符

##### 介绍

> 对数值类型的变量进行运算

##### 图示

| 运算符 | 运算                                                     | 范例                                 | 结果                            |
| ------ | -------------------------------------------------------- | ------------------------------------ | ------------------------------- |
| +      | 正号                                                     | +7                                   | 7                               |
| -      | 负号                                                     | b = 11; -b                           | -11                             |
| +      | 加                                                       | 9 + 9                                | 18                              |
| -      | 减                                                       | 10 - 8                               | 2                               |
| *      | 乘                                                       | 7 * 8                                | 56                              |
| /      | 除                                                       | 9 / 9                                | 1                               |
| %      | 取余                                                     | 11 % 9                               | 1                               |
| ++     | 自增（前）： 先运算后赋值<br />自增（后）： 先赋值后运算 | a = 2; b = ++a;<br />a = 2; b = a++; | a = 3;b = 3;<br />a = 1;b = 2;  |
| --     | 同上                                                     | a = 2;b = --a;<br />a = 2;b = a--    | a = 1; b = 1;<br />a = 1;b = 2; |
| +      | 字符串相加                                               | “hsp” + "edu"                        | "hsp edu"                       |

```java
System.out.println(10 / 4);//从数学来看时2.5，java中是2
System.out.println(10.0 / 4);//java是2.5
double d = 10 / 4;
System.out.println(d);//java中是2， 2 => 2.0

//%的本质： a % b = a - a / b * b
System.out.println(-10 % 3);//-1
System.out.println(10 % 3);//1
System.out.println(-10 / -3);//-1
```

##### 细节

1. 取余本质： a % b = a - a / b * b
2. 对于除号"/"，它的整数除和小数除是有区别的：整数之间做除法时， 只保留整数部分而舍弃小数部分

##### 题目

```java
int i = 1;
i = i++;//规则使用临时变量：（1）temp = i;（2）i = i + 1;（3）i = temp;
System.out.println(i);//1

int i = 1;
i = ++i;//规则使用临时变量：（1）i = i + 1;（2）temp = i;（3）i = temp;
System.out.println(i)//2
```

1. 假如还有59天放假，问：合XX个星期零XX天

    ```java
    int days = 59;
    int weeks = days / 7;
    int leftDays = days % 7;
    System.out.println(days + "天合" + weeks + "个星期零" + leftDays)
    ```

    

2. 华氏温度转换：5 / 9 * (华氏温度 - 100), 求出华氏温度对应的摄氏度

    ```java
    double F = 234.6;
    double C = 5 / 9 * (F - 100);
    System.out.println(C);
    ```

#### 关系运算符

##### 介绍

> 结果都是boolean型

##### 图示

| 运算符     | 运算               | 范例                    | 结果  |
| ---------- | ------------------ | ----------------------- | ----- |
| ==         | 相等于             | 8 == 7                  | false |
| !=         | 不等于             | 8 != 7                  | true  |
| <          | 小于               | 8 < 7                   | false |
| >          | 大于               | 8 > 7                   | true  |
| <=         | 小于等于           | 8 <= 7                  | false |
| >=         | 大于等于           | 8 >= 7                  | true  |
| instanceof | 检查是否是类的对象 | "hsp" instanceof String | true  |

#### 逻辑运算符

##### 一览

1. 短路与 `&&`， 短路或 `||`， 取反` ！`
2. 逻辑与 `&`， 逻辑或` |`， 逻辑异或 `^`

##### 图示

| a    | b    | a & b | a && b | a \| b | a \|\| b | !a   | a ^ b |
| ---- | ---- | ----- | ------ | ------ | -------- | ---- | ----- |
| T    | T    | T     | T      | T      | T        | F    | F     |
| T    | F    | F     | F      | T      | T        | F    | T     |
| F    | T    | F     | F      | T      | T        | T    | T     |
| F    | F    | F     | F      | F      | F        | T    | F     |

##### && 和 &

1. `&&`短路与： 如果第一个条件为`false`， 则第二个条件不会判断， 最终结果为`false`， 效率高

2. `&`逻辑与： 不管第一个条件是否为`false`， 第二个条件都要判断， 效率低

3. 开发中， 使用的基本是短路与`&&`， 效率高

    ```java
    int a = 4;
    int b = 9;
    
    //短路与
    if (a < 1 && ++b < 50) {
        System.out.println("ok300");
    }
    System.out.println("a = " + a + "b = " + b);//a = 4;b = 9
    
    //逻辑与
    if (a < 1 & ++b < 50) {//先执行，再判断
        System.out.println("ok300");
    }
    System.out.println("a = " + a + "b = " + b);//a = 4;b = 10
    ```

##### || 和 |

1. `||`短路或： 如果第一个条件为`false`， 则第二个条件不会判断， 最终结果为`false`， 效率高

2. `|`逻辑或： 不管第一个条件是否为`false`， 第二个条件都要判断， 效率低

3. 开发中， 使用的基本是短路或`||`， 效率高

    ```java
    int a = 4;
    int b = 9;
    
    //短路或
    if (a > 1 || ++b > 4) {
        System.out.println("ok300");
    }
    System.out.println("a = " + a + "b = " + b);//a = 4;b = 9
    
    //逻辑或
    if (a < 1 | ++b < 50) {//先执行，再判断
        System.out.println("ok300");
    }
    System.out.println("a = " + a + "b = " + b);//a = 4;b = 10
    ```


#### 赋值运算符

- 基本赋值运算符

- 复合赋值运算符

    > a += b; [等价 a = a + b]
    >
    > a -= b;  [等价 a = a - b]

##### 特点

1. 运算顺序从左到右

2. 左边只能是变量，右边可以是变量、表达式、常量值

3. 复合赋值运算符会进行类型转换

    ```java
    byte b = 3;
    b += 2;//等价 b = (byte)(b + 2)
    b++;// (byte)(b + 1)
    ```

#### 三元运算符

##### 基本语法

> 条件表达式？表达式1：表达式2

##### 规则

1. 如果条件表达式为`true`， 运算后的结果是表达式1；

2. 如果条件表达式为`false`， 运算后的结果是表达式2；

    [^口诀]:一灯大师：一真大师

##### 案例

```java
int a = 10;
int b =99;
//1.a > b 为false
//2.返回 b--。 先返回b 的值， 然后再 b-1
//3.返回的结果是99
int result = a > b ? a++ : b--;
//修改
int result = a < b ? a++ : b--;//10
System.out.println("a = " + a);//11
System.out.println("b = " + b);//99
```

##### 使用细节

1. 表达式1和表达式2要为可以赋给接收变量的类型（或可以自动转换、强制转换）

    ```java
    int a = 3;
    int b =8;
    int c = a > b ? a : b;//true
    int c = a > b ? 1.1 : 3.4;//false
    int c = a > b ? (int)1.1 : (int)3.4;//true
    double d = a > b ? a : b + 3;//true 自动转换int -> double
    ```

    

2. 三元转换符可以转换成if-else语句

    ```java
    int res = a > b ? a++ : --b;
    
    if (a > b) {
        res = a++;
    }else {
        res = --b;
    }
    ```
    

##### 实现三个数的最大值

```java
int n1 = 55;
int n2 = 33;
int n3 = 123;

/*思路
	1.先得到 n1 和 n2 中最大的数， 保存到max1
	2.然后再求出 max1 和 n3 中最大的数， 保存到max2
*/

int max1 = n1 > n2 ? n1 : n2;
int max2 = max1 > n3 ? max1 : n3;

//使用一条语句实现,推荐上面方法
int max = (n1 > n2 ? n1 : n2) > n3 
    		? (n1 > n2 ? n1 : n2) : n3;
```

#### 运算符优先级

1. 运算符有不同的优先级， 如下表，上一行运算符总优先于下一行

    |      | .    []    {}    ;     ,                     |
    | ---- | -------------------------------------------- |
    | 单目 | ++    --    ~    ！                          |
    | 算术 | *    /    %    +    -                        |
    | 位移 | <<    >>    >>>                              |
    | 比较 | >    <    <=    >=    instanceof    ==    != |
    | 逻辑 | &    ^    \    &&    \|\|                    |
    | 三元 | ?    :                                       |
    | 赋值 | =    *=    /=    %=                          |

2. 只有单目运算符、赋值运算符是从右往左运算的

#### 标识符命名规则和规范

##### 概念

1. Java对各种变量、方法和类等命名时使用的字符序列称为标识符
2. 凡是自己可以起名字的地方都叫标识符

##### 规则

1. 由26个英文字母大小写， 0-9， 或$组成
2. 数字不能开头 int 3ab = 1;//false
3. 不可以使用关键字和保留字，但能包括关键字和保留字
4. 严格区分大小写，长度无限制
5. 标识符不能有空格int a b = 90;

##### 练习

```java
hsp;//T
hsp12;//T
1hsp;//F	数字不能开头
h-s;//F		不能由-
x h;//F 	有空格
h$4;//T
class;//F	关键字
goto;//F	保留字
stu_name;//T
```

##### 规范

1. 包名： 多单词组成时所有字母都小写
2. 类名、接口名； 多单词组成时， 所有单词的首字母大写，**大驼峰**
3. 变量名和方法名；多单词组成时， 第一个单词首字母小写， 第二个单词开始每个单词大写，**小驼峰**
4. 常量名： 所有字母都大写， 多单词时用下划线连接

#### 键盘输入

##### 介绍

> 在编程中， 需要接收用户输入的数据， 就可以使用键盘输入语句来获取

##### 步骤

1. 导入该类所在的包，java.util.*
2. 创建该类对象（声明变量）
3. 调用里面的功能

##### 案例

```java
Scanner scan = new Scanner(System.in);
//接收输入
System.out.println("请输入姓名：");
String name = scan.next();
System.out.println("请输入年龄：");
int age = scan.nextInt();

System.out.println("人的信息如下：");
System.out.println("名字=" + name + "年龄" + age);
```

#### 进制

##### 介绍

1. 二进制： 0，1， 满2进1.以0b或0B开头

2. 十进制： 0-9， 满10进1

3. 八进制： 0-7， 满8进1， 以数字0开头；

4. 十六进制： 0-9以及A（10）- F（15）， 满16进1， 以0X或0x开头表示， 此处A-F不区分大小写

    ```java
    int n1 = 0b1010;
    int n2 = 1010;
    int n3 = 01010;
    int n4 = 0x10101;
    ```

##### 图示

| 十进制 | 十六进制 | 八进制 | 二进制 |
| ------ | -------- | ------ | ------ |
| 0      | 0        | 0      | 0      |
| 1      | 1        | 1      | 1      |
| 2      | 2        | 2      | 10     |
| 3      | 3        | 3      | 11     |
| 4      | 4        | 4      | 100    |
| 5      | 5        | 5      | 101    |
| 6      | 6        | 6      | 110    |
| 7      | 7        | 7      | 111    |
| 8      | 8        | 10     | 1000   |
| 9      | 9        | 11     | 1001   |
| 10     | A        | 12     | 1010   |
| 11     | B        | 13     | 1011   |
| 12     | C        | 14     | 1100   |
| 13     | D        | 15     | 1101   |
| 14     | E        | 16     | 1110   |
| 15     | F        | 17     | 1111   |
| 16     | 10       | 20     | 10000  |

##### 进制转换（基本功）

###### 其他转十

1. 二进制转十进制

    [^规则]:从最低位（右边）， 将每个位上的数提取出来， 乘以2的（位数-1）次方， 然后求和

    - 0b1011 = 1 * 2^0^  + 1 * 2^1^ + 0 * 2^2^ + 1 * 2^3^  = 11

2. 八进制转十进制

    [^规则]:从最低位（右边）， 将每个位上的数提取出来， 乘以8的（位数-1）次方， 然后求和

    - 0234 = 4 * 8^0^ + 3 * 8^1^ + 2 * 8^2^ + 0 = 156

3. 十六进制转十进制

    [^规则]:从最低位（右边）， 将每个位上的数提取出来， 乘以16的（位数-1）次方， 然后求和

    - 0x23A = 10 * 16^0^ + 3 * 16^1^ + 2 * 16^2^ = 570

4. 练习

    > 0b110001100 = 1 * 2^2^ + 1 * 2^3^ + 1 * 2^7^ + 1 * 2^8^ = 396
    >
    > 02456 = 6 * 8^0^ + 5 * 8^1^ + 4 * 8^2^ + 2 * 8^3^ = 1326
    >
    > 0xA45 = 5 * 16^0^ + 4 * 16^1^ + 10 * 16^2^ = 2629

###### 十转其他

1. 十进制转二进制

    [^规则]: 将该数不断除以2， 直到商为零为止， 然后将每步得到的余数倒过来， 就是对应的二进制

    - 34 -> 0b00100010 （补齐八位）

2. 十进制转八进制

    [^规则]: 将该数不断除以8， 直到商为零为止， 然后将每步得到的余数倒过来， 就是对应的八进制

    - 131 -> 0203

3. 十进制转十六进制

    [^规则]: 将该数不断除以16， 直到商为零为止， 然后将每步得到的余数倒过来， 就是对应的十六进制

    - 237 -> 0xED

4. 练习

    > 123转二 --> 01111011
    >
    > 678转八 --> 1246
    >
    > 8912转十六 --> 22D0

###### 其他转其他

1. 二进制转八进制

    [^规则]:从低位开始， 将二进制数每三位一组， 转成对应的八进制数即可

    - 0b11 **(3)** 00 **(2)** 101 **(5)**  --> 325

2. 二进制转十六进制

    [^规则]:从低位开始， 将二进制数每四位一组， 转成对应的十六进制数即可

    - 0b1101(D)0101(5) --> 0xD5

3. 练习

    > 0b11100101转八 --> 345
    >
    > 0b1110010110转十六 --> 396

4. 八进制转二进制

    [^规则]: 将八进制数每一位，转成对应的一个3位数的二进制数即可

    - 0237 --> 0b010011111

5. 十六进制转八进制

    [^规则]:将十六进制数每一位，转成对应的一个4位数的二进制数即可

    - 0x23B --> 001000111011

6. 练习

    > 01230转成二进制 --> 0b1010011000
    >
    > 0xAB29转成二进制 --> 0b1010101100101001

#### 位运算

##### 思考

###### 1)

```java
int a = 1 >> 2;//1向右位移两位
int b = -1 >> 2;
int c = 1 << 2;
int d = -1 << 2;
int e = 3 >> 2;//

System.out.println("a = " + a);
System.out.println("b = " + b);
System.out.println("c = " + c);
System.out.println("d = " + d);
System.out.println("e = " + e);
```

###### 2)

```java
~2 = ?;//按位取反
2 & 3 = ?;//
2 | 3 = ?;//
~~5 = ?;
13 & 7 = ?;
5 | 4 = ?;
-3 ^ 3 = ?;
```

##### 原码、反码、补码（重点、难点）

1. 

##### 位运算符

------

### 程序控制结构

------

### 数组、排序和查找

------

### 面向对象编程（基础部分）

------

### 房屋出租系统

------

### 面向对象编程（中级部分）

------



## 第二阶段 ⚙️

### 面向对象编程（高级部分）

------

### 枚举和注解

------

### 异常

------

### 常用类

------

### 集合

------

### 泛型

------

### 坦克大战1

------

### 多线程编程

------

### 坦克大战2

------

### IO流

------

### 坦克大战3

------

## 第三阶段 🛖

### 网络编程

------

### 多用户即时通信系统

------

### 反射

------

### 零基础学MySQL

------

### JDBC和数据库连接池

------

### 满汉楼

------

### 正则表达式

------

### 算法——骑士周游问题

------

## 总结 📒
