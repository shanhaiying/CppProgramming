Table of Contents
=================

* [第 2章　程序的基本组成　11](#%E7%AC%AC-2%E7%AB%A0%E7%A8%8B%E5%BA%8F%E7%9A%84%E5%9F%BA%E6%9C%AC%E7%BB%84%E6%88%9011)
  * [2\.1　程序的基本结构　11](#21%E7%A8%8B%E5%BA%8F%E7%9A%84%E5%9F%BA%E6%9C%AC%E7%BB%93%E6%9E%8411)
    * [2\.1\.1　注释　12](#211%E6%B3%A8%E9%87%8A12)
    * [2\.1\.2　预编译　12](#212%E9%A2%84%E7%BC%96%E8%AF%9112)
    * [2\.1\.3　名字空间　13](#213%E5%90%8D%E5%AD%97%E7%A9%BA%E9%97%B413)
    * [2\.1\.4　主程序　13](#214%E4%B8%BB%E7%A8%8B%E5%BA%8F13)
  * [2\.2　常量与变量　14](#22%E5%B8%B8%E9%87%8F%E4%B8%8E%E5%8F%98%E9%87%8F14)
    * [2\.2\.1　变量定义　14](#221%E5%8F%98%E9%87%8F%E5%AE%9A%E4%B9%8914)
    * [2\.2\.2　数据类型　16](#222%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B16)
    * [2\.2\.3　常量与符号常量　21](#223%E5%B8%B8%E9%87%8F%E4%B8%8E%E7%AC%A6%E5%8F%B7%E5%B8%B8%E9%87%8F21)
    * [\*2\.2\.4　C\+\+11的扩展　24](#224c11%E7%9A%84%E6%89%A9%E5%B1%9524)
  * [2\.3　数据的输入/输出　25](#23%E6%95%B0%E6%8D%AE%E7%9A%84%E8%BE%93%E5%85%A5%E8%BE%93%E5%87%BA25)
    * [2\.3\.1　数据的输入　25](#231%E6%95%B0%E6%8D%AE%E7%9A%84%E8%BE%93%E5%85%A525)
    * [2\.3\.2　数据的输出　26](#232%E6%95%B0%E6%8D%AE%E7%9A%84%E8%BE%93%E5%87%BA26)
  * [2\.4　算术运算　27](#24%E7%AE%97%E6%9C%AF%E8%BF%90%E7%AE%9727)
    * [2\.4\.1　算术表达式　27](#241%E7%AE%97%E6%9C%AF%E8%A1%A8%E8%BE%BE%E5%BC%8F27)
    * [2\.4\.2　各种类型的数值间的混合运算　27](#242%E5%90%84%E7%A7%8D%E7%B1%BB%E5%9E%8B%E7%9A%84%E6%95%B0%E5%80%BC%E9%97%B4%E7%9A%84%E6%B7%B7%E5%90%88%E8%BF%90%E7%AE%9727)
    * [2\.4\.3　强制类型转换　27](#243%E5%BC%BA%E5%88%B6%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A227)
    * [2\.4\.4　数学函数库　28](#244%E6%95%B0%E5%AD%A6%E5%87%BD%E6%95%B0%E5%BA%9328)
    * [\*2\.4\.5　C\+\+11的扩展　29](#245c11%E7%9A%84%E6%89%A9%E5%B1%9529)
  * [2\.5　赋值运算　29](#25%E8%B5%8B%E5%80%BC%E8%BF%90%E7%AE%9729)
    * [2\.5\.1　赋值表达式　29](#251%E8%B5%8B%E5%80%BC%E8%A1%A8%E8%BE%BE%E5%BC%8F29)
    * [2\.5\.2　赋值的嵌套　30](#252%E8%B5%8B%E5%80%BC%E7%9A%84%E5%B5%8C%E5%A5%9730)
    * [2\.5\.3　复合赋值运算　31](#253%E5%A4%8D%E5%90%88%E8%B5%8B%E5%80%BC%E8%BF%90%E7%AE%9731)
    * [2\.5\.4　自增和自减运算符　32](#254%E8%87%AA%E5%A2%9E%E5%92%8C%E8%87%AA%E5%87%8F%E8%BF%90%E7%AE%97%E7%AC%A632)
  * [2\.6　程序规范及常见错误　33](#26%E7%A8%8B%E5%BA%8F%E8%A7%84%E8%8C%83%E5%8F%8A%E5%B8%B8%E8%A7%81%E9%94%99%E8%AF%AF33)
  * [2\.7　小结　34](#27%E5%B0%8F%E7%BB%9334)
  * [2\.8　习题　34](#28%E4%B9%A0%E9%A2%9834)

---

# 第 2章　程序的基本组成　11
## 2.1　程序的基本结构　11

**代码清单2-1 求解一元二次方程**

```cpp
// 文件名： 2-1.cpp
//  用标准公式求解一元二次方程

#include <iostream>
#include <cmath>
using namespace std;

int main()
{
 	 double a, b, c, x1, x2, dlt;

	 cout << "请输入方程的3个系数：" << endl;
    cin >> a >> b >> c;

    dlt = b * b - 4 * a * c;
    x1 = (-b + sqrt(dlt)) / 2 / a;
    x2 = (-b - sqrt(dlt)) / 2 / a;

    cout << "x1=" << x1 << "   x2=" << x2 << endl;

    return 0;
}
```
### 2.1.1　注释　12
### 2.1.2　预编译　12
### 2.1.3　名字空间　13
### 2.1.4　主程序　13
## 2.2　常量与变量　14
### 2.2.1　变量定义　14
### 2.2.2　数据类型　16
### 2.2.3　常量与符号常量　21
### *2.2.4　C++11的扩展　24
## 2.3　数据的输入/输出　25
### 2.3.1　数据的输入　25
### 2.3.2　数据的输出　26
## 2.4　算术运算　27
### 2.4.1　算术表达式　27
### 2.4.2　各种类型的数值间的混合运算　27
### 2.4.3　强制类型转换　27
### 2.4.4　数学函数库　28
### *2.4.5　C++11的扩展　29
## 2.5　赋值运算　29
### 2.5.1　赋值表达式　29
### 2.5.2　赋值的嵌套　30
### 2.5.3　复合赋值运算　31
### 2.5.4　自增和自减运算符　32
## 2.6　程序规范及常见错误　33
## 2.7　小结　34
## 2.8　习题　34
