### if语句判断

1. #### if里的条件可以赋值
2. #### if的条件里赋值的变量作用域就在这个if语句里
   ```go
   if contents, err := ioutil.ReadFile(filename); err != nil {
       fmt.Println(err)
   } else {
       fmt.Printf("%s\n", contents)
   }

   // 这里会报错。contents 作用域不同
   // fmt.Printf("%s\n", contents)
   ```

### switch语句
1. switch语句中，每个case会自动break
2. switch后面可以没有表达式
```go
func eval(a, b int, op string) int {
    var result int
    
    switch op {
        case "+":
           result = a + b
        case "-":
           result = a -b
        case "*":
           result = a * b
        case "/":
           result = a / b
        default:
           panic("unsupported operator:" + op)
    }

    return result
}

func grade(score int) string {
    var g := ""
    switch {
        case score < 0 || score > 100
           panic(fmt.Sprintf("Wrong score: %d", score))
        case score < 60:
           g = "F" // 或者 return "F"
        case score < 80:
           g = "C"
        case score < 90:
           g = "B"
        case score <= 100:
           g = "A"
    }
    return g
}
```