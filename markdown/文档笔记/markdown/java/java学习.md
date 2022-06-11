## 安装开发环境

JDK 是一个软件包，其中包含各种工具和实用程序，可以开发、打包、监控和部署为任何标准 Java 平台构建的应用程序，包括 Java 平台标准版  (Java SE); Java 平台，微型版 (Java ME);和 Java 平台企业版 (Java EE)。

### 卸载JDk

1. 删除Java安装目录
2. 删除环境变量JAVA_HOME
3. 删除path下关于JAVA的目录
4. Java -version
4. Eclipse IDE

安装JDK
百度搜索JDK8，找到下载地址
同意协议，下载电脑对应的版本，如64位操作系统下载 jdk-8u281-windows-x64.exe
双击安装JDK
记住安装路径
配置环境变量
我的电脑-》属性-》系统高级设置-》环境变量
系统变量 新建–> JAVA_HOME 输入对应的jdk安装路径
path变量–>% JAVA_HOME%\bin
测试是否成功 cmd–>Java -version

<font color = red>安装程序</font> IDEA

SDKs属性选择JDK

在idea中配置好jdk，之后测试使用

### Hello world

1. 新建一个文件夹，存放代码
2. 新建一个Java文件

- 文件名后缀为.java
- hello.java
- 注意系统后缀名

3. 编写代码

~~~java
public class hello{
	public static void main(String[] args){
		System.out.print("Hello,woeld!");
	}
}
~~~

4. 编译Javac.java文件，会生成一个class文件

5. 运行class文件，Java class文件

   ![image-20220403175040416](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220403175040416.png)

可能遇到的情况：

1. 每个单词的大小写不能出现问题，Java严格区分大小写
2. 文件名不要使用中文，尽量使用英文
3. **文件名和类**必须一致，并且首字母大写
4. 符号中可能会有中文符号
5. 注意环境变量

#### idea操作

**一. 基础输入操作**



![avatar](D:\Desktop\Program item directory\markdown_project file\markdown\java\image\Java.png)

##### psvm直接自动输入编写操作

![avatar](D:\Desktop\Program item directory\markdown_project file\markdown\java\image\java (2).png)

##### sout直接自动输入编写操作

![avatar](D:\Desktop\Program item directory\markdown_project file\markdown\java\image\java (3).png)

## 注释

1. 单行注释 //
2. 多行注释 /* */
3. 文档注释 /** */

##标识符和关键字

- Java 所有的组成部分都需要名字。类名、变量名、方法名都被称为**标识符**

##数据类型

![avatar](D:\Desktop\Program item directory\markdown_project file\markdown\java\image\java (4).png)

```java
//整数
int num1 = 10; //最常用，只要别超过21亿（2^31-1）
byte num2 = 20; //-128~127
short num3 = 30;
long num4 = 30L; //long类型数字后面要加个L(尽量用大写，小写l容易与1搞混)

```

```java
//小数：浮点数
float num5 = 50.1F; //float类型数字后面要加个F
double num6 = 3.141592653589793238;

```

```java
//字符
char name = '国';
//字符串, String不是关键字，是类
//String namea = "薛之谦";

```

```java
//布尔值：是非
boolean flag = true
    
```

## 扩展

```java
//整数扩展： 二进制0b		八进制0		十进制		十六进制0x
int i = 10;
int i2 = 010; //八进制 8
int i3 = 0x10; //十六进制 16

```

```java
//浮点数扩展：
//面试题：银行业务字母怎么表示钱? BigDecimal(数学工具类)
//float double是有问题的，最好避免使用浮点数进行比较
float f = 0.1f; 	//0.1
double d = 1.0/10;  //0.1
System.out.println(f==d); //false
//浮点数 位有限，舍入误差，大约
//最好避免使用浮点数进行比较
float f1 = 23131313131f;
float f2 = f1+1;
System.out.println(f1==f2); //true

```

```java
//字符扩展：所有字符本质还是数字
char c1 = 'a';
char c2 = '中';

System.out.println(c1);		//a
System.out.println((int)c1);//强制类型转换,97
System.out.println(c2);		//中
System.out.println((int)c2);//强制类型转换,20013

//编码 Unicode表（97=a,65=A）2字节 0-65536
//U000~UFFFF 十六进制（u0061=a,相当于十进制的97）
System.out.println('\u0061');  //a '\'是转义字符

```

```java
//布尔值扩展
boolean flag = true;
if(flag==true){} //新手
if(flag){}	//老手这样写 Less is More(代码要精简易读)

```



##类型转换

![avatar](D:\Desktop\Program item directory\markdown_project file\markdown\java\image\java (5).png)

```java
//强制转换 （类型）变量名 高--低
//自动转换 低--高
int i = 128;
byte b = (byte)i; //强制转换 内存溢出 -128~127
double d =i; //自动转换

System.out.println(i); //128
System.out.println(b); //-128
System.out.println(d); //128.0
/*
   注意点：
   1.不能对布尔值进行转换
   2.不能把对象类型转换为不相干的类型
   3.在把高容器转换到低容量的时候，强制转换
   4.可能存在内存溢出，或者精度问题
 * */
System.out.println((int)23.7); //23 丢失精度
char c = 'a';
int n = c+1;
System.out.println(n); //98
System.out.println((char)n); //b

```

```java
//当操作数比较大时，注意溢出问题
//JDK7新特性，数字之间可以用下划线分割
int money = 10_0000_0000; //10亿，下划线不会被打印出来
System.out.println(money); //1000000000
int years = 20;

int total = money*years;  //数据大，溢出
System.out.println(total); //-1474836480

long total2 = money*years; //默认是int，转换前就有溢出问题
System.out.println(total2); //-1474836480

long total3 = money*(long)years; //先把一个数转Long
System.out.println(total3); //20000000000

```



## 变量

变量：就是可以变化的量

Java是一种强类型语言，每个变量都必须声明其类型。

Java变量是程序中最基本的存储单元，其要素包括变量名，变量类型和<font color= red>作用域</font>

```java
type varName [=value] [{,varName[=value]}];
//数据类型 变量名 = 值；可以使用逗号隔开来声明多个同类型变量。
```

注意事项：

- 每个变量都有类型，类型可以是基本类型，也可以是引用类型。(string引用类型)
- 变量名必须是合法标识符。
- 变量声明是一条完整的语句，因此每一个声明都必须以分号结束

Demo07

```java
public class Demo07{
    public static void main(String[] args){
        //int a,b,c;
        int a = 1;
        int b = 2;
        int c = 3;
        String name ="qinjiang";
        char x = "x";
        double pi = 3.14;
        
    }
}
```

#### 变量作用域

- 类变量
- 实例变量
- 局部变量

```java
public class  Variable{				//类
     static int = allClicks = 0; //类变量
    String stc="Hello world";	//实例变量
    public void method(){
        int i = 0;	//局部变量
    }
        
}
```

