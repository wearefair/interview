# iOS Take Home Excercise

Using Swift

Create an iOS App that let a user find a car from a database of cars, show them the articles that are related to the car they selected if there are any available, and show them the nearest dealership by manufature near them and the direction / address to there. i.e. if they are interested in a honda civic, show them the nearest honda dealership. 

# Data Source
You should be able to source the vehicle make / model data, articles, and dealer by brand via edmund's API: http://developer.edmunds.com/api-documentation/overview/

# Images
Unforunately there is no free image apis available for cars, but luckily we can use truecar's image urls for our demo needs, here are some sample urls:
https://a.tcimg.net/v/model_images/v1/2014/gmc/acadia/all/190x97/side
https://a.tcimg.net/v/model_images/v1/2014/gmc/acadia/all/190x97/f3q
https://a.tcimg.net/v/model_images/v1/2017/gmc/acadia-limited/all/360x185/side
https://a.tcimg.net/v/model_images/v1/2017/gmc/acadia-limited/all/360x185/f3q

Plug in the correct year / make / model / trim with data from the edmunds api, and the urls will return an image if there are matchs, or a placeholder image if nothing is there. Don't worry too much about accuracy here, as long as your app demonstrates that it can pull atleast some images correctly.

* feel free to use your own source for car images if available, but they must be hosted and accessed asynchronously. The image source should also be in the public domain so reviewers can view the app without special setups.

# Testing
There should be atleast some high level test coverage of the basic functionalities of your app, demonstrating your ability to test your code.

# Bonus points
For anything that you think would make your demo stand out, i.e. none traditional navigation methods, cool presentation / animation styles



