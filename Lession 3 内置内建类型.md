### Go内建变量类型 

+ 布尔型
  ```go
  bool,string
  ```

+ 整型：`(u)int8`表示长度为8，`uintptr`不定长，系统64位则长度为64
  ```go
  // 有符号
  int,int8,int16,int32,int64,uintptr
  // 无符号
  (u)int,(u)int8,(u)int16,(u)int32,(u)int64,uintptr
  ```
+ 字符型(没有char,只有rune)
  ```go
  byte  //字符型8位
  rune  //字符型32位
  ```
+ 浮点型
  ```go
  float32,float64
  complex64,complex128  //复数类型
  ```

### 强制类型转换

+ 例子
  ```go
  var a, b int = 3, 4
  var c int 
  c = int(math.Sqrt(float64(a*a + b*b)))
  ```