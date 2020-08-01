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