局部变量：必须声明和初始化值

实例变量：从属于对象；如果不自行初始化，这个类型的默认值	0	0.0

Demo08

```java
public class Demo08{
    
    //类变量 static 
    static double salary = "2500";
    //属性：变量
    //实例变量：从属于对象；如果不自行初始化，这个类型的默认值	0  0.0
    //布尔值：默认是folse
    //除了基本类型，其余默认值都是null；
    
    String name;
    int age;
    //main方法
    public static void main(String[] args){
      
        //局部变量：必须声明和初始化值
        int i = 10;
        System.out.println(i);
        
        //变量类型 变量名字 = new Demo08();
        Demo08 demo08 = new Demo08();
        System.out.println(demo08.age);
        System.out.println(demo08.name);
        
        //类变量 static
        System.out.println(salary);
        
    }
    //其他方法
    public void add(){
        System.out.println(i);
    
    }
}
```

## 常量

常量：

- 初始化后不能再改变的值！不会变动的值。

- 所谓常量可以理解成一种特殊的变量，它的值被设定后，在程序运行过程中不允许被改变。

```java
final 常量名 = 值；
final double PI = 3.14;
```

- 常量名一般使用大写字母。

```java
//修饰符 不存在先后顺序，static可以写final后面
static final doube PI=3.14; //类变量，该类下的全局范围

```



```java
public class Demo09{
    
    //修饰符，不存在先后顺序
    static final double PI = 3.14;
    
    public static void main(String[] args){
        System.out.println(PI);
    }
}
```

####命名规范

- ​	所有的变量、方法、类名:见名知意
  - 类成员变量：首字母小写和驼峰原则：monthSalary 除了第一个单词以外，后面的单词首字母大写 lastname 	lastName
  - 局部变量：首字母小写和驼峰原则
  - 常量：大写字母和下划线：MAX_VALUE
  - 类名：首字母大写和驼峰原则：Man，GoodMan
  - 方法名：首字母小写和驼峰原则:run(),runRun()

####Java关键字大全



将Java关键字进行分类，并将Java关键字含义整理成表，如下表所示：

| Java关键字类别       | Java关键字   | 关键字含义                                                   |
| :------------------- | :----------- | :----------------------------------------------------------- |
| 访问控制             | private      | 一种访问控制方式：私用模式，访问控制修饰符，可以应用于类、方法或字段（在类中声明的变量） |
| 访问控制             | protected    | 一种访问控制方式：保护模式，可以应用于类、方法或字段（在类中声明的变量）的访问控制修饰符 |
| 访问控制             | public       | 一种访问控制方式：共用模式，可以应用于类、方法或字段（在类中声明的变量）的访问控制修饰符。 |
| 类、方法和变量修饰符 | abstract     | 表明类或者成员方法具有抽象属性，用于修改类或方法             |
| 类、方法和变量修饰符 | class        | 声明一个类，用来声明新的Java类                               |
| 类、方法和变量修饰符 | extends      | 表明一个类型是另一个类型的子类型。对于类，可以是另一个类或者抽象类；对于接口，可以是另一个接口 |
| 类、方法和变量修饰符 | final        | 用来说明最终属性，表明一个类不能派生出子类，或者成员方法不能被覆盖，或者成员域的值不能被改变，用来定义常量 |
| 类、方法和变量修饰符 | implements   | 表明一个类实现了给定的接口                                   |
| 类、方法和变量修饰符 | interface    | 接口                                                         |
| 类、方法和变量修饰符 | native       | 用来声明一个方法是由与计算机相关的语言（如C/C++/FORTRAN语言）实现的 |
| 类、方法和变量修饰符 | new          | 用来创建新实例对象                                           |
| 类、方法和变量修饰符 | static       | 表明具有静态属性                                             |
| 类、方法和变量修饰符 | strictfp     | 用来声明FP_strict（单精度或双精度浮点数）表达式遵循IEEE 754算术规范 |
| 类、方法和变量修饰符 | synchronized | 表明一段代码需要同步执行                                     |
| 类、方法和变量修饰符 | transient    | 声明不用序列化的成员域                                       |
| 类、方法和变量修饰符 | volatile     | 表明两个或者多个变量必须同步地发生变化                       |
| 程序控制             | break        | 提前跳出一个块                                               |
| 程序控制             | continue     | 回到一个块的开始处                                           |
| 程序控制             | return       | 从成员方法中返回数据                                         |
| 程序控制             | do           | 用在do-while循环结构中                                       |
| 程序控制             | while        | 用在循环结构中                                               |
| 程序控制             | if           | 条件语句的引导词                                             |
| 程序控制             | else         | 用在条件语句中，表明当条件不成立时的分支                     |
| 程序控制             | for          | 一种循环结构的引导词                                         |
| 程序控制             | instanceof   | 用来测试一个对象是否是指定类型的实例对象                     |
| 程序控制             | switch       | 分支语句结构的引导词                                         |
| 程序控制             | case         | 用在switch语句之中，表示其中的一个分支                       |
| 程序控制             | default      | 默认，例如：用在switch语句中，表明一个默认的分支。Java8 中也作用于声明接口函数的默认实现 |
| 错误处理             | try          | 尝试一个可能抛出异常的程序块                                 |
| 错误处理             | catch        | 用在异常处理中，用来捕捉异常                                 |
| 错误处理             | throw        | 抛出一个异常                                                 |
| 错误处理             | throws       | 声明在当前定义的成员方法中所有需要抛出的异常                 |
| 包相关               | import       | 表明要访问指定的类或包                                       |
| 包相关               | package      | 包                                                           |
| 基本类型             | boolean      | 基本数据类型之一，声明布尔类型的关键字                       |
| 基本类型             | byte         | 基本数据类型之一，字节类型                                   |
| 基本类型             | char         | 基本数据类型之一，字符类型                                   |
| 基本类型             | double       | 基本数据类型之一，双精度浮点数类型                           |
| 基本类型             | float        | 基本数据类型之一，单精度浮点数类型                           |
| 基本类型             | int          | 基本数据类型之一，整数类型                                   |
| 基本类型             | long         | 基本数据类型之一，长整数类型                                 |
| 基本类型             | short        | 基本数据类型之一,短整数类型                                  |
| 基本类型             | null         | 空，表示无值，不能将null赋给原始类型（byte、short、int、long、char、float、double、boolean）变量 |
| 基本类型             | true         | 真，boolean变量的两个合法值中的一个                          |
| 基本类型             | false        | 假，boolean变量的两个合法值之一                              |
| 变量引用             | super        | 表明当前对象的父类型的引用或者父类型的构造方法               |
| 变量引用             | this         | 指向当前实例对象的引用，用于引用当前实例                     |
| 变量引用             | void         | 声明当前成员方法没有返回值，void可以用作方法的返回类型，以指示该方法不返回值 |
| 保留字               | goto         | 保留关键字，没有具体含义                                     |
| 保留字               | const        | 保留关键字，没有具体含义，是一个类型修饰符，使用const声明的对象不能更新 |

<font size=2><font color=red>Java所有的组成部分都需要名字。类名、变量名以及方法名都被称为表示符。</font></font>

java标识符

- <font size=3>所有的标识符都应该以字母（A-Z或者a-z），美元符（$)，或者下划线(_)开始</font>
- 首字母之后可以是字母（A-Z或者a-z），美元符（$)，或者下划线(_)或数字的任何字符组合
- <font color=red>不能使用关键字作为变量名或方法名</font>
- 标识符是<font color=red>大小写敏感</font>的
- ![avatar](D:\Desktop\Program item directory\markdown_project file\markdown\java\image\java (6).png)
- 合法标识符例子：age、$salary、_value、_1_value
- 非法标识符例子：~~123abc、-salary、#abc~~
- <font size=2>尽量不要使用中文命名，养成全英文操作命名文件的习惯，也不建议使用拼音，主要是显得很LOW</font>

####Java运算符

Java语言支持如下运算符：

算术运算符：+，-，*，/，%，++，--

赋值运算符 =

关系运算符：>,<,>=,<=,==,!=instanceof

逻辑运算符：&&，||，！

位运算符：&，|，^,~,>>,<<,>>>(了解！)

条件运算符？：

扩展赋值运算符：+=，-=，*=，/=

基本运算

```java
package operator;
public class Demo01;{
    public static void main(String[]args){
        //二元运算符
        //ctrl + D :复制当前行到下一行
        int a = 10;
        int b = 10;
        int c= 10;
        int d = 10;
        System.out.println(a+b);
        System.out.println(a-b);
        System.out.println(a*b);
        System.out.println(a/(double)b);
    }
}
```

#### 自增自减运算

a++,,++a

```java
// ++自增 --自减 单目运算符
int a = 3;
int b = a++; //b=a,a=a+1 先赋值 即b=3 a=4
int c = ++a; //a=a+1,c=a 先自增 即a=5 c=5

System.out.println(a); //5
System.out.println(b); //3
System.out.println(c); //5

```

```java
//幂运算 2^3 2*2*2=8
double pow = Math.pow(2,3); // (底数，指数)double型
System.out.println(pow); //8.0

```

```java
//扩展：笔试题 i=5 s=(i++)+(++i)+(i--)+(--i) s=?
int i=5;
int s=(i++)+(++i)+(i--)+(--i);
System.out.println(s); //24

```

####逻辑运算

- && 逻辑与运算：两个变量都为真，结果为true
- || 逻辑与运算：两个变量有一个为真，结果为true
- ! 取反，真变为假，假变为真

```java
// 与(snd) 或(or) 非(取反)
boolean a = true;
boolean b = false;

System.out.println(a&&b); // false
System.out.println(a||b); // true
System.out.println(!(a&&b)); // true

int c=5;
boolean d = (c<5)&&(c++<5); //第一个值为false，后面就不进行判定了
System.out.println(d); //false
System.out.println(c); //5 c++未执行

```



逻辑运算符

```java
public class Demo07 {
    public static void main(String[] args) {
        //与（and)  或(or)   非(取反)
        boolean a = true;
        boolean b = false;

        System.out.println("a && b: "+(a&&b)); //逻辑与运算：两个变量都为真，结果才为true
        System.out.println("a || b: "+(a||b)); //逻辑或运算：两个变量有一个为真，结果才为true
        System.out.println("!(a && b): "+( a&&b)); //如果时真，则变为假，如果是假则变为真

        //短路运算
        int c =5;
        boolean d = (c<4)&&(c++<4);
        System.out.println(d);
        System.out.println(c);
    }
}

```

####位运算：

```java
/*
    A = 0011 1100
    B = 0000 1101

    A&B 0000 1101 按位与
    A|B 0011 1101 按位或
    A^B 0011 0001 异或
    ~B  1111 0010 非

    面试题：2*8 怎么算最快？ 2<<3
    <<左移  *2 效率极高！！
    >>右移  /2
   */
System.out.println(2<<3); // 16

```



####三元运算符

```java
int a = 10;
int b = 20;

a+=b; // a = a+b
a-=b; // a = a-b

System.out.println(a); //10
//字符串连接符 + ，转化为String类型,然后拼接    注意！！
System.out.println(""+a+b); //1020
System.out.println(a+b+""); //30 先进行运算，再转为String拼接
System.out.println(a+b+"str"); //30str

```

```java
// x ? y : z
//如果x为真，则结果为y,否则为z
//if(x) y; else z;
int score = 80;
String type = score<60?"及格":"不及格";
System.out.println(type); //及格

```

#### Java包机制

为了更好地组织类，Java提供了包机制，用于区别类名的命名空间。

包语句的语法格式为：

```java
pckage pkg1[.pkg2[.pkg3..]]
```

**一般利用公司域名倒置作为包名**；

为了能够使用某一个包的成员，我们需要在Java程序中明确导入该包，使用"import"语句可以完成此功能

```java
import package1[.packge2...].(classname|*);
```

**包的本质就是一个文件夹**

#### JavaDoc

javadoc命令是用来生成自己API文档的

javaDoc:也可以解释为Java的文档注释

参数信息：

@author：作者名

@version：版本号

@since：指明需要最早使用的jdk版本

@param：参数名

@return：返回值情况

@throws：异常抛出情况

```java
/**
 * @author Kuangshen
 * @version 1.0
 * @since 1.8
 */
public class Demo05 {
    String name;

    /**
     * @author kuangshen
     * @param name
     * @return
     * @throws Exception
     */
    public String test(String name) throws Exception{
        return name;
    }
    
}

```

1. 打开某个类所在文件夹下的cmd命令行
2. 输入：javadoc -encoding UTF-8 -charset UTF-8 Doc(类名).java
3. 会自动生成该类有关的API文档，查看文件夹发现多了一些文件
4. 打开 index.html（首页）查看文档注释

cmd:命令javadoc -encoding UTF-8 -charset UTF-8 doc.java

![avatar](D:\Desktop\Program item directory\markdown_project file\markdown\java\image\java (7).png)

![avatar](D:\Desktop\Program item directory\markdown_project file\markdown\java\image\java (8).png)

####用户交互Scanner

通过Scanner类来获取用户的输入

基本语法：

```java
Scanner s = new Scanner(System.in);
```

java.util.Scanner是Java5的新特征

> 通过**Scanner**类的net()与nextLine()方法获取输入的字符串，在读取前我们一般需要使用 hasNext()与hasNextLine()判断是否还有输入的数据

####**用户输入**

####nex():

1. 一定要读取到有效字符后才可以结束输入。
2. 对输入有效字符之前遇到的空白，next()方法会自动将其去掉。
3. 只有输入有效字符后才将其后面输入的空白作为分隔符或者结束符。
4. <font face="黑体" size=5>next()不能得到带有空格的字符串</font>。

```java
package scanner;
import java.util.Scanner;
public class Dem03 {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        System.out.println("Receive packets in next mode");

        if(scanner.hasNext()){
            String str = scanner.next();
            System.out.print("The output is:"+str);
        }
scanner.close();
    }
}

```



```java
package scanner;
import java.util.Scanner;
//为了使用的对象Scanner，我们需要导入java.util.Scanner包
public class Demo1 {
    public static void main(String[] args) {
        //创建Scanner对象
        Scanner scanner = new Scanner(System.in);
        //System.in代表输入
//        创建一个扫描器对象，用于接收键盘数据
        System.out.println("使用next方式接收");
//判断用户有没有输入字符串
        //在读取前我们一般使用 hasNext 与 hasNextLine 判断是否还有输入的数据。
        if(scanner.hasNext()){
//使用next方式接收
            String str = scanner.next();  //程序会等待用户输入完毕
            System.out.print("输出的内容为："+str);
        }
//凡是属于IO流的类如果不关闭会一直占用资源，用完就要关闭掉
        scanner.close();
    }
}

```

---

IDEA输出的中文文字为乱码：此处应该修改文件编码

什么是IO流

- I : **Input**
- O : **Output**

通过IO可以完成硬盘文件的**读和写**。

- 往内存中**去**：叫做**输入(Input)**。或者叫做**读(Read)**。

- 从内存中**出来**：叫做**输出(Output)**。或者叫做**写(Write)**。

  **Java要掌握的流**（16个）

  1. 文件专属：
     java.io.FileInputStream（掌握）
     java.io.FileOutputStream（掌握）
     java.io.FileReader
     java.io.FileWriter

  2. 转换流：（将字节流转换成字符流）
     java.io.InputStreamReader
     java.io.OutputStreamWriter

  3. 缓冲流专属：
     java.io.BufferedReader
     java.io.BufferedWriter
     java.io.BufferedInputStream
     java.io.BufferedOutputStream

  4. 数据流专属：
     java.io.DataInputStream
     java.io.DataOutputStream

  5. 标准输出流：
     java.io.PrintWriter
     java.io.PrintStream（掌握）

  6. 对象专属流：
     java.io.ObjectInputStream（掌握）
     java.io.ObjectOutputStream（掌握）

  7. File文件类
     java.io.File

---



####nextLIne():

1. 以Enter为结束符，也就是说nextLIne()方法返回的是输入回车之前的所有字符。
2. 可以获得空白

```java
//从键盘接收数据
Scanner scanner = new Scanner(System.in);
System.out.println("请输入数据：");

String str = scanner.nextLine();
System.out.println("输入的内容为："+str);
scanner.close();

```

```java
System.out.println("请输入整数：");
if(scanner.hasNextInt()){
    int i=scanner.nextInt();
    System.out.println("输入的整数为："+i);
}else {
    System.out.println("输入的不是整数数据");
}

```



```java
package scanner;
import java.util.Scanner;
public class Demo2 {
    public static void main(String[] args) {
//        从键盘接收数据
        Scanner scanner = new Scanner(System.in);
        System.out.println("使用nextLine方式接收：");
//判断是否还有输入
        if(scanner.hasNextLine()){
            String str = scanner.nextLine();
            System.out.println("输出的内容为:"+str);
        }
scanner.close();
    }
}

```

可以使用nextLong()，nextFloat()，nextDouble()和next()方法来分别从用户获取long，float，double和string输入。

---

*关于windows电脑IDEA控制台无法准确输出中文问题：更新时间为2022年解决办法，软件版本为IDEA2020.3——将所有的UTF-8设置修改为GBK*

![avatar](D:\Desktop\Program item directory\markdown_project file\markdown\java\image\java (9).png)

**未知原因引起每次重启都会对于中文Unicode出现影响**

---

######获取浮点，双精度和字符串输入

```java
import java.util.Scanner;

class Input {
    public static void main(String[] args) {
    	
        Scanner input = new Scanner(System.in);
    	
        //获取float输入
        System.out.print("Enter float: ");
        float myFloat = input.nextFloat();
        System.out.println("Float entered = " + myFloat);
    	
        //获取double输入
        System.out.print("Enter double: ");
        double myDouble = input.nextDouble();
        System.out.println("Double entered = " + myDouble);
    	
        //获取字符串输入
        System.out.print("Enter text: ");
        String myString = input.next();
        System.out.println("Text entered = " + myString);
    }
}
```

整数和小数：

```java
package scanner;
import java.util.Scanner;
public class Dem04 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        //从键盘接收数据
        int i = 0;
        float f = 0.0f;
        System.out.println("请输入整数:");
        if(scanner.hasNextInt()) {
            i = scanner.nextInt();
            System.out.println("整数数据:" + i);
        }else{
            System.out.println("输入的不是整数数据!");
        }
        System.out.println("请输入小数:");
        //如果。。。。那么
        if(scanner.hasNextFloat()) {
             f = scanner.nextFloat();
            System.out.println("小数数据:" + f);
        }else{
            System.out.println("输入的不是小数数据!");
        }
    }
}

```

## Java流程控制

####顺序结构

<font face="微软你雅黑">Java的基本结构就是顺序结构，除非特别指明，否则就按照顺序一句一句执行。</font>

![avatar](D:\Desktop\Program item directory\markdown_project file\markdown\java\image\java (10).png)

顺序结构是最简单的算法结构。

> 语句与语句之间，框与框之间是从上到下的顺序进行的，它是由若干个依次执行的处理步骤组成的，<font color=red>**它是任何一个算法都离不开的一种基本算法结构。**</font>

#### if选择结构

- if单选择结构 if( )
- if双选择结构 if( ){ }else{ }
- if多选择结构 if( ){ }else if{ }else{}
- 嵌套的if结构 if( ){ if( ) }

if单选结构：if语句对条件表达式进行一次测试，若测试为真，则执行下面的语句，否则跳过该语句。

if双选择结构：：当条件表达式为真时，执行语句块1，否则，执行语句块2。也就是else部分。

```java
int a = 80;
if(a>60){
    System.out.println("及格");
    if(a>80) System.out.println("且优秀");
}else if(a>0){
    System.out.println("不及格");
}else {
    System.out.println("缺考");
}

```

#### switch多选择结构

```java
char grade = 'C'; //JDK新特性 可以是字符串(字符本质还是数字)
switch (grade){
    case 'A':
        System.out.println("优秀");
        break; //可选，跳出当前结构
    case 'B':
        System.out.println("良好");
        break;
    case 'C':
        System.out.println("合格");
        break;
    default: //默认，以上值没匹配到
        System.out.println("不及格");
        break;
}

```

