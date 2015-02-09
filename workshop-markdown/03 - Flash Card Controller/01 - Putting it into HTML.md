# Putting our flash card into HTML

Before we start dealing with scope, controllers or anything else Angular, let's place our flash card onto our page
statically. Here is the HTML for our flash card.

```html
<div class="flash-card">
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

Refresh, and you'll see the flash card in all its plain glory! But this flash card is static and non-interactive;
Angular can make it dynamic!
