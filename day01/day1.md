# day1

## 0. 在vscode中配置环境
https://code.visualstudio.com/docs/languages/java
在安装过程中遇到Javac和Java版本不一致的冲突问题，通过修改环境变量中的顺序来解决了该问题。

## 1. 新的名词
JDK
JVM
跨平台
J2SE/J2ME/J2EE  Java SE和Java EE
JRE
编译工具(javac.exe) 打包工具(jar.exe)
Java源文件/Java字节码文件
与C++区别的关键字：interface byte boolean abstract final synchronized extends implements super instanceof package import native strictfp transient volatile 
## 2. 计算机基础(了解)
	(1)计算机
	(2)计算机硬件
	(3)计算机软件
	(4)软件开发
	(5)计算机语言
	(6)人机交互方式(掌握)
		A:图形化界面方式
		B:命令行方式
	(7)键盘的功能键认识
	(8)常用的快捷键(掌握 自己补齐快捷键)
		A:全选
		B:复制
		C:粘贴
		D:剪切
		E:撤销
		F:保存

## 3. DOS命令(理解)
	(1)切换盘符(掌握)
		d: 回车
	(2)显示某目录下的所有文件或者文件夹(掌握)
		dir 回车
	(3)创建文件夹
		md 文件夹名称 回车
	(4)删除文件夹
		rd 文件夹名称 回车
	(5)进入目录(掌握)
		单级进入 cd 目录名称 
		多级进入 cd 目录名称1\目录名称2\...
	(6)回退目录(掌握)
		单级回退 cd..
		回退根目录 cd\
	(7)删除文件
		del 文件名称
		*.txt 可以表示多个文件名称
	(8)清屏(掌握)
		cls
	(9)退出
		exit
	(10)扩展DOS命令
		删除带内容的文件夹
		rd /s 文件夹名称 会提示是否删除
		rd /q /s 文件夹名称 直接删除

## 4. Java语言发展史(了解)
	(1)Java之父
	(2)JDK的版本
		1.4.2
		1.5
		1.6
		1.7
		1.8
	(3)Java语言的平台
		JavaSE
		JavaEE
		JavaME(Android)
	(4)Java语言的特点

## 5. JDK,JRE,JVM(掌握)
	(1)JVM
		保证Java语言跨平台。针对不同的操心系统提供不同的JVM。

		问题：java语言是跨平台的吗?JVM是跨平台的吗?
	(2)JRE
		java程序的运行环境。包括JVM和核心类库
	(3)JDK
		java开发环境。包括JRE和开发工具(javac,java)

## 6. JDK的下载，安装，卸载(掌握)
	(1)下载
		到官网下载，或者百度也可以。
	(2)安装
		安装版 安步骤一步步安装即可。开发工具一般建议不要有空格和中文。
		绿色版 解压就可以使用
	(3)卸载
		安装版 通过360或者控制面板
		绿色版 直接删除文件夹即可

## 7.HelloWorld案例(掌握)
	(1)写程序
		class HelloWorld {
			public static void main(String[] args) {
				System.out.println("HelloWorld");
			}
		}
	(2)解释该程序
		A:class是用来定义类的，格式是: class 类名 {}
		B:程序要独立运行，必须有主方法，格式是：
			public static void main(String[] args) { }
		C:程序要输出内容，必须有输出语句，格式是：
			System.out.println("HelloWorld");
	(3)程序的编译和运行
		A:javac命令编译程序，后面跟的是文件名称
			javac HelloWorld.java
		B:java命令执行程序，后面跟的是class文件名称，不含扩展名
			java HelloWorld
	(4)一个Java程序的开发流程
		A:编写Java源程序
		B:通过javac命令编译java程序，生成字节码文件
		C:通过java命令运行字节码文件

## 8. HelloWorld案例常见问题(理解)
	(1)文件名和类名可以不一致，但是建议一致
	(2)找不到文件
	(3)单词写错误(包括大小写，拼写)
	(4)括号匹配问题，建议大家写程序的时候，成对写括号
	(5)中英文问题，java程序一般都是英文状态的
	(6)末尾缺少分号		
	
## 9. path环境变量(理解)
	(1)为什么要配置path环境变量
		为了让javac和java命令可以在任意目录下使用
	(2)如何配置
		A:方式1 直接修改path，在前面追加JDK的bin目录
		B:方式2(掌握) 
			新建JAVA_HOME: JDK的安装目录
			修改path: %JAVA_HOME%\bin;后面是以前的环境变量

## 10. classpath环境变量(理解)
	(1)为什么要配置classpath环境变量
		为了让class文件可以在任意目录下运行
	(2)如何配置
		新建：classpath，把你想要在任意目录下运行的class文件所在目录配置过去即可。
		注意：将来在执行的时候，有先后顺序关系
	(3)path和classpath的区别
		path是为了让exe文件可以在任意目录下运行
		classpath是为了让class文件可以在任意目录下运行

## 11 . 注释(掌握)
	(1)注释:用于解释说明程序的文字
	(2)分类：
		A:单行：//注释文字
		B:多行：/* 注释文字 */
		C:文档注释：/** 注释文字 */
	(3)带注释的HelloWorld案例
	(4)注释的作用：
		A:解释说明程序，提高程序的阅读性
		B:帮助我们调试程序

## 12. 关键字(掌握)
	(1)关键字:被Java赋予特定含义的单词
	(2)特点:全部小写
	(3)注意事项：
		A:goto和const作为保留字存在，目前不使用
		B:类似于Editplus这样的高级记事本，会对关键字有特殊颜色标记，方便记忆

## 13. 标识符(掌握)
	(1)标识符：给类，接口，方法或者变量起名字的符号
	(2)组成规则：
		A:英文字母大小写
		B:数字
		C:_和$
	(3)注意事项：
		A:不能以数字开头
		B:不能是Java中的关键字
		C:区分大小写
			Student,student 这是两个名称
	(4)常见命名方式：
		A:包 其实就是文件夹,用于解决相同类名问题
			全部小写
			单级：com
			多级：cn.itcast

		B:类或者接口
			一个单词：首字母大写
				Student,Person,Teacher
			多个单词：每个单词的首字母大写
				HelloWorld,MyName,NameDemo

		C:方法或者变量
			一个单词：全部小写
				name,age,show()
			多个单词：从第二个单词开始，每个单词首字母大写
				myName,showAllStudentNames()

		D:常量
			一个单词：全部大写
				AGE
			多个单词：每个单词都大写，用_连接
				STUDENT_MAX_AGE