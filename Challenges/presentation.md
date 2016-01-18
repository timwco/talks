# Code Challenge

---

#### Quiz 1

## FizzBuzz

> Write a program that prints the numbers from 1 to 100. But for multiples of three print “Fizz” instead of the number and for the multiples of five print “Buzz”. For numbers which are multiples of both three and five print “FizzBuzz”.


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

#### Quiz 3

## Constructors & Prototypes

> Take the `challenges.js` file, copy it into your `main.js` file and make sure all of the `console.assert()`'s pass.
