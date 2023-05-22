###### c++如何实现多态？

就是用指向父类的指针指向子类，调用子类的成员函数。

例如：

```c++
#include<bits/stdc++.h>
class A{
    Public:
    virtaul void fun(){cout<<"A:printf"};
};
class B{
    public:
    virtual void fun(){cout<<"B:printf"}
};
void main(){
    A a;
    B b;
    A*a=&a;
    B*b=&b;
    a=b;//父类指针指向子类，对子类成员函数进行调用
    a->fun();//输出结果为 B:printf
}
```

##### c++指针和引用的区别

sizeof 

##### struct与class的区别，class的底层是什么来实现的？

class底层用struct实现

##### 联合体的特点，sizeof联合体和struct有什么区别



##### 虚函数和纯虚函数的区别，纯虚函数是否可以实例化



##### 虚函数怎么样才能调用到子类的方法



##### 重载、重写、重定义的区别？



##### 左值右值

左值的英文简写为“lvalue”，右值的英文简写为“rvalue”。很多人认为它们分别是"left value"、"right value" 的缩写，其实不然。lvalue 是“loactor value”的缩写，可意为存储在内存中、有明确存储地址（可寻址）的数据，而 rvalue 译为 "read value"，指的是那些可以提供数据值的数据（不一定可以寻址，例如存储于寄存器中的数据）。

##### 左值引用，右值引用

```
//左值引用适用于左值，常量左值引用只能引用常量左值
int num=10;
int &a=num//true
int &c=10//false
const int &c=num//false
const int num=10;
const int &c=num//true
//c++11中增加了右值引用 可以引用右值，还能修改
int && b=10;
b=11;
cout<<b<<endl;//此时b就能被修改了
//左值引用情况
	int num = 10;
	int& a = num;	//编译成功，非常量左值引用支持引用非常量左值
	const int num2 = 100;
	int& b = num2;	//编译失败，非常量左值引用不支持引用常量左值
	int& c = 10;	//编译失败，非常量左值引用不支持引用右值
 
	const int& d = num;		//编译成功，常量左值引用支持引用非常量左值
	const int& e = num2;	//编译成功，常量左值引用支持引用常量左值
	const int& f = 100;		//编译成功，常量左值引用支持引用右值
//右值引用情况
	int num = 10;
	const int num2 = 100;
	int&& a = num;	//编译失败，非常量右值引用不支持引用非常量左值
	int&& b = num2;	//编译失败，非常量右值引用不支持引用常量左值
	int&& c =10;	//编译成功，非常量右值引用支持引用非常量右值
	const int&& d = num;	//编译失败，常量右值引用不支持引用非常量左值
	const int&& e = num2;	//编译失败，常量右值引用不支持引用常量左值
	const int&& f = 100;	//编译成功，常量右值引用支持引用右值

```

lamda表达式





