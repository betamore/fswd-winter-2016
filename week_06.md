# Cookies, Sessions, Redis, Gulp, User Creation

## Cookies
Cookies store bits of info about you in your browser. Their most common use is to store login info, which is what happens when you click "Remember me" on a website. Cookies can also be used to store search preferences, what you bought, pages you visited, etc.

Cookies can be temporary (aka session cookies), and disappear when the browser is closed. Or cookies can be persistent, and only expire at a set future date.

## Sessions
Sessions temporarily store information about each user that visits a website. A session is never saved to the browser or to a user's computer. Sessions are commonly used to store things that are frequently accessed from the database. Sessions can be implemented in many different ways, one of which is Redis.

## Redis
Redis is an in-memory (meaning in the RAM) data store. Redis functions as a fast, temporary database, which is useful for storing user sessions and passing messages between services. A few basic commands are below.

`SET key value` stores a particular `value` at a certain `key`. This `value` can later be retrieved with `GET key`. The `value` can also be incremented by `INCR key`, which increases the `value` by 1, or by `INCRBY key num`, which increases the `value` by `num`.
```
SET a 1
GET a, returns 1
INCR a, returns 2
INCRBY a 4, returns 6
```

`LPUSH list value` and `RPUSH list value` push `value` on to the left end and right end of `list`, respectively. `LRANGE list start end` returns you the `list` values from `start` to `end`. To get the whole `list`, use `LRANGE list 0 -1`.
```
LPUSH list 'a'
RPUSH list 'b'
RPUSH list 'c'
LRANGE list 0 1, returns a,b
```

`SADD set value` adds `value` to `set`. A `set` has no order and can contain no duplicates. So if you add the same value to the `set`, it won't change. To access the `set` values, use `SMEMBERS set`.
```
SADD set 'a'
SADD set 'b'
SADD set 'a'
SMEMBERS set, returns a,b
```

`ZADD zset score value` adds `value` and gives it a particular `score`. The score means that the `zset` can be ordered. Retrieve values from `zset` using `ZRANGE zset start end`. Similar to `LRANGE`, use `ZRANGE zset 0 -1` to get the whole `zset`.
```
ZADD zset 3 'a'
ZADD zset 1 'b'
ZADD zset 7 'c'
ZRANGE zset 0 -1, returns b,a,c
```

To start learning Redis, [check out the tutorial here](http://try.redis.io/)

Learn more about Redis at [http://redis.io/](http://redis.io/)

## Gulp
Gulp is a tool that automates tasks for you, such as minifying code, restarting server on file change, and running tests.

This is a basic task `basicTask` and how you run it on the command line.
```
gulp.task('basicTask', function() {
    console.log("Running my task!");
});

$ gulp basicTask
```

This is a more complex task that starts up your server for you and restarts it whenever a file changes.
```
gulp.task('server', function() {
    var server = gls('.');
    server.start().then(function(result) {
        console.log('Server exited with result:', result);
    });
    return gulp.watch(srcFiles, function(file) {
        console.log(file);
        server.start.apply(server);
    });
});

$ gulp server
```

Learn more about Gulp at [http://gulpjs.com/](http://gulpjs.com/)
