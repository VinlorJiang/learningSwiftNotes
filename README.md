# learningSwiftNotes
学习swift过程的笔记


## 阅读 The Swift Programming Language 中文版 -v1.8.pdf 记录：
### 1. 简单值
* 1.1 把值转换成字符串的一种方法:把值写到括号中，并且在括号之前写一个反斜杠，即： \() ，栗子：

```
let apples = 3
let appleSummary = "I have \(apples) apples"
```
* 1.2 使用方括号[]创建数组和字典，使用下标或者键key来访问元素， 栗子：
```
var shooingList = ["catfish","water"]
shoopingList[1] = "bottle of water"

var occupations = ["Malcolm":"Captain","Kaylee":"Mechanic",]
occupations["Jayne"] = "Public Relations"
```
* 1.2.1 创建空数组或者字典,使用初始化方法：
```
let emptyArray = [String]()
let emptyDictionary = [String : Float]()
```
* 1.2.2  创建空数组或空字典的时候，如果类型被推导出来，可使用下面方式创建：
```
shoopinglist = []
occupations = [:]
```
### 2.控制流
* 2.1 可选值：
1）在类型后面加一个问号来标记这个变量的值是可选的；
2）一个可选的值是一个具体的值或者 是 nil 以表示值缺失；
3）可以一起使用 if 和 let 来处理值缺失的情况：如果变量的可选值是 nil，条件会判断为 false，大括号中的代码会被跳过。如果不是 nil，会将值解包并赋给 let 后面的常量，这样代码块中就可以使用这个值了。
```
var optionalString: String? = "Hello"
print(optionalString == nil)

var optionalName: String? = "John Appleseed"
var greeting = "Hello!"
if let name = optionalName {
    greeting = "Hello, \(name)"
}
```
* 2.2 另一种处理可选值的方法是通过使用 ?? 操作符来提供一个默认值.
```

 let nickName: String? = nil
 let fullName: String = "John Appleseed"
 let informalGreeting = "Hi \(nickName ?? fullName)"
```
* 2.3 运行 switch 中匹配到的子句之后，程序会退出 switch 语句，并不会继续向下运行，所以不需要在每个子句结尾 写 break .
* 2.4 可以在循环中使用 ..< 来表示范围,栗子：
```
 var total = 0
 for i in 0..<4 { // 0,1,2,3不等于4
 total += i 
 }
 print(total)
```
### 3.函数和闭包：
* 3.1 默认情况下，函数使用它们的参数名称作为它们参数的标签，在参数名称前可以自定义参数标签，或者使用 _ 表示不使用参数标签。如：
```
func greet(_ person: String, on day: String) -> String {
    return "Hello \(person), today is \(day)."
}
greet("John", on: "Wednesday")  // 函数调用person参数名称酒没显示出来
```
* 3.1 函数可以嵌套，被嵌套的函数可以访问外侧函数的变量；
* 3.2 使用 in 将参数和返回值类型声明与闭包函数体进行分离，栗子：
```
 numbers.map({
     (number: Int) -> Int in
     let result = 3 * number
     return result
})
```
### 4.对象和类
* 4.1 使用 class 和类名来创建一个类，如：
```
class Shape {
    var numberOfSides = 0
    func simpleDescription() -> String {
        return "A shape with \(numberOfSides) sides."
    }
}
```
* 4.2 要创建一个类的实例，在类名后面加上括号。使用点语法来访问实例的属性和方法,栗子：
```
var shape = Shape()
shape.numberOfSides = 7
var shapeDescription = shape.simpleDescription()
```

## 闭包：
### 1.闭包表达死语法：闭包的函数体部分由关键字 in 引入。该关键字表示闭包的参数和返回值类型定义已经完成，闭包函数体即将开始。
```
{ (parameters) -> retureType in
statements
}
```
> uhijlk;
