build-lists: true

## AngularJS Workshop

Tim Whitacre - The Iron Yard

bit.ly/ng-ws

### Wifi

Network: Student
User: apollosrc\uop-ga-dunwoody
Pass: internet

---

![inline](assets/angular-js.png)


---

![inline](assets/learning.png)

---

## What is AngularJS?

AngularJS is a JavaScript framework that lets you build well structured, easily testable, and maintainable front-end applications.

---

## History & Future

- Originally created in 2010 by Misko Hevery and Adam Abrons, now run by the Google team.
- Everything should be a component - see Angular v2.0

---

## Two Parts to Angular

1. UI - Declarative - What happens in the HTML.
2. App - Imperative - What happens in the JavaScript.

---

## Wait... wat?

What do you mean, "what happens in the HTML"? Isn't this a JavaScript framework?

---

## Why use AngularJS?

* Helps with organization of JavaScript
* Works well with other libraries (but requires none of them)
* Ability to create extremely fast websites
* It is easy to write tests for - _because of modules_

---

## Also Community

![inline](assets/graph.gif)

---

## MVC

Um... so is AngularJS an MVC?

---

## Model

The model is made up of plain JS objects. No need for inheriting or extending. We also don't need to use any special getter/setter methods to access it. This means that we write less boilerplate code.

---

## ViewModel

It is an object that provides specific data and methods to a specific view. `$scope` is just a regular JS object with a small API created to detect changes to its state.

---

## Controller

The controller is used for setting initial state and mutating the `$scope` with methods.

---

## View

The view is the HTML that exists after AngularJS has parsed and compiled the HTML to included rendered markup and bindings.

---

## Module

> A method that instantiates and wires together the different parts of the application.

```js
angular.module('app', []);
```

---

## Module Setter

```js
angular.module('app', []);
```

---

## Module Getter

```js
angular.module('app');
```

---

## `$scope`

- This is our "Imperative" part
- The `$scope` is a reference to your data. The controller defines the behavior and the view handles the layout.

--- 

## Directives

- This is our "Declaritive" part
- A directive is a marker on a HTML tag that tells AngularJS to run or reference some JS code.

- `ng-repeat`
- `ng-click`
- `ng-show`
- `ng-class`

---

## TWO-WAY DATA BINDING

> AKdf AngularJS

![inline](assets/2way.png)

---
<br><br><br><br><br><br><br><br><br><br><br><br>
### [fit] ... yeah, but is two-way data binding good?

---

## Let's Build!
