# CS568 - Assignment 1 - ES6
- Create arrow functions with zero, one, multiple parameters. Return values with/without curly brackets.
- Practice call/bind/apply. Borrow and carry a function.
- Implement a child class and super class. NodeJS is the fastest way to execute your code. Refer the following code. You just need package.json.

*package.json*
```
{
  "name": "lesson-1",
  "version": "1.0.0",
  "type": "module"
}
```
*Person.js*
```
class Person {
  constructor(age){
    this.age = age;
  }
  sayYourAge = () => 'My age is ' + this.age;
}
export default Person;
```
*Student.js*
```
import Person from './person.js';
class Student extends Person {
 constructor(name) {
   super(17);
   this.name = name;
 }
 sayHi = () => `Hi. I am ${this.name} and ${this.age} years old`;
}
export default Student;
```

*App.js*
```
import Student from './student.js';
import {minutesInHour} from './helper.js';
import {sayHi} from './helper.js';

const student1 = new Student('Bob');
console.log(student1.sayHi());
console.log(student1.sayYourAge());
console.log(sayHi());
console.log(minutesInHour);
```

- Practice destructuring.
```
function sayHi({name}) ...

const obj = {
  name: 'name',
  age: 'age'
}

sayHi(obj);
```
- Practice spread operator.
- Practice splice, slice, map, find, findIndex, filter array methods. Write code that finds an element in an array then removes it by its index.
