**# html-css-toboolist**

**v1** - Expanded on the exercise by making the lists collapsable with smooth transitions. 
- Thanks to the lesson on CSS selectors I was able to use the selector nth-of-type() to minimise repitition in the animation code.
- Tried to keep in mind intelligent class naming but can certainly be optimised further, will need to study and implement BEM.

**v2** - Implemented some changes based on Daniele Capano's fork.
- Switching to display: grid allows the animation of grid-template-rows, cleaner and more consistent than using the 100vh hack (originally I had opted to avoid using things not yet covered in our lessons but the previous solution had too many problems).
- Using specific selectors (label .list-title-arrow) instead of nth child allows the arrow to be placed back into the label. This allows for a better HTML structure and no longer requires the use of the position: relative trick to have the label include the arrow.
- Similarly, using a single repeated class (.collapsable) for the animated divs allows it to be selected directly (~ .collapsable) and makes for easier to write and read CSS.
- No need to repeat the transform line once the element is given it, although for the collapsable divs it was kept to allow different animation timings for opening and closing (when closing, the opacity would animate first, and vice versa when opening).
