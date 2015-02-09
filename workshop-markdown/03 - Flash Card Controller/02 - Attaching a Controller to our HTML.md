# Attaching a controller to our flash card

In Angular, a controller allows to us easily manage the scope of a template. We can place properties, methods on this
scope (which is just a Javascript object!) within our controller so the template can be dynamic and take actions based
on different user actions.

Let's register a new controller with the name `FlashCardController` into our application's ecosystem.

<hint title="How to register a controller">

In `app.js`:

```javascript
app.controller('FlashCardController', function () {
});
```

</hint>

Now that we've registered a controller into our application, we can attach that controller to our HTML.

<hint title="How to reference a controller in HTML">

In our HTML, let's attach the controller to our `.flash-card <div>`.

```html
<div class="flash-card" ng-controller="FlashCardController">
```

Once again, using the exact name is paramount!

</hint>