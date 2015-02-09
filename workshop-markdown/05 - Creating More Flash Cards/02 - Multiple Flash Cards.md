# Multiple flash cards

We have our `MainController` placing our flash cards array on the scope. How can we use this array to create multiple
flash cards while maintaining the functionality we've built for our single flash card?

<hint title="About controllers">
Angular controllers, like our `FlashCardController` do not have to be used 1-to-1 with an Angular template. They can
be reused lots of times!
</hint>

<hint title="Another clue">
Remember ngRepeat? Repeated elements create their own scopes and can have their own controllers!
</hint>