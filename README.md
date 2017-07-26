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
** 1）在类型后面加一个问号来标记这个变量的值是可选的；
     2）一个可选的值是一个具体的值或者 是 nil 以表示值缺失；
     3）可以一起使用 if 和 let 来处理值缺失的情况：如果变量的可选值是 ，条件会判断为 ，大括号中的代码会被跳过。如果不是 ，会将值解包并赋给 后面的常         量，这样代码块中就可以使用这个值了。
