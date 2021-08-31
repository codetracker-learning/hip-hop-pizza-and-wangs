# MVP Definition - It Gets the Job Done

## Problem

It's January of 2020 and you've just been contacted by a Ma and Pa resturant called "Hip Hop: Pizza and Wangs" that saw your LinkedIn post where you offered your development services to anyone in need to help build out your portfolio. You had just graduated from a Coding Bootcamp and needed all the real experience you could get to help you land your first Job in tech.

"Hip Hop: Pizza and Wangs" have been getting a lot of traffic to their store since placing an ad on Facebook and they can't seem to keep up with the new influx of orders using their current pencil and paper method.

They would like to have a a POS (point of sale) system built for them to help with keeping up with the times as well as their orders! After hearing their story you happily accept their request.

You call up your developer buddies to help you build out this appication so that you can get it up and running for them as soon as possible.

### Part 1: ERDs and Authentication

* Clone this repo
* Create a setup branch
* Do all the stuff needed when setting up the project. Reference the webpack instructions if needed. These include making the updates to the `.env` file
  * Create a new firebase project, database, and enable google authentication, etc.
* Create an authentication branch and add a navbar with a logout button, and place the google login button somewhere for you to test
  * Note: There are components that you can use to get started and style later. We just want you to get your auth set up by yourself.**
* When your user is**logged out** they should see the navbar with only a brand.  And an h1 on the page that says Hip Hop Pizza and Wings (make a `homeLoggedOut` component for this)
* When your user is logged in they should see a navbar with a brand and a logout button and an H1 on the page that says, Welcome user! (make a `homeLoggedIn` component for this)

### Part 2: READ

#### Setup

* Create some JSON data.
* Import that data into firebase

#### Acceptence Criteria

* As an authenticated user, when the app first loads, I should see a home screen that Welcome's the user with their name and a button that reads "View Orders".
* As an authenticated user, I should be able to see a list of all of the orders.
* As an authenticated user, I should be able to see the following details from a single order:
  * Order Name
  * Order Status (open or close)
  * Customer Phone Number
  * Customer Email Address
  * Order Type (phone or in-person)
* As an authenticated user, I should be able see a lists of all of the order item's associated with an order in the order's details view. The following information should be seen from each item:
  * Order Item Name
  * Order Item Price

### Part 3: DELETE

* As an authenticated user, I should be able to delete an order item from an order.
* As an authenticated user, I should be able to delete an order.
* As an authenticated user, when I delete one of the orders all order items that were associated to that order should be deleted as well.

### Part 4: CREATE

* As an authenticated user, when the app first loads, I should see a home screen that has a button that reads "Create Order".
* As an authenticated user, I should be able to create an order.
* As an authenticated user, I should be able to add an order item to an order.

### Part 5: UPDATE

* As an authenticated user, I should be able to update the following information on an order: Order Name, Customer Phone Number, Customer Email Address, and Order Type
* As an authenticated user, I should be able to update the following information on an order item: Item name and Item Price

### Part 6: Revenue

* As an authenticated user, when I'm looking at an order, I should be able to click a button that will take me to a Close Order Form. I should be able to input the following information:
  * Payment Type (cash, check, debit, credit, or mobile-payment)
  * Tip Amount
* As an authenticated user, when I submit the Close Order form, the order's status should change from "Open" to "Closed".
* As an authenticated user, when I submit the Close Order form, a new revenue node is created with the following information:
  * Total Order Amount (including tip)
  * Date
  * Payment Type
  * Tip Amount
  * Order Type
* As an authenticated user, I should __NOT__ be able to close an order that has already been closed.
* As an authenticated user, when the app first loads, I should see a home screen that has a button that reads "View Revenue".
* As an authenticated user, I should be able to see the sum of all of the Revenue made to date.

### Part 7: Deploy and Readme

* As a user, I should be able to use your app on the internet - it should be deployed using Netlify.
* As a developer, I want to see an amazing README for this project.
