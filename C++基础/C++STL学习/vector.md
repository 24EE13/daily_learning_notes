# STL之Vector容器
由Luogu的Xuan_Wellfish编写
---  
**vector**是类似于数组的容器，储存连续且类型相同的数据，并且长度可变 

## vector数组的定义  

`vector<类型名> arr(长度,初值)`<br>   
`vector<类型名> arr(长度)`      
`vector<类型名> arr`     
`vector<vector<类型名> > arr`     
`vector<vector<类型名> > arr(行长度)`     
`vector<vector<类型名> > arr(行长度,vector<类型名>(列长))`       
`vector<vector<类型名> > arr(行长度,vector<类型名>(列长,初值))`      

## vector数组的访问  

访问方法与普通数组类似
`arr[下标]`   


## vector类的一些方法   

### 尾接和尾删   

`arr.push_back()`   
`arr.pop_back()`   

**注意：**  

- 当arr确定了长度时，使用push_back会直接将添加的元素放在数组最后面，并增加数组长度   

### 获取大小   

`arr.size()`

- 获取到元素个数,不管元素是什么类型

### 删除元素   

单个删除   
`arr.erase(迭代器)`  

- 会删除对应元素，但不会释放已分配的内存空间
- 参数不是直接的下标！！ 

全部清空   

`arr.clear()`   

- 会删除所有元素，但不会释放已分配的内存空间   

### 内存管理  

`arr.shrink_to_fit()`    

- 释放多余内存，capacity() 变为 0  

`arr.capacity() `   

- 表示：vector 已经向操作系统申请的内存空间

`arr.reserve(n)`   

-  作用是：主动要求 vector 提前分配能容纳至少 n 个元素的内存空间


**一些值得注意的点：**    
- 由**vector**类型定义的二维数组，在一维基础上的*类型名*里，不要将`> >`写成`>>`。（这可能会报错）  
- 二维数组一旦要初始化列，就一定要确定列长。   
- 如果没有定义数组的长度（不管是行还是列），不能直接通过下标访问它












