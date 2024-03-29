# Working with Live Data

---

## HTTP RESPONSE CODES

* 200 OK
* 301 Moved Permanently
* 400 Bad Request
* 401 Unauthorized
* 403 Forbidden
* 404 Not Found
* 500 Internal Server Error
* 503 Service Unavailable
* 550 Permission denied


---

## AJAX

### Asynchronous JavaScript and XML

#### Processes a web request immediately without leaving the current page

---

## $.ajax()

### Perform an asynchronous HTTP (Ajax) request. <br><br><br>

```javascript
$.ajax({
  url: 'https://api.github.com/users/twhitacre',
  dataType: 'json'
});
```

---

## $.getJSON()

### Get JSON-encoded data using a GET HTTP request. <br><br><br>

```javascript
$.getJSON( 'https://api.github.com/users/twhitacre' );
```

---

## .then()

### Handlers called when the Deferred object is resolved. <br><br><br>

```javascript
$.getJSON( 'https://api.github.com/users/twhitacre' ).then( 
  function (res) {
    console.log(res);
  },
  function (error) {
    console.log(error);
  }
);
```














