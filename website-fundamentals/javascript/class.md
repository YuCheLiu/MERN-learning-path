# Class

```javascript
class ClassName {
  constructor() { ... }
  method_1() { ... }
  method_2() { ... }
  method_3() { ... }
}
```

### class keyword&#x20;

In JavaScript, Classes are template for creating object.

declare a class with curly brackets:

```javascript
class Name{
}
```

instance properties

```javascript
class School{
    constructor(name){
        this.name = name;
    }
}
```

sub classing using extends keyword

{% code title="Student Class" %}
```javascript
class Student extends School{
    constructor(studentName, SchoolName){
        this.studentName = studentName;
        this.SchoolName = SchoolName;
    }
}
```
{% endcode %}

Super class calls with super keyword

```javascript
class Student extends School{
    constructor(studentName, SchoolName){
        super(SchoolName); => call School also.
        this.studentName = studentName;
        this.SchoolName = SchoolName;
    }
}
```
