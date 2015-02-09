# Using ng-class

Let's use `ng-class` in our application. We are displaying an indicator of a correct and incorrect answer in our HTML.

```html
<h2 class="answer-feedback" ng-show="answered">
    <span ng-show="answeredCorrectly">Yeah, you got it right!</span>
    <span ng-show="!answeredCorrectly">Nope, you got it wrong.</span>
</h2>
```

But no matter if it is the correct text or the incorrect text, it's always the same color! We can use `ng-class` to
solve this problem. In our `public/style.css`, we've included some rules about styling the `.answer-feedback <h2>`
element.

```css
.answer-feedback.correct {
    color: green;
}
.answer-feedback.incorrect {
    color: red;
}
```

Using `ng-class`, how can we correctly style our answer feedback?