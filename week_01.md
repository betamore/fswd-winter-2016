# Requests and Responses, JS concepts, Tests, Git

## Requests and Responses

Request - A message sent from a client (typically a browser) to a server (typically a remote computer). Common requests include a URL and GET or POST as methods.

  * GET - This request happens whenever you type a URL into a browser and hit go.
  * POST - This request usually happens whenever you submit a form.

Response - A message sent after a request from a server to a client. This includes a status code and the page contents. Status codes let the client know what happened with the request. Common codes are

  * 200 - This tells the client that everything is okay.
  * 301 - This tells the client to redirect to another page.
  * 404 - This tells the client that they did something wrong.
  * 503 - This tells the client that the server did something wrong.
  
For more detailed information on requests and responses, take a look at the [requests spec](https://www.w3.org/Protocols/rfc2616/rfc2616-sec5.html) and the [responses spec](https://www.w3.org/Protocols/rfc2616/rfc2616-sec6.html)

And to explore responses more, play with [curl](https://en.wikipedia.org/wiki/CURL#Examples_of_cURL_use_from_command_line) on the command line
  
## JS Concepts

  var (variables) - This is used to declare a variable for storing information. You can store anything at all: Numbers, Strings, Objects, Functions, etc.

    var person = {name: 'Bob', age: 21};
    var total = 2107;
    var location = 'Betamore';
    var sayHi = function () { console.log('Hi'); };
  
  if / else (conditionals) - These are used to check for certain conditions and respond accordingly.
  
    if (isRaining) {
      useUmbrella();
    } else if (isTooHot) {
      wearSunscreen();
    } else {
      jog();
    }
  
  function - This is used to create functions so you don't have to repeat the same code everywhere.
  
    function add(x, y) {
      return x + y;
    }
    
    add(2, 3);
  
  for (loops) - A loop is used to iterate through a collection of items and repeat the same code on the entire collection.
  
    var letters = ['a', 'b', ..., 'y', 'z'];
    for (var i = 0; i < letters.length; i += 1) {
      console.log(letters[i]);
    }
  
  For more information on JS basics, see [MDN's crash course](https://developer.mozilla.org/en-US/Learn/Getting_started_with_the_web/JavaScript_basics#Language_basics_crash_course)
  
## Tests

  If you don't write tests, you'll have to test all your code yourself, which gets annoying eventually. Writing tests also allows you to create large codebases without worrying about the smaller pieces. In general, each test should be focused on one particular part of your code and your tests as a whole should cover an expansive number of test cases.

## git (Version Control)

  `git` is a command line tool used for version control. Version control can be thought of like Google Drive or Dropbox for coding. It allows a developer to keep track of changes to their work and easily collaborate with other coders. `git` is often used with GitHub, an online site for publishing your code.
  
  For more information on version control, see the [wiki page](https://en.wikipedia.org/wiki/Version_control)
  
  For more information on `git` specifically, see its [website](https://git-scm.com/)
