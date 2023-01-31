**Author**: [@LinaYahya](https://github.com/LinaYahya)

# Intro to Functions (Mentor Notes)

This notes will help mentor delivering the workshop.

The workshop delivery based on discussion with students. Try to create a repel or working on any text editor you prefer, Introduce a block of code, give students 3-5 minutes thinking on flow, ask questions and hear answers.

**Notes to Keep in mind:**
- don't assume all things is clear to all students.
- workshop seems easy, But It's a bit tricky.
- You need to hard prepare to this workshop, assume you will asked a lot of questions and a tricky one.
- understanding functions, call stack essential in this time of the course.
- As a best case student's will understand 70% of the content of the workshop and that's totally fine.
- this workshop is one of the most interesting workshops we have, So have fun!


The workshop delivery on two parts, Here is listed the points to cover in this workshop, keep in mind that there's examples on the workshop, related to every point, Maybe you can create more!

It refer to you how to lead the discussion, But I assume that you need whiteboard to help! 

### Part 1: Functions Basics
1. **function anatomy**
    - what is a function
    - describe the anatomy of the function 
    - how can we invoke the function? 
    - parameters vs arguments
    - calling a function with missing arguments   
    - greet vs greet()
    - What function would return if there's no `return`
    - assign return value to variable `const full_name  = findName(whatever)`

start with asking questions about why to create and use functions, whats the anatomy of functions, make sure that it's clear to everyone the difference between declaring a function and calling it, explain what `return` keyword is, What if function doesn't return anything.
Also you need to explain assignment of function return value `const result = func()`

2. **function declaration vs function expression**
    - differences
    - can we omit function name
    - How to call function expression 
    - can we access function by name (in what scope it will be defined)  

make sure to highlight difference between function expression and arrow functions, as many people confused with!

Try to have an example of both functions declared calling them before - *just a quick explanation Introduce Hoisting* (**Don't go deeper**)

```js
    sayHi();
    getName();

    const sayHi = () => console.log('1');

    function getName(name){
        return name
    }
```

Create a function expression named one, try to access name `greet` anywhere :arrow_down: 

```js
const sayHi = function greet(){
// Do anyting
}
```
Can we access `greet` anywhere? What's the point of the name can we omit it? 


3. **Functions are first-class objects**
    - `myFunc` instanceof `Function`
    - `myFunc` instanceof `Object`
    - `Function` instanceof `Object`
    - `Object` instanceof `Function`
    - can we add a property to a function
    - can we store a function in an array, object

Explain objects in JS, and the phrase says `Everything is an object in JS`, Does function is an object, Does it have methods `console.dir` would help on this, try to add properties to your function!

If function is an object, can we store it in array, other objects, How we can call it? 


4. **Pass a function as an argument**
  
    start with an example to pass a function to another as an argument,
    ```js
        function sayHi() {
          console.log("Hello world");
        }
        function tellGreet(func) {
          // callback
          func();
        }
    ```
    - `tellGreet(sayHi)`
    - `tellGreet(sayHi())` 
    
What's the output? what's the difference between them, Can we make the last one pass?

Here everything will be hazy, take your time to explain differences! 

5. **Callback and Higher order functions**
    
Now we can introduce callbacks based on the previous point. Introduce higher order function by creating examples to return a function from a function 
    
    
6. **Start with call-stack and functions execution**

Check [funception](https://github.com/GSG-CA/curriculum/blob/main/coursebook/week-2/intro-to-functions-slides.md#funception) a good example to start with!
It's worthy to spend time on this, Be prepared that even you might get confused with this!


### Part 2: Call Stack and Intro to Synchronous and Asynchronous 

7. call stack and runtime environment
     - [graph of js runtime ](https://i.ibb.co/LS0WPv2/js.png)
     - play with [Loupe](http://latentflip.com/loupe/?code=JC5vbignYnV0dG9uJywgJ2NsaWNrJywgZnVuY3Rpb24gb25DbGljaygpIHsKICAgIHNldFRpbWVvdXQoZnVuY3Rpb24gdGltZXIoKSB7CiAgICAgICAgY29uc29sZS5sb2coJ1lvdSBjbGlja2VkIHRoZSBidXR0b24hJyk7ICAgIAogICAgfSwgMjAwMCkc7Cn0pOwoKY29uc29sZS5sb2coIkhpISIpOwoKc2V0VGltZW91dChmdW5jdGlvbiB0aW1lb3V0KCkgewogICAgY29uc29sZS5sb2coIkNsaWNrIHRoZSBidXR0b24hIik7Cn0sIDUwMDApOwoKY29uc29sZS5sb2coIldlbGNvbWUgdG8gbG91cGUuIik7!!!PGJ1dHRvbj5DbGljayBtZSE8L2J1dHRvbj4%3D) as a visualization to help you understand how JavaScript's call stack/event loop/callback queue interact with each other.
     - Maybe you can visualize DOM events on Loupe
 
8. Recursion 

9. Start with async
    ```js
    function fakeSyncNetworkRequest() {
      for (let i = 0; i < 5000000000; i += 1) { }
      console.log("one");
    }
    ```      
    
  - Introduce `setTimeout` , Synch Vs. Async Don't go deeper


### Out of scope
In this workshop, you gonna introduce a lot of concepts and terminologies, try to focus on functions, call stack, callbacks, and get a sneak peek to asynchronous javascript.

So for new concepts, such as hoisting and asynchronicity give a quick intro only don't go deeper. Keep in mind that next week we will go deeper with Asynchronous Callbacks, hoisting, and closures.