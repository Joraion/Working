# # jorion

java 有6种基本数据类型,

包括整数类byte.int. short.long

浮点类float.double

字符类char

布尔类boolean

其中整数类能由小转大 即 byte→short→int→long,若需要由long往byte转,则会损失精度.

Java中的常量与变量:常量为基本不变的数,如1.2.3.4,变量即 为随机赋值的常量,即a = 1.2.3

字符串:即将一堆字符拼接到一起,用" " +  来表示,String为一个类 ,也可以将字符串总拼接.

自增/自减
前置自增:++a, 运算前先将变量+1之后再做相应运算
后置自增:a++, 做完相应运算后再将变量+1的运算,之后使用+1后的数值.
自减同理

赋值:为变量制定一个值之后做运算,Java里面可以对多个值同时赋值.

流程控制语句:
1.顺序结构
如
System.out.println("你好吗");
System.out.println("你在哪");
System.out.println("吃过饭了吗");
此次编译过后程序将在命令窗口依次打出"你好吗""你在哪""吃过饭了吗"

2分支结构
(1)if分支:


1)if(条件){
	若条件为TRUE(boolean 类型非TRUE即FALSE),则执行代码
}




2)if (条件){
	若条件为TRUE,执行此处代码
}else{
	若条件为FALSE,则执行此处代码
}




3)if(条件){
	若条件为true,执行此处代码
}else if(条件){
	若条件为TRUE,执行此处代码
}else if(条件){
	若条件为TRUE,执行此处代码
}else{
	若上述条件均为FALSE,则执行此处代码.
}
注:if只能有一个,而else if可以有多个甚至N个,else只能有一个或者零个





switch分支:
switch分支的类型可以是byte.short.int,char.string

switch(表达式)
case 值:
  若case值与表达式内类型值相等,则执行此处代码
break;
.....
default;
     若上述case值均不为表达式内类型值,则执行此处代码
break;

注:case 类可以有多个甚至N个,break为分支结束标志,若break去掉,则会出现将所有case后的执行代码
执行一遍.



循环结构:
(1)for循环
for(赋值语句;循环条件;迭代语句){
   此处为循环体
}

for(int a = 3;a<=5;a++)
{
   System.out.println("a=" + a);
}
当a的值大于5时循环结束

嵌套循环
for循环体内增加一个for循环

for(int a = 1;a<=4;a++){
	for(int b =2 ;b<=3,b++)	{
	System.out.println("a" + "b" "=" + a + b);
	}
	}


while循环:


int a =1

while(循环条件)
{
   循环体
   迭代语句
   }
循环体的循环条件 == 循环体执行次数 +1 



do while循环:

int a=1
do {
    循环体
   a++ 
   }
while(循环条件)
循环条件的次数 = 循环体执行的次数

两者区别:while循环先对循环条件进行判断,若条件为TRUE则进入循环体,直到循环条件为FALSE
         do while循环则无论条件正确与否都先执行一次循环体

例如:
int a = 4
while(a>=5)
{
   System.out.println("a" + "=" + a);
   a++}


int a = 4
do{
    System.out.println("a" + "=" + a);
    a++
    }
   while(a>=5)



最后while循环不执行循环体
而do while循环执行一次 输出a=5.





Java的三个关键词 break  , continue ,  return.

1,break 
主要为switch分支结构中结束某个当前分支的作用
	switch (条件)
	{
	case 值:
   //执行代码
	break;
	}
	default;


若为for循环
则:若为for内部循环则不影响外部循环.
   若要结束外部循环,则需要在外部for循环加上break标签.但不影响内部循环.


2,continue:
在嵌套循环中忽略本次满足的if条件的循环转而进行下一轮循环.
若要忽略外循环某一条件,则需在外循环中添加标签continue
continue不能用在switch分支中;


3,return:
用于直接结束程序,当条件满足时return将不再执行接下来的程序进而结束整个程序
将结果返还给上一级

数组:当有多个类型(byte short int long float double char)相同切功能相同的变量时
用数组将这些变量打包成一块即成数组

静态数组:
语法:
	
	(1)数组类型[] 数组名称 = new 数组类型[]{元素1,元素2,元素3,元素4);

	(2)数组类型[] 数组名称 = {元素1,元素2,元素3,元素4};
      
      	(3)数组类型 数组名称[] = {元素1,元素2,元素3,元素4};
 
 	获取数组的长度:
             
	     	System.out.println("数组名称.length+" + 数组名称.length);
 
 	获取数组中某一元素:
	         
		 	int 变量 = 数组名称[元素索引];注:第一个元素索引为0;
			
				System.out.println("数组名称[元素索引]=" + 变量); 
 
 	遍历数组中的所有元素:
		
 
	(1)for循环:
	 for (int A = 0;A<数组名称.length ;A++ )
	 {
			 System.out.println("数组名称["+A+"]="+数组名称[元素索引]);
	 }
		
		
		
         (2)while循环:
		int A = 0
		while (A<数组名称.length)
		{
			 System.out.println("数组名称["+A+"]="+数组名称[元素索引]);
			 A++;
		 }

	(3)for each
		for( int 变量F : 数组名称)
	{
			 System.out.println("变量F = " + 变量F);

	}

给数组中元素赋值:
	   数组名称[元素索引] = [数值];
		int 变量O = 数组名字[元素索引];
