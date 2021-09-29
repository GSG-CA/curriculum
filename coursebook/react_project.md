# React Week Project

## E-commerce website

Your project for this week is to build an e-commerce web app using react, and nodejs. Your app basically should have five pages: 
- The main page which contains the list of products.
- Signup page.
- Login page.
- Cart page.
- Product page.

The app is only for one seller/company.

## Description
- A complete figma should be designed for every page and linked in the readme file.
- Project should be built by react and nodejs.
- Routes basically will be:
  - /login, /signup.
  - /cart (get, post, delete).
  - /products (get).
- Adding product will be by insert fakedata to your db.
- Fixing eslint errors is a must.
- You can build your components with antd or material-ui.
- A website lets customers view products from the main page.
- The list of products is dynamically generated from an api.
- Using pagination to load more products.
- Product images loaded lazily (using library for images lazy-loading)
- There must be filter products by price, category and search by name.
- There must be a page for a specific product.
- The customer can add products to the cart but he has to login first.
- If the user logged in then he can view the cart page.
- Take care of user messages, After login or adding product to cart page.
- Before deleting product display pop confirm to ensure product deletion.
- App deployed to heroku. 

## User Stories:
- The user can view existing products from the main page even if he’s not logged in.
- The user can filter products by price, by categories, and search by name.
- The user can view products by moving to the product page.
- The user can add products to the cart.
- If the user is not logged in, Then user should be directed to the login page.
- After I logged in, I should be redirected to the cart page If I was redirected from there, or to the main page by default.
- User can view product’s on his cart from the cart page.
- User can delete product from cart.
 