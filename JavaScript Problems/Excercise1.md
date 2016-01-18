## Scope

```js
(function() {
   var a = b = 5;
})();
 
console.log(b); // What will this output?
```

---

## Scope (Strict Mode)

```js
(function() {
   'use strict';
   var a = b = 5;
})();
 
console.log(b); // What will this output?
```

---

## Create “native” methods

Define a `repeatify` function on the `String` object. The function accepts an integer that specifies how many times the string has to be repeated. The function returns the string repeated the number of times specified. For example:

```js
console.log('hello'.repeatify(3));
```

---

## Hoisting

```js
function test() {
   console.log(a);
   console.log(foo());
    
   var a = 1;
   function foo() {
      return 2;
   }
}
 
test(); // What will this output?
```
---

## JavaScript Context (`this`)

```js
var fullname = 'John Doe';
var obj = {
   fullname: 'Colin Ihrig',
   prop: {
      fullname: 'Aurelio De Rosa',
      getFullname: function() {
         return this.fullname;
      }
   }
};
 
console.log(obj.prop.getFullname());
 
var test = obj.prop.getFullname;
 
console.log(test());
```

---

## JavaScript `call()` and `apply()`

Fix the previous question’s issue so that the last `console.log()` prints `Aurelio De Rosa`.