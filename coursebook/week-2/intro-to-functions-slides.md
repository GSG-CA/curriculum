
# Functions

They're great.

---

# What is a function?

A function takes an `input` and returns an `output`

---

Know your function

```javascript=
function myFunction(argument1, argument2) {
  console.log("first argument:", argument1);
  console.log("second argument:", argument2);
}
```

Note:

1.  **Qs** about anatomy of a function: name, arguments, body
2.  **Q:** What does it mean to _call_ a function?
3.  **Q:** What does it mean to _invoke_ a function?
4.  **Q:** What will this function _do_ if called as `myFunction("hello", "world")`?
5.  **Q:** What will this function _return_?
6.  Explain difference between output and side effects

---

Know your function

https://repl.it/@sima_qian/functionreturnsundefined?lite=true

Note:

1.  Type `myFunction("hello", "world")`
2.  **Q:** What will happen when we run this?
3.  **Q:** What will this function return?
4.  Run.
5.  **Q:** How can we change the returned value?
6.  Add `return 0` as last line of `myFunction`
7.  Comment out `return 0` and return second `console.log`
8.  **Q:** What will it return now?

---

### Functions are first-class objects

---

![](https://media.giphy.com/media/3WmWdBzqveXaE/giphy.gif)

---

### Functions are first-class objects

(everything is an object)

Note:

1.  In JavaScript, everything is an object

---

https://repl.it/@sima_qian/everythingisanobject?lite=true

Note:

1.  `foo()`
2.  **Run repl**
3.  **Q:** `$ foo instanceof Function //true`
4.  **Q:** `$ foo instanceof Object //true`
5.  **Q:** `$ Function instanceof Object //true`
6.  **Q:** `$ Function instanceof Function //true`
7.  Good [stackoverflow description](https://stackoverflow.com/a/23623598) of `instanceof`

---

### Functions are first-class objects

They are treated like any other variable

---

You can store a named function in a variable

```javascript=
function foo() {
  console.log("Hello world");
}

var myFunction = foo;
```

---

You can store a named function in a variable

https://repl.it/@sima_qian/functioninavariable?lite=true

Note:

1.  `myFunction()`
2.  Type `myFunction`
3.  **Q:** What will happen when we run this?

---

You can store an anonymous function in a variable

```javascript=
var myAnonFunction = function() {
  console.log("Hello anon");
}
```

---

You can store an anonymous function in a variable

https://repl.it/@sima_qian/anonfunctioninavariable?lite=true

Note:

1.  **Q:** `myAnonFunction()`
2.  **Q:** `myAnonFunction`
3.  Directly compare with `myFunction`

---

You can store a function in an object

---

What's an object?

![](https://media.giphy.com/media/xT8qB4HMK24AVjZwuk/giphy.gif)

Note:

1.  **Q:** What is an object?
2.  **Q:** If a function is an object, how can we store it inside an object?

---

Here's one I made earlier

```javascript=
var myDoggoObject = {
  name: "Mackerel",
  breed: "Beagle",
  likes: ["tennis balls", "flip-flops", "food"],
  legs: 4,
  goodBoy: true
}
```

![](https://i.imgur.com/YbR9BCM.png)

Note:

1.  Objects are a way to store data.
2.  A way to group related data
3.  Objects are made of `name: value` pairs

---

You can store a function in an object

https://repl.it/@sima_qian/functioninobject?lite=true

Note:

1.  **Q:** How do we access data in an object?
2.  `myObject.name`
3.  `myObject.likes`
4.  Add `bark: function() { console.log("woof!") }`
5.  **Q:** How can we call this method?
6.  `myDoggoObject.bark()`
7.  **Q:** What will `myDoggoObject.bark` do?

---

You can store a function in an array

```javascript=
var myArray = [0, 1, 2, 3, 4];

var functionsArray = [
  function() { console.log("I'm the first element") },
  function() { console.log("I'm the second element") }
]
```

Note:

1.  Explain zero-indexing

---

You can store a function in an array

https://repl.it/@sima_qian/functionsinarray?lite=true

Note:

1.  **Q:** How do we access the first number?
2.  `myArray[0]`
3.  Add `function() {console.log("hello from index 5!")}`
4.  **Q:** How can we call this function?
5.  `myArray[5]()`

---

You can pass a named function as an argument to another function

```javascript=
function myFunction() {
  console.log("Hello world");
}

function foo(fun) {
  fun();
}
```

---

You can pass a named function as an argument to another function

https://repl.it/@sima_qian/functionasargument?lite=true

Note:

1.  `myFunction()`
2.  `foo(myFunction)`
3.  `foo("a string") //error`
4.  **Q:** What will `foo(myFunction())` do?
5.  Add `console.log(fun)` and run
6.  So we can pass the output of a function as an argument
7.  We just don't want to do that here
8.  `myFunction()`
9.  Add `return 0` to end of `myFunction`
10. `myFunction`
11. **Oops! Q:** What did I do wrong?
12. `myFunction()`
13. `foo(myFunction)`
14. **Q:** why do we get `undefined` again?
15. Change to `return fun()` in `foo`
16. Any questions?

---

You can pass an anonymous function as an argument to another function

```javascript=
function foo(fun) {
  fun();
}
```

---

You can pass an anonymous function as an argument to another function

https://repl.it/@sima_qian/anonfunctionasargument?lite=true

Note:

1.  `foo(function() {console.log("hello anon")})`

---

You can return a function from a function

```javascript=
function greetSomeone(greeting) {
  return function(name) {
    console.log(greeting, name);
  }
}
```

---

You can return a function from a function

https://repl.it/@sima_qian/functionreturnsfunction?lite=true

Note:

1.  **Q:** What does `greetSomeone` do?
2.  **Q:** How can we make a function that always uses the greeting "hello"?
3.  `var sayHello = greetSomeone("hello")`
4.  **Q:** How can we use this to say "hello world"?
5.  `sayHello("world")`

---

## :rotating_light: JARGON ALERT :rotating_light:

![](https://media.giphy.com/media/HUkOv6BNWc1HO/giphy.gif)

---

A function that is passed as an argument to another function is known as a

`callback function`

---

A function that takes another function as an argument and/or returns a function is known as a

`higher-order function`

---

# Funception

![](https://media.giphy.com/media/l0HlHSB8v5yRtBlHW/giphy.gif)

---

What's going on here?

```javascript=
foo1(foo2(foo3()));
```

---

Funception

https://repl.it/@sima_qian/funception?lite=true

Note:

1.  Let's define these functions first
2.  `foo1() { console.log(1) }`
3.  `foo2() { console.log(2) }`
4.  `foo3() { console.log(3) }`
5.  **Oops! Q:** What have I done wrong here?
6.  Correct mistake.
7.  **Q:** In which order will the numbers be logged? Vote.
8.  **Q:** What is `typeof foo3()`?
9.  **Q:** What is `typeof foo2(foo3())`?
10. Let's change it up a bit
11. Just call `foo1()`
12. `foo3` returns `"1"`
13. `foo2` assigns `var y = foo3()` and returns `Number(y)`
14. Explain `Number` is a built-in function
15. `foo1` assigns `var x = foo2()` and returns `x * 3`
16. **Q:** What will the result be? `//3`

---

# What was the point of that?

Let's talk about the `call stack`.

---

```javascript=
function foo1() {
  var x = foo2();
  return x * 3;
}

function foo2() {
  var y = foo3();
  return Number(y);
}

function foo3() {
  return "1";
}

foo1();
```

---

<img src="https://i.imgur.com/JhNoOrD.png" height="500px" />

---

<img src="https://i.imgur.com/RZ7orLX.png" height="500px" />

---

<img src="https://i.imgur.com/6P4eA36.png" height="500px" />

---

<img src="https://i.imgur.com/r8aBDPa.png" height="500px" />

---

<img src="https://i.imgur.com/OBdSjDh.png" height="500px" />

---

<img src="https://i.imgur.com/JEFeqLV.png" height="500px" />

Note:

1.  **Q:** Where does stack overflow get its name?

---

# Calling back callbacks

![](https://media.giphy.com/media/l1J9HX2NOtjEpIxJC/giphy.gif)

---

Recall that a `callback function` is a function that is passed as an argument to another function

---

Let's take it up a notch

```javascript=
function firstFunction() {
  console.log("I'm the first function");
}

function secondFunction(callback) {
  callback();
  console.log("I'm the second function and I expect a callback as an input");
}
```

---

Let's take it up a notch

https://repl.it/@sima_qian/onecallback?lite=true

Note:

1.  `secondFunction(firstFunction)`

---

Let's add another callback!

```javascript=
function firstFunction() {
  console.log("I'm the first function");
}

function secondFunction(callback) {
  callback();
  console.log("I'm the second function and I expect a callback as an input");
}

function thirdFunction(callback) {
 callback();
 console.log("I'm the third function, I'm also expecting a callback as an input");
}
```

---

Let's add another callback!

https://repl.it/@sima_qian/twocallbacks?lite=true

Note:

1.  Type `thirdFunction(secondFunction(firstFunction))`
2.  **Q:** What do we expect to happen?
3.  Run.
4.  **Q:** Can someone talk us through what happened?
5.  **Q:** How can we fix it?
6.  **Solution:** `thirdFunction(function() {secondFunction(firstFunction)})`
7.  Recap: to go more than one layer deep in callbacks, you need to wrap functions in anonymous functions.

---

## Can a callback function can take arguments?

---

Of course it can!

```javascript=
function firstFunction(number) {
  console.log("I'm the first function and I expect an input:", number);
}

function secondFunction(callback) {
  var number = 1;
  callback(number);
  console.log("I'm the second function and I expect a callback as an input");
}
```

---

A callback function can take arguments

https://repl.it/@sima_qian/callbackwitharguments?lite=true

Note:

1.  `secondFunction(firstFunction)`
2.  Type `secondFunction(firstFunction(1))`
3.  **Q:** Would this work? `(NO)` Why not?
4.  **Q:** What type of error would we expect?

---

5 MINUTE BREAK

![](https://media.giphy.com/media/5gZW718dxT6XoBvWEl/giphy.gif)

---

# Time to asynchronous get

![](https://media.giphy.com/media/3ohuAxV0DfcLTxVh6w/giphy.gif)

---

## :rotating_light: JARGON ALERT :rotating_light:

![](https://media.giphy.com/media/HUkOv6BNWc1HO/giphy.gif)

---

### Synchronous vs. Asynchronous

![](https://media.giphy.com/media/xT39DdoX1AwKgVW8j6/giphy.gif)

Note:
Bake Off analogy
They don't sit around while waiting for one cake to bake!

---

**Synchronous code:**

- waits for each action to complete before moving on to the next one

**Asynchronous code:**

- doesn't have to wait, so can execute multiple actions at the same time

Note:

1.  JavaScript is a synchronous language
2.  But can behave asynchronously
3.  **Q:** How did people feel about event loop video?
4.  **Q:** What is synchronous code?
5.  **Q:** What is asynchronous code?

---

A taste of asynchronicity...

https://repl.it/@sima_qian/asynchelloworld?lite=true

Note:

1.  **Q:** What is asynchronous code?
2.  **Q:** What do we expect the code to do when we run it?
3.  Run.
4.  **Q:** How might we delay the first `console.log`? (Testing general knowledge/awareness of `setTimeout`)
5.  Wrap first `console.log` in `setTimeout`:

```
setTimeout(function() {
 console.log("Hello");
}, 3000);
```

6.  **Q:** What do we expect the code to do when we run it?
7.  Run.
8.  **Q:** What will happen with `setTimeout` of `0`?

---

## What's the point here?

---

### _Life_ isn't synchronous

When you're dealing with the internet, or even just large datasets, things take time.

You don't want your entire program to stop and wait for a request for data over the internet to come back.

Note:

1.  **Q:** What is asynchronous code?
2.  **Q:** What is synchronous code?

---

You want your program to be able to send off a request over the internet and then do some other stuff while it waits for data to come back.

Note:

1.  **Q:** What is synchronous code?
2.  **Q:** What is asynchronous code?

---

### Be careful when mixing synchronous and asynchronous code

```javascript=
function asyncAddOne(number, callback) {
  setTimeout(function() {
    callback(number + 1);
  }, 3000);
};
```

Note:

1.  **Q:** Can someone talk through this function?
2.  **Q** What does `asyncAddOne` return?

---

https://repl.it/@sima_qian/syncasyncmix?lite=true

Note:

1.  Type `var x = 0;`
2.  Type `asyncAddOne(10, function(newValue) { x = newValue; });`
3.  Type `console.log(x);`
4.  **Q:** What will happen when we run this? Will `x` be logged as `11`? Or `0`? Hands up.
5.  Run.
6.  **Q:** Why did that happen?
7.  Add `console.log(x);` inside callback.
8.  Run.

---

### A challenge:

```javascript=
function asyncAddOne(number, callback) {
  setTimeout(function() {
    callback(number + 1);
  }, 3000);
};

function asyncMultiplyThree(number, callback) {
  console.log("result from first function:", number);
  setTimeout(function() {
    callback(number * 3);
  }, 3000);
};
```

Multiply the result of the `asyncAddOne` using `asyncMultiplyThree`

e.g. `(10 + 1) * 3`

Note:

1.  **Q:** Can someone talk through `asyncMultiplyThree`?
2.  Type out code in own editors
3.  Don't change either function
4.  Want to `console.log` final result
5.  **10 MINS**, then cast

---

https://repl.it/@sima_qian/syncasyncchallenge?lite=true"

Note:

```javascript=
asyncAddOne(10, function(newNumber) {
  asyncMultiplyThree(newNumber, function(result) {
    console.log("final result:", result);
  })
});
```
