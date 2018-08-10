# React Take Home Exercise

Create an react web app to merchandise vehicles

The web app should have the following features:
* A Car Listing Page
  * The car listing page should display a list of cars retrieved from the vehicle index API endpoint provided. At least the following information should be made available to the user
    * Vehicle Make, Model, Trim, and Year
    * Car Image
    * Start Fee and Monthly Fee
    * Use screen shot as guidance if needed.
  * Implement pagination using the data from the index api response
    * Note when calling the stub index endpoint, you will always get the same response data. So handle that as you see fit.
  * When clicking on a specific car, redirect the user to the car detail page.
* Car Details Page
  * Load the vehicle data from the vehicle specific API endpoint, do not pass in data from the index API response!
    * Only two of the vins have valid stubs, for other requests please implement proper API error handling.
  * Showcase the vehicle, using provided design as guidance.
  * Implement a car images gallery for browsing through all images of the car.
  * Implement a mileage slider to allow viewing of different prices based on mileage selected.
* Vehicle Favoriting
  * User should be able to favorite and unfavorite cars on the car listing and car details page.
  * Favorites should be tracked and persisted locally.
  * The favorites on the car listing and vehicle detail page should be in sync.

We suggest using https://github.com/ReactJSResources/react-webpack-babel to help you quickly get started on the exercise.
Use the two attached screen shots as references to what the vehicle listing and detail page should resemble. It's up to you to decide whether you want to implement it as is, or come up with your own vision of the user experience.

# Data Source
Stubbed API endpoints are available via apiary here:
https://interviewapi3.docs.apiary.io/#reference/0/vehicles
  * For car listing: https://private-4e19e-interviewapi3.apiary-mock.com/vehicles?page={page_number}
  * For car details: https://private-4e19e-interviewapi3.apiary-mock.com/vehicles/{vehicle_vin}
    * Out of the 10 vehicles returned, here are only 2 vehicles detail endpoints stubbed out.  Those 2 vehicles will be the only ones you'll be able to get to Car Details page on. For the other vehicles, go ahead and do error handling for them.

For car image urls that are no longer working, feel free to implement placeholders.

# Testing
There should be at least some high level unit test coverage of the basic functionalities of the app which demonstrate your ability to test your code.
React component testing would be a bonus.

# Bonus points
For anything that you think would make your demo stand out, i.e. non-traditional navigation methods, cool presentation / animation styles.
As mentioned above, React component testing will be a bonus.

# How we review
Your application will be reviewed by at least two of our engineers.  We do take into consideration your experience level. We will attempt to apply the following guidelines during the review process, regardless of the type of interview project submitted.

**We value quality over feature-completeness**. It is fine to leave things out provided you call them out in your project's README. The goal of this code sample is to help us understand what you consider production-ready code. You should consider this code ready for final review before deploying to production.

The aspects of your code we will assess include:
* **Architecture**: how clean is the separation between concerns, i.e. API vs Frontend?
* **Code quality**: is the code simple, easy to understand, and maintainable?  Are there any code smells or other red flags? Is the coding style consistent with the language's guidelines? Is it consistent throughout the codebase?
* **Clarity**: does the project have enough comments and documentations to explain the problem and solution? Are technical tradeoffs or shortcuts explained?
* **Correctness**: does the application do what was asked? If there is anything missing, does the README explain why it is missing?
* **Security**: are there any obvious vulnerabilities?
* **Testing**: how thorough are the automated tests? Will they be difficult to change if the requirements of the application were to change? Are there some unit and some integration tests?
  * We're not looking for full coverage (given time constraint) but just trying to get a feel for your testing skills.
* **UX**: Is the UI intuitive and easy to use?
* **Technical choices**: do choices of libraries, data storage / handling, architecture etc. seem appropriate for the application?

Bonus point (those items are optional):

* **Scalability**: will technical choices scale well? If not, is there a discussion of those choices in the README?
* **Production-readiness**: does the code include monitoring? logging? proper error handling?
