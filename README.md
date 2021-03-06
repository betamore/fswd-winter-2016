# Intro to Full Stack Web Development (Winter 2016)

## Table of Contents
  * [Notes](#notes)
  * [Units](#units)
    * [Unit 1: Fundamentals and Programming Refresher](#unit-1-fundamentals-and-programming-refresher)
      * [Lab 1: Testing, FizzBuzz, and Fibonacci](https://github.com/betamore/fswd-winter-2016-lab-1)
      * [Lab 2: Hello World Web Server in Node](https://github.com/betamore/fswd-winter-2016-lab-2)
      * [Homework](#homework)
    * [Unit 2: Intro to Express and jQuery](#unit-2-intro-to-express-and-jquery)
      * [Lab 3: Wild Wild Web](https://github.com/betamore/fswd-winter-2016-lab-3)
      * [Lab 4: GETs, POSTs, and templates](https://github.com/betamore/fswd-winter-2016-lab-4)
      * [Homework](#homework-1)
    * [Unit 3: Data Storage and Templating](#unit-3-data-storage-and-templating)
      * [Lab 5: All Your (Data)Base Are Belong To Us](https://github.com/betamore/fswd-winter-2016-lab-5/tree/78e1ecd08213659f08bb72996c89b2b0a5d6b4e9)
      * [Lab 6: Are you suggesting that coconuts migrate?](https://github.com/betamore/fswd-winter-2016-lab-5/tree/fswd-lab-6)
      * [Homework](#homework-2)
      * [Project: Todo](#todo)
    * [Unit 4: Authentication, Authorization, and Sessions](#unit-4-authentication-authorization-and-sessions)
    * [Unit 5: Advanced Forms](#unit-5-advanced-forms)
    * [Unit 6: Application Structure with MVC](#unit-6-application-structure-with-mvc)
      * [Project: Multi-user/list Todo](#multi-userlist-todo)
    * [Unit 7: Advanced JavaScript](#unit-7-advanced-javascript)
    * [Unit 8: Single Page Applications](#unit-8-single-page-applications)
    * [Unit 9: TBD](#unit-9-tbd)
    * [Unit 10: Build Your Own App!](#unit-10-build-your-own-app)
  * [Labs](#labs)
  * [Projects](#projects)
    * [Todo](#todo)
    * [Multi-user/list Todo](#multi-userlist-todo)
    * [Build Your Own App!](#build-your-own-app)
  * [Resources](#resources)

## Notes
  * [Week 1 - Requests and Responses, JS concepts, Tests, Git](week_01.md)
  * [Week 2 - HTML, CSS, DOM, Node Server, Express](week_02.md)
  * [Week 3 - Databases, ORMs, SQL, Sequelize](week_03.md)
  * [Week 4 - Templates, Jade](week_04.md)
  * [Week 5 - Migrations, Deployment, Angular](week_05.md)
  * [Week 6 - Cookies, Sessions, Redis, Gulp](week_06.md)

## Units

### Unit 1: Fundamentals and Programming Refresher

* Overview of the web
  * Requests and responses
* Introduction to Git
  * Cloning
  * Push
  * Pull request
* JavaScript
  * Loops and other control structures
  * Functions
  * Testing
* Using the command line
  * Git
  * Navigating directories
  * Running tests
* [Lab 1: Testing, FizzBuzz, and Fibonacci](https://github.com/betamore/fswd-winter-2016-lab-1)
* [Lab 2: Hello World Web Server in Node](https://github.com/betamore/fswd-winter-2016-lab-2)

#### Homework

* [Eloquent JavaScript][ELJS] Chapters 1-4
* [Pro Git][PG] Chapters 1-2

### Unit 2: Intro to Express and jQuery

* Node HTTP Server
* Intro to Express application framework
* Middleware and static files
* Running a server application
* HTML, CSS, the DOM
* [Lab 3: Wild Wild Web](https://github.com/betamore/fswd-winter-2016-lab-3)
* [Lab 4: GETs, POSTs, and templates](https://github.com/betamore/fswd-winter-2016-lab-4)

#### Homework

* [Eloquent JavaScript][ELJS] Chapters 20, 12-14, 17, 18

### Unit 3: Data Storage and Templating

* Intro to SQL and databases
* ORMs
* Server-side templating
* Application deployment with Heroku
* [Lab 5: All Your (Data)Base Are Belong To Us](https://github.com/betamore/fswd-winter-2016-lab-5/tree/78e1ecd08213659f08bb72996c89b2b0a5d6b4e9)
* [Lab 6: Are you suggesting that coconuts migrate?](https://github.com/betamore/fswd-winter-2016-lab-5/tree/fswd-lab-6)

#### Homework

* Tutorial: [Intro to SQL][SQLB]
* [Jade](http://jade-lang.com)

#### Project: Todo

### Unit 4: Authentication, Authorization, and Sessions

* Cookies
* Users and passwords
* Logging in and out
* Access control schemes
* Development tools!
* More robust templating
* Angular forms

### Unit 5: Advanced Forms

* Form validation with Angular
* AJAX
* Sending email

### Unit 6: Application Structure with MVC

* Programming patterns, disciplines, and methodologies (Oh my!)

#### Project: Multi-user/list Todo

### Unit 7: Advanced JavaScript

### Unit 8: Single Page Applications

### Unit 9: TBD

### Unit 10: Build your own app!

## Labs

* [Lab 1: Testing, FizzBuzz, and Fibonacci](https://github.com/betamore/fswd-winter-2016-lab-1)
* [Lab 2: Hello World Web Server in Node](https://github.com/betamore/fswd-winter-2016-lab-2)
* [Lab 3: Wild Wild Web](https://github.com/betamore/fswd-winter-2016-lab-3)
* [Lab 4: GETs, POSTs, and templates](https://github.com/betamore/fswd-winter-2016-lab-4)
* [Lab 5: All Your (Data)Base Are Belong To Us](https://github.com/betamore/fswd-winter-2016-lab-5/tree/78e1ecd08213659f08bb72996c89b2b0a5d6b4e9)
* [Lab 6: Are you suggesting that coconuts migrate?](https://github.com/betamore/fswd-winter-2016-lab-5/tree/fswd-lab-6)

## Projects

### Todo

It's the hello world of web apps! We will be building a web
application for a single user to track a single to do list. We will
build a web interface for the list that will allow the user to create,
update, remove, and mark (or unmark) as completed to do items. The
todo list data will be stored in a SQL database (in Postgresql). The
backend server will be written in Node and Express (and deployed to
Heroku) and the front end will be implemented with a combination of
Angular and jQuery. The source code will be stored in Git and
published on GitHub.

#### Topics Covered

* Frontend:
  * jQuery
  * Angular
    * Directives
    * Controllers
    * Services
    * Components
* Backend:
  * Express
  * Sequelize
  * Routes
  * Database models
  * Jade Templates
* Web tech and terminology
  * Requests
  * Responses
  * GET/POST
  * Deployment/heroku
  * Testing/CI, coverage

### Multi-user/list Todo

We will take our Todo application and expand it to allow for more than
one user, and for any given user to have access to more than one todo
list.

#### Topics Covered

* Cookies
* Authentication (who is the user)
* Authorization (what can the user access)
* Model relations
* Building APIs
* AJAX
* Single Page Applications

### Build your own app

Use your new found skills to start building something awesome!

## Resources

### Books

* JavaScript
  * [Eloquent Javascript][ELJS]
  * [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS/blob/master/README.md)
* Git
  * [Pro Git][PG]


### Library/Framework Documentation

* [Express](http://expressjs.com)
* [Sequelize](http://docs.sequelizejs.com/en/latest/)
* [Jade](http://jade-lang.com)
* [jQuery](http://api.jquery.com)
* [AngularJS](https://angularjs.org)

### Technical/Service Documentation

* [HTTP](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)
  * [HTTP Status Codes](https://httpstatuses.com)
  * [HTTP Requests](http://www.tutorialspoint.com/http/http_requests.htm)
  * [HTTP Response](http://www.tutorialspoint.com/http/http_responses.htm)
* [Heroku (nodejs)](https://devcenter.heroku.com/categories/nodejs)
* [GitHub](https://help.github.com)

### Tutorials

* [Introduction to SQL][SQLB]
* Git
  * [https://try.github.io/levels/1/challenges/1](https://try.github.io/levels/1/challenges/1)
  * [Hello World](https://guides.github.com/activities/hello-world/)

[ELJS]: http://eloquentjavascript.net
[PG]: https://git-scm.com/book/en/v2
[SQLB]: http://sqlbolt.com/lesson/introduction
