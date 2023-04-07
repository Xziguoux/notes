#cpp

# 1 前置

## 1.1 初始化
初始化系统总结
[Initialization - cppreference.com](https://en.cppreference.com/w/cpp/language/initialization)
### 1.1.1 value initialization
```cpp
std::string s{}
```

### 1.1.2 direct initialization
```cpp
std::string s("hello")
```

### 1.1.3 copy initialization
```cpp
std::string s = "hello"
```
### 1.1.4 list initialization
```cpp
std::string s{"a", "b", "c"}
```
### 1.1.5 aggregate initial
```cpp
char a[3] = {"a", "b"}
```
### 1.1.6 reference initial
```cpp
char &c  = a[0]
```

### 默认初始化
以上均初始化均

### 1.2 不同变量类型初始化
#### non-local 
	所有具有静态存储类型的non local变量初始化均在程序启动，main函数运行前进行，对于线程的non-local初始化实在thread launch，函数执行之前近进行的，初始化集中在以下两个阶段
##### static initialization
两个形式
- 如果可能，常量初始化
- 否则， non-local staitc 和thread-local 会采用零值初始化






**in-class initializer**
- [c++11 - What exactly is the in-class-initializer? - Stack Overflow](https://stackoverflow.com/questions/53100271/what-exactly-is-the-in-class-initializer)
- [CppCoreGuidelines/CppCoreGuidelines.md at master · isocpp/CppCoreGuidelines · GitHub](https://github.com/isocpp/CppCoreGuidelines/blob/master/CppCoreGuidelines.md#c48-prefer-in-class-initializers-to-member-initializers-in-constructors-for-constant-initializers)

default-initialize 
[Default initialization - cppreference.com](https://en.cppreference.com/w/cpp/language/default_initialization)
constructor initializer list
[Constructors and member initializer lists - cppreference.com](https://en.cppreference.com/w/cpp/language/constructor)

# 2 类的构造函数

## 2.1 默认构造函数与合成默认构造函数
问题：
- 什么是默认构造函数
- 默认构造函数什么情况下启用
- 什么是合成构造函数，什么情况编译器会进行合成
## 2.2 用户定义构造函数
## 2.3 代理构造函数
## 2.4 转换构造函数
## 2.5 继承构造函数
## 2.6 拷贝构造函数
## 2.7 赋值运算符
## 2.8 移动构造函数和移动复制运算符
## 2.9 析构函数


# 3 参考
https://zhuanlan.zhihu.com/p/271732707?utm_source=ZHShareTargetIDMore&utm_medium=social&utm_oi=556839182773825536