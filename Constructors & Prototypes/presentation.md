# Constructors & Prototypes

### This will be fun, I promise.

---

# First, `this`

Yep, literally the keyword `this`, let's talk about that.

> In JavaScript, `this` is a reference to a specific object. The value of `this` is determined by how a function is called and many times where it is used.

---

## `this` is a pronoun?

> Tim is an instructor at The Iron Yard, `he` really enjoys it.

---

## Constructors

> The constructor property is a reference to the function that created an object.

<br /><br />

```js
var Person = function () {

};
```

---
<br /><br />

```js
var Person = function (name, age, favorite_color) {
	this.name = name;
	this.age = age;
	this.favorite_color = favorite_color;
};
```

---

## Instances with `new`

> The `new` operator creates an instance of a user-defined object type  or of one of the built-in object types that has a constructor function.

<br /><br />

```js
var me = new Person('Tim', 30, 'Orange');
```

---
<br />

```js
var Person = function (name, age, favorite_color) {
	this.name = name;
	this.age = age;
	this.favorite_color = favorite_color;
};
```
<br />

```js
var me = new Person('Tim', 30, 'Orange');
```

---

## Demos

---

## Prototypes

(Not to be confused with [Prototype](http://prototypejs.org/) the JS Library)

> Prototypes allow you to easily define methods to all instances of a particular object.

<br />

> The beauty is that the method is applied to the prototype, so it is only stored in the memory once, but every instance of the object has access to it

---

## Prototypes

```js
Person.prototype.greeting = function () {
	console.log('Hi, ' + 'my name is ' + this.name );
};
```

---

## Demos
