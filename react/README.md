# React Take Home Exercise

Create an app to organize vehicles in React

The app should have the following functionality:
* Car Listing
  * Each Item should display:
    * Vehicle Make, Model, Trim, and Year
    * Car Image
    * Start Fee and Monthly Fee
  * Have pagination functionality
  * Can click into an item to go to a Car Detail page
  * A way to display that the item has been marked as Removed
* Car Details
  * Display data also displayed from listing
  * Have a slide show of car images
  * An interaction to mark the vehicle as removed, as well as to undo the remove
  * Change the price of vehicle via a slider
* Changes "saved" in Car Details page should be reflected when going back to the Car Listing page

We suggest using https://github.com/ReactJSResources/react-webpack-babel to help you quickly get started on the exercise.
There are 2 screenshots of samples of what our listing and detail pages look like.  They are not meant
to be exactly what we expect these pages to look like, but as a reference to how these pages would look like.

# Data Source
Stubbed endpoints is available here:
https://interviewapi3.docs.apiary.io/#reference/0/vehicles/vehicles-index

Out of the 10 vehicles returned, here are only 2 vehicles detail endpoints stubbed out.  Those 2 vehicles will be the only ones you'll be able
to get to Car Details page on.  For the other vehicles, go ahead and do error handling for them.

# Testing
There should be at least some high level unit test coverage of the basic functionalities of the app which demonstrate your ability to test your code.
React component testing would be a bonus.

# Bonus points
For anything that you think would make your demo stand out, i.e. non-traditional navigation methods, cool presentation / animation styles.
As mentioned above, React component testing will be a bonus.