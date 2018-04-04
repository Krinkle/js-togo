# 06: Objects

This exercise is about the difference between primitive values
and object values.

* **primitive**: Any data that is not an object, including the types `string`, `number`, `boolean`, `null`, and `undefined`. Primitives are immutable. That means their value cannot be changed. When a transformation is applied to a primitive, a new value is created each time
(e.g. through math, through casting, or through concatenation).
* **object**: All values that are not primitive. This includes arrays and functions. An object is a collection that can hold data and/or functionality. The values associated with an object are stored in a property. Each property has a name and a value. The simplest way to create an object is using the "object literal" syntax, which consists of curly braces.

Consider the following examples:

```js
var a = 123;
var b = a;
a = a + 777;
a; // 900
b; // 123

var x = 'Hello';
var y = 'World';
var z = x + ' ' + y;
z; // "Hello World"
x; // "Hello"
y; // "World"
```

```js
var person = {
	firstName: 'Mira',
	lastName: 'Meadows',

	age: 10,

	interests: ['music', 'running'],

	addInterest: function (topic) {
		this.interests.push(topic);
	}
};

person.firstName; // "Mira"
person.interests[0]; // "music"
person.interests.length; // 2
person.age; // 10

person.addInterest('technology');
person.interests.length; // 3
person.interests[2]; // "technology"
```

Write a program that will create two objects that describe
different persons. Store these objects in an array.

Then iterate through the array and call a method "birthday" on
each of the persons. Log their full name and age both before
and after the "birthday" call.

Expected outcome:

<pre>
06-objects/$ node main.js
Mira Meadows (age 11)
Mira Meadows (age 12)
Ricky Rogers (age 7)
Ricky Rogers (age 8)
</pre>

Bonus:
* Wish them a happy birthday.
* Show their previous and current age on the same line.

<pre>
06-objects/$ node main.js

Mira Meadows (age 11 => 12)
Mira, Happy Birthday!

Ricky Rogers (age 7 => 8)
Ricky, Happy Birthday!
</pre>
