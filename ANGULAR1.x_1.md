# Angular 1.x Part 1 Notes

## What is Angular?

### From the Angular website

HTML is great for declaring static documents, but it falters when we try to use it for declaring dynamic views in web-applications. AngularJS lets you extend HTML vocabulary for your application. The resulting environment is extraordinarily expressive, readable, and quick to develop.

### What does this mean?

- Angular is designed for dynamic views for web applications.
- Angular uses similar language constructs for HTML.


## How do we initialize an angular app?

```html
<!DOCTYPE HTML>
<html>
  <!-- First declare the name of the app and root controller. -->
  <body ng-app="myApp" ng-controller="myController">

    <!-- Include the angular script in angular.min.js -->
    <script src="angular.min.js"></script>
    <!-- Write your own custom module and declare the controller -->
    <script>
    var myApp = angular.module('myApp', [])
    myApp.controller("myController", function() {
      //This functions runs on initialization...
    })
    </script>
  </body>
</html>
```

## What is data binding?

### From the Angular website

Data-binding is an automatic way of updating the view whenever the model changes, as well as updating the model whenever the view changes. This is awesome because it eliminates DOM manipulation from the list of things you have to worry about.

### What does this mean?

- Whenever the model changes (`$scope` or `$rootScope`), the HTML updates to match it.
- Traversing variables are easier to do with Angular.

### How do we do it?

```html
<!DOCTYPE HTML>
<html>
  <!-- First declare the name of the app and root controller. -->
  <body ng-app="myApp" ng-controller="myController">
    <!-- Bind the $scope.message variable to the HTML Input -->
    <input type="text" ng-model="message"/>
    <!-- You can also bind it directly to the HTML -->
    <p>My message is: {{message}}</p>
    <!-- Include the angular script in angular.min.js -->
    <script src="angular.min.js"></script>
    <!-- Write your own custom module and declare the controller -->
    <script>
    var myApp = angular.module('myApp', [])
    myApp.controller("myController", function($scope) {
      //This functions runs on initialization...
      //The message will start off as "Hello" in the input box and in the paragraph tag.
      $scope.message = "Hello"
    })
    </script>
  </body>
</html>
```

## How do we trigger events?

### Example of events

```html
<!DOCTYPE HTML>
<html>
  <!-- First declare the name of the app and root controller. -->
  <body ng-app="myApp" ng-controller="myController">
    <!-- Bind the $scope.message variable to the HTML Input -->
    <!-- the onChange function `logMessage()` fires every time you input text into the input. -->
    <input type="text" ng-model="message" onChange="logMessage()"/>
    <!-- You can also bind it directly to the HTML -->
    <p>My message is: {{message}}</p>
    <!-- The onClick function `logMessage()` fires every time you press the button. -->
    <button onClick="logMessage()">Press this button</button>
    <!-- Include the angular script in angular.min.js -->
    <script src="angular.min.js"></script>
    <!-- Write your own custom module and declare the controller -->
    <script>
    var myApp = angular.module('myApp', [])
    myApp.controller("myController", function($scope) {
      //This functions runs on initialization...

      //The message will start off as "Hello" in the input box and in the paragraph tag.
      $scope.message = "Hello"

      //console.log a message with this function. Note that you cannot use regular function on `onChange` and `onClick` events.
      $scope.logMessage = function() {
        console.log("Messaged logged...")
      }
    })
    </script>
  </body>
</html>
```

## Summary

- Angular.js makes it easier to interpolate Javascript variables in HTML
- Angular.js uses data binding to mix $scope and $rootScope variables and functions into HTML.
- Angular app is simple to initialize and you can have as many controllers and apps as you want in a HTML page.
