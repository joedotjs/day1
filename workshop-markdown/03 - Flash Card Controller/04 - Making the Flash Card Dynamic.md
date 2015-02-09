# Making the flash card dynamic

Our template has access to our scope, so let's configure that scope with a bit of data. In our `FlashCardController`,
let's place this set of data on our $scope with the property `flashCard`.

```javascript
$scope.flashCard = {
    question: 'What is Angular?',
    answers: [
        { text: 'A front-end framework for great power!', correct: true },
        { text: 'Something lame, who cares, whatever.', correct: false },
        { text: 'Some kind of fish, right?', correct: false }
    ]
};
```

This is pretty simple. We have an object with a property `question` with the value of the question's text. Then we have
an array of objects on the `answers` property and each of those objects is the `text` of the answer and whether that
answer is `correct` or not. Let's now look at our `index.html`.

```html
<div class="flash-card" ng-controller="FlashCardController">
    <h1>Is this a flash card?</h1>
    <ul class="flash-card-answers">
        <li class="flash-card-answer">
            I mean, yeah.
        </li>
        <li class="flash-card-answer">
            No, it's not.
        </li>
        <li class="flash-card-answer">
            What's a flash card?
        </li>
    </ul>
</div>
```

Let's replace the `<h1>Is this a flash card?</h1>` with the dynamic data from our scope.

<hint title="Putting the question text on our scope">

In our html, we replace

`<h1>Is this a flash card?</h1>`

with

`<h1>{{ flashCard.question }}</h1>`

`flashCard` is the key on our scope, which the template accesses. This key's value is an object with a key `question`
which is a string. We use interpolation (fancy word for `{{ }}`) to place that string in our template. Easy!

</hint>
