# Angular 1.x Part 2 Notes

## How do we iterate through arrays in Angular?

```html
<!DOCTYPE HTML>
<html>
  <body ng-app="myApp" ng-controller="myController">

    <!-- This iterates through $scope.myArray. -->
    <p ng-repeat="arrayValue in myArray">{{arrayValue}}</p>
    <!-- This iterates through $scope.myArray2 and accesses the value "key". -->
    <p ng-repeat="arrayValue in myArray2" track-by="$index">{{arrayValue.key}}</p>
    <!-- Note that we had to use `track-by` in order to make sure duplicates are allowed. -->
    <script src="angular.min.js"></script>
    <script>
    var myApp = angular.module('myApp', [])
    myApp.controller("myController", function($scope) {
      //Declare an array in $scope
      $scope.myArray = [1, 2, 3, 4, 5]
      //Declare an array with objects in $scope
      $scope.myArray2 = [
        {key: 'value1'},
        {key: 'value2'}
        {key: 'value3'}
      ]
    })
    </script>
  </body>
</html>
```

## How do we make a SPA (Single Page Application)

```html
<!DOCTYPE HTML>
<html>
  <body ng-app="myApp" ng-controller="myController">

    <!-- Make sure you specify ng-view inside a div inside your app. -->
    <div ng-view></div>

    <script src="angular.min.js"></script>
    <!-- Make sure to include the angular.route.js script in your root HTML file. -->
    <script src="angular.route.js"></script>
    <script>
    var myApp = angular.module('myApp', [])

    myApp.config(function($routeProvider) {
      //You initialize the $routeProvider with `.when()` routes
      $routeProvider
      .when('/', {
        template: '<p>I am route 1 I display on /#/</p>'
      })
      .when('/route2', {
        template: '<p>I am route 2 I display on /#/route2</p>'
      })
      //Remember you can also reference HTML pages for better separation of concern
      //You can do this by doing `templateUrl` instead of `template`
    })

    myApp.controller("myController", function() {

    })
    </script>
  </body>
</html>
```

## Summary

- Iterating through arrays you use the `ng-repeat` function and access `$scope` variables
- SPA is initialized by using the `.config()` function.
