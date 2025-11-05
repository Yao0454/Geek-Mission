# 学习如何使用markdown

#打个空格是标题 一共有六级标题

# 这是一级标题
## 这是二级标题
### 这是三级标题
#### 这是四级标题
##### 这是五级标题
###### 这是六级标题

单个星号之间的文字会变为斜体 
- *斜体文字*

两个星号之间的文字会加粗
- **加粗的文字**

两个波浪线之间的文字会划删除线
- ~~这是被删除的文字~~

然后就是Markdown中的列表，分为：
- 有序列表
- 无序列表

### 有序列表
- 用数字加点即可实现

1. 项目1
2. 项目2
3. ......

### 无序列表
- 用短横线就行了

- 项目1
- 项目2
- ......


# MD里的代码块
- Python
```Python
def add_num(a : int, b: int) -> int:
    return a + b

if __name__ == "__main__":
    print(add_num(1, 2))
```
- C++
```C++
include <iostream>

int main(void) {
    std::cout << "Hello World!" << std::endl;
} 
```
- Go
```Go
package main

import "fmt"

func main() {
    fmt.Println("Hello World")
}
```


## 分割线

--- 

"---"就是分割线

