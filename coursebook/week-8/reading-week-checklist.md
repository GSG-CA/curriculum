# Checklist of things to think about & challenges after first 8 weeks

A checklist of things to look at and see if you can answer after the first eight weeks of the program.

This is **long** and somewhat difficult in places - you probably won't be able to thoroughly look through all of it! Instead **look at the things you think are most challenging first** 

You should definitely not be concerned if you can't answer everything yet - 8 weeks is not enough time to come to grips with it all! 

Think of this as a learning aid to help you find the things you don't understand, and then ask your fellow students/mentors on discord! After the break maybe we can find a time to talk about it as a cohort to find things people struggle with.

It is roughly in order of when it was taught, but look at it in whichever order you choose.

For the challenges, I suggest you open a repo, and save them all there.

## Contents

- [Github](#github)
- [Javascript](#javascript)
- [DOM Manipulation](#DOM-Manipulation)
- [HTML/CSS](#HTML/CSS)
- [HTTP](#HTTP)
- [Callbacks](#callbacks)
- [Testing](#testing)
- [node](#node)
- [Databases](#databases)
- [Deploying](#deploying)
- [Auth](#auth)
- [Express](#express)
- [Coding Best Practices](#coding-best-practices)

---

### Github
- [ ] Why do we use github/git?
- [ ]  What happens when you `clone` a repository?
- [ ] What happens when you `fork` a repository?
- [ ] What happens when we do `git pull origin master`
- [ ] How do we create a new branch on our local machine?
- [ ] When we make a change to a file, how do we tell git to track it?
- [ ] When we have finished working on a branch, how do we make sure that our changes do not cause a conflict with master? (this can all be done **locally**)
- [ ] What does `git push origin [branch-name]` do?
- [ ] Why do we make pull requests instead of just changing master directly?
- [ ] Why is it important to run our team member's branches when they make a pull request?
- [ ] This is the working process you should follow, try to explain what happens at each step/why we do it:
    - `git clone [repository]`
    - `git checkout -b new-feature`
    *make some changes to index.js*
    - `git add index.js`
    - `git commit -m "added a cool new feature"`
    *since we started, our partner has merged another branch into master*
    - `git checkout master`
    - `git pull origin master`
    - `git checkout new-feature`
    - `git merge master`
    *merge conflict happens in index.js we fix it*
    - `git add index.js`
    - `git commit -m "fix merge conflict"`
    - `git push origin new-feature`

---

### Javascript
- #### Using these array and string methods:
	-   `.map()`
	-   `.filter()`
	-   `.find()`
	-   `.replace()`
	-   `.reduce()`
	-   `forEach()`
- [ ] complete the challenges in comments [here](https://gist.github.com/m4v15/08db7adb3856f7393672ded7a52f5e45)

---

### DOM Manipulation

- [ ] What is DOM manipulation?
- [ ] Try to write an HTML & JS file that:
    - has a title, a text input and a button
    - when a user types something in the input, and clicks the button, it should change the title to what the user type
    - add another button to the html that will change the colour of the title
- [ ] Why should we always use `eventListeners` in Javascript and not inline `onClick` handlers in the HTML? 

---

### HTML/CSS
- [ ] Why is accessibility important?
- [ ] How do we test for accesbility?
- [ ] What is semantic HTML?
- [ ] Convert [the html linked here](https://gist.github.com/m4v15/28d64be4fb3495aa1ff3a91bf4336bb1) to use semantic HTML instead of divs.
- [ ] Using flexbox, change the layout of the above HTML to [something like this] https://www.figma.com/file/ewvTXphnscgQ2HD5gHkyHRz8/BASIC-DESGIN?node-id=0%3A1
- [ ] You should use media queries to make it work for both desktop _and_ mobile - without media queries, it should match the mobile design (i.e. be mobile first).

---

### HTTP
- [ ] What does the Status Code of an HTTP response tell us?
- [ ] What are some common Status codes?
- [ ] What are HTTP methods and what are the different methods intended for?

---

### Callbacks

- [ ] Why is it important to use asynchronous functions in Node?
- [ ] What are error-first callbacks, and why is it important to follow that pattern in your own code?
- Take the following code:
```js

const getUsernameFromDatabase = (email, callback) => {
  const database = db.get("data")
  const user = database.find(user => user.email === email)
  const username = user ? user.username : null
  if (!username){
      callback(new Error('No user found'))
  }
  callback(null, username)
}
```
- [ ] Write code which would call the above function and:
    - [ ] if there is an error, it should `console.log` to the user "Sorry there was a problem"
    - [ ] if it finds a user it should `console.log` to the user "Marhaba {username}!"
- [ ] Finish writing the below function so that when it inserts data into the database it uses the second argument as an *error first* callback. If the insert is successful it should send back `true` in the callback (remembering it is error first).
```js
const addUser = (data, cb) => {
    db_connection.query('INSERT INTO users (name, email,password) VALUES ($1, $2, $3)', [name, email, password], (error) => {
    // write your code here
    })
}
```

- [ ] Hard challenge! [Parallel Functions](https://github.com/foundersandcoders/master-reference/blob/master/coursebook/week-3/morning-challenge.md)

---

### Testing

- [ ] **WITHOUT writing the function itself,** using tape, write tests for a function which can take two numbers, and a string. The string should be a mathematical operation: "add", "subtract", "times" or "divide"
- The function should return the first number, then the mathematical operation of it combined with the second number:
    - (3, 2, "add") should return 5
    - (3, 2, "subtract") should return 1
    - (3, 2, "times") should return 6
    - (3, 2, "divide") should return 1.5
    - (2, 3, "subtract") should return -1
    - (2, 3, "divide") should return 0.667
- [ ] After writing some tests, try to write the function. Keep adding tests and developing the function until it can pass everything.
- [ ] What is the difference between `equal` and `deepEqual` in Tape?

---

### Node
- [ ] How do you initialise an `npm` or `node` project?
- [ ] What is the only script that an `npm` project starts with, how do you add one?
- [ ] What is the difference between `dependencies` and `devDependencies`?
- [ ] What is the difference between package.json and package-lock.json
    - package-lock.json is automatically generated for any operations where npm modifies either the node_modules tree, or package.json . It describes the exact tree that was generated, such that subsequent installs are able to generate identical trees, regardless of intermediate dependency updates.
    - [good medium article](https://medium.com/coinmonks/everything-you-wanted-to-know-about-package-lock-json-b81911aa8ab8)
- [ ] build a simple server that can:
    -  [ ] serve an html page with CSS and JS when you got to the `/` endpoint
    -  [ ] when a user makes a request to `GET /students` return a JSON of all your cohort's students
    - [ ] when a user makes a request `POST /students` with the payload `{name: 'Mavis'}` it returns plain text which says `Hello Mavis`

- [ ] using supertest, test each of the routes on your server:
	- [ ] check for status codes
	- [ ] check the body response is correct
- [ ] what is the difference between `querystring.parse` and `url.parse`?
- [ ] what is the output from `querstring.stringify({search:'javascript'})` (hint: RUN THIS AND FIND OUT!)
- [ ] what is the output from `url.parse('https://www.codewars.com/users/m4v15/completed')` (hint: RUN THIS AND FIND OUT!)
- If I have the following file structure:
```
-public
  -index.html
  -index.js
  -index.css
-src
  -database
    -db_connect.js
  -app.js
  -server.js
```
- [ ] What file path should I use to `require` the `db_connect` file if I am in `app.js`
- [ ] What is the file path to `index.html` from `app.js`

---

### Databases
You should know:
- [ ] how to create a database
- [ ] how to connect to a database using `node-postgres (pg)`
- [ ] how to build a database
- [ ] what is a database schema?
- [ ] why we use different database urls for production, development and testing?
- [ ] if you've used the `pg` module and created a [database connection pool](https://node-postgres.com/features/pooling), how would you use the `.query` method to query the database?  
	- [ ] what are parameterized queries?
-  **Challenge**:
    - [ ] make a database of users and books, where each user can have multiple books and each book can be owned by multiple users (many to many)
    - [ ] write a small node script that will return the books of a particular user
    - [ ] you will need:
        - a SQL build script
        - a database connection javascript file
        - a database build javascript file
        - a config.env file
        - a app.js javascript file that has a function that takes a name of a user (a string) and queries the database, returning the name of the books that user has
        - Hint:
		    - build script should have 3 tables: users (id, username, location), books (id, name), userbooks(user_id, book_id)

---

### Deploying
- [ ] how to set up travis
	- [ ] How to make travis run your tests
	- [ ] How to make travis run something else (eg a linting script)
	- [ ] **Bonus hard check** how to make travis build its own database for testing on....
- [ ] How to set your app up on heroku
	- [ ] If your heroku app doesn't deploy, how can you find out what the problem is?
	- [ ] How do you provision a database on heroku
	- [ ] How do you add environment variables on heroku
- [ ] What should we store in `config.env` file? Why?
	- [ ] Do the variable values in my `config.env` file have to be the same as their values on heroku?

---

### Auth

- [ ] how to hash and compare using bcrypt
- [ ] how to save and read a cookie on the server
- [ ] how to write a JWT on the server
- [ ] why is a JWT secure?
- [ ] how to secure a route and allow people with a valid jwt through

---

### Express

- [ ] Convert the server from the node section to an express server. 
    - [ ] Use express router
    - [ ] add a logger.
    - [ ] You should be putting post requests on the `req.body`
- [ ] What is express middleware? 

---


### Coding Best Practices
- [ ] **eslint**
	- [ ] Why is linting important? Why should all of your code have the same style?
	- [ ] Install eslint on an old project of yours, and use the airbnb style guide. Try to fix all of the problems.
	- [ ] create your own eslint config with all your favorite rules
		- create a `.eslintrc.json` in root and copy the code below into your file
		- add the eslint rules you would like to enforce. You can find them all in [eslints docs](https://eslint.org/docs/rules/)
		- stuck? further details on eslint configuration [can be found here](https://eslint.org/docs/user-guide/configuring)
``` 
		{
    "rules": {
        "if-curly-formatting": 1
    }
}

```
		
- [ ] **Prettier** set up prettier on your editor
	- [ ] set it to follow the rules in an eslint config file if one is in the repo
	- [ ] set it to format on save
- [ ] how should you debug your code if things are going wrong? Give some different steps
- [ ] You **need** to get very comfortable typing on an english keyboard with both hands. Having speed to try things out will help **a lot** when you don't understand things.
