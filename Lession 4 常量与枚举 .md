## 常量定义关键字 `const`

1. ### 常量
   + #### 函数内定义常量
      ```go
      func consts() {
            const filename = "abc.txt"
            const a, b = 3, 4
            var c int
            c = int(math.Sqrt(a*a + b*b))
            fmt.Println(filename, c)
      }
      ```

   + #### 包内定义常量
      ```go
      package main
      const filename = "abc.txt"
      ```

   + #### `const()`定义
      ```go
      const (
         filename = "abc.txt"
         a, b = 3, 4
      )
      ```

   + #### const数值，编译器可以推测变量类型
      ```go
      const a, b = 3, 4
      var c int
      // 编译器可以推测变量类型
      c = int(math.Sqrt(a*a + b*b))
      ```

2. ### 枚举
   + `iota`实现自增值
     ```go
     const (
        cpp = iota
        _
        python
        golang
        javascript
     )
     fmt.Println(cpp,python,golang,javascript) // 0 2 3 4

     const (
        b = 1 << (10 * iota)
        kb
        mb
        gb
        tb
        pb
     )
     fmt.Println(b,kb,mb,gb,tb,pb) 
     // 1 1024 1048576 1073741824 1099511627776 1125899906842624
     ```
   