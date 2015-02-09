# Bootstrapping an Angular application

Now that we've included our `angular.js` library and `app.js` in our HTML, let's get our Angular application running.

As proof of concept, let's put an Angular expression in our `<body>` tag: `{{ 2+2 }}`. Refresh, and you'll notice that
the page just has the `{{ 2+2 }}`, not what Angular would normally evaluate: `4`. This is because our Angular app is not
running.

There are two steps to bootstrapping our Angular app:

<hint title="Step 1">

We need to register our application or "module" in Javascript. We have access to angular globally, so we can
simply do this in our `app.js` file, :

```javascript
var app = angular.module('FlashCards', []);
```

`angular.module` takes the name of your application (very important!) and an array of *dependencies* for your
application. For now, we have none, but get excited for upcoming workshops!

</hint>

<hint title="Step 2">

In step 1, we registered our application in Javascript. Now, we need to attach it to our HTML. We accomplish this with
`ng-app`:

```html
<body ng-app="FlashCards">
    {{ 2+2 }}
</body>
```

Notice that the value of `ng-app` is the *same name* as the application we registered in our Javascript. This is
critical and something that will come up again and again with Angular. Make sure you use the same name!

</hint>

After bootstrapping the application, we'll see that what previously outputted as `{{ 2+2 }}` is now `4`, which means
our Angular application is active in our HTML!


