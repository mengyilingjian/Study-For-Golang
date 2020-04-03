## 变量定义
1. ### 使用`var`关键字
   + #### 定义变量
      ```go
       var a, b, c bool = true, false, true
       var s1, s2 string = "hello", "world"
       var d, e, f, g = 3, 4, true, "string"
       ```
   + #### 定义变量可放在函数内，或者直接放包内
     ```go
     // 变量在函数内
     func demo(){
         var a int = 30
     }
     ```
     ```go
     // 变量在main包内
     package main
     var (
     	aa = 56
     	bb = true
     	cc = "kkk"
     )
     ```
   + #### 使用var()集中定义变量
     ```go
     var (
         a = 1
         b = true
         c = "kkk"
     )
     ```
     
2. ### 使用`:=`定义变量
    + #### 变量定义
      ```go
      a,b,i,s1,s2 := true,false,3,"hello","world"
      ```
    + 只能在函数内使用`:=`
      ```go
      func demo(){
          a,b,c := 1,true,"hello"
      }
      ```