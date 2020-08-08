## Javascript Concepts


#### Javascript Objects

*Objects* are used to store and access different types of data in a <code>key: value</code> pair, where *key* is a unique identifier for the value.
The values can be accessed using the object and the specific key.

For example,
<pre>
  <code>
    var obj = {
        firstName: 'user',
        age: 22,
        nationality: 'Indian'
    }
  </code>
</pre>

*(Not to be confused with JSON)*
*JSON* will always have <code>"key": "value"</code> pairs within double-quotes. Whereas, JS Objects can have keys with/without quotes and single/double quotes both
apply.


###### Object Constructors

*Object Constructors* are functions that can be called to create new Objects.

For example,
<pre>
  <code>
    var createObj = function(firstName, age, nationality) {
        this.firstName = firstName,
        this.age = age,
        this.nationality = nationality
    }
</pre>

Calling the function createObj with the necessary parameters will create a new Object. The constructor returns the created object, therefore, it can be assigned
to a variable for use.


###### The Prototype

*Prototype* is an object that the created object is inherited from. 

In other words, every JS Object is inherited from some prototype objects. Thus, the created object has access to **methods** and **properties** of the prototype.
Examples of prototypes: Array prototype, Object prototype

For example, 
<pre>
  <code>
    var obj = new Object();
  </code>
</pre>

(OR)

<pre>
  <code>
    var obj = {};
  </code>
</pre>
Both times, the variable *obj* will have prototype as *Object* which is the class every Object is inherited from.
Similarly, arrays created with <code>var arr = new Array()</code> (or) <code>var arr = []</code> will have prototype *Array*
