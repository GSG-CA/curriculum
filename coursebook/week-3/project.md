## API week project

Your project this week is to build a simple web app (ideally just a single page). You must query at least two APIs and use the results to update the DOM.

What you choose to build and how you choose to display the data is entirely up to you!

During the planning phase we suggest you spend time on:

- Exploring APIs you are interested in working with
- Considering your user journey
- Deciding what you need to build for your Minimum Viable Product (MVP) and splitting up the tasks

### Choosing your APIs

See the list of public APIs [here](https://github.com/public-apis/public-apis).

You can choose to use other APIs if you prefer, but make sure to do your research and check that what you want to do with the API is possible before you start to code.

#### Things to check before you start:

- Are there issues with CORS requests?
- Is there a high enough rate limit?
- Is a free API key available?
- Are you able to use the API without user authentication (oAuth)?
- Is good documentation available?

### Requirements

- Your app queries at least two APIs using the XMLHttpRequest method
- Your app features some dynamic content
- A clearly defined user journey, documented in your readme.
- A well-considered architecture for your app - think back to the workshops from the beginning of this week. Try to modularise your code, or break it down into separate files. Document any key decisions about how you structure your code in your readme!
- Code: break your JavaScript down into small functions with a clear input and output; this will make it easy to write tests
- Tests: write tests for your pure functions. We don't expect tests on the DOM or on the response from an API.
- Design: aim for a responsive, mobile-first design

- Take appropriate measures when it comes to [concealing private information](https://gist.github.com/derzorngottes/3b57edc1f996dddcab25) (i.e. your API key!)

### Keep in mind

- If using a private API key, you won't be able to deploy to GitHub pages this week (if you're not using an API key, go for it!)
- Try and do a little bit of TDD in pairs
- Don't repeat yourself! Try to reuse and refactor bits of existing code where possible.
- Minimise DOM manipulation to keep your app efficient
