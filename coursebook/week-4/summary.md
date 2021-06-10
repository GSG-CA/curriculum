# Week 4
This week you will be introduced to *Node.js*, *Node Package Manager (npm)*, Node servers, and you will then build your own server and API as part of your team projects.

## What is a server?
A server is a computer program that provides functionality for other programs or devices, called clients. The computer, that a server program runs in, is also frequently referred to as a server.

#### How do the clients and the server interact?
A typical client-server relationship can be summarised in the following steps:

1. A client sends a **request** to the server.  
This involves an action (e.g. `GET` and other types of actions following the <b>C</b>reate <b>R</b>ead <b>U</b>pdate <b>D</b>elete model) and a route/url.  
2. When the server receives the request:
  - it tries to match the route
  - if the route is found, it does something
  - it sends back a **response**

## What is Node.js?

#### The JavaScript beginnings

At the beginning, [Netscape](https://en.wikipedia.org/wiki/Netscape) created JavaScript as feature of its browser to make websites more interactive. It will make them able to run some small scripts and animations on websites when they were almost static content.  

If you want to know more about the JavaScript beginnings [read this wikipedia article](https://en.wikipedia.org/wiki/JavaScript#Beginnings_at_Netscape).

#### The Node.js environment

In mid-2000s the popularity of JavaScript started growing with web applications like Gmail. And after Google open sourced [Chromium](https://en.wikipedia.org/wiki/Chromium_%28web_browser%29), people started to think about taking its JavaScript [V8 engine](https://en.wikipedia.org/wiki/V8_%28JavaScript_engine%29) to use it also outside of the browser.

Node.js is this new environment out of the browser that runs JavaScript and is consistently growing 100% per year. Unlike JavaScript that runs on the browser, the Node.js enviroment doesn't have access to the `window` global object, or to the [DOM](https://en.wikipedia.org/wiki/Document_Object_Model). On the other hand, Node.js lets you access the file system, network or other stuff that other languages like php gives you by default in their standard libraries.

So, in one sentence Node.js is Javascript for the server and this new cool environment will allow us to build web servers (back-end) and command line applications using JavaScript.

> If the difference between front-end and back-end is still not clear by now, read [this article](https://en.wikipedia.org/wiki/Front_and_back_ends). In a few words, the front-end is everything you see in your browser, and the back-end is the program you are running in your server.

## Node package manager

Node package manager (npm from now) is a tool for managing packages that come with Node.js. It is the largest package manager in the world that allows us to install packages/modules as dependencies of our projects and also publish our own packages.

> In one sentence, [Packages/modules](https://docs.npmjs.com/how-npm-works/packages#what-is-a-module) are small programs we can integrate with our projects.

Node.js comes with npm installed. However, npm gets updated more frequently than Node does, so it's good to check if we have the latest version.

#### Common npm commands

* `npm init`: Initialize a package and create a `package.json` that stores meta data about your app or module.

* `npm search MODULE_NAME`: Search a module in the npm registry.

* `npm install MODULE_NAME`: Install MODULE\_NAME locally.

  * `npm install -g MODULE_NAME`: Install MODULE\_NAME globally.

  * `npm install --save MODULE_NAME`: Install MODULE\_NAME locally and add it as a dependency in the package.json.

  * `npm install --save-dev MODULE_NAME`: install MODULE\_NAME locally and add it as a development devependency in the package.json.

* `npm --version`: Check current installed version
