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


#### Object Constructors

*Object Constructors* are functions that can be called to create new Objects.

For example,
<pre>
  <code>
    var createObj = function(firstName, age, nationality) {
        this.firstName = firstName,
        this.age = age,
        this.nationality = nationality
    }
  </code>
</pre>

Calling the function createObj with the necessary parameters will create a new Object. The constructor returns the created object, therefore, it can be assigned
to a variable for use.


#### The Prototype

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

If, however, we use *object constructors* to create objects, the prototype for this object will have a *constructor* property that will have value equal to the constructor function used to create the object.

Example of prototype usage:
<pre>
  <code>
    var Student = function (name, grade) {
        this.name = name,
        this.grade = grade
    }
    Student.prototype.sayName = function () {
        console.log(this.name);
    }
  </code>
</pre>

**Protoype Inheritance** can be done using many methods, like defining the <code>__proto__</code> property of the object while creating.
However, at this point, the proper way of using *prototype inheritance* is by using <code>Object.create</code> to assign a copy of the parent prototype to the
prototype of the child object.
For example,
<pre>
  <code>
    var student = function (name) {
        this.name = name
    }
    student.prototype.getName = function () {
        console.log(this.name);
    }
    var midSchoolStudent = function (name, grade) {
        this.name = name;
        this.grade = grade;
    }
    midSchoolStudent.prototype = Object.create(student.prototype);
    
    var s1 = new midSchoolStudent('qwerty', 7);
    s1.getName(); //logs qwerty
  </code>
</pre>

**Note**: Always use <code>Object.create</code> while chaining prototype for inheritance, otherwise, it will directly assign the prototype of the parent object and not a copy of it. This can lead to unpredicted behaviour.
For example,using the above example to demonstrate:
<pre>
  <code>
    var student = function (name) {
        this.name = name
    }
    student.prototype.getName = function () {
        console.log(this.name);
    }
    var midSchoolStudent = function (name, grade) {
        this.name = name;
        this.grade = grade;
    }
    midSchoolStudent.prototype = student.prototype; //Never ever do this!
    
    var highSchoolStudent = function (name, grade) {
        this.name = name;
        this.grade = grade;
    }
    highSchoolStudent.prototype = student.prototype
    highSchoolStudent.prototype.getName = function () {
        console.log("NOPE! I don't think so");
    }
    
    var s1 = new midSchoolStudent('qwerty', 8);
    s1.getName(); //logs "NOPE! I don't think so" since the getName function got edited using the highSchoolStudent prototype
  </code>
</pre>
