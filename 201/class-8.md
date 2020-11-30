
# LAYOUT (HTML / CSS)

### Normal flow (Position: Static)
* (HTML)
``` 
<body>
    <h1>The Evolution of the Bicycle</h1>
    <p>In 1817 Baron von Drais invented a walking
        machine that would help him get around the
        royal gardens faster...</p> 
</body>

```
*(CSS)

```
body {
    width: 750px;
    font-family: Arial, Verdana, sans-serif; color: #665544;
}

h1 {
    background-color: #efefef; padding: 10px;
}

p{
    width: 450px;
}
```

In normal flow, each block-level element sits on top of the next one. Since this is the default way in which browsers treat HTML elements, you do not need a CSS property to indicate that elements should appear in normal flow, but the syntax would be:
`position: static;`

I have not specified a width property for the heading element, so you can see how it stretches the width of the entire browser window by default.

The paragraphs are restricted
to 450 pixels wide. This shows how the elements in normal flow start on a new line even if they do not take up the full width of the browser window.

### Relative Positioning (Position : relative)

* (HTML)
```
<body>
    <h1>The Evolution of the Bicycle</h1>
    <p>In 1817 Baron von Drais invented a walking
     machine that would help him get around the
    royal gardens faster...</p> 
</body>
```
* (CSS)
```
p.example { 
    position: relative; 
    top: 10px;
    left: 100px;
}
```
Relative positioning moves an element in relation to where it would have been in normal flow.

For example, you can move it 10 pixels lower than it would have been in normal flow or 20% to the right.

You can indicate that an element should be relatively positioned using the position property with a value of relative.

You then use the offset properties (top or bottom and left or right) to indicate how far to move the element from where it would have been in normal flow.

To move the box up or down, you can use either the top or bottom properties.

To move the box horizontally, you can use either the left or right properties.

The values of the box offset properties are usually given in pixels, percentages or ems.

