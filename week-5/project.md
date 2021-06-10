# Week 5 Project

Create a web app that includes some form of user input and provides users with content from an API that is regularly updated - e.g. the same user input submitted at different times could result in different content being retrieved. 💁‍

A good example could be a news app but feel free to be creative!

The key difference between this project and your API week project is that you will be making your **API calls from the back-end** and **testing your server**.


### Example:

#### User Stories:
'As a student at GSG code academy I want to know all the train departure times from Gaza station, so that I can get home in time for dinner'.🚉🍛

'As a regular commuter, I want to input which direction of travel I am interested in so that I can see information that is relevant to me.'

This news feed could be created with data provided via the [TFL API](https://api.tfl.gov.uk/).

You can build on this user story or create your own user stories as long as they are consistent and the below specs are fulfilled.

### Goals:
1) Write your server using expressJS

2) Use at least 1 API that uses an Access Key and make your API calls from the back-end (try using the `node-fetch` node module)

3) Add the api data to your webpage using DOM manipulation on the Front End (try using `Fetch API` instead of `XMLHttpRequest`)

3) Your server should contain a minimum of 2 routes

4) We expect to see lots of tests! Modularise your code and test all your pure functions. Write tests for as much of your back-end and front-end logic as you can. We don't expect tests on the DOM.

5) Test your server routes by injecting fake HTTP requests using Supertest (including testing for 404's). _Note - **you are not required to test any server route that makes an API call**, as this will make the test impure (a test that depends on an external factor is not reliable)_

6) Host your project on Heroku.
7) Use module.exports and require to break a single large server file into smaller modules.

8) Consider a good server file structure based on what we have discussed over the week.

9) Employ continuous integration on your project with Travis or a similar tool.

10) Include Error Handling. For example:
  - if a user attempts to make a request to a non-existent route to your server (404 - as mentioned above), provide the user with a custom response.    
  - if there is a programmer error on your server (e.g. a handler function does not act as intended), provide the user with a custom response (500 status code).


11) Display continuous integration badges on your project README. 

### Stretch goal 😊:

12) Research and use Nock to mock the response of external API calls in your tests, and write tests for server routes that make API calls.

