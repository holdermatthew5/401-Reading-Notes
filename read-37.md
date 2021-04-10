# React I

It looks like html is rendered by just passing in the "html" (it's actually still JS) as an argument to a method on the ReactDOM object called render along with the element you wish to append it to.

Since the rendered html is only sent by the repo and the browser actually does the work of rendering it you can't just change an html element after it's rendered and hope for it to change on screen as well. That element has to be recreated from scratch and rerendered all over again (feels a bit tedious).

A component seems to be a class that pulls from React.component. It seems they're intended to create a global html template that can be used in any function, but I feel like we'd be able to do that with mustache too. They don't have to return html they can run normal JS operations as well because they are actually JS.

The html can use template literals by passing a "prop" into the function that creates the element and using it as intended in curly braces. The curly braces seem to be able to replace quotes in attributes. Thes functions are used by assigning them to the element variable as an html tag (`<funcName argument="value" />` where 'funcName' is the component that returns the desired html, 'argument' is a child of the props object, and value is the value to be used in the html being rendered).

It says React apps generally have one App compnent near the top and that they use data from other components which makes me wonder if these apps often get a stack overflow error (assuming a stack overflow error is actually just calling too many functions before completing any).

## Tailwind-CSS

Tailwind-CSS looks like it's just a massive CSS file with presets that we can use by adding the name of the preset to the class attribute. This could be cool for simplicity, but takes away a bit of creativity (so far just that I can't create my own color I have to choose one of theirs instead, but I'm expecting more). This could be kinda cool to use in React tho if we want to make it change regularly or dynamically change colors after certain events or with certain values found.

If I have to add tailwind as a dependency that could also weigh down the app if it is really just a giant CSS file with presets.

It sounds like purge CSS gets rid of any unnecessary classes (styling that isn't changing anything).

## Next.js

I wish I'd've seen this walk-through yesterday. This probably would've made it alot easier to get started (assuming it showed me how to get around that npx command error).