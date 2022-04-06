# CSS-Interview-Questions
## Problems
1. How to add comments on css?
2. Why do we use pseudo-class?
2. Ans. A pseudo-class is used to define a special state of an element.
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
