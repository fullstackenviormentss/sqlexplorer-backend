# SQL-Explorer Backend (JS-Oracle)

A small version of sqlexplorer backend which connects and evaluates queries against Oracle Database.

Questions for assignments are kept in original Postgres Database similar to original php version of sqlexplorer.

sql_to_pdf is the php part which generated pdf with answers from questions. Dependencies are *geshi* and *tcpdf*.


## server API

### POST
User
/api/evaluate 

Admin
/api/assignment
/api/assignment/:assignmentId/question
/api/questions

### GET

User

```
/api/db/list // list possible assignments
```

Admin
```
/api/db/:dbname for wwwsqldesigner to generate Schema Images
/api/pdf/:id pdf solution
```

Question / assignment  management
```
/api/questiontext/:id
/api/question/:id
/api/question
/api/scorm/:id
/api/logs
/api/logs/:user_id
/api/tags
/api/assignment/list
/api/assignment/:id
```

## Dependencies documentation

This project depends upon these packages :

* `mssql` - A Microsoft SQL Server client - https://www.npmjs.com/package/mssql
* `object.reduce` - A library that allows using `reduce` with Objects - https://www.npmjs.com/package/object.reduce

### Misc documentation

* `tedious` - The `mssql` package is based on the Tedious driver - http://tediousjs.github.io/tedious/getting-started.html