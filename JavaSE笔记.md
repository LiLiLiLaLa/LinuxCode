# JavaSE笔记
@(Java)[JavaSE]
## Day01
### 解决javac的编码问题  
使用如下命令编译： **javac -encoding UTF-8 *.java **
### Java标识符
* 字母、数字、下划线组成 
* 不能使用关键字
* 不能以数字开头
* 采用有意义的简单命名

小驼峰命名法：myFucntion()、myFirst、myFirstInt

大驼峰命名法：MyClass()、MyFirst、AnimalCat

Java的源文件命名必须和public类的名称相同

常量命名：命名全大写 INT_MAX、DOUBLE_MAX
### Java的数据类型
#### 数值型
* 整型： byte[-218,127] -1字节、short、int[-2^31,2^31-1]-4字节、long-8字节（默认为0）
* 浮点型：double、float（默认值0.0)
* 字符型：char（默认值\u0000）
* 布尔型：boolean（默认值false)
#### 引用数据类型
数组、类、接口

### 数据类型的使用：
* 描述整数用int
* 描述小数用double
* long类型一般用于描述时间、日期、内存或者文件大小
* 编码装换或者二进制流的操作使用byte
* char一般用于描述中文

### 整型
1、在Java中任何一个整型常量都是int类型，所以在Java中声明一个long类型的常量，需要在后面加一个`L`或者`l`(推荐使用大写)
2、大类型与小类型做数值运算的时候，小类型自动提升成大类型，无需强制类型转换
3、大类型转为小类型必须强制类型转换，但是可能会丢失内容
>例外：byte与int类型的转换
```java
int num = 10;
byte a = num; //error 需要强转
byte a = 120; //OK
byte a = 130; //error 需要强转
```
**整型常量复制给byte变量时，若常量值在byte类型的保存范围中可以直接复制，无需强制类型转换**
**整型变量无论是都在byte类型的范围类，一律需要强转**

### 小数
1、小数默认为double类型，要声明为float类型，需要在后面加`f`
BigDecimal类用来计算精度超高的浮点数
2、所有的数据类型的默认值必须结合类来观察，主方法中数据类型不存在默认值:
```java
public class Test{
    public static void main(String[] args) {
        int i;
        Ststem.out.println(i);
    }
}
```




