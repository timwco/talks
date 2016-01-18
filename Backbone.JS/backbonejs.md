
![inline](assets/backbone-js.gif)

---

## Backbone.JS

> Backbone.js gives structure to web applications by providing models with key-value binding and custom events, collections with a rich API of enumerable functions, views with declarative event handling, and connects it all to your existing API over a RESTful JSON interface.

---

## Backbone.JS Parts

* Models
* Views
* Collections
* Routes

---

The cool thing about Backbone as opposed to other MVC(ish) Frameworks is that all of these parts are independent. They don't require each other to work and you are free to choose when and if you pick any of them.

---

## Backbone.JS Models

> Basically a Backbone Model is a constructor that determines the shape that your data will be.<br><br>

> Backbone.Model is basically just a plain old constructor. It does have one fancy method though. In fact all of the parts of Backbone do. It's the `extend` method.

---

## Backbone.JS Extend Method

> In Backbone's world, `extend` means "take this object literal, use it's properties and methods and overwrite any conflicting properties". Its cool because you end up with your own customized version of Backbone.Model.

---

```js
var TimsCoolModel = Backbone.Model.extend ({

  initialize: function () {
    console.log("Look Ma! I'm doing programming!!");
  }

});
```

---

## NOOP

> An empty function<br><br>

> A noop is a function that doesn't do anything and has no return value (other than default `undefined`).<br><br>

> Why have these? Well they are there for us to fill in as we need to.<br><br>

---

## BackboneJS Model Instance

```js
var coolInstance = new TimsCoolModel({
  name: "Fido",
  type: "Dog",
  cool: true
});
```

---

## How Do We Access Properties?

get: `model.get();`

set: `model.set();`

---

## BackboneJS Collections

> They are a pretty simple mechanism. Collections are meant to store an array of model instances and also house methods that are useful for working with a group of models.

---

```js
var TimsCoolCollection = Backbone.Collection.extend ({

  model: TimsCoolModel,
  url: 'http://my-api-url-endpoint'

});
```

---


> Demos

---

## BackboneJS Views

> Used to reflect what your application data models look like.

---

> Think of Backbone Views as a Trapper Keeper® for what would otherwise be a garbled mess of jQuery events.

---

```js
var PersonView = Backbone.View.extend({

  el: $('.hero-unit'),

  template: function(model){ return 'Hello Jack!'; },

  initialize: function () { this.render(); },

  render: function () { this.$el.html(this.template);}

});
```

---

> Demos

---

## BackboneJS Router

> Provides methods for routing client-side pages, and connecting them to actions and events. For browsers which don't yet support the History API, the Router handles graceful fallback and transparent translation to the fragment version of the URL.

---

> Client Side vs Server Side 

---

## So BackboneJS Routers?

* Allows you to navigate through the app with out page load
* Allows you to create bookmarkable links in a SPA

---

## When do we need one?

* Large view change
* Need for bookmarkable link

---

```js
 var PostRouter = Backbone.Router.extend({
  initialize: function () {
    Backbone.history.start();
  },
  routes: {
    "posts/:id": "getPost"
  },
  getPost: function (id) {
    alert("Loading Post " + id);
  }
});

// Create an Instance
var post_router = new PostRouter();
```

---

> Demos

