## 1. Hoisting
**Q. What is hoisting?**

A.
* Hoisting is JavaScript's default behavior of moving declarations to the top of the current scope.
* In JavaScript a variable can be used before it has been declared
* JavaScript only hoists declarations, not initialisations.

**Examples:**

```
x = 4;
console.log(x); // will output 4
var x;
```

```
x = 4;
console.log(x); // will output 4
var x = 6;
```

```
var x = 4;
console.log(x, y); // will output 4, undefined
var y = 10;
```

`y` is undefined in the last example because only the declaration (var y) and not the initialisation (=7) is hoisted to the top.

**Notes:**
* To avoid bugs, always declare all variables at the beginning of every scope.
* JavaScript in strict mode does not allow variables to be used if they are not declared.

## 2. Arrays
**Q. How do you check if an object is an array or not?**

A.

**Q. How to empty an array in JavaScript?**

A. There are many ways you can empty an array in JavaScript and they have have different effects on referenced variables.

**Example**

`var arrayList =  ['a','b','c','d','e','f'];`

Method 1
`arrayList = [];`
Note: If you have referenced this array from another variable, then the original reference array will remain unchanged.

Method 2
`arrayList.length = 0;`
Note: This way of emptying the array also updates all the reference variables that point to the original array.

Method 3
`arrayList.splice(0, arrayList.length);`
Note: This way of emptying the array will also update all the references to the original array.

Method 4
```
while(arrayList.length){
  arrayList.pop();
}
```

## Objects


## Closures



## Promises



## Async/await




## Operators

**Q. How does the `===` operator work?**

A. The identity operator returns true if the operands are strictly equal with no type conversion.

Operator Examples

```
3 === 3  // true

3 === '3' // false

var object1 = {'value': 'key'}, object2 = {'value': 'key'};
object1 === object2 //false

0 == 1 // false

0 == "0" // true

0 === "0" // false

true == 1 // true

false == 0 // true

1 + 2 + "3" // "33"

1 + "2" + "3" // "123"

"1" + 2 // "12"

"1" + "3" + 2 // 132
```

Features of comparisons:
* Two strings are strictly equal when they have the same sequence of characters, same length, and same characters in corresponding positions.
* Two numbers are strictly equal when they are numerically equal (have the same number value). NaN is not equal to anything, including NaN. Positive and negative zeros are equal to one another.
* Two Boolean operands are strictly equal if both are true or both are false.
* Two distinct objects are never equal for either strict or abstract comparisons.
* An expression comparing Objects is only true if the operands reference the same Object.
* Null and Undefined Types are strictly equal to themselves and abstractly equal to each other.

**Q. How does Chai do deep equal?**

A. Deep Eql is a module which you can use to determine if two objects are "deeply" equal - that is, rather than having referential equality (a === b), this module checks an object's keys recursively, until it finds primitives to check for referential equality.

More info: https://github.com/chaijs/deep-eql

## setTimeOut

**Q. How does setTimeout work?**


## Misc.

**Q. What is a potential issue with using ```typeof bar === "object"``` to determine if `bar` is an object?**

A. Although typeof bar === "object" is a reliable way of checking if bar is an object, the surprising gotcha in JavaScript is that null is also considered an object!
To avoid this issue you could also check if `bar` is `null`:
`console.log((bar !== null) && (typeof bar === "object"));  // logs false`