####循环结构

######**while循环**

while是最基本的循环，它的结构为：

```java
while(布尔表达式){
    //循环内容
}
```

只要布尔表达式为ture，循环就会一直执行下去。

大多数情况是会让循环停止下来，需要一个让表达式失效的方式来结束循环。

少数部分情况需要循环一直执行，比如服务器的请求响应监听等。

循环条件一直为true就会造成无限循环【死循环】，我们正常的业务编程中应该尽量避免出现死循环。这会影响程序性能或者造成程序卡死崩溃

```java
//计算1+2+3+...+100
int i=0;
int sum=0;
while(i<100){
    i++;
    sum+=i;
}
System.out.println(sum); //5050

```

######do…while循环

对于 while 语句而言，如果不满足条件，则不能进入循环。但有时候我们需要即使不满足条件，也至少 执行一次。

> do…while 循环和 while 循环相似，不同的是，do…while 循环至少会执行一次。

> While和do-While的区别： while先判断后执行。dowhile是先执行后判断！ Do...while总是保证循环体会被至少执行一次！这是他们的主要差别。

```java
//先执行后判断，至少执行一次
do{
    i++;
    sum+=i;
}while(i<100) //跟上面效果一样

```

###### **for循环**

虽然所有循环结构都可以用 while 或者 do...while表示，但 Java 提供了另一种语句 —— for 循环，使一 些循环结构变得更加简单。

 for循环语句是支持迭代的一种通用结构，<font color="red">是最有效、最灵活的循环结构。 </font>

for循环执行的次数是在执行前就确定的。语法格式如下：

```java
for(初始化；布尔表达式；更新){
    //代码语句
}
```



```java
//计算0-100之间的奇数和偶数的和

```



```java
//（初始化;条件判断;迭代）
for(int i=0;i<100;i++){
    i++;
    sum+=i;
}
for(; ; ){...} //死循环

```

```java
//练习：输出1-1000能被5整除的数，每行输出3个
for (int i = 1; i <= 1000; i++) {
    if(i%5==0){
        System.out.print(i+"\t"); //输出完不换行
    }
    if(i%(3*5)==0){
        System.out.println();
    }
}

```

```java
//练习2：输出九九乘法表
for(int i=1;i<=9;i++){
    for(int j=1;j<=i;j++){
        System.out.print(j+"*"+i+"="+i*j+"\t");
    }
    System.out.println();
}

```

增强for循环

```java
int [] numbers = {10,20,30,40,50}; //定义一个数组
for (int x:numbers){
    System.out.println(x); //遍历数组的元素 10 20 30 40 50
}
//相当于
for(int i=0;i<5;i++){
    System.out.println(numbers[i]);
}

```

#### break & continue

- break可用在任何循环的主体部分，用于**强行退出循环**，也可以用在switch语句。

```java
public static void main(String[] args) {
        int i = 0;
        while(i<100){
            i++;
            System.out.println(i);
            if (i == 30) {
                break;
                //跳出循环
```



- continue用于循环语句中，**终止某次循环过程**，跳过剩余语句，之间进行下一次循环条件判断。

```java
public static void main(String[] args) {
        int i = 0;
        while (i < 100) {
            i++;
            if (i % 10 == 0) {
                System.out.println();
                continue;
                //continue 适用于任何循环控制结构中。作用是让程序立刻跳转到下一次循环的迭代。
                //在 for 循环中，continue 语句使程序立即跳转到更新语句。
                //在 while 或者 do…while 循环中，程序立即跳转到布尔表达式的判断语句。

            }
            System.out.println(i);

        }
    }
}
//continue用于循环语句中，终止某次循环过程，跳过剩余语句，之间进行下一次循环条件判断。
```



**break&continue的区别**

break在任何循环语句的主体部分，均可用break控制循环的流程。break用于强行退出循环，不执行循 环中剩余的语句。(break语句也在switch语句中使用) continue 语句用在循环语句体中，用于终止某次循环过程，即跳过循环体中尚未执行的语句，接着进行 下一次是否执行循环的判定。

/n*带标签的continue



- 标签：后面跟一个冒号的标识符 label:

  ```java
  //打印101-150之间所有的质数
  int count = 0;
  outer:for(int i=101;i<=150;i++){
      for (int j=2;j<i/2;j++){
          if(i%j==0)
              continue outer; //不建议使用标签
      }
      System.out.print(i+" ");
  }
  
  ```

  ####流程控制练习

```java
//打印等腰空心三角形
/*  例如：输入为4时
          *
         * *
        *   *
       * * * *
*/
Scanner scanner = new Scanner(System.in);
int n = scanner.nextInt(); //n为三角形高
for(int i=1;i<=n;i++){
    for(int j=1;j<=2*n-1;j++){
        if(i!=n){ //若不为最后一行
            if(i+j==n+1)
                System.out.print("*"); //三角形左腰边
            else if(i+j==n+2*i-1)
                System.out.print("*"); //三角形右腰边
            else System.out.print(" ");
        }
        else if(j%2!=0){  //最后一行，底边
            System.out.print("*");
        }else {
            System.out.print(" ");
        }
    }
    System.out.println(); //换行
}

```

## java方法

```java
System.out.println()
    //System是系统类
    //out是标准输出对象
    //println()是一个方法
```

Java方法是语句的集合，它们在一起执行一个功能。

- 方法是解决一类问题的步骤的有序组合

- 方法包含于类或对象中 

- 方法在程序中被创建，在其他地方被引用

设计方法的原则：方法的本意是功能块，就是实现某个功能的语句块的集合。我们设计方法的时候，最 好保持方法的原子性，<font color=red>就是一个方法只完成1个功能，这样利于我们后期的扩展。</font>



#### 方法的定义

Java的方法类似于其它语言的函数，是一段<font color = red>用来完成特定功能的代码片段</font>，一般情况下，定义一个方法包含以下语法：

<font color=red>方法包含一个方法头和一个方法体</font>。下面是一个方法的所有部分：

- 修饰符：修饰符，这是可选的，告诉编译器如何调用该方法，定义了该方法的访问类型。
- 返回值类型：方法可能会返回值。returnValueType是方法返回值的数据类型。有些方法执行所需的操作，但没有返回值。在这种情况下，returnValueType是关键字void.
- 方法名：是方法的实际名称。方法名和参数表共同构成方法签名。
- 参数类型：参数像是一个占位符。当方法被调用时，传递值给参数。这个值被称为实参或变量。参数列表是指方法的参数类型、顺序和参数的个数。参数是可选的，方法可以不包含任何参数。

形式参数：在方法被调用时用于接收外界输入的数据。

实参：调用方法时实际传给方法的数据。

