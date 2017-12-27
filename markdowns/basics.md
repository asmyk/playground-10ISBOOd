# Before we start
I mentoined eailer about virtual dom. Ok, so what is virtual dom? You can think about Virtual DOM like an DOM representation, but expressed in JS Object notation form. See at example below:

```javascript
{
    tag: "div",
    props: {"className": "text-center", "id": "my-text"},
    children: "Welcome to the jungle!"
}
```

This is an Virtual DOM representation for following HTML:

```HTML
<div class="text-center" id="my-text">
    Welcome to the jungle!
</div>
```

Ok, what when we would like to create nested objects hierarchy? Look at this:

```javascript
{
    tag: "div",
    props: {"className": "text-center", "id": "my-text"},
    children: [{
        tag: "div",
        props: {"className": "title",},
        children: "I'm header"
    },{
        tag: "span",
        props: {"className": "subtitle",},
        children: "with fancy subheader"
    }]
}
```

Our framework should generate something like this:

```HTML
<div class="text-center" id="my-text">
    <div class="title">
        I'm header
    </div>
    <span class="subtitle">
        with fancy subheader
    </span>
</div>
```

# Create element

TECHIO> open --port 8080 /code/basics/index.html

# Attributes?

# Component's childrens

# Render