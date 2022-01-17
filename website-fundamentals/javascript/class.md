# Class

```
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

```
class Name{
}
```

instance properties

```
class School{
    constructor(name){
        this.name = name;
    }
}
```

sub classing using extends keyword

{% code title="Student Class" %}
```
class Student extends School{
    constructor(studentName, SchoolName){
        this.studentName = studentName;
        this.SchoolName = SchoolName;
    }
}
```
{% endcode %}

Super class calls with super keyword

```
class Student extends School{
    constructor(studentName, SchoolName){
        super(SchoolName); => call School also.
        this.studentName = studentName;
        this.SchoolName = SchoolName;
    }
}
```
