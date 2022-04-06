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
