# HTML, CSS, DOM, Node Server, Express

## HTML (Hyper Text Markup Language)
HTML uses tags to markup text for the web. A basic HTML file is below.
```
<html>
<head></head>
<body>
  <h1>Hello Word</h1>
  <ul id="todo-list">
    <li class="task">Groceries</li>
    <li class="task">Laundry</li>
  </ul>
</body>
</html>
```
`html`, `head`, and `body` tags are required in every HTML document. The `head` tag is not seen by the user and contains things like information for search engines and links to external files (e.g. CSS or JS). The `body` tag contains everything on a page that a user sees.

Learn more about HTML on [MDN (Mozilla Developer Network)](https://developer.mozilla.org/en-US/docs/Web/HTML).

## CSS (Cascading Style Sheets)
CSS uses selectors (tags, classes, and IDs being the most commong) to identify HTML elements and style them. The below CSS will style the above HTML.
```
/* tag selector */
h1 {
  color: blue;
}
/* class selector */
.task {
  font-size: 24px;
}
/* ID selector
#todo-list {
  background-color: red;
}
```
CSS contains many other kinds of selectors, which you can see [here on MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

Since using CSS to style a page can be so complex and be a project in and of itself, it is recommend to use a CSS framework, like [Bootstrap](http://getbootstrap.com/getting-started/) or [Foundation](http://foundation.zurb.com/sites/docs/) to do most of the styling for you.

## DOM (Document Object Model)
The DOM is a standardized convention for interacting with an HTML page and can be accessed with any programming language, though it is most often accessed through client side JavaScript.

This example is shamelessly stolen from [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction).

```
<script>
  // using built in DOM methods
  window.onload = function() {
    // create a couple of elements in an otherwise empty HTML page
    var heading = document.createElement("h1");
    var headingText = document.createTextNode("Big Head!");
    heading.appendChild(headingText);
    document.body.appendChild(heading);
  }
  // using jQuery
  $(document).ready(function () {
    var heading = $('<h1/>');
    var headingText = 'Big Head!';
    heading.text(headingText);
    $('body').append(heading);
  })
</script>
```

Using the built in DOM methods can be a bit verbose, which is why most people prefer to use jQuery or some other client side framework to interact with the DOM.

## Node Server
Node has a built in HTTP library, which allows us to a create a simple server.
```
var http = require('http');

// create a server and give it a function to use
// to respond to requests
var server = http.createServer(function (request, response) {
    console.log(request.method + ' request for "' + request.url + '"');
    response.end("Hello world!");
});
```
The above example shows how easy it is to get a server started with Node. But the standard HTTP library is not easy to use if you want to do more complex things. This is where Express comes in.

## Express
Express is a web application and server framework built for Node. Express allows to specify particular HTTP methods for particular routes.

Here is a simple GET request to the root URL `/` that renders the `index.jade` file using Jade Templating.
```
app.set('view engine', 'jade');

app.get('/', function(request, response) {
  response.render('index');
});
```

Here is a slightly more complex GET request to `/todo`. That finds all the tasks of app and returns them in either JSON or HTML.
```
app.get('/todo', function(req, res) {
  Task.findAll().then(function(todos) {
    res.format({
      'text/html': function() {
        if (!todos) {
          res.end('No todos');
        } else {
          res.end('All known todos: ' +
            todos.map(function(t) { return t.title; }));
        }
      },
      'application/json': function() {
          res.json(todos);
      }
    });
  });
});
```

See the [docs on expressjs.com](http://expressjs.com/)
