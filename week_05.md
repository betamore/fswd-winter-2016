# Migrations, Deployment, Angular

## Migrations
Migrations are used to create and modify parts of your database. Migrations can create tables, add columns to tables, remove tables, change column names, etc. In our case, we can use Sequelize to create migration files and migrate them.

To create a migration file, run this line in the terminal.
```
sequelize migration:create
```

That will generate this file where you need to fill out the logic.
```
module.exports = {
  up: function(queryInterface, Sequelize) {
    // logic for transforming into the new state
  },

  down: function(queryInterface, Sequelize) {
    // logic for reverting the changes
  }
}
```

Once you have filled out your migration logic, run this line to run the migrations.
```
sequelize db:migrate
```

For more on Sequelize migrations, [read the docs here](http://docs.sequelizejs.com/en/latest/docs/migrations/).

## Deployment
Deployment is the process of taking your app code on your computer and publishing it to a remote server for everyone to access and use. There are many hosting services to deploy your code to including, but not limited to: [Google Cloud](https://cloud.google.com/), [Amazon Web Services](http://aws.amazon.com/), and [Heroku](https://www.heroku.com/).

## Angular
Angular is a frontend JavaScript framework. It extends HTML with custom attributes to make your HTML more powerful. Angular has many different parts, some of which are: controllers, expressions, directives, filters, modules, and services.

After reading the below, see the [docs for more information](https://angularjs.org/).

### Modules
A module groups together various other pieces (like services, controllers, and directives) of Angular. In one app, it might make sense to have modules for login, user lists, todo lists, etc.

To create a new module, just do
```
var todosModule = angular.module('todosModule', []);
```

### Controllers
A controller deals with the behavior of a module. Controllers can also handle the `$scope` (or state) of the module.

In our case, we can use a controller to handle the behavior of adding a todo in our app, like so
```
todosModule.controller('TodosController', function($scope, $interval, todoService) {
  var todosController = this;

  todosController.addTodo = function () {
    /* code here */
  };
});
```

### Expressions
An expression is code similar to JavaScript that is contained within curly braces like so `{{ expression }}` or with functions in `ng` attributes like `ng-click=functionExpression()`.

### Directives
Directives are custom attributes that you can attach to an HTML element. Built-in directives start with `ng`. You can also create your own custom directives. Some common built-ins are

* `ng-repeat="item in items"` - Loops through items to display the child element repeatedly
* `ng-if="expression"` - Shows an element if the expression returns true

To look into custom directives, [see here](https://docs.angularjs.org/guide/directive).

### Filters
Filters translate your data into a different format or filters it. For instance, you can `reverse` or `uppercase` text. You can also use the `currency` filter to format numbers into a standard currency format. For more on filters, see [here](https://docs.angularjs.org/guide/filter).

### Services
Services can be used to organize your code and share it easily to different parts of your app. Common uses for services include fetching data and communicating with APIs. For more on services, see [here](https://docs.angularjs.org/guide/services).
