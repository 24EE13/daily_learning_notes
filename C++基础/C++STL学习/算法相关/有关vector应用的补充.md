# vector、sort与迭代器相关


*sort在#include<algorithm>头文件中*


1. 
众所周知
我们可以通过sort来给vector排序
假设有一个名为b的vector<int>

```cpp
sort(b.begin(),b.end());
```
这样可以给b从小到大排序

可是如果我们要从大到小排序呢？

```cpp
sort(b.begin(),b.end(),greater<int>());
```
*ps:如果b是一个二维数组，那么会比较每一行的第一个元素*

我们可以传入第三个参数来更改我们的排序方式，最常见的就是`greater<int>()`从大到小排序。
greater里的<>可以传入float、long、double等等。

但是如果我们想自定义排序方式，或者说根据某排序方式排序字符串或自定义类型呢？

```cpp
bool cmp(int x,int y){
	return x % 10 > y % 10;//从大到小
}
```

我们可以自定义返回值为bool的方法来满足我们的排序需求。

2. 
vector的元素查找方法(不是用b.find()!!!)

```cpp
find(b.begin(), b.end(), 查找元素);
```

3. 
vector 的遍历中

```cpp
for(auto it = b.begin();it != b.end();it++){
    cout << *it;
}
```
其中这个*it是b中的元素,it是指针，可以与整数常量加减运算。
例如可以通过it != a.end()-1 来判断是否达到了最后一个元素。
