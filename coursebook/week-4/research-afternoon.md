## Research afternoon

The move from writing JavaScript in the browser to writing in Node.js isn't just about learning a few new pieces of syntax and functionality. So far, all of your code has been on the client side – the 'front end'. Node.js opens up a whole new world (a new, fantastic point of view) of coding: the server side, or 'back end'. 

Don't be fooled by the fact that the code looks superficially the same – even though Node and browsers both use JavaScript as a scripting language, the kind of code you're likely to write on the server side will be very different from your client-side code. Most organisations still make a distinction between their back-end developers and front-end developers – and even if you find yourself working across both (the 'full stack'), it's important to understand the distinction in order to maintain the [separation of concerns](https://en.wikipedia.org/wiki/Separation_of_concerns).

Adding a back end doesn't necessarily make your software more complex. Some of the most complex web applications run almost entirely on the front end (so-called 'thick client' apps), while adding some server-side code to handle common tasks like templating can make it much simpler to scale up your website quickly.

It's very important to understand how the server and client relate to each other, and the roles that they'll play in your application – the **Architecting** section explores some of those ideas. Node also comes with its own features and approaches that will be unfamiliar if you've only written client-side code before – the **Engineering** section examines a few of the key ones. 

The **Deploying** section looks at some of the places you might deploy your code, and some of the things you'll need to bear in mind if your code's going to run in different environments.




### Topic 1: Architecting

- *Separation of concerns*: What kind of tasks are normally handled in the back end, and which are more usually handled in the front end? Why?

- *Client side vs server side*: Some tasks – such as templating and validation – can be implemented on either the client or the server. What are the pros and cons of running code on the client, rather than the server (and vice versa)?

- *Alternative back-end technologies*: Which other technologies (programming languages and servers) might be used instead of Node on the back end? What are some of the pros and cons of using Node in your stack, rather than one of those alternatives?

- *Writing for different environments*: Why might you have to write JavaScript differently if it's going to run in the browser, rather than in Node? What tools can help bridge the gap?


### Topic 2: Engineering

- *Modules*: Why is it a good idea to modularise your code? What are `require` and `module.exports`? Why can't you use them in the browser? How might you modularise client-side code?

- *Asyncronous functions*: Why should you use asyncronous forms of functions wherever possible in Node? What are error-first callbacks, and why is it important to follow that pattern in your own code? Why should you avoid using `throw` in callbacks? When might you use the syncronous form of a function instead?

- *Input/output (the `fs` and `path` modules)*: What kind of tasks does the `fs` module enable you to perform that you wouldn't be able to in the browser? What are some of the issues of working with paths when accessing a file system? How does the `path` module help, and why should you use it instead of manually writing file paths as strings?

- *Working with URLs (the `url` and `querystring` modules)*: What is a `urlObject` and how is it structured? Why is it important to be able to turn JavaScript objects into querystrings and back again? Why is it a bad idea to build a query string manually from other strings (think about URL encoding and escape characters)?


### Topic 3: Deploying

- *Cloud platforms*: What is PaaS? Why is it useful to be able to deploy your code to a cloud platform, rather than running it locally? What services are there that can provide you with a platform for your code? [Heroku](http://www.heroku.com) is a good start, but try to find some others. If you have time, try to deploy a simple server to Heroku as a demo.

- *Environment variables*: Why might some variables in your code need to change for different environments? Why is it a bad idea to include those variables in a public repository? What modules might you use to help manage environment variables? (Look at [env2](https://github.com/dwyl/env2) from our neighbours at DWYL.) If you can, write some sample code to show how it works.

### Topic 4: Design Patterns

- Define what a design pattern is in JavaScript
- Compare and contrast creational, structural, and behavioral design patterns
- Implement and examine real world use cases for multiple design patterns
- What is the module design pattern
