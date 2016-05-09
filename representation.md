# Representation 表达式

在Java平台中，数字类型是被当作JVM原始类型物理存储的，除非是我们需要一个可能为空的数字类型引用或者涉及到了泛型，后者的数字类型是装箱类型。

注意，装箱数值类型是不保护唯一ID的：

```kotlin
val a: Int = 10000
print(a === a) // Prints 'true'
val boxedA: Int? = a
val anotherBoxedA: Int? = a
print(boxedA === anotherBoxedA) // !!!Prints 'false'!!!
```

另一方面，数值是相等的：
```kotlin
val a: Int = 10000
print(a == a) // Prints 'true'
val boxedA: Int? = a
val anotherBoxedA: Int? = a
print(boxedA == anotherBoxedA) // Prints 'true'
```
