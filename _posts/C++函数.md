#### string
- 索引可以采用at()
#### vector数组排序
```c
sort(intervals.begin(), intervals.end(), [](const vector<int>& a, const vector<int>& b){return a[0] < b[0] || (a[0] == b[0] && a[1] < b[1]);});
```
https://blog.csdn.net/m0_46331490/article/details/117391123
#### Lambda表达式语法
![Pasted image 20240401104633.png](Pasted%20image%2020240401104633.png)
#### vector插入
```c
​
#include <iostream>
#include <vector>
#include <array>
using namespace std;
int main()
{
	std::vector<int> demo{1,2};
	//第一种格式用法
	demo.insert(demo.begin() + 1, 3);//{1,3,2}
	//第二种格式用法
	demo.insert(demo.end(), 2, 5);//{1,3,2,5,5}
	//第三种格式用法
	std::array<int,3>test{ 7,8,9 };
	demo.insert(demo.end(), test.begin(), test.end());//{1,3,2,5,5,7,8,9}
	//第四种格式用法
	demo.insert(demo.end(), { 10,11 });//{1,3,2,5,5,7,8,9,10,11}
	for (int i = 0; i < demo.size(); i++)
	{
		cout << demo[i] << " ";
	}
	return 0;
}
```
#### vector二维数组
- **使用构造函数初始化指定大小，元素初始化为零**：

cppCopy code

`std::vector<std::vector<int>> vec(3, std::vector<int>(4, 0));`

这将创建一个3行4列的二维`vector`，所有元素初始化为0。

#### 访问二维`vector`的元素

可以通过双层下标访问二维`vector`的元素，例如`vec[i][j]`表示访问第`i`行第`j`列的元素：

cppCopy code

`int element = vec[1][2]; // 访问第2行第3列的元素`

#### 修改二维`vector`

二维`vector`的大小和内容都可以动态修改。例如，添加新行或列：

- **添加新行**：

cppCopy code

`vec.push_back(std::vector<int>{10, 11, 12});`

- **在特定行添加新元素**：

cppCopy code

`vec[0].push_back(13);`

#### 遍历二维`vector`

遍历二维`vector`通常使用嵌套循环：

cppCopy code

```
for(size_t i = 0; i < vec.size(); ++i) 
{   
	for(size_t j = 0; j < vec[i].size(); ++j) 
	{         
		std::cout << vec[i][j] << " ";     
	}     
	std::cout << std::endl; 
}
```

这里使用了`size()`方法来获取行数和当前行的列数。