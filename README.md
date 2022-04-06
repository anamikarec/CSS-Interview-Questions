# CSS-Interview-Questions
## Problems
1. How to add comments on css?
2. Why do we use pseudo-class?
3. How is specificity applied?
4. What method allows an element to be moved from its current position?
5. what properties does flex model have?
6. What is the difference between flex and grids?
7. Give an example where we have to use grids and where you have to use flexbox?
8. Give an example where you cannot use flexbox, and you can only use grids?
9. What are combinators? give examples of how you can use them
10. What does object-fit do?
11. What does rotate do?
12. What rule can be used to define animations
13. When working with attribute selectors, how can you select elements which contain a particular attribute value?
14. What does @media do?
15. What can be used to override properties of an element
16. How can you select every alternate elements in a list of elements using css?
17. What is the ranking of selectors with respect to specificity
18. how can we apply same styles to multiple selectors?
19. What are the differences between relative and absolute in CSS?


- ```Ans1```. To comment in CSS, simply place your plain text inside /* */ marks. This tells  the browser that they are notes and should not be rendered on the front end.
- ```Ans2.``` A pseudo-class is used to define a special state of an element.
   1. For example, it can be used to:
   2. Style an element when a user mouses over it.
   3. Style visited and unvisited links differently.
   4. Style an element when it gets focus.
   5. Pseudo-class names are not case-sensitive.
   6. Pseudo-classes can be combined with HTML classes.
   7. When you hover over the link in the example, it will change color:
```js
    selector:pseudo-class {
    property: value;
    }
    Like 
    /* mouse over link */
    a:hover {
    color: #FF00FF;
    }
    
    /* selected link */
    a:active ;
    color: #0000FF;
    }
```

- ```Ans3``` If there are two or more CSS rules that point to the same element, the selector with the highest specificity value will "win", and its style declaration will be applied to that HTML element. Think of specificity as a score/rank that determines which style declarations are ultimately applied to an element.
```js
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    .test {color: green;} 
    p{
    color: red;
    } 
    #ptag{
        color:yellow;
    }
    </style>
    </head>
    <body>
    <p class="test" id="ptag">Hello World!</p>

    </body>
    </html>
```

- ```Ans4:```The translate() method moves an element from its current position (according to the parameters given for the X-axis and the Y-axis).
```js
<!DOCTYPE html>
<html>
<head>
<style> 
div {
  width: 300px;
  height: 100px;
  background-color: yellow;
  border: 1px solid black;
  transform: translate(50px,100px);
}
</style>
</head>
<body>
<div>
This div element is moved 50 pixels to the right, and 100 pixels down from its current position.
</div>

</body>
</html>
```

- ```Ans5.``` The flex property is a shorthand property for:
- flex-grow
- flex-shrink
- flex-basis
- The flex property sets the flexible length on flexible items.
- Note: If the element is not a flexible item, the flex property has no effect.


- ```Ans6.``` Grid and flexbox. The basic difference between CSS Grid Layout and CSS Flexbox Layout is that flexbox was designed for layout in one dimension - either a row or a column. Grid was designed for two-dimensional layout - rows, and columns at the same time.
```js
<div class="wrapper">
  <div>One</div>
  <div>Two</div>
  <div>Three</div>
  <div>Four</div>
  <div>Five</div>
</div>

​​.wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
Flex Example :
.wrapper {
  width: 500px;
  display: flex;
  flex-wrap: wrap;
}
.wrapper > div {
  flex: 1 1 150px;
}
```


- ``` Ans7.``` If you are using flexbox and find yourself disabling some of the flexibility, you probably need to use CSS Grid Layout. An example would be if you are setting a percentage width on a flex item to make it line up with other items in a row above. In that case, a grid is likely to be a better choice.
- Use a grid when you already have the layout structure in mind, and flex when you just want everything to fit.


- ```Ans8.``` When we want to implement a 2d design by using the grid and lest us says we want 5 elements in 1 row and 10 elements in 2nd row and 1 elements in 3rd row.

- ```Ans9```. A combinator is something that explains the relationship between the selectors. A CSS selector can contain more than one simple selector.
```js
1.Descendant combinator
.box p {
    color: red;
}  
  
<div class="box"><p>Text in .box</p></div>
<p>Text not in .box</p>
```
```js  
ii) Child combinator
ul > li {
    border-top: 5px solid red;
}  
<ul>
    <li>Unordered item</li>
    <li>Unordered item
        <ol>
            <li>Item 1</li>
            <li>Item 2</li>
        </ol>
    </li>
</ul>
```
```js
iii)Adjacent sibling combinator
The adjacent sibling selector (+) is placed between two CSS selectors. It matches only those elements matched by the second selector that are the next sibling element of the first selector. For example, to select all <img> elements that are immediately preceded by a <p> element.
p + img
```
```js
iv)General sibling combinator
If you want to select siblings of an element even if they are not directly adjacent, then you can use the general sibling combinator (~). To select all <img> elements that come anywhere after <p> elements, we'd do this: p ~ img
```

- ```Ans19:~``` position: relative places an element relative to its current position without changing the layout around it, whereas position: absolute places an element relative to its parent's position and changing the layout around it.
