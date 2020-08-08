### Lesson 1:

**data-xyz**: The *data-* attribute is used to add custom data to your HTML page. This helps to create the custom attributes in tags that you can manipulate and use accordingly.

**audio**: The audio tag helps to play audio using the *play()* function.

**selectors**: Selectors of type *tag-name[attribute=attr-value]* (tag-name can be replaced with id or classname) can help select the proper html element where the provided attribute matches the attribute value.

**querySelectorAll**: Selects all the elements that matches the query provided as argument. Returns a *nodeList*. **Not Array**


### Lesson 2:

**transform-origin**: Specifies the point from which any transformation such as rotation begins. In case of rotation, the origin specified becomes the axis of rotation. By default this property is at *50%* or the middle. *0%* would signify the left-most position of the element and *100%* would be the right-most.

**transform-timing-function**: Can be specified using keywords (ease-in, ease-out, etc) and also *bezier curves*. Bezier curves are represented by *4* points. Starting at 0 and ending at 1, the middle points are at *x=0.25* and *x=0.75* and the values to be provided are the y-values at those x-values. This represents the speed of transition over 4 control points.

**Date**: Date function can be used to get the current date.
  *getSeconds* will provide the seconds from the date object. Similarly, for minutes and hours.
  To describe this in a clock, describe each time-unit as a fraction of *360deg*.
  (For our purposes, we add the "degrees as a fraction of *360deg*" to 90, since we initially rotated our div by 90 to get to '*12o' clock*' position.)


### Lesson 3:
##### Array using JS:

**sort**: sort is a prototype function available on arrays. Sort takes a compare function as its argument that 
 *returns 1* if *sorting is not required*,
 *returns -1* if *sorting is required*,
 *returns 0* if *both the values are equal*

Sort returns a copy of the array on which it is called sorted according to the *compare function. *

[Array.prototype.sort - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)
 
**reduce**: reduce is a prototype function that helps in looping over an array and cumulate the elements of an array according to any particular operation. It takes a callback function with *2 arguments*, (value upto this point, current value) where the value upto this point is the cumulative value of the array upto but **not including** the present array value. *Current value* is the present value that has to be cumulated using any operation.

Reduce returns the cumulative value from the array on which it is called.

[Array.prototype.reduce - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)

**filter**: filter is a prototype function that takes a callback function as its argument. The callback function gives the *filtering condition*, returning boolean only.

Filter returns an array that has only the elements that evaluated to *true* using the callback function.

[Array.prototype.filter - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

**map**: map is a prototype function in arrays that take a callback function as its argument. The callback function performs certain operations on each element of the array and returns the processed elements.

Map returns a copy of the array on which it was called with transformations applied to *each element*.

[Array.prototype.map - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

**some**: some is a prototype function that takes a callback function which consists of a conditional to return either *true* or *false*. If any of the element passes the conditional in the callback function, return value of some will be *true* else *false*.
Used to check if any element exists that fulfills the requirements. Can be chained with other prototype methods to be useful.

[Array.prototype.some - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)

**every**: Similar to __*Array.prototype.some*__ except *every* element of array must fulfill conditional in callback function for this function to return *true* else it returns *false*.

[Array.prototype.every - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)

**find**: find is a prototype function that takes a callback function as its argument containing a conditional for finding any element satisfying the conditions. It returns the first element in the array that returns *truthy* from the callback function.

[Array.prototype.find - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find)

**findIndex**: It is a prototype function similar to __*Array.prototype.find*__. The only difference is that this function returns the *index* of the first element satisfying the conditionals in the *callback function*.

[Array.prototype.findIndex](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex)
