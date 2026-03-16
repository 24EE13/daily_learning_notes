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



