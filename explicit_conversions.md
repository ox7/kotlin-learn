# Explicit Conversions 类型转换

  **较小的数值类型不能隐式的转换成较大的数值类型**，这意味著，在没有显示转换情况下，我们不能分配一个```Byte```类型的值给```Int```类型的变量
  
  ```kotlin
val b: Byte = 1 // OK, literals are checked statically
val i: Int = b // ERROR
  ```
我们可以显示的转换来扩展数字类型
```kotlin
val i: Int = b.toInt() // OK: explicitly widened
```
每个数字类型都有如下的转换：

- toByte(): Byte
- toShort(): Short
- toInt(): Int
- toLong(): Long
- toFloat(): Float
- toDouble(): Double
- toChar(): Char

隐式的转换是很明显，因为类型可以从上下文推断出来。为了合适的转换算术操作是被重载的，如：

```kotlin
val l = 1L + 3 // Long + Int => Long
```