# Data Structures and algorithms in JS <!-- omit in toc -->

# Table of content <!-- omit in toc -->

- [1. Big O](#1-big-o)
- [Memory](#memory)
- [2. Arrays](#2-arrays)
  - [Big O](#big-o)
  - [Memory](#memory-1)

## 1. Big O

## Memory

## 2. Arrays

Stored in order. Smallest footprint.

### Big O

1. lookup: O(1)
2. push: O(1)
3. insert: O(n)
4. delete: O(n)

### Memory

```javascript
var groceries = ["apples", "bananas", "cucumbers", "potatoes"];
```

If we were on a 32 bit system, that translates into 4 shelves of 8 bits, which translates in 4\*4 = 16 bytes of storage

| Shelf |          |
| ----- | -------- |
| 0     | 00000000 |
| 1     | 00000000 |
| 2     | 00000000 |
| 3     | 00000001 |
| 4     | 00000000 |
| 5     | 00000000 |
| 6     | 00000000 |
| 7     | 00000111 |
