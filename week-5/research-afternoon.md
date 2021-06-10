## Express Middlewares

- What are express middlewares?
- What functionality do they provide?
- What are some examples of useful express middleware and 
how do you use them ([several useful examples](https://blog.jscrambler.com/setting-up-5-useful-middlewares-for-an-express-api/))

## Continuous Integration

- Research what Continuous Integration is and what assurances it can provide when building an application.
- Create a basic Node project on Github that includes some tests with Tape, then sync your project with an online CI tool. Add a new feature to your project, commit your changes, then check on your CI tool to ensure your tests are still passing and your project build is passing. A popular tool is [Travis](https://travis-ci.org/), [this](https://github.com/dwyl/learn-travis) excellent tutorial will come in handy.
- (Bonus) after verifying the latest changes, display the [build](https://camo.githubusercontent.com/3de407029531b1bcff394070e6d820d3f883a8c5/68747470733a2f2f7472617669732d63692e6f72672f6e6a736669656c642f6d79736974652e7376673f6272616e63683d6d6173746572) .svg file provided and display it at the top of your projects' README.md file.

## Streams and Buffers

- Research what streams and buffers are in Node, how are they used in conjunction?
- Create a file `streamFile.js`, so that when a user runs the command `node streamFile.js bigtextfile.txt`, it **streams** the contents of the file to the users terminal.
  - Need a big file? How about a [book](https://www.gutenberg.org/).
  - To start with, you could hardcode the file path `bigtextfile.txt` into the `js` file instead of passing it as a command-line argument.
- (Bonus) Allow an additional argument to be provided in the command to specify a time interval of how often a chunk of text from the file is streamed to the terminal. E.G `node streamFile.js bigtextfile.txt 1s`

## Debugging

- What’s debugging? And why it’s important in the development process?
- What’s breakpoints and when to use it. 
- Demo of debugging JavaScript in Chrome DevTools.
- Demo of debugging in VScode or any other editors.

