
# Array Methods

In JavaScript, you can have two types of methods:

- **Static methods** These are called on the class itself.
- **Instance methods** These are called on the class instance.

## Static Methods

In the context of arrays, the static method means the method is not tied to a particular instance of an array. In other words, you do not need an array object to call a static method.

#### **`Array.isArray()`**

Array.isArray() method checks whether an object is an array or not.

```js
Array.isArray([1, 2, 3])       // true
Array.isArray("Hello")         // false
Array.isArray({test: "value"}) // false
Array.isArray(undefined)       // false
Array.isArray(null)            // false
```

## Instance Methods

An instance method is a method that is called on a particular array object. An instance method uses the instance information to perform a task, such as to sort the array.


#### **`pop()`, `push()`, `shift()` and `unshift()`**


- `pop()` removes the last element from an array and returns that element. This method changes the length of the array.
- `push()` adds one or more elements to the end of an array and returns the new length of the array.
- `shift()` removes the first element from an array and returns that removed element. This method changes the length of the array.
- `unshift()` adds one or more elements to the beginning of an array and returns the new length of the array.

```js
const arr = [1, 2, 3]

arr.pop()
console.log(arr) // [1, 2]

arr.push(3,4)
console.log(arr) // [1, 2, 3, 4]

arr.shift()
console.log(arr) // [2, 3, 4]

arr.unshift(1)
console.log(arr) // [1, 2, 3, 4]
```

#### **`forEach()`**

forEach() iterates over the elements of an array and executes a provided function once for each array element.

```js
const arr = ["JS", "Java", "Python"]

arr.forEach(function (element, index, array) {
    console.log(index + " : " + element)
})

// 0 : JS
// 1 : Java
// 2 : Python
```

#### **`map()`**

map() creates a new array populated with the results of calling a provided function on every element in the calling array.

```js
const nums = [3, 5, 4]

const evenNums = nums.map(function (num, index, array) {
    return num * 2
})

console.log(nums) // [3, 5, 4]
console.log(evenNums) // [6, 10, 8]
```

#### **`filter()`**

filter() creates creates a new array filled with the elements from the given array that pass the test implemented by the provided function.

```js
const nums = [3, 5, 4]

const evenNums = nums.filter(function (num, index, array) {
    const isEeven = num % 2 === 0

    return isEeven
})

console.log(nums) // [3, 5, 4]
console.log(evenNums) // [4]
```

```js
const arr = [true, {}, undefined, [], [1, 2], null, "0", 0, false, "false", "undefined", 24]

const truthy = arr.filter(function (element, index, array) {
    return element
})

console.log(truthy) // [true, {}, [], [1, 2], '0', 'false', 'undefined', 24]
```

#### **`reduce()`**

reduce() executes a reducer function on each element of the array and returns a single output value.

```js
const nums = [1, 2, 3, 4];
const initialValue = 0;

const sumWithInitial = nums.reduce(function (accumulated, currentValue, currentIndex, array) {
    return accumulated + currentValue
}, initialValue);

console.log(sumWithInitial); // 10
```

Q) write a function that finds the maximum element in a numeric array using the reduce() method.

#### **`some()`**

some() tests whether at least one element in the array passes the test implemented by the provided function. It returns true if, in the array, it finds an element for which the provided function returns true; otherwise it returns false. It doesn't modify the array.

```js
const arr = [1, 2, 4, 2]

const isOdd = arr.some(e => (e + 1) % 2 === 0)

console.log(isOdd) // true
```

#### **`every()`**

every() tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.

```js
const arr = [1, 2, 4, 2, null]

const isTruthy = arr.every(Boolean)

console.log(isTruthy) // false
```

#### **`includes()`**

includes() determines whether an array includes a certain value among its entries, returning true or false as appropriate.

```js
const pets = ['cat', 'dog'];

console.log(pets.includes('cat')); // true
console.log(pets.includes('lion')) // false
```

#### **`indexOf()` and `findIndex()`**

- `indexOf()` returns the first index at which a given element can be found in the array, or -1 if it is not present.

- `findIndex()` returns the index of the first element in an array that satisfies the provided testing function. If no elements satisfy the testing function, -1 is returned.

```js
const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];

console.log(beasts.indexOf('bison')); // 1

console.log(beasts.indexOf('giraffe')); // -1

console.log(beasts.findIndex(beast => beast.length === 3)) // 0

console.log(beasts.findIndex(beast => beast.length === 8)) // -1
```

> ***check this useful article:*** 
>
>[The JavaScript Array Handbook – JS Array Methods Explained with Examples](https://www.freecodecamp.org/news/the-javascript-array-handbook/)
