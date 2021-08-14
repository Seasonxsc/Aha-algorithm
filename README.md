# 啊哈！算法（Golang）

1. 一大波数正在靠近——排序
2. 栈、队列、链表
3. 枚举！很暴力
4. 万能的搜索

## 第1章 一大波数正在靠近——排序

* 桶排序

* 冒泡排序

  冒泡排序的精髓在于双重嵌套循环。如何确定边界条件成了这个算法的痛点。

  假设存在N个数，每一轮排序都是如下操作：

  索引<span style="color:red">**0~N-1**</span>的数 比较+交换

  索引<span style="color:red">**0~N-2**</span>的数 比较+交换

  索引<span style="color:red">**0~N-3**</span>的数 比较+交换

  …

  索引<span style="color:red">**0~1**</span>的数     比较+交换

  必须承认，最后一次排序一定是索引为<span style="color:red">**0~1**</span>的数进行比较和交换操作，一共做了<span style="color:red">**N-1**</span>次。故设定循环如下：

  ```go
  length := len(arr)
  for e := length - 1; e >= 1; e--{
      for i := 0; i < e; i++{
          /* 因内循环的操作均针对arr[i]与arr[i+1]，所以设定其边界为i<e */
          …
      }
  }
  ```

* 冒泡排序（结构体版）

* 快速排序

## 第2章 栈、队列、链表

+ 队列

+ 栈

  * 回文数

    需要对字符串进行操作。Go语言提供了byte与rune两种类型。
  
    ```go
    type byte = uint8	/* 既可以表示二进制数据，又可以表示ASCII定义的英文字符 */
    type rune = int32	/* 表示单个统一码代码点 */
    ```
  
    ```go
    package main
    
    import "fmt"
    
    func main() {
    	verse := "云想衣裳花想容，春风拂槛露华浓"
    
    	for i, v := range []rune(verse) {
    		fmt.Printf("(%d, %c)", i, v)
    	}
    }
    ```

    output:
  
    (0, 云)(1, 想)(2, 衣)(3, 裳)(4, 花)(5, 想)(6, 容)(7, ，)(8, 春)(9, 风)(10, 拂)(11, 槛)(12, 露)(13, 华)(14, 浓)
  
  * 有效的括号
  
    
  
    
  
    

