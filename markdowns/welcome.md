# Intro

In this tutorial we develop from scratch React-like framework in Vanilla JS. We will use virtual-dom concept for building UI and update data. If you are React developer or just starting with React - it is great opportunity to learn how things works under the hood.

By the end of this text, you will have your own framework built on React fundamentals.

# Project structure

For this tutorial I will use my own project starter. It's very basic starter based on webpack/babel with unit tests. No heavy code :) https://github.com/asmyk/webpack-es6-starter - You can use your own starter as you like.

# First step

Let's look for app structure:

```html
<html>

<body>
    <div id="rootElement"> </div>
</body>

</html>
```

```javascript
   let rootEl = document.getElementById("rootElement"); // get dom element 

   let header = FireDOM.createElement("div", {}, "This is header!"); // create vdom component
   let content = FireDOM.createElement("div", {}, "This is content!"); // create vdom component
   let app = FireDOM.createElement("div", {}, header, content) // render div and place header and content components inside

   FireDOM.render(rootEl, app); // mount app component to the dom node
```

In next page we will implement create elements and render to make this sample works. 