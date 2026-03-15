

## 暴力枚举
 
从前往后枚举？从后往前枚举？


## 二分查找
顾名思义，就是找值。    

前提：元素按顺序排列。  

看下面洛谷的例题


### 题目描述

输入 $n$ 个不超过 $10^9$ 的单调不减的（就是后面的数字不小于前面的数字）非负整数 $a_1,a_2,\dots,a_{n}$，然后进行 $m$ 次询问。对于每次询问，给出一个整数 $q$，要求输出这个数字在序列中第一次出现的编号，如果没有找到的话输出 $-1$ 。

### 输入格式

第一行 $2$ 个整数 $n$ 和 $m$，表示数字个数和询问次数。

第二行 $n$ 个整数，表示这些待查询的数字。

第三行 $m$ 个整数，表示询问这些数字的编号，从 $1$ 开始编号。

### 输出格式

输出一行，$m$ 个整数，以空格隔开，表示答案。
---
这里如果用一般的遍历数组会TLE，因此外面要找一个时间复杂度更小的算法来解决这个问题。

细节问题：  
1. 判断完后left或right等于？  
2. while停止的条件？  
3. 求中点的方程？  
4. 判断是否是要求的数？

``` cpp
#include <bits/stdc++.h>

using namespace std;

typedef long long ll; 

vector<ll> a;

ll func(vector<ll>& a,ll left,ll right,ll t){
	ll mid = left+(right-left)/2;
	
	while(left < right){
		if(a[mid] >= t){
			right = mid;
			mid =left+(right-left)/2;
		}
		if(a[mid] < t){
			left = mid + 1;
			mid = left+(right-left)/2;
		}	
	}
	if(a[mid] == t)return mid+1;	
	else return -1;
}

int main() {
    
    vector<ll> a;
    vector<ll> b;
	ll n,m;
	cin >> n >> m;
	ll temp;
	
	for(int i = 0;i < n;i++){
		scanf("%lld",&temp);
		a.push_back(temp);
	}
	
	for(int i = 0;i < m;i++){
		scanf("%lld",&temp);
		printf("%lld ",func(a,0,n-1,temp));
	}

    return 0;
}
```








