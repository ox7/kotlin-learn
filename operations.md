# Operations 操作符

位操作符，示例：

```kotlin
val x = (1 shl 2) and 0x000FF000
```

位操作符列表（**仅支持```Int```和```Long```类型**）：

- shl(bits) – signed shift left (Java’s << )
- shr(bits) – signed shift right (Java’s >> )
- ushr(bits) – unsigned shift right (Java’s >>> )
- and(bits) – bitwise and
- or(bits) – bitwise or
- xor(bits) – bitwise xor
- inv() – bitwise inversion


