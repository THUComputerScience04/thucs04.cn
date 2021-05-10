---
title: OOP某节课的笔记
date: 2021/05/08 
author: Teburile
categories: Note
tags: [OOP,笔记]
---

## 模板与STL初步

类模板：使用参数类型 <typename T> 用类型T来定义模板类

```c++
template <typename T> class A{
	T a;
}
```

## 命名空间

防止名称冲突，引入namespace 关键字

```c++
namespace A{
	int x;
	int y;
}
```

在使用时

```c++
using namespace A;
```

或者是

```c++
using namespace A::x;
```

## STL库

STL：Standard Template Library

包含四个组件：算法，容器，函数，迭代器

STL的命名空间是std

一般使用using namespace std::名称

大型工程当中不推荐引入整个命名空间

### STL容器

容器是包含、放置数据的工具，通常为数据结构，包括：

* 简单容器
* 序列容器
* 关系容器

#### pair 容器

```c++
template <class T1,class T2> struct pair{
	T1 first;
	T2 second;
};

std::pair<int,int> t;

//或者
auto t = std::make_pair("abc",7);
```

pair 支持小于、等于、大于比较运算符

先比较第一个元素，再比较第二个元素，要求元素类型支持比较运算符

#### tuple 容器

tuple 是多个元素的pair，要求在使用时就确定内部由多少个元素

```c++
template<class T1,class T2,class T3> class tuple{
	T1 a;
	T2 b;
	T3 c;
};

a=std::get<0>(tuple1);
b=std::get<1>(tuple2);

//
auto t=std::make_tuple(1,2,3);

int x,y,z;
std::tie(x,y,z)=std::make_tuple(1,2,3);

//使用tuple可以使函数返回多个返回值
std::tuple<int,double> f(int x){
	return std::make_tuple(x,double(x)/2);
}
```

#### vector容器

可以自动扩展容量的数组，允许以下标来访问（高速）

```c++
//创建
std::vector<int> x;
//当前数组长度
int y=x.size();
//清空
x.clear();
//在末尾添加、删除
x.push_back(0);
x.pop_back();
//在中间添加、删除
x.insert(x.begin()+1,5);
x.erase(x.begin()+1);
x.erase(iterator first,iterator last);//删除一段
//删除一些元素后，后面的元素依次向前挪动，而迭代器指向的vector的位置不变
```

迭代器：一种检查容器内元素并遍历元素的数据类型，使用上类似于指针

以vector 为例，要求类T有迭代器

```c++
//定义
template<class T,class Allocator = std::allocator<t>>
class vector{
	class iterator{
		...
	};
};

vector<int>::iterator iter;//定义一个迭代器

iter=x.begin(); //返回第一个元素的迭代器；
iter=x.end();//返回最后一个元素+1位置的迭代器

//iterator使用
//移动
iter +=3;
//求元素位置差
int dist=iter1-iter2;

//应用
vector<int> vec;
for(vector<int>::iterator it = vec.begin();it != vec.end(); it++){
	...;
}
//可以用 auto 来定义it的类型
//也可以写成
for (auto x:: vec){
    ...;
}
```

在扩大vector的大小后，可能会使得所有迭代器失效:Push_back 使得vector扩张后，整个vector可能移动位置，扩大所申请的容量。vector 搬迁后，iterator 不变，原来的指向会有问题。 

#### list容器

底层是双向链表，要求类T有迭代器

```c++
//创建
template<class T,class Allocator = std::allocator<T>> class list;
std::list<int> l;

//插入操作
l.push_front(1);
l.push_back(2);
//查询 返回迭代器
std::find(l.begin(),l.end(),1);
//插入指定位置：
l.insert(it,4);
```

list不支持下标的随机访问，支持高速在任意位置插入、删除数据，访问主要依赖于迭代器，操作不会导致迭代器失效（除指向被删除元素的迭代器外）

#### set容器

不重复元素构成的无序集合

无序：不保持插入顺序，容器内部排列顺序根据元素大小排列（复杂度为 log n）

要求类Key 支持比较，有迭代器

```c++
//定义
template<class Key, class Compare = std::less<Key>,class Allocator = std::allocator<Key>> class set;
//插入
s.insert(1);
//查询 返回迭代器
s.find(2);
//删除
s.erase(s.find(2));
//统计
s.count(2);//2的个数，总是0或者1
```

#### map 容器

map常用作过大的稀疏数组或以字符串为下标的数组

复杂到为 log n

要求类Key有比较、迭代器

```c++
//定义
template<class Key,class Compare = std::less<Key>,class Allocator = std::allocator<std::pair<const Key T>>> class map;
```

map中的key互不相同，可以通过下标key来访问

查询：find(key) 统计：count(key)

删除：使用迭代器 erase；