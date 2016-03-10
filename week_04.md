# Templates, Jade

## Templates
Templates are like Mad Libs. It's pre-created and can be used over and over again. Templates don't only exist in code but everywhere. You may have a template email for people who won't stop spamming you. Or  you might have a spreadsheet set up for taxes you copy every year. In web programming, a template refers to an HTML page, or piece of an HTML page, where variables get filled in when the template gets rendered.

## Jade
Jade is a specific templating language that also offers a shorthand syntax for HTML. The below Jade code will render the same HTML we saw in [Week 2](week_02.md)
```
//- in Jade
html
  head
  body
    h1 Hello World
    ul#todo-list
      li.task Groceries
      li.task Laundry

<!-- in HTML -->
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

Jade also offers the ability use a layout with your templates. A layout is typically code that is on every page, and allows you the ability to not have to retype it everywhere. For example, most websites have a menu on every page, and that menu could go in the layout.

```
//- layout.jade
html
  head
    include ./includes/bootstrap.jade
    script(src="/browser-bundle.js")
    block title
      title Hello #{username}!

  body(ng-app="myApp")
    .container
      .well
        block body

//- index.jade
extends ./layout.jade

block body
  h1 Hello #{username}!

  p
    | This is coming from the
    code index.jade
    | file
```
Here the index file extends the `layout.jade` file. Everything under the `block body` in the `index.jade` will replace the `block body` in the `layout.jade` file.

The above code also demonstrates how to insert data into your HTML file. When you tell Express to render a Jade file, you can give it a data argument, and Jade will use this data when rendering HTML.
```
// inside an Express route
response.render('index', { username: 'Alice' });

//- in Jade
h1 Hello #{username}!

<!-- rendered in HTML -->
<h1>Hello Alice!</h1>
```

Try the [interactive Jade tutorial here](http://naltatis.github.io/jade-syntax-docs/).

Or read the [Jade docs here](http://jade-lang.com/)