方法体：方法体包含具体的语句，定义该方法的功能。

```java 
修饰符	返回值	方法名（参数类型 参数名）{
    。。。
        方法体
    。。。
        return 返回值；
}
```

#### 方法调用

调用方法：对象名.方法名（实参列表）

Java支持两种调用方法的方式，根据方法是否返回值来选择。

当方法返回一个值的时候，方法调用通常被当作一个值。例如：

```java
int larger = max(30,40);
```

如果方法返回值是void,方法调用一定是一条语句。

```java
System.out.println("Hello ,world");
```

#### 方法的重载

重载就是在一个类中，有相同的函数名称，但形参不同的函数

方法的重载的规则：

- <font color=red>方法名称必须相同</font>。
- <font color=red>参数列表必须不同（个数不同、或类型不同、参数排列顺序不同等）</font>。
- 方法的返回类型可以相同也可以不相同。
- 仅仅返回类型不同不足以成为方法重载。

实现理论：

方法名称相同时，编译器会根据调用方法的参数个数，参数类型等逐个去匹配，以选择对应的方法，如果匹配失败，则编译器报错。

#### 命令行传参

有时候希望运行一个程序的时候再传递给它消息。这要靠传递命令行参数给main()函数实现。

```java
public class CommandLine {
        public static void main(String args[]){
            for(int i=0; i<args.length; i++){
                System.out.println("args[" + i + "]: " + args[i]);
            }
        }
    }
}
```



```java
package method;
//命令行传参
public class Dem05 {
    public static void main(String[] args) {
        //args.Length 数组长度
        for (int i = 0; i < args.length; i++) {
            System.out.println("args["+ i +"]:"+args[i]);

        }
    }
}
//      cmd     javac Dem05.java -encoding gbk
```



![image-20220504214016395](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220504214016395.png)

#### 可变参数（不定项参数）

- jdk1.5开始，Java支持传递同类型的可变参数给一个方法。

- 在方法声明中，在指定参数类型后加一个省略号（...)。

- 一个方法中只能指定一个可变参数，它必须时方法的最后一个参数。任何普通参数必须在它之前声明。

## 递归

递归是一种常见的解决问题的方法，即把问题逐渐简单化。递归的基本思想就是<font color=red>“自己调用自己”</font>，一个 使用递归技术的方法将会直接或者间接的调用自己。

- A方法调用B方法，
- 递归就是A方法调用B方法，自己调用自己
- 利用递归可以用简单的程序来解决一些复杂的问题。它通常把一个大型复杂的问题层层转化为一个与原问题相似的规模较小的问题来求解，递归策略只需少量的程序就可以描述出解体过程所需要的多次重复计算，大大地减少了程序地代码量。递归地能力在于用有限的语句来定义对象的无限集合。
- 递归结构包括两部分：

1、<font color =red>递归头：什么时候不调用自身方法。如果没有头，将陷入死循环。</font>

2、<font color = red>递归体：什么时候需要调用自身方法。</font> 

## 数组

数组的定义：

- 数组是**相同类型数据**的有序集合
- 数组描述的是相同类型的若干个数据，按照一定的先后次序排列组合而成。
- 其中，每一个数据称作一个数组元素，每一个数组元素可以通过一个下标来访问它们。

#### 数组的四个基本特点：

1. 其长度是确定的。数组一旦被创建，它的大小就是不可以改变的。

2. 其元素必须是相同类型，不允许出现混合类型。

3. 数组中的元素可以是任何数据类型，包括基本类型和引用类型。

4. 数组变量属引用类型，数组也可以看成是对象，数组中的每一个元素相当于该对象的成员变量。

    数组本身就是对象，Java中对象是在堆中的，因此数组无论保存原始类型还是其他对象类型，**数组对象本身是在堆中的。**

#### 数组声明创建

1. 声明数组

首先必须声明数组变量，才能在程序中使用数组。

```java
dataType[] arrayRefvar; //首选的方法
或
    
dataType arrayRefvar[];//效果相同，但不是首选方法
//建议使用dataType[]arrayRefVar的声明风格声明数组变量。dataType arrayRefVar[]风格来自C/C++语言，在Java中采用是为了让C/C++程序员能够快速理解Java语言。
double[] myList;//首选的方法
或
 double myList[];//x
```

2、创建数组

 java语言中使用new操作符来创建数组，语法如下：

```java
dataType[] arrayRefVar = new dataType[arraySize];
```

- 使用dataType[arraySize]创建了一个数组。
- 把新创建的数组的引用赋值给变量arrayRefVar.

数组变量的声明，和创建数组可以用一条语句完成，如下所示：

```java
dataType[] arrayRefVar = new dataType[arraySize];
```



> 数组元素是通过索引访问的，数组索引从0开始。所以索引值从0到arrayRefVar.length-1.

获取数组长度:

```java
arrays.length
```

```java
public static void main(String[] args) {
//1.声明一个数组
int[] myList = null;
//2.创建一个数组
myList = new int[10];
//3.像数组中存值
myList[0] = 1;
myList[1] = 2;
myList[2] = 3;
myList[3] = 4;
myList[4] = 5;
myList[5] = 6;
myList[6] = 7;
myList[7] = 8;
myList[8] = 9;
myList[9] = 10;
// 计算所有元素的总和
double total = 0;
for (int i = 0; i < myList.length; i++) {
total += myList[i];
}
System.out.println("总和为： " + total);
}
```

```java
package array;

public class ArrayDemo01 {
    //变量的类型     变量的名字 = 变量的值；

    public static void main(String[] args) {
        int[]nums;//1.声明一个数组

        nums = new int[10];//2.创建一个数组
        //3.给数组元素中赋值
        nums[0] = 1;
        nums[1] = 2;
        nums[2] = 3;
        nums[3] = 4;
        nums[4] = 5;
        nums[5] = 6;
        nums[6] = 7;
        nums[7] = 8;
        nums[8] = 9;
        nums[9] = 10;
//4.计算所有元素的和
        int sum = 0;
        for (int i = 0;i < nums.length ; i++){
            //nums.length获取数组的长度
            sum = sum + nums[i];
        }
        System.out.println("总和为："+sum);
        
         
    }
}
```

#### 内存分析

![avatar](D:\Desktop\Program item directory\markdown_project file\markdown\java\image\java (11).png)

####数组的三种初始化：

- 静态初始化：除了用new关键字来产生数组以外，还可以直接在定义数组的同时就为数组元素分配空间并赋值。

```java
int[] a = {1,2,3};
Man[] mans = {new Man(1,1) new Man(2,2)};
```

- 动态初始化：数组定义，为数组元素分配空间、赋值的操作、分开进行。

```java
int[] a = new int[2];
a[0]=1;
a[1]=2;
```

