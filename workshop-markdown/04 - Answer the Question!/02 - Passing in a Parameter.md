# Passing in a parameter

We have our `answerQuestion` method firing when we click, but this function needs to receive a parameter. That parameter
is our matching answer. How can we pass this answer into our `answerQuestion` method when we click?

<hint title="Solution">

```html
<li class="flash-card-answer"
    ng-repeat="answer in flashCard.answers"
    ng-click="answerQuestion(answer)">
    {{ answer.text }}
</li>
```

In our template, we can access properties on our scope, including in the parameters of our function call. Because
`ng-repeat` creates a new scope for every iteration, `answer` is on our scope and able to be placed as our parameter.

If we update our `answerQuestion` method to `console.log` out the parameter:

```javascript
$scope.answerQuestion = function (theAnswer) {
   console.log(theAnswer);
};
```

* Note: the name of the parameter in our method does not have to match key on the scope (`answer`).

We now see `console.log`'d the object that matches our clicked answer.

</hint>