# Right or wrong?

Our `answerQuestion` method is taking in our answer, which means we need to accomplish a few things:

- First, we need to evaluate if the question is correct or incorrect.
- Second, we need to mark our flash card as answered so it cannot be answered again.
- Third, we need to display a message stating if the user answered correctly or not.

Here is some HTML to add to your template underneath the answers:

```html
<h2 class="answer-feedback" ng-show="answered">
    <span ng-show="answeredCorrectly">Yeah, you got it right!</span>
    <span ng-show="!answeredCorrectly">Nope, you got it wrong.</span>
</h2>
```

`ng-show` is another tool we can use in our templates to hide/show elements based on if a *value on
the scope* (like `answered` and `answeredCorrectly`) returns true or false (shows if the value is true).

Using this template, let's have our `answerQuestion` method manage our scope so that we can get this
template to work correctly.
