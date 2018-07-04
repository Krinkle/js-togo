# 07: Inheritance

This exercise is about understanding how object inheritance works in JavaScript.

When you try to access a property on an object, if there is no property for that
name, then JavaScript will automatically look at a different object, to see
if the property exists there. This other object is called the "prototype".

An object can only have one prototype, and when you create an object, you
can decide which prototype object to use. The simplest way to do this
is by using the built-in `Object.create` utility.

Consider the following examples:

```js
// Create a plain object.
var foo = {};
foo.a = 12;

// Create a plain object, with 'foo' referenced as its prototype.
var bar = Object.create(foo);
bar.b = 'Hello';

console.log(bar.b); // "Hello"
console.log(bar.a); // 12 -- This value comes directly from `foo`
```

Recreate the above example and try the following:

* Add a line of code that reads `foo.b` and logs its value.
  It should say `undefined`.
* Add code that changes `foo.a` and then log the value of `bar.a`.
  It should say the current value as in `foo`.
* Add code that creates another property in `foo`, for example `foo.c = 1;`.
  Access it from `bar` by logging the result of `bar.c`.
  This newly added property is also visible through `bar`.

At no point does JavaScript "update" values from the prototype.
Instead, every time you access a value, it will first check for
properties on the object directly. Then, if no property is found,
it will check if the object has a prototype. If there is one, it
looks for the property there. This all happens in real-time.

This cycle can repeat within the prototype object as well.
This means you can create a chain of linked objects.

```js
var base = {
	firstName: '',
	greeting: function () {
		console.log('Hello ' + this.firstName);
	}
};
```

Re-create the following example. Then extend the program to also
create two derivative objects of `base`. One for "Alice" and one
for "Bob".

At the end, a call to `console.log(alice.greeting());` and
`console.log(bob.greeting())` should produce the following:

```js
Hello Alice
Hello Bob
```
