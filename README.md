# API-REST-Expenditure Control
REST API for Expense Management

What will be used?

* RESTFul.
* DDD.
* Microservices.
* SOAPUI for load testing.
* Data storage (REDIS, MongoDb).
* Using git.
* Communication encryption, with key exchange. (Noise Protocol Framework.)
* CQRS.
* Docker File + Docker Compose.


* Functionality: Card Spending Integration
  Only accredited systems can include new expenses
  A volume of 100,000 inclusions per second is expected
  Expenses will be reported through the JSON protocol, following the pattern:
    { "description": "alfanumeric", "value": American double, "usercode": numeric, "date": Date in UTC format }.
    

* Functionality: Spending filter
  Since I login as an authenticated client
  And I accessed the expense listing interface
  And set the date filter equal to 27/03/1992
  So I would like to see my spending just for this day.

* Functionality: Expense categorization
  Since I login as an authenticated client
  When I access an expense detail
  And this one doesn't have a category
  So I should be able to include a category for this

* Functionality: Category suggestion
  Since I login as an authenticated client
  When I access the expense detail that does not have a category
  And I start typing the category I want
  Then a list of category suggestions should be displayed, these based on categories already entered by other users.

* Functionality: Automatic Spending Categorization
  In the expense integration process, the category must be automatically included.
  if the description of an expense is the same as the description of any other expense already categorized by the customer
  it must receive this category at the time of its inclusion.

