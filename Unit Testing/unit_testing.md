# JavaScript Testing

---

# Unit Testing

> Unit testing is the practice of testing specific areas or "units" of our code.

---

# Unit Testing Pros

- Helps to identify failures in your code. Especially helpful as our codebase grows.
- Forces you to write better code
- Prevents code from breaking in the future

---

# Unit Testing Cons

* Time Commitment

---

# How Do We Start Testing

* You could write a simple test suite!

---

```js
function it(description, contents){
  console.log('\n\n"It '+ description + '"');
  contents();
}

function expect(target) {
  return {
    toBe: function(expectation) {
      if (target === expectation) {
        console.log('\n     %cPASSED', 'color:green;', 'Expected', target, 'to be', expectation );
        return true;
      } else {
        console.log('\n     %cFAILED', 'color:red;', 'Expected', target, 'to be', expectation );
        return false;
      }
    }
  }
}
```

---

```js
it("should make Sadie happy when Mason pets her", function(){
  expect(sadie.status).toBe('normal');
  mason.pet(sadie);
  expect(sadie.status).toBe('happy');
});
```

---

# Testing Frameworks

* [QUnit](http://qunitjs.com/)
* [Jasmine](http://jasmine.github.io/)
* [Mocha](http://mochajs.org/)

---

# [Mocha](http://mochajs.org/)

> Mocha is a feature-rich JavaScript test framework running on node.js and the browser, making asynchronous testing simple and fun.

```js
$ npm install -g mocha
```

---

# [Chai](http://chaijs.com/)

> Chai is a BDD / TDD assertion library for node and the browser that can be delightfully paired with any javascript testing framework.

---

# TDD & BDD

> Test Driven Development <br>

> Behavior Driven Development <br>

> The idea of writing tests first, having them all fail (because of no code) then writing code to make the tests pass.

---


# Which Do We Use?

> In many cases, the choice between the two comes down to your testing framework. Since Mocha includes both, we are only going to focus on BDD.

---

> ASSERT, EXPECT & SHOULD()

---

# assert

> The way to assert that if somethings passes/fails. Also provides an optional message to display if the message fails.

```js
var cake = 'The cake is a liar.';
assert.typeOf(cake, 'string', 'cake is a string');
```

---

# expect

> Similar, except you chain together natural language assertions.

```js
var cake = 'The cake is a liar.';
expect(cake).to.be.a('string');
```

---

# should

> Very similar to `expect` but it allows you extend each object with should to start a chain.

```js
var cake = 'The cake is a liar.';
cake.should.be.a('string').with.length(19);
```

---

```js
describe('My String', function(){
  it('should be a string', function(){
    var my_string = "The cow jumped over the moon";
    expect(my_string).to.be.a('string');
  });

  it('should have a length of 28', function(){
    var my_string = "The cow jumped over the moon";
    expect(my_string).to.have.length.of(28);
  });
  
});
```

---

> Demos