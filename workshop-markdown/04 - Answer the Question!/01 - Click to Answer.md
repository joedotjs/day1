# Click to answer

Very commonly in browser UIs, we want to trigger some function off of a user `click` event. Doing this is very
convenient with Angular.

Let's first attach a method on our flash card scope. Let's call that method `answerQuestion`. This function should
simply just `console.log` anything you want -- so we can eventually see when it is called.

Remember! Scopes in Angular are *just Javascript objects*.

<hint title="Attaching a method to our scope">

In our `FlashCardController` in `app.js`:

```javascript
$scope.answerQuestion = function () {
    console.log('I was called!');
};
```

</hint>

Now to call this method on click. We're going to attach this `click` event to our answer elements. How do we do it?

<hint title="Attaching a click handler">

In our Angular templates, we can use `ng-click`!

Note, the following HTML may differ from yours (based on the last chapter):

```html
<ul class="flash-card-answers">
    <li class="flash-card-answer"
        ng-repeat="answer in flashCard.answers"
        ng-click="answerQuestion()">
        {{ answer.text }}
    </li>
</ul>
```

Click on one of our answers and you will see our scopes `answerQuestion` method fire off!

</hint>