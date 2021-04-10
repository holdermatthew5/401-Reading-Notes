# React II

React has conditionally rendered content. Adding conditional and after the variable expression to be evaluated will enact this behavior. The content that comes after conditional and will render if the expression evaluates to truthy. This conditional block is contained with curly braces and used where needed as regular react html.

```
<div>
    {greet && <h1>Sah duh</h1>}
</div>
```

There is an if/else form of the conditional block as well refered to as in-line conditional. In a b tag we open curlies write our evaluated statement a question mark and the content to be rendered if truthy next to the content to be rendered if falsey seperated by a colon.

```
<div>
    The user is <b>{isLoggedIn ? 'currently' : 'not'}</b> logged in.
</div>
```

A list can be converted to a list of li tags by iterating through the list and adding each value to the new list contained within the li tags curlies. Placing this new list in a ul tag will render a bulleted list of the values in the list.
