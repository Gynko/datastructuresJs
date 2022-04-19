# Data Structures and algorithms in JS <!-- omit in toc -->

# Table of content <!-- omit in toc -->

- [1. Big O](#1-big-o)
- [2. Memory](#2-memory)
- [3. Arrays](#3-arrays)
  - [3.1. Memory](#31-memory)
  - [3.2. Methods and Big(O)](#32-methods-and-bigo)
  - [3.3. Two types of arrays: static and dynamic](#33-two-types-of-arrays-static-and-dynamic)
  - [3.4. Building an array in js from scratch, using classes](#34-building-an-array-in-js-from-scratch-using-classes)
  - [Strings and arrays](#strings-and-arrays)

# 1. Big O

# 2. Memory

# 3. Arrays

Stored in order. Smallest footprint.

## 3.1. Memory

```javascript
var groceries = ["apples", "bananas", "cucumbers", "potatoes"];
```

If we are on a 32 bit system, each "memory slot" takes 4 times 8 bits or 4 times 1 Byte. So our array with 4 elements occupies 4 Bytes times 4 = 16 Bytes. There location is adjacent.

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

When i type groceries[2], I ask the computer to look at shelf number 2.

## 3.2. Methods and Big(O)

1. push: adds an element in the end => O(1)
2. pop: removes last element => O(1)
3. unshift: adds an element at the beginning of the array => O(n)
4. splice: adds an element at index => O(n)

## 3.3. Two types of arrays: static and dynamic

1. Fixed arrays are fixed in size, meaning that you specify their size when creating them and it won't change. In Js arrays are dynamic. When adding a new element, the algorithm will usually create in a new memory slot an array with the double amount of entries.

## 3.4. Building an array in js from scratch, using classes

```javascript
class MyArray {
  constructor() {
    this.length = 0;
    this.data = {};
  }

  get(index) {
    return this.data[index];
  }

  push(item) {
    this.data[this.length] = item;
    this.length++;
    return this.length;
  }

  pop() {
    const lastItem = this.data[this.length - 1];
    delete this.data[this.length - 1];
    this.length--;
    return item;
  }

  delete(index) {
    const item = this.data[index];
    this.shiftItems(index);
  }

  shiftItems(index) {
    for (let i = index; i < this.length - 1; i++) {
      this.data[i] = this.data[i + 1];
    }
    delete this.data[this.length - 1];
    this.length--;
  }
}

var newArray = new MyArray();
newArray.push("hello");
newArray.push("world");
newArray.pop();
console.log(newArray);
```

## Strings and arrays

If you have a problem involving strings, you should think of it as an array question. Strings are simply arrays of characters.

If you get a problem such as reverting a string, it will be about reversing an array.
