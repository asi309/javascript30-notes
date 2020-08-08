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

