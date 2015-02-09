# One is the loneliest number

We definitely want our flash card app to have more than one flash card, but so far we've only built functionality
to use our `FlashCardController` on one `.flash-card <div>` element.

Let's start the process of making it as many as we need. Create a new controller in your `app.js` called
`MainController`. On the scope for that controller, let's attach the following data to the scope on a `flashCards` key.

```javascript
$scope.flashCards = [
    {
        question: 'What is Angular?',
        answers: [
            { text: 'A front-end framework for great power!', correct: true },
            { text: 'Something lame, who cares, whatever.', correct: false },
            { text: 'Some kind of fish, right?', correct: false }
        ]
    },
    {
        question: 'What is a controller?',
        answers: [
            { text: 'Something that manages my front-end routes', correct: false },
            { text: 'A function that allows me to manage a scope', correct: true },
            { text: 'An Angular template', correct: false }
        ]
    },
    {
        question: 'What does {{ }} do?',
        answers: [
            { text: 'It runs some Javascript', correct: false },
            { text: 'It looks for variables in HTML', correct: false },
            { text: 'It runs an Angular expression that accesses my $scope', correct: true }
        ]
    }
];
```

Let's then attach our `MainController` to our template on the `<body>` element. Now our template can access our array
of flash cards by accessing the `flashCards` key. Try it out by interpolating `{{ flashCards }}` anywhere within your
`<body>` tag.