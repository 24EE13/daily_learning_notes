# STL之Map容器   

**map**映射，原理是红黑树，有序键值对结构

> 0->3
> 1->2
> 2->4
> ...



## map的定义：

`map<键类型,值类型,比较器> mp`

## map 的添加元素：
`mp[key] = value`
`mp.insert({key,value})`
以上是插入一对键值的。

往map里添加key和value时是一起添加的（也就是说——不可以直接分开添加key和value！！！）。

## map的遍历


## map的一些小技巧

因为map在通过key访问value时，如果没找到，会直接返回0（准确来说value是int时会这样），可以通过这个来查找map中是否存在某value。

*补充：*
*如果 value 是数值类型（int/float 等），会返回该类型的零值（比如 int 返回 0，float64 返回 0.0）；*
*如果 value 是字符串，返回空字符串 ""；*
*如果 value 是布尔类型，返回 false；*
*如果 value 是指针 / 切片等，返回 nil。*



