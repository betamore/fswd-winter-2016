# Databases, ORMs, SQL, Sequelize

## Databases
A database is where and how data gets stored. A Database Management System (or DBMS) is what allows you to interact with a database. Popular DBMSs include MySQL, PostgreSQL, Mongo, and Redis.

With a DBMS, you can define the data, create it, read it, update it, or delete it. The data can be stored in a table, a collection, and also as a key value pair.

## ORMs (Object Relational Mappings)
An ORM wraps the functionality of a database language, like SQL or Mongo, into a package that you can use with the language (Python, JavaScript, etc) you're already coding in.

## SQL (Structured Query Language) and Sequelize
SQL is a language for interacting with databases. Sequelize is an ORM for SQL. SQL queries and their Sequelize versions are below.

You can define data
```
-- in SQL
CREATE TABLE posts (
  author VARCHAR(100),
  content VARCHAR(1000),
  likes INT
);

// in Sequelize
var Post = sequelize.define('Post', {
  author: Sequelize.STRING,
  content: Sequelize.TEXT,
  likes: Sequelize.INTEGER
});
```

You can create data
```
-- in SQL
INSERT INTO posts
VALUES ('Alice', 'Dear Readers, ...');

// in Sequelize
User.create({
  author: 'Alice',
  content: 'Dear Readers, ...'
});
```

You can read data
```
-- in SQL
SELECT author, content
FROM posts
WHERE likes > 25;

// in Sequelize
Posts.findAll({
  attributes: ['author', 'content'],
  where: {likes: {$gt: 25}}
});
```

You can update data
```
-- in SQL
UPDATE posts
SET author='Bob'
WHERE author='Alice';

// in Sequelize
Posts.update(
  { author: 'Bob' },
  { where: {author: 'Alice'} }
);
```

You can delete data
```
-- in SQL
DELETE FROM posts
WHERE author='Bob';

// in Sequelize
Posts.destroy({
    where: { author: 'Bob' }
});
```

Learn more about SQL at the MDN-recommended [SQLZoo](http://sqlzoo.net/wiki/SQL_Tutorial)

Read the [docs on Sequelize here](http://docs.sequelizejs.com/en/latest/).