```java
 public static void main(String[] args) {
        //静态初始化 :创建 + 赋值
        int[] a = {1,2,3,4,5,6,7,8};
        System.out.println(a[0]);

        //动态初始化:默认初始化
        int[] b = new int[10];
        b[0] = 10;
        b[1] = 20;
        System.out.println(b[0]);
        System.out.println(b[1]);
    }
}
```



数组的默认初始化：

数组是引用类型，它的元素相当于类的实列变量，因此数组一经分配空间，其中的每个元素也被按照实列变量同样的方式被隐式初始化。

```java
public static void main(String[] args) {
int[] a=new int[2];
boolean[] b = new boolean[2];
String[] s = new String[2];
System.out.println(a[0]+":"+a[1]); //0,0
System.out.println(b[0]+":"+b[1]); //false,false
System.out.println(s[0]+":"+s[1]); //null, null
}
```

#### 数组的边界

下标的合法区间：[0，length-1],如果越界就会报错；

> <font face ="黑体" color=red size=3>ArrayIndexOutOfBoundsException:数组下标越界异常！</font>

```java
public static void main(String[] args) {
int[] a=new int[2];
System.out.println(a[2]);
}
```

```html
Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: 2
at com.kuang.chapter3.Demo03.main(Demo03.java:6)
```

>数组是相同数据类型(数据类型可以为任意类型)的有序集合 数组也是对象。

> 数组元素相当于对象的成员变量(详情请见内存图) 

> <font size=4>数组长度是确定的，不可变的。如果越界，则报：ArrayIndexOutofBounds</font>

#### 数组使用

数组的元素类型和数组的大小都是确定的，所以当处理数组元素的时候，我们通常使用基本循环或者For-Each循环。

如何创建、初始化和操纵数组：

```java
 public static void main(String[] args) {
            double[] myList = {1.9, 2.9, 3.4, 3.5};
// 打印所有数组元素
            for (int i = 0; i < myList.length; i++) {
                System.out.println(myList[i] + " ");
            }
// 计算所有元素的总和
            double total = 0;
            for (int i = 0; i < myList.length; i++) {
                total += myList[i];
            }
            System.out.println("Total is " + total);
// 查找最大元素
            double max = myList[0];
            for (int i = 1; i < myList.length; i++) {
                if (myList[i] > max) {
                    max = myList[i];
                }
            }
            System.out.println("Max is " + max);
        }
    }
}
```

```java
package array;

public class ArrayDemo03 {
    public static void main(String[] args) {
        int[] arrays = {1,2,3,4,5};//定义了一个数组Defines an array
        //打印全部的数组元素
        for(int i = 0; i < arrays.length; i++){  //arrays.length获取数组的长度
            System.out.println(arrays[i]);
        }
        System.out.println("=====================");
        //计算所有元素的和
        int sum = 0;
        for(int i =0;i < arrays.length;i++){
            sum += arrays[i];
        }
        System.out.println("sum="+sum);
        System.out.println("======================");
        //查找最大元素
        int max = arrays[0];

        for(int i = 1; i < arrays.length ; i++){
            if(arrays[i]>max){
                max = arrays[i];
            }
        }
        System.out.println("max="+max);
    }
}

```

##### Fof-Each循环

JDK 1.5 引进了一种新的循环类型，被称为 For-Each 循环或者加强型循环，它能在不使用下标的情况下 遍历数组。

```java
for(type element: array){
            System.out.println(element);
        }



        public static void main(String[] args) {
            double[] myList = {1.9, 2.9, 3.4, 3.5};
// 打印所有数组元素
            for (double element: myList) {
                System.out.println(element);
            }
        }
```

#####数组作方法入参

数组可以作为参数传递给方法。

例如，打印一个int数组中元素的方法：

```java
public static void printArray(int[] array){
    for(int i = 0; i<array.length;i++){
        System.out.print(array[i]+"");
    }
}
```

##### 数组返回值

result数组作为函数的返回值

```java
public static int[] reverse(int[] list) {
int[] result = new int[list.length];
for (int i = 0, j = result.length - 1; i < list.length; i++, j--) {
result[j] = list[i];
}
return result;
}
```

#### 多维数组

多维数组可以看成是数组的数组，比如二维数组就是一个特殊的一维数组，其每一个元素都是一个一维数组。

多维数组的动态初始化（以二维数组为例）

```java 
int a[][] = new int[2][5];
```

将以上的数组a看作是一个两行五列的数组

二维数组可以直接解释为数组的嵌套：

```java
package array;

public class ArrayDemo5 {
    public static void main(String[] args) {

        int[][] array = {{1,2},{3,4},{5,6},{7,8}};

        for (int i = 0; i < array.length; i++) {
            for (int j = 0; j < array[i].length ; j++) {
                System.out.println(array[i][j]);

            }

        }

    }
    //打印数组元素
    public static void printArray(int[] arrays) {
        for (int i = 0; i < arrays.length; i++) {
            System.out.print(arrays[i] + "");

        }
    }
}

```

一个数组中包括了两个或者多个数组

![avatar](D:\Desktop\Program item directory\markdown_project file\markdown\java\image\java (12).png)

#### Arrays类

- 数组的工具类java.uti.Arrays

- 由于数组对象本身并没有什么可以供我们调用，但API中提供了一个工具类Arrays供我们使用，从而可以对数据对象进行一些基本的操作。

- **查看JDK帮助文档**

- Arrays类中的方法都是static修饰的静态方法，在使用的时候可以直接使用类名调用，而”不用“使用对象来调用（注意：是”不用“而不是”不能“）

- 具有一下常用功能：
  - 给数组赋值：通过fill方法。
  - 对数组排序：通过sort方法，按升序。
  - 比较数组：通过equals方法比较数组中元素是否相等。
  - 查找数组元素：通过binarySearch方法能对排序好的数组进行二分查找法操作。
  - ![avatar](D:\Desktop\Program item directory\markdown_project file\markdown\java\image\java (13).png)
  
  

#### 冒泡排序

冒泡排序（Bubble Sort），是一种计算机科学领域的较简单的排序算法。 **它重复地走访过要排序的元素列，依次比较两个相邻的元素，如果他们的顺序（如从大到小、首字母从 A到Z）错误 就把他们交换过来。走访元素的工作是重复地进行直到没有相邻元素需要交换，也就是说该元素列已经 排序完成。** 这个算法的名字由来是因为越大的元素会经由交换慢慢“浮”到数列的顶端（升序或降序排列），就如同 碳酸饮料中二氧化碳的气泡最终会上浮到顶端一样，故名“冒泡排序”。 冒泡排序算法的原理如下：**1. 比较相邻的元素。如果第一个比第二个大，就交换他们两个。 2. 对每一对相邻元素做同样的工作，从开始第一对到结尾的最后一对。在这一点，最后的元素应该会 是最大的 数。 3. 针对所有的元素重复以上的步骤，除了最后一个。 4. 持续每次对越来越少的元素重复上面的步骤，直到没有任何一对数字需要比较。**

