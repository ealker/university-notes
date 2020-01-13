# Testing 

# Automated Testing 

## Build Systems 

## Continuous Integration 

## Test Doubles 

Martin Fowler has an informative [article](https://martinfowler.com/bliki/TestDouble.html) on test doubles. 

- Test Stub:

- Test Spy: are a type of stub that records how many responses that were sent. 

- Dummy Object: a dummy object is passed to functions/methods as a way to satisfy the parameter requirements of the method in question.

- [Mock Object](https://martinfowler.com/articles/mocksArentStubs.html):

- Fake Object: 

# Test Driven Development 

Minimum amount of code needed to pass the tests. 

Red, Green, Refactor: Write the tests firsts, they should fail. Then write the code nescessary for the tests to pass, then refactor the code. 

Tests can act as a form of documentation - if you have an inventory system that is used by a library for example you could have unit test names such as `testCountAllBooksInInventory()` or `testFindAuthorBySurname()`.  

## TDD in the context of XP



# Acceptance Testing 

What is the difference between coding tests (unit testsing, integration testsing, system testing) and acceptance tests? 

Coding testsing are defined by the software development team whereas acceptance tests are defined by the customer. 