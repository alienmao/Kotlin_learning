# Basic Syntax

## Defining Packages
Package specification should be at the top of the source file:
必须要在源文件的顶上

```

  package my.demo

  import java.util.*

// ...

```
## Defining functions
定义函数<br>
Function having two Int parameters with Int return Type:

```
fun sum(a: Int, b: Int): Int {
    return a + b
}

fun main(args: Array<String>) {
    print("sum of 3 and 5 is ")
    println(sum(3, 5))
}
```

Function with an expression body and inferred return type:
```
fun sum(a: Int, b: Int) = a + b

fun main(args: Array<String>) {
    println("sum of 19 and 23 is ${sum(19, 23)}")
}
```
Function returning no meaningful value:
```
fun printSum(a: Int, b: Int): Unit {
    println("sum of $a and $b is ${a + b}")
}

fun main(args: Array<String>) {
    printSum(-1, 8)
}
```
Unit return type can be omitted(省略):
```
fun printSum(a: Int, b: Int) {
    println("sum of $a and $b is ${a + b}")
}

fun main(args: Array<String>) {
    printSum(-1, 8)
}
```

## Defining local variables
### Val
只读本地常量
```
val a： Int = 1
val b=2
val c: Int  // Type required when no initializer is provided
c=3
```
### Mutable variable:
不定的变量
```
fun main(args: Array<String>) {
    var x = 5 // `Int` type is inferred
    x += 1
    println("x = $x")
}
```

## Comments
```
// This is an end-of-line comment

/* This is a block comment
   on multiple lines. */
```
块注释可以被嵌套

## Using string templates
```
fun main(args: Array<String>) {
    var a = 1
    // simple name in template:
    val s1 = "a is $a"

    a = 2
    // arbitrary expression in template:
    val s2 = "${s1.replace("is", "was")}, but now is $a"
    println(s2)
}
```
