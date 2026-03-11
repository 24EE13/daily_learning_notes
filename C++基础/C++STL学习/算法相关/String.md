# String

## string初始化

`string a`
`string a = "hello world`
`string a("hello world")`
`string a = b`

这里的最后一个是可行的，不想像c的数组，可以用已经初始化的数组来给另一个未初始化的数组赋值。

***注意！：与c的字符数组不同的是——最后没有用'\0'来作为结束符***



## string输入

1. `cin >> s`
*这种情况遇到空格就会停止输入*

2. `istream& getline(istream& is,string& str,char deline)`
*参数一一般是cin，参数二是存放输入对象，参数三是结束输入的符号，参数三可选，默认为`'\n'`*

## string输出
1. `cout << s`
2. 循环输出`s[i]`


**补充说明**：istream是c++里的标准输入流（对应的，ostream是标准输出流），cin是标准输入流对象。

## string 的成员函数（方法）

### size（）

`s.size()`

用于获取字符串长度，包括空字符。

### 迭代器begin（）和end（）

`s.begin()`
`s.end()`

前者返回第一个字符的位置，后者返回最后一个字符的下一位置。

*这里返回迭代器的类型是`string::iterator`,可以将它当作类型名使用，也可以通过解引用`*`符号来获取字符串里的元素*

*小技巧*
```cpp
for(string::iterator it;it < s.end();it++){
    continue;
}
```
与
```cpp
for(auto it;it < s.end();it++){
    continue;
}
```

可以用`auto`来自动判断类型。

### push_back()

`s.push_back('a')`

在字符串最后面添加元素，并且会增加字符串长度。

### pop_back()

`s.pop_back()`
删除字符串最后面的元素，并且会减少字符串长度。

### insert()

`string& insert(size_t pos,const string& str)`
`string& insert(size_t pos,const char* s)`
`string& insert(size_t pos,int n,char c)`
例：
`s.insert(s.begin()+6,"world!")`

第一个参数是插入的下标位置(一定是迭代器类型的！！)，str是待插入字符串，s是c语言风格的字符数组，n是字符个数，c是待插入字符。

### find()

`size_t find(const string& str,size_t pos = 0)const`
`size_t find(const char* s,size_t pos = 0)const`
`size_t find(char c,size_t pos = 0)const`

参数同上（insert）
find返回找到的第一个下标，没有找到会返回npos。

*npos本质上是string里的常量，它的值为-1*

### substr()

`string substr(size_t pos = 0, size_t len = npos) const;`

返回`string`
默认从0开始到字符串末尾结束。pos是截取起点，len是截取长度。



