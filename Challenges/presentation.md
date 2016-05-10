# Code Challenge

---

#### Quiz 1

## FizzBuzz

> Write a program that prints the numbers from 1 to 100. 

> But for multiples of three print “Fizz” instead of the number and for the multiples of five print “Buzz”. 

> For numbers which are multiples of both three and five print “FizzBuzz”.


---

#### Answers

```
for (var i=1; i <= 100; i++) {
  if (i % 15 === 0){
    console.log('FizzBuzz');
  } else if (i % 3 === 0) {
    console.log('Fizz');
  } else if (i % 5 === 0) {
    console.log('Buzz');
  } else {
    console.log(i);
  }
}
```

#### Resources

- [Solutions](https://gist.github.com/jaysonrowe/1592432)
- [Arithmetic Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators)

---

#### Quiz 2

## Form Builder

> Take the following `array` and write a small form builder that will create a registration form. 

```
[
  { type: 'text', label: 'Name' },
  { type: 'email', label: 'Email' },
  { type: 'password', label: 'Password' },
  { type: 'submit', label: 'Register' }
]
```

---
## Hoisting Quiz

#### Think Closures, Scope & Global Namespaces

1. Write down the output
2. Write down "why" that output came out


---

```
var myvar = 'my value';

(function() {
  console.log(myvar);
  var myvar = 'local value';
})();

```

---

```
var flag = true;

function test() {
  if (flag) {
    var flag = false;
    console.log('Switch flag from true to false');
  } else {
    flag = true;
    console.log('Switch flag from false to true');
  }
}
test();

```

---

```
var message = 'Hello world';

function saySomething() {
  console.log(message);
  var message = 'Foo bar';
}
saySomething();

```

---

```
var message = 'Hello world';

function saySomething() {
  console.log(message);
  message = 'Foo bar';
}
saySomething();

```

---

```
function test() {
  console.log(a);
  console.log(foo());

  var a = 1;

  function foo() {
    return 2;
  }
}

test();

```

---

```
(function() {
  console.log(bar);
  foo();

  function foo() {
    console.log('aloha');
  }

  var bar = 1;
  baz = 2;
})();

```

---
```
var run = false;

function fancy(arg1, arg2) {
  if (run) {
    console.log('I can run');
  } else {
    console.log('I can\'t run');
  }

  function run() {
    console.log('Will I run?');
  }
}
fancy();

```

---

```
var run = false;

function fancy(arg1, arg2) {
  if (run) {
    console.log('I can run');
  } else {
    console.log('I can\'t run');
  }

  var run = function() {
    console.log('Will I run?');
  }
}
fancy();
```