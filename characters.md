# Characters 字符
字符以```Char```类型表示，且和数字类型不一样

```kotlin
fun check(c: Char) {
  if (c == 1) { // ERROR: incompatible types
  // ...
  }
}
```

字符以单引号表示:```'1'```

将字符转换成数字类型：

```kotlin
fun decimalDigitValue(c: Char): Int {
  if (c !in '0'..'9')
  throw IllegalArgumentException("Out of range")
  return c.toInt() - '0'.toInt() // Explicit conversions to numbers
}
```