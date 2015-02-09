# Managing the Flash Card Scope

We've attached a controller to our flash card element, so we can now manage the scope of this element. This allows for
dynamic output of our HTML. Let's work towards that.

First, we need to gain access to the element's scope in our controller.

<hint title="Gain access to scope">

In our controller function, we can define a parameter of `$scope` in order to gain access to the object that
the template uses for its values.

```javascript
app.controller('FlashCardController', function ($scope) {
    // We now have access to our scope using $scope.
});
```

</hint>

Now, we can place properties and methods on that $scope. Remember, scope is just a Javascript object to which both the
template and the controller have access.