```java
package array;

import java.util.Arrays;

public class ArrayDemo07 {
    public static void main(String[] args) {
        int[]a = {1,4,5,6,10,8,9,7,2,3,45,65,75,85,95,100};

        int[]sort =sort(a);//调用完我们自己写的排序方法以后，返回一个排序的数组

        System.out.println(Arrays.toString(sort));



    }
    //冒泡排序：
    //1、比较数组中，两个相邻的元素，如果第一个数比第二个数大，我们就交换他们的位置
    //2、每一次比较，都会产生出一个最大，或者最小的数字；
    //3、下一轮测试可以少一次排序
    //4、依次循环，直到结束！
    public static int[] sort(int[] array){
        int temp = 0;
        //外层循环，判断我们要走多少次；
        for (int i = 0; i < array.length-1; i++) {
            //内层循环，比价判断两个数，如果第一个数，比第二个数大，则交换位置
            for (int j = 0; j < array.length-1-i ; j++) {
                if(array[j+1]<array[j]){  //这个位置的大于小于符号可以确定数列的排序方向大到小还是小到大；
                    temp = array[j];
                    array[j] = array[j+1];
                    array[j+1] = temp;
                }
            }
        }
        return array;
    }
}

```



优化后：

```java
package array;

import java.util.Arrays;

public class ArrayDemo07 {
    public static void main(String[] args) {
        int[]a = {1,4,5,6,10,8,9,7,2,3,45,65,75,85,95,100};

        int[]sort =sort(a);//调用完我们自己写的排序方法以后，返回一个排序的数组

        System.out.println(Arrays.toString(sort));



    }
    //冒泡排序：
    //1、比较数组中，两个相邻的元素，如果第一个数比第二个数大，我们就交换他们的位置
    //2、每一次比较，都会产生出一个最大，或者最小的数字；
    //3、下一轮测试可以少一次排序
    //4、依次循环，直到结束！
    public static int[] sort(int[] array){
        int temp = 0;
        //外层循环，判断我们要走多少次；
        for (int i = 0; i < array.length-1; i++) {

            boolean flag = false; //通过没有flag标识位减少没有意义的比较

            //内层循环，比价判断两个数，如果第一个数，比第二个数大，则交换位置
            for (int j = 0; j < array.length-1-i ; j++) {
                if(array[j+1]<array[j]){  //这个位置的大于小于符号可以确定数列的排序方向大到小还是小到大；
                    temp = array[j];
                    array[j] = array[j+1];
                    array[j+1] = temp;
                    flag = true; //每循环一次，flag为true ，循环排好以后没有产生比较就会false;
                }
            }
            if(flag==false){ //如果没有进行比较就退出这个循环
                break;
            }
        }
        return array;
    }
}

```

#### 稀疏数组

- 当一个数组中大部分元素为0，或者为同一值时，可以使用稀疏数组来保存该数组。
- 稀疏数组的处理方式是：
  - 记录数组一共有几行几列，有多少个不同值
  - 把具有不同值的元素和行列及值记录在一个小规模的数组中，从而缩小程序的规模

```java
package array;

public class ArrayDemo08 {
    public static void main(String[] args) {
        //创建一个二维数组 11*11 0：表示没有棋子 1：表示黑棋 2：表示白棋
        int[] [] array1 = new int[11][11];
        array1[1][2] = 1;
        array1[2][3] = 2;
        //输出原始数组
        System.out.println("输出原始的数组");

        for (int[] ints : array1) {
            for (int anInt : ints) {
                System.out.print(anInt+"\t");
            }
            System.out.println();
        }
        System.out.println("=======================");
        //1.转换为稀疏数组来保存
        //2.获取有效值的个数
        int sum =0;
        for (int i = 0; i <11 ; i++) {
            for (int j = 0; j <11 ; j++) {
                if(array1[i][j]!=0){
                    sum++;

                }

            }

        }
        System.out.println("有效的个数:"+sum);

        //2.创建一个稀疏数组的数组
        int[][] aaray2 = new int[sum+1][3];

        aaray2[0][0] = 11;
        aaray2[0][1] = 11;
        aaray2[0][2] = sum;

        //遍历二维数组，将非零的数组，存放稀疏数组中
        int count = 0;
        for (int i = 0; i < array1.length ; i++) {
            for (int j = 0; j < array1[i].length ; j++) {
                if (array1[i][j]!=0){
                    count++;
                    aaray2[count][0] = i;
                    aaray2[count][1] = j;
                    aaray2[count][2] = array1[i][j];
                }
            }
        }
        //输出稀疏数组
        System.out.println("输出稀疏数组");

        for (int i = 0; i < aaray2.length; i++) {
            System.out.println(aaray2[i][0]+"\t"
                    +aaray2[i][1]+"\t"
                    +aaray2[i][2]+"\t");

        }
        System.out.println("=========================");
        System.out.println("还原");
        //1.读取稀疏数组的值
        int[][] array3 = new int[aaray2[0][0]] [aaray2[0][1]];
        //2.给其中的元素还原它的值
        for (int i = 1; i < aaray2.length ; i++) {
            array3[aaray2[i][0]][aaray2[i][1]] = aaray2[i][2];

        }
        //打印
        System.out.println("输出还原的数组");

        for (int[] ints : array3) {
            for (int anInt : ints) {
                System.out.print(anInt+"\t");
            }
            System.out.println();
        }

    }
}

```

## 面向对象编程

> 面向对象&面向过程

> 面向过程思想：
>
> - 步骤清晰简单，第一步做什么，第二步做什么
> - 面向过程适合处理一些较为简单的问题
>
> 面向对象思想：
>
> - 物以类聚，分类的思维模式，思考问题首先会解决问题需要哪些分类，然后对这些分类进行单独思考，最后，才对某个分类下的细节进行面向对象过程的思索
> - 面向对象适合处理复杂问题，适合处理需要多人协作的问题！
> - <font size = 4 color =red>对于描述复杂的事物，为了从宏观上把握、从整体上合理分析，我们需要使用面向对象的思路来分析整个系统。但是，具体到微观操作，仍然需要面向对象过程的思路去处理</font>

> 面向对象编程（Object-Oriented Programming ,OOP)
>
> - 面向对象编程的本质就是：<font size =4 color =red>以类的方式组织代码，以对象的组织（封装）数据</font>。
>
> 抽象
>
> - 三大特性：
>
>   - <font size=5 color =red>封装</font>
>
>   - <font size=5 color =red>继承</font>
>
>   - <font size=5 color =red>多态</font>
>
> - 从认识角度考虑是先有对象后有类。对象，是具体的事物。类，是抽象的，是对对象的抽象
> - 从代码运行角度考虑是先有类后有对象。类是对象的模板。
