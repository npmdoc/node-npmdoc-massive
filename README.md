# api documentation for  [massive (v2.6.0)](https://github.com/robconery/massive-js#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-massive.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-massive) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-massive.svg)](https://travis-ci.org/npmdoc/node-npmdoc-massive)
#### A small query tool for Postgres that embraces json and makes life simpler

[![NPM](https://nodei.co/npm/massive.png?downloads=true)](https://www.npmjs.com/package/massive)

[![apidoc](https://npmdoc.github.io/node-npmdoc-massive/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-massive_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-massive/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-massive/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-massive/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Rob Conery",
        "email": "robconery@gmail.com"
    },
    "bin": {
        "massive": "bin/massive.js"
    },
    "bugs": {
        "url": "https://github.com/robconery/massive-js/issues"
    },
    "contributors": [
        {
            "name": "Karl Seguin",
            "email": "karl@openmymind.net"
        },
        {
            "name": "John Atten",
            "email": "xivsolutions@gmail.com"
        },
        {
            "name": "Dian Fay",
            "email": "dian.m.fay@gmail.com"
        }
    ],
    "dependencies": {
        "args-js": "^0.10.12",
        "async": "^2.1.4",
        "commander": "^2.6.0",
        "deasync": "^0.1.1",
        "glob": "^7.0.5",
        "pg": "^6.1.0",
        "pg-query-stream": "^0.7.0",
        "promise-polyfill": "^6.0.2",
        "strip-bom": "^2.0.0",
        "underscore": "^1.8.2"
    },
    "description": "A small query tool for Postgres that embraces json and makes life simpler",
    "devDependencies": {
        "eslint": "^2.13.1",
        "istanbul": "^0.4.2",
        "mocha": "^2.5.3",
        "sinon": "^1.12.2"
    },
    "directories": {
        "example": "example",
        "test": "test"
    },
    "dist": {
        "shasum": "aef14db9b8a3ccf3a42f03c09d7cd3e9cb4c96b6",
        "tarball": "https://registry.npmjs.org/massive/-/massive-2.6.0.tgz"
    },
    "eslintConfig": {
        "extends": "eslint:recommended",
        "env": {
            "node": true,
            "mocha": true
        },
        "rules": {
            "semi": 2
        }
    },
    "gitHead": "9ed7b29cfe86613ddefb0fd08f51102a960aec2f",
    "homepage": "https://github.com/robconery/massive-js#readme",
    "keywords": [
        "postgres",
        "pg",
        "postgresql"
    ],
    "license": "BSD-3-Clause",
    "main": "index.js",
    "maintainers": [
        {
            "name": "robconery",
            "email": "rob@wekeroad.com"
        }
    ],
    "name": "massive",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/robconery/massive-js.git"
    },
    "scripts": {
        "coverage": "istanbul cover _mocha -- -R dot",
        "lint": "eslint .",
        "posttest": "npm run lint",
        "test": "mocha"
    },
    "version": "2.6.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module massive](#apidoc.module.massive)
1.  [function <span class="apidocSignatureSpan">massive.</span>connect (args, next)](#apidoc.element.massive.connect)
1.  [function <span class="apidocSignatureSpan">massive.</span>connectSync ()](#apidoc.element.massive.connectSync)
1.  [function <span class="apidocSignatureSpan">massive.</span>executable (args)](#apidoc.element.massive.executable)
1.  [function <span class="apidocSignatureSpan">massive.</span>loadSync ()](#apidoc.element.massive.loadSync)
1.  [function <span class="apidocSignatureSpan">massive.</span>query (args, object)](#apidoc.element.massive.query)
1.  [function <span class="apidocSignatureSpan">massive.</span>queryable ()](#apidoc.element.massive.queryable)
1.  [function <span class="apidocSignatureSpan">massive.</span>runner (connectionString, defaults)](#apidoc.element.massive.runner)
1.  [function <span class="apidocSignatureSpan">massive.</span>table (args)](#apidoc.element.massive.table)
1.  object <span class="apidocSignatureSpan">massive.</span>arg_types
1.  object <span class="apidocSignatureSpan">massive.</span>document
1.  object <span class="apidocSignatureSpan">massive.</span>document_table
1.  object <span class="apidocSignatureSpan">massive.</span>executable.prototype
1.  object <span class="apidocSignatureSpan">massive.</span>query.prototype
1.  object <span class="apidocSignatureSpan">massive.</span>queryable.prototype
1.  object <span class="apidocSignatureSpan">massive.</span>runner.prototype
1.  object <span class="apidocSignatureSpan">massive.</span>table.prototype
1.  object <span class="apidocSignatureSpan">massive.</span>where

#### [module massive.arg_types](#apidoc.module.massive.arg_types)
1.  [function <span class="apidocSignatureSpan">massive.arg_types.</span>findArgs (args, source)](#apidoc.element.massive.arg_types.findArgs)
1.  [function <span class="apidocSignatureSpan">massive.arg_types.</span>forArgs (args)](#apidoc.element.massive.arg_types.forArgs)
1.  [function <span class="apidocSignatureSpan">massive.arg_types.</span>queryArgs (args)](#apidoc.element.massive.arg_types.queryArgs)
1.  [function <span class="apidocSignatureSpan">massive.arg_types.</span>searchArgs (args, source)](#apidoc.element.massive.arg_types.searchArgs)
1.  [function <span class="apidocSignatureSpan">massive.arg_types.</span>whereArgs (args, source)](#apidoc.element.massive.arg_types.whereArgs)

#### [module massive.document](#apidoc.module.massive.document)
1.  [function <span class="apidocSignatureSpan">massive.document.</span>formatArray (args)](#apidoc.element.massive.document.formatArray)
1.  [function <span class="apidocSignatureSpan">massive.document.</span>formatDocument (args)](#apidoc.element.massive.document.formatDocument)

#### [module massive.document_table](#apidoc.module.massive.document_table)
1.  [function <span class="apidocSignatureSpan">massive.document_table.</span>executeDocQuery ()](#apidoc.element.massive.document_table.executeDocQuery)
1.  [function <span class="apidocSignatureSpan">massive.document_table.</span>findDoc ()](#apidoc.element.massive.document_table.findDoc)
1.  [function <span class="apidocSignatureSpan">massive.document_table.</span>findDocSync ()](#apidoc.element.massive.document_table.findDocSync)
1.  [function <span class="apidocSignatureSpan">massive.document_table.</span>getWhereForDoc (conditions, offset, prefix)](#apidoc.element.massive.document_table.getWhereForDoc)
1.  [function <span class="apidocSignatureSpan">massive.document_table.</span>saveDoc (args, next)](#apidoc.element.massive.document_table.saveDoc)
1.  [function <span class="apidocSignatureSpan">massive.document_table.</span>saveDocSync ()](#apidoc.element.massive.document_table.saveDocSync)
1.  [function <span class="apidocSignatureSpan">massive.document_table.</span>searchDoc ()](#apidoc.element.massive.document_table.searchDoc)
1.  [function <span class="apidocSignatureSpan">massive.document_table.</span>searchDocSync ()](#apidoc.element.massive.document_table.searchDocSync)
1.  [function <span class="apidocSignatureSpan">massive.document_table.</span>setAttribute (id, key, val, next)](#apidoc.element.massive.document_table.setAttribute)
1.  [function <span class="apidocSignatureSpan">massive.document_table.</span>setAttributeSync ()](#apidoc.element.massive.document_table.setAttributeSync)

#### [module massive.executable](#apidoc.module.massive.executable)
1.  [function <span class="apidocSignatureSpan">massive.</span>executable (args)](#apidoc.element.massive.executable.executable)
1.  [function <span class="apidocSignatureSpan">massive.executable.</span>super_ (args)](#apidoc.element.massive.executable.super_)

#### [module massive.executable.prototype](#apidoc.module.massive.executable.prototype)
1.  [function <span class="apidocSignatureSpan">massive.executable.prototype.</span>invoke ()](#apidoc.element.massive.executable.prototype.invoke)

#### [module massive.query](#apidoc.module.massive.query)
1.  [function <span class="apidocSignatureSpan">massive.</span>query (args, object)](#apidoc.element.massive.query.query)

#### [module massive.query.prototype](#apidoc.module.massive.query.prototype)
1.  [function <span class="apidocSignatureSpan">massive.query.prototype.</span>format (where)](#apidoc.element.massive.query.prototype.format)
1.  [function <span class="apidocSignatureSpan">massive.query.prototype.</span>queryOptions ()](#apidoc.element.massive.query.prototype.queryOptions)
1.  [function <span class="apidocSignatureSpan">massive.query.prototype.</span>selectList ()](#apidoc.element.massive.query.prototype.selectList)

#### [module massive.queryable](#apidoc.module.massive.queryable)
1.  [function <span class="apidocSignatureSpan">massive.</span>queryable ()](#apidoc.element.massive.queryable.queryable)
1.  [function <span class="apidocSignatureSpan">massive.queryable.</span>super_ (args)](#apidoc.element.massive.queryable.super_)

#### [module massive.queryable.prototype](#apidoc.module.massive.queryable.prototype)
1.  [function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>count ()](#apidoc.element.massive.queryable.prototype.count)
1.  [function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>countSync ()](#apidoc.element.massive.queryable.prototype.countSync)
1.  [function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>find ()](#apidoc.element.massive.queryable.prototype.find)
1.  [function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>findOne ()](#apidoc.element.massive.queryable.prototype.findOne)
1.  [function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>findOneSync ()](#apidoc.element.massive.queryable.prototype.findOneSync)
1.  [function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>findSync ()](#apidoc.element.massive.queryable.prototype.findSync)
1.  [function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>search (args, next)](#apidoc.element.massive.queryable.prototype.search)
1.  [function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>searchSync ()](#apidoc.element.massive.queryable.prototype.searchSync)
1.  [function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>where ()](#apidoc.element.massive.queryable.prototype.where)
1.  [function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>whereSync ()](#apidoc.element.massive.queryable.prototype.whereSync)

#### [module massive.runner](#apidoc.module.massive.runner)
1.  [function <span class="apidocSignatureSpan">massive.</span>runner (connectionString, defaults)](#apidoc.element.massive.runner.runner)

#### [module massive.runner.prototype](#apidoc.module.massive.runner.prototype)
1.  [function <span class="apidocSignatureSpan">massive.runner.prototype.</span>end ()](#apidoc.element.massive.runner.prototype.end)
1.  [function <span class="apidocSignatureSpan">massive.runner.prototype.</span>executeSqlFile (args, next)](#apidoc.element.massive.runner.prototype.executeSqlFile)
1.  [function <span class="apidocSignatureSpan">massive.runner.prototype.</span>query ()](#apidoc.element.massive.runner.prototype.query)
1.  [function <span class="apidocSignatureSpan">massive.runner.prototype.</span>stream ()](#apidoc.element.massive.runner.prototype.stream)

#### [module massive.table](#apidoc.module.massive.table)
1.  [function <span class="apidocSignatureSpan">massive.</span>table (args)](#apidoc.element.massive.table.table)
1.  [function <span class="apidocSignatureSpan">massive.table.</span>super_ ()](#apidoc.element.massive.table.super_)

#### [module massive.table.prototype](#apidoc.module.massive.table.prototype)
1.  [function <span class="apidocSignatureSpan">massive.table.prototype.</span>containsPk (args)](#apidoc.element.massive.table.prototype.containsPk)
1.  [function <span class="apidocSignatureSpan">massive.table.prototype.</span>delimitedPrimaryKeyName ()](#apidoc.element.massive.table.prototype.delimitedPrimaryKeyName)
1.  [function <span class="apidocSignatureSpan">massive.table.prototype.</span>destroy (args, next)](#apidoc.element.massive.table.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">massive.table.prototype.</span>destroySync ()](#apidoc.element.massive.table.prototype.destroySync)
1.  [function <span class="apidocSignatureSpan">massive.table.prototype.</span>insert (data, next)](#apidoc.element.massive.table.prototype.insert)
1.  [function <span class="apidocSignatureSpan">massive.table.prototype.</span>insertSync ()](#apidoc.element.massive.table.prototype.insertSync)
1.  [function <span class="apidocSignatureSpan">massive.table.prototype.</span>primaryKeyName ()](#apidoc.element.massive.table.prototype.primaryKeyName)
1.  [function <span class="apidocSignatureSpan">massive.table.prototype.</span>save (args, next)](#apidoc.element.massive.table.prototype.save)
1.  [function <span class="apidocSignatureSpan">massive.table.prototype.</span>saveSync ()](#apidoc.element.massive.table.prototype.saveSync)
1.  [function <span class="apidocSignatureSpan">massive.table.prototype.</span>search ()](#apidoc.element.massive.table.prototype.search)
1.  [function <span class="apidocSignatureSpan">massive.table.prototype.</span>searchSync ()](#apidoc.element.massive.table.prototype.searchSync)
1.  [function <span class="apidocSignatureSpan">massive.table.prototype.</span>update (conditions, fields, next)](#apidoc.element.massive.table.prototype.update)
1.  [function <span class="apidocSignatureSpan">massive.table.prototype.</span>updateSync ()](#apidoc.element.massive.table.prototype.updateSync)

#### [module massive.where](#apidoc.module.massive.where)
1.  [function <span class="apidocSignatureSpan">massive.where.</span>docPredicate (result, condition, value, conditions)](#apidoc.element.massive.where.docPredicate)
1.  [function <span class="apidocSignatureSpan">massive.where.</span>forTable ()](#apidoc.element.massive.where.forTable)
1.  [function <span class="apidocSignatureSpan">massive.where.</span>generate (result, conditions, generator)](#apidoc.element.massive.where.generate)
1.  [function <span class="apidocSignatureSpan">massive.where.</span>isPkSearch (conditions)](#apidoc.element.massive.where.isPkSearch)
1.  [function <span class="apidocSignatureSpan">massive.where.</span>parseKey (key)](#apidoc.element.massive.where.parseKey)
1.  [function <span class="apidocSignatureSpan">massive.where.</span>predicate (result, condition, value)](#apidoc.element.massive.where.predicate)



# <a name="apidoc.module.massive"></a>[module massive](#apidoc.module.massive)

#### <a name="apidoc.element.massive.connect"></a>[function <span class="apidocSignatureSpan">massive.</span>connect (args, next)](#apidoc.element.massive.connect)
- description and source-code
```javascript
connect = function (args, next) {
  //override if there's a db name passed in
  if (args.db) {
    args.connectionString = "postgres://localhost/"+args.db;
  } else if (!args.connectionString) {
    return next(new Error("Need a connectionString or db (name of database on localhost) to connect."));
  }

  var massive = new Massive(args);

  //load up the tables, queries, and commands
  massive.loadTables(function(err, db) {
    if (err) { return next(err); }

    self = db;

    massive.loadDescendantTables(function () {
      if (err) { return next(err); }

      massive.loadViews(function() {
        if (err) { return next(err); }

        massive.loadFunctions(function(err, db) {
          if (err) { return next(err); }

          db.loadQueries(); // synchronous

          next(null, db);
        });
      });
    });
  });
}
```
- example usage
```shell
...
Once Massive is installed, you can use it by calling 'connect' and passing in a callback which will give you your database instance
:

'''javascript
var massive = require("massive");

//you can use db for 'database name' running on localhost
//or send in everything using 'connectionString'
massive.connect({db : "myDb"}, function(err,db){
  db.myTable.find();
});
'''
## Usage

One of the key features of Massive is that it loads all of your tables, Postgres functions, and local query files up as functions
 (this is really cool, you want this. See below for more info). Massive is fast, and does this quickly. However, there is a one-
time execution penalty at intialization while all this happens. In most situations it makes sense to do this once, at application
 load. From there, maintain a reference to the Massive instance (Massive was conceived with this usage in mind). For example, if
 you are using Express as your application framework, you might do something like this:
...
```

#### <a name="apidoc.element.massive.connectSync"></a>[function <span class="apidocSignatureSpan">massive.</span>connectSync ()](#apidoc.element.massive.connectSync)
- description and source-code
```javascript
connectSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
...
var http = require('http');
var massive = require("massive");
var connectionString = "postgres://massive:password@localhost/chinook";

// connect to Massive and get the db instance. You can safely use the
// convenience sync method here because its on app load
// you can also use loadSync - it's an alias
var massiveInstance = massive.connectSync({connectionString : connectionString})

// Set a reference to the massive instance on Express' app:
app.set('db', massiveInstance);
http.createServer(app).listen(8080);
'''
From there, accessing the db is just:
...
```

#### <a name="apidoc.element.massive.executable"></a>[function <span class="apidocSignatureSpan">massive.</span>executable (args)](#apidoc.element.massive.executable)
- description and source-code
```javascript
executable = function (args) {
  Entity.apply(this, arguments);

  this.sql = args.sql;
  this.filePath = args.filePath;
  this.singleRow = args.singleRow;
  this.singleValue = args.singleValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.loadSync"></a>[function <span class="apidocSignatureSpan">massive.</span>loadSync ()](#apidoc.element.massive.loadSync)
- description and source-code
```javascript
loadSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.query"></a>[function <span class="apidocSignatureSpan">massive.</span>query (args, object)](#apidoc.element.massive.query)
- description and source-code
```javascript
query = function (args, object) {
  this.source = object.delimitedFullName;
  this.columns = args.columns || "*";
  this.only = args.only || false;
  this.order = args.order || (object.hasOwnProperty("pk") ? util.format('"%s"', object.pk) : "1");
  this.orderBody = args.orderBody || false;
  this.offset = args.offset;
  this.limit = args.limit;
  this.stream = args.stream;
  this.single = args.single || false;
}
```
- example usage
```shell
...
    }
  }
  return result;
};

Massive.prototype.run = function(){
  var args = ArgTypes.queryArgs(arguments);
  this.query(args);
};
Massive.prototype.runSync = DA(Massive.prototype.run);

Massive.prototype.loadQueries = function() {
  walkSqlFiles(this, this.scriptsDir);
};
...
```

#### <a name="apidoc.element.massive.queryable"></a>[function <span class="apidocSignatureSpan">massive.</span>queryable ()](#apidoc.element.massive.queryable)
- description and source-code
```javascript
queryable = function () {
  Entity.apply(this, arguments);

  // create delimited names now instead of at query time
  this.delimitedName = "\"" + this.name + "\"";
  this.delimitedSchema = "\"" + this.schema + "\"";

  // handle naming when schema is other than public:
  if(this.schema !== "public") {
    this.fullname = this.schema + "." + this.name;
    this.delimitedFullName = this.delimitedSchema + "." + this.delimitedName;
  } else {
    this.fullname = this.name;
    this.delimitedFullName = this.delimitedName;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.runner"></a>[function <span class="apidocSignatureSpan">massive.</span>runner (connectionString, defaults)](#apidoc.element.massive.runner)
- description and source-code
```javascript
runner = function (connectionString, defaults) {
  this.connectionString = connectionString;
  this.defaults = defaults;

  if (defaults) {
    _.each(defaults, function (v, k) {
      pg.defaults[k] = v;
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.table"></a>[function <span class="apidocSignatureSpan">massive.</span>table (args)](#apidoc.element.massive.table)
- description and source-code
```javascript
table = function (args) {
  Queryable.apply(this, arguments);

  this.pk = args.pk;

  _.extend(this,DocumentTable);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.massive.arg_types"></a>[module massive.arg_types](#apidoc.module.massive.arg_types)

#### <a name="apidoc.element.massive.arg_types.findArgs"></a>[function <span class="apidocSignatureSpan">massive.arg_types.</span>findArgs (args, source)](#apidoc.element.massive.arg_types.findArgs)
- description and source-code
```javascript
findArgs = function (args, source) {
  args = Args([
    {conditions : Args.ANY | Args.Optional, _default : {}},
    {options : Args.OBJECT | Args.Optional, _default: {}},
    {next : Args.FUNCTION | Args.Optional, _default : function(err,res){
      if(err) console.log(err);
      else console.log(res);
    }}
  ], args);

  if (_.isFunction(args.conditions)) {
    //this is our callback as the only argument, caught by Args.ANY
    args.next = args.conditions;
    args.conditions = {};
  }

  args.query = new Query(args.options, source);

  return args;
}
```
- example usage
```shell
...
var params = ["{"+key+"}", val, id];
var sql = util.format("update %s set body=jsonb_set(body, $1, $2, true) where %s = $3 returning *;", this.fullname, pkName);
this.executeDocQuery(sql, params, {single:true}, next);
};
exports.setAttributeSync = DA(this.setAttribute);

exports.findDoc = function() {
var args = ArgTypes.findArgs(arguments, this);

var where = this.getWhereForDoc(args.conditions);

if (where.pkQuery) { args.options.single = true; }

var sql = args.query.format(where.where);
...
```

#### <a name="apidoc.element.massive.arg_types.forArgs"></a>[function <span class="apidocSignatureSpan">massive.arg_types.</span>forArgs (args)](#apidoc.element.massive.arg_types.forArgs)
- description and source-code
```javascript
forArgs = function (args) {
  return Args([
    {conditions: Args.OBJECT},
    {generator: Args.STRING | Args.Optional, _default: 'predicate'},
    {placeholderOffset: Args.INT | Args.Optional, _default: 0},
    {prefix: Args.STRING | Args.Optional, _default: ' \nWHERE '}
  ], args);
}
```
- example usage
```shell
...
  }
});

return result;
};

exports.forTable = function () {
var args = ArgTypes.forArgs(arguments);

if (_.isEmpty(args.conditions)) {
  return {
    where: args.prefix + 'TRUE',
    params: []
  };
}
...
```

#### <a name="apidoc.element.massive.arg_types.queryArgs"></a>[function <span class="apidocSignatureSpan">massive.arg_types.</span>queryArgs (args)](#apidoc.element.massive.arg_types.queryArgs)
- description and source-code
```javascript
queryArgs = function (args){
  args = Args([
    {sql : Args.STRING | Args.Required},
    {params : Args.ARRAY | Args.Optional, _default : []},
    {options : Args.OBJECT | Args.Optional, _default : {single : false}},
    {next : Args.FUNCTION | Args.Optional, _default : function(err,res){
      if(err) console.log(err);
      else console.log(res);
    }}
  ], args);
  if(!_.isArray(args.params)) args.params = [args.params];
  return args;
}
```
- example usage
```shell
...
      result = filter.join(", ");
    }
  }
  return result;
};

Massive.prototype.run = function(){
  var args = ArgTypes.queryArgs(arguments);
  this.query(args);
};
Massive.prototype.runSync = DA(Massive.prototype.run);

Massive.prototype.loadQueries = function() {
  walkSqlFiles(this, this.scriptsDir);
};
...
```

#### <a name="apidoc.element.massive.arg_types.searchArgs"></a>[function <span class="apidocSignatureSpan">massive.arg_types.</span>searchArgs (args, source)](#apidoc.element.massive.arg_types.searchArgs)
- description and source-code
```javascript
searchArgs = function (args, source) {
  args = Args([
    {fields : Args.OBJECT | Args.Optional, _default: {}},
    {options: Args.OBJECT | Args.Optional, _default: {}},
    {next : Args.FUNCTION | Args.Optional, _default: function(err, res){
      if(err) console.log(err);
      else console.log(res);
    }}
  ], args);

  args.query = new Query(args.options, source);

  return args;
}
```
- example usage
```shell
...
var Document = require("./document");
var Where = require("./where");
var ArgTypes = require("./arg_types");
var DA = require("deasync");

//Searching query for jsonb docs
exports.searchDoc = function(){
var args = ArgTypes.searchArgs(arguments, this);
assert(args.fields.keys && args.fields.term, "Need the keys to use and the term string");
var params = [args.fields.term];
//yuck full repetition here... fix me...
if(!_.isArray(args.fields.keys)){
  args.fields.keys = [args.fields.keys];
}
var tsv;
...
```

#### <a name="apidoc.element.massive.arg_types.whereArgs"></a>[function <span class="apidocSignatureSpan">massive.arg_types.</span>whereArgs (args, source)](#apidoc.element.massive.arg_types.whereArgs)
- description and source-code
```javascript
whereArgs = function (args, source){
  args = Args([
    {where : Args.STRING | Args.Optional, _default : "true"},
    {params : Args.ANY | Args.Optional, _default : []},
    {next : Args.FUNCTION | Args.Optional, _default : function(err,res){
      if(err) console.log(err);
      else console.log(res);
    }}
  ], args);

  if(!_.isArray(args.params)) args.params = [args.params];

  args.query = new Query({}, source);
  return args;
}
```
- example usage
```shell
...
var args;
var where;

if (_.isObject(arguments[0])) {
  args = ArgTypes.findArgs(arguments, this);
  where = _.isEmpty(args.conditions) ? {where : " "} : Where.forTable(args.conditions);
} else {
  args = ArgTypes.whereArgs(arguments, this);
  where = {where: " where " + args.where};
}

args.query.columns = "COUNT(1)";
args.query.order = null;
var sql = args.query.format(where.where);
...
```



# <a name="apidoc.module.massive.document"></a>[module massive.document](#apidoc.module.massive.document)

#### <a name="apidoc.element.massive.document.formatArray"></a>[function <span class="apidocSignatureSpan">massive.document.</span>formatArray (args)](#apidoc.element.massive.document.formatArray)
- description and source-code
```javascript
formatArray = function (args){

  var result = [];
  _.each(args, function(doc){
    result.push(this.formatDocument(doc));
  }.bind(this));
  return result;
}
```
- example usage
```shell
...
    if(err){
      args.next(err,null);
    }else{
      //only return one result if single is sent in
      if(args.options.single){
        doc = Document.formatDocument(res);
      }else{
        doc = Document.formatArray(res);
      }
      args.next(null,doc);
    }
  });
};
...
```

#### <a name="apidoc.element.massive.document.formatDocument"></a>[function <span class="apidocSignatureSpan">massive.document.</span>formatDocument (args)](#apidoc.element.massive.document.formatDocument)
- description and source-code
```javascript
formatDocument = function (args){
  var returnDoc = null;
  if(args){
    returnDoc = args.body || {};
    returnDoc.id = args.id || null;
  }
  return returnDoc;
}
```
- example usage
```shell
...
var _ = require("underscore")._;

//A simple helper function to manage document ids
exports.formatArray = function(args){

var result = [];
_.each(args, function(doc){
  result.push(this.formatDocument(doc));
}.bind(this));
return result;
};

exports.formatDocument = function(args){
var returnDoc = null;
if(args){
...
```



# <a name="apidoc.module.massive.document_table"></a>[module massive.document_table](#apidoc.module.massive.document_table)

#### <a name="apidoc.element.massive.document_table.executeDocQuery"></a>[function <span class="apidocSignatureSpan">massive.document_table.</span>executeDocQuery ()](#apidoc.element.massive.document_table.executeDocQuery)
- description and source-code
```javascript
executeDocQuery = function () {
  var args = ArgTypes.queryArgs(arguments);
  var doc = {};
  this.db.query(args.sql, args.params, args.options, function(err,res){
    if(err){
      args.next(err,null);
    }else{
      //only return one result if single is sent in
      if(args.options.single){
        doc = Document.formatDocument(res);
      }else{
        doc = Document.formatArray(res);
      }
      args.next(null,doc);
    }
  });
}
```
- example usage
```shell
...
  var where = this.getWhereForDoc(args.fields.where, 1, " AND ");
  whereString = where.where;
  params = params.concat(where.params);
}

var sql = args.query.format(util.format(" WHERE to_tsvector(%s) @@ to_tsquery($1) %s", tsv, whereString));

this.executeDocQuery(sql, params, args.options, args.next);
};
exports.searchDocSync = DA(this.searchDoc);

exports.saveDoc = function(args, next) {
assert(_.isObject(args), "Please pass in the document for saving as an object. Include the primary key for an UPDATE.");
var sql, params = [];
var pkName = this.primaryKeyName();
...
```

#### <a name="apidoc.element.massive.document_table.findDoc"></a>[function <span class="apidocSignatureSpan">massive.document_table.</span>findDoc ()](#apidoc.element.massive.document_table.findDoc)
- description and source-code
```javascript
findDoc = function () {
  var args = ArgTypes.findArgs(arguments, this);

  var where = this.getWhereForDoc(args.conditions);

  if (where.pkQuery) { args.options.single = true; }

  var sql = args.query.format(where.where);

  this.executeDocQuery(sql, where.params, args.options, args.next);
}
```
- example usage
```shell
...

db.saveDoc("my_documents", newDoc, function(err,res){
  //the table my_documents was created on the fly
  //res is the new document with an ID created for you
});

//you can now access the document right on the root
db.my_documents.findDoc(1, function(err,doc){
  //you now have access to the doc
});

//run a 'contains' query which flexes the index we created for you
db.my_documents.findDoc({price : 99.00}, function(err,docs){
  //1 or more documents returned
});
...
```

#### <a name="apidoc.element.massive.document_table.findDocSync"></a>[function <span class="apidocSignatureSpan">massive.document_table.</span>findDocSync ()](#apidoc.element.massive.document_table.findDocSync)
- description and source-code
```javascript
findDocSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.document_table.getWhereForDoc"></a>[function <span class="apidocSignatureSpan">massive.document_table.</span>getWhereForDoc (conditions, offset, prefix)](#apidoc.element.massive.document_table.getWhereForDoc)
- description and source-code
```javascript
getWhereForDoc = function (conditions, offset, prefix) {
  var where = {pkQuery: false};
  if(_.isFunction(conditions) || conditions == "*") {
    // no criteria provided - treat like select *
    where.where = "";
    where.params = [];
    return where;
  }

  if (Where.isPkSearch(conditions)) {
    //assume it's a search on ID
    conditions = {id : conditions};
  }

  if (_.isObject(conditions)) {
    var keys = _.keys(conditions);

    if (keys.length === 1) {
      var operator = keys[0].match("<=|>=|!=|<>|=|<|>");
      var property = keys[0].replace(operator, "").trim();
      if (property == this.primaryKeyName()) {
        // this is a query against the PK...we can use the
        // plain old table "where" builder:
        where = Where.forTable(conditions, 'predicate', offset, prefix);

        // only a true pk query if testing equality
        if ((operator === null || operator === "=") && !_.isObject(conditions[keys[0]])) {
          where.pkQuery = true;
        }
      } else {
        where = Where.forTable(conditions, 'docPredicate', offset, prefix);
      }
    } else {
      where = Where.forTable(conditions, 'docPredicate', offset, prefix);
    }
  }

  return where;
}
```
- example usage
```shell
...
  });
  tsv= util.format("concat(%s)", formattedKeys.join(", ' ',"));
}

var whereString = "";

if (args.fields.where) {
  var where = this.getWhereForDoc(args.fields.where, 1, " AND ");
  whereString = where.where;
  params = params.concat(where.params);
}

var sql = args.query.format(util.format(" WHERE to_tsvector(%s) @@ to_tsquery($1) %s", tsv, whereString));

this.executeDocQuery(sql, params, args.options, args.next);
...
```

#### <a name="apidoc.element.massive.document_table.saveDoc"></a>[function <span class="apidocSignatureSpan">massive.document_table.</span>saveDoc (args, next)](#apidoc.element.massive.document_table.saveDoc)
- description and source-code
```javascript
saveDoc = function (args, next) {
  assert(_.isObject(args), "Please pass in the document for saving as an object. Include the primary key for an UPDATE.");
  var sql, params = [];
  var pkName = this.primaryKeyName();
  var pkVal = args[pkName];

  // if there's a primary key, don't store it in the body as well
  params.push(JSON.stringify(_.omit(args, pkName)));

  if (pkVal) {
    sql = util.format("update %s set body = $1 where %s = $2 returning *;", this.fullname, pkName);
    params.push(pkVal);
  } else {
    sql = "insert into " + this.fullname + "(body) values($1) returning *;";
  }

  this.executeDocQuery(sql, params, {single : true}, next);
}
```
- example usage
```shell
...
price : 99.00,
tags : [
  {name : "Simplicity", slug : "simple"},
  {name : "Fun for All", slug : "fun-for-all"}
]
};

db.saveDoc("my_documents", newDoc, function(err,res){
//the table my_documents was created on the fly
//res is the new document with an ID created for you
});

//you can now access the document right on the root
db.my_documents.findDoc(1, function(err,doc){
//you now have access to the doc
...
```

#### <a name="apidoc.element.massive.document_table.saveDocSync"></a>[function <span class="apidocSignatureSpan">massive.document_table.</span>saveDocSync ()](#apidoc.element.massive.document_table.saveDocSync)
- description and source-code
```javascript
saveDocSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.document_table.searchDoc"></a>[function <span class="apidocSignatureSpan">massive.document_table.</span>searchDoc ()](#apidoc.element.massive.document_table.searchDoc)
- description and source-code
```javascript
searchDoc = function (){
  var args = ArgTypes.searchArgs(arguments, this);
  assert(args.fields.keys && args.fields.term, "Need the keys to use and the term string");
  var params = [args.fields.term];
  //yuck full repetition here... fix me...
  if(!_.isArray(args.fields.keys)){
    args.fields.keys = [args.fields.keys];
  }
  var tsv;
  if(args.fields.keys.length === 1){
    tsv = util.format("(body ->> '%s')", args.fields.keys[0]);
  }else{
    var formattedKeys = [];
    _.each(args.fields.keys, function(key){
      formattedKeys.push(util.format("(body ->> '%s')", key));
    });
    tsv= util.format("concat(%s)", formattedKeys.join(", ' ',"));
  }

  var whereString = "";

  if (args.fields.where) {
    var where = this.getWhereForDoc(args.fields.where, 1, " AND ");
    whereString = where.where;
    params = params.concat(where.params);
  }

  var sql = args.query.format(util.format(" WHERE to_tsvector(%s) @@ to_tsquery($1) %s", tsv, whereString));

  this.executeDocQuery(sql, params, args.options, args.next);
}
```
- example usage
```shell
...
});
'''

This works the same for documents as well (more on documents in next section):

'''javascript
//full text search...
db.my_documents.searchDoc({
  keys : ["title", "description"],
  term : "Kauai"
}, function(err,docs){
  //docs returned with an on-the-fly Full Text Search for 'Kauai'
});
'''
...
```

#### <a name="apidoc.element.massive.document_table.searchDocSync"></a>[function <span class="apidocSignatureSpan">massive.document_table.</span>searchDocSync ()](#apidoc.element.massive.document_table.searchDocSync)
- description and source-code
```javascript
searchDocSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.document_table.setAttribute"></a>[function <span class="apidocSignatureSpan">massive.document_table.</span>setAttribute (id, key, val, next)](#apidoc.element.massive.document_table.setAttribute)
- description and source-code
```javascript
setAttribute = function (id, key, val, next){
  if (typeof val === 'string') { val = JSON.stringify(val); }
  if (Array.isArray(val)) { val = JSON.stringify(val); }

  var pkName = this.primaryKeyName();
  var params = ["{"+key+"}", val, id];
  var sql = util.format("update %s set body=jsonb_set(body, $1, $2, true) where %s = $3 returning *;", this.fullname, pkName);
  this.executeDocQuery(sql, params, {single:true}, next);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.document_table.setAttributeSync"></a>[function <span class="apidocSignatureSpan">massive.document_table.</span>setAttributeSync ()](#apidoc.element.massive.document_table.setAttributeSync)
- description and source-code
```javascript
setAttributeSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.massive.executable"></a>[module massive.executable](#apidoc.module.massive.executable)

#### <a name="apidoc.element.massive.executable.executable"></a>[function <span class="apidocSignatureSpan">massive.</span>executable (args)](#apidoc.element.massive.executable.executable)
- description and source-code
```javascript
executable = function (args) {
  Entity.apply(this, arguments);

  this.sql = args.sql;
  this.filePath = args.filePath;
  this.singleRow = args.singleRow;
  this.singleValue = args.singleValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.executable.super_"></a>[function <span class="apidocSignatureSpan">massive.executable.</span>super_ (args)](#apidoc.element.massive.executable.super_)
- description and source-code
```javascript
super_ = function (args) {
  this.schema = args.schema || 'public';
  this.name = args.name;
  this.db = args.db;

  // create delimited names now instead of at query time
  this.delimitedName = "\"" + this.name + "\"";
  this.delimitedSchema = "\"" + this.schema + "\"";

  // handle naming when schema is other than public:
  if(this.schema !== "public") {
    this.fullname = this.schema + "." + this.name;
    this.delimitedFullName = this.delimitedSchema + "." + this.delimitedName;
  } else {
    this.fullname = this.name;
    this.delimitedFullName = this.delimitedName;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.massive.executable.prototype"></a>[module massive.executable.prototype](#apidoc.module.massive.executable.prototype)

#### <a name="apidoc.element.massive.executable.prototype.invoke"></a>[function <span class="apidocSignatureSpan">massive.executable.prototype.</span>invoke ()](#apidoc.element.massive.executable.prototype.invoke)
- description and source-code
```javascript
invoke = function () {

  var args = Array.prototype.slice.call(arguments);
  var next = args.pop();
  var opts = {};
  var params = [];

  if (!_.isFunction(next)) {
    throw "Function or Script Execution expects a next function as the last argument";
  }

  if (!_.isArray(_.last(args)) && _.isObject(_.last(args))) {
    opts = args.pop();
  }

  if (_.isArray(args[0])) {          // backwards compatible -- db.function([...], ?opts, callback)
    params = args[0];
  } else {
    params = args;
  }

  // console.log("invoke next: ", next);
  // console.log("invoke opts: ", opts);
  // console.log("invoke params: ", params);

  var singleRow = this.singleRow && !opts.stream;
  var singleValue = this.singleValue;

  if (opts.stream) {
    this.db.stream(this.sql, params, null, function (err, stream) {
      if (err) return next(err);
      if (singleValue) {
        var singleValueTransform = SingleValueStream();
        return next(null, stream.pipe(singleValueTransform));
      } else {
        return next(null, stream);
      }
    });
  } else {
    this.db.query(this.sql, params, null, function (err, rawData) {
      var data = rawData;
      if (err) return next(err);
      try {
        if (singleRow) {
          if (!Array.isArray(data)) {
            return next(new Error("Was expecting an array"));
          }
          data = data[0] || null;
          if (singleValue) {
            data = _processSingleValue(data);
          }
        } else {
          if (singleValue) {
            data = data.map(_processSingleValue);
          }
        }
      } catch (e) {
        err = e;
      }
      return next(err, data);
    });
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.massive.query"></a>[module massive.query](#apidoc.module.massive.query)

#### <a name="apidoc.element.massive.query.query"></a>[function <span class="apidocSignatureSpan">massive.</span>query (args, object)](#apidoc.element.massive.query.query)
- description and source-code
```javascript
query = function (args, object) {
  this.source = object.delimitedFullName;
  this.columns = args.columns || "*";
  this.only = args.only || false;
  this.order = args.order || (object.hasOwnProperty("pk") ? util.format('"%s"', object.pk) : "1");
  this.orderBody = args.orderBody || false;
  this.offset = args.offset;
  this.limit = args.limit;
  this.stream = args.stream;
  this.single = args.single || false;
}
```
- example usage
```shell
...
    }
  }
  return result;
};

Massive.prototype.run = function(){
  var args = ArgTypes.queryArgs(arguments);
  this.query(args);
};
Massive.prototype.runSync = DA(Massive.prototype.run);

Massive.prototype.loadQueries = function() {
  walkSqlFiles(this, this.scriptsDir);
};
...
```



# <a name="apidoc.module.massive.query.prototype"></a>[module massive.query.prototype](#apidoc.module.massive.query.prototype)

#### <a name="apidoc.element.massive.query.prototype.format"></a>[function <span class="apidocSignatureSpan">massive.query.prototype.</span>format (where)](#apidoc.element.massive.query.prototype.format)
- description and source-code
```javascript
format = function (where) {
  var from = this.only ? " FROM ONLY " : " FROM ";

  return "SELECT " + this.selectList() + from + this.source + where + this.queryOptions();
}
```
- example usage
```shell
...
};

Massive.prototype.documentTableSql = function(tableName){
var docSqlFile = __dirname + "/lib/scripts/create_document_table.sql";
var sql = fs.readFileSync(docSqlFile, {encoding: 'utf-8'});

var indexName = tableName.replace(".", "_");
sql = util.format(sql, tableName, indexName, tableName, indexName, tableName);
return sql;
};


Massive.prototype.dropTable = function(table, options, next) {
var sql = this.dropTableSql(table, options);
this.query(sql, function(err, res) {
...
```

#### <a name="apidoc.element.massive.query.prototype.queryOptions"></a>[function <span class="apidocSignatureSpan">massive.query.prototype.</span>queryOptions ()](#apidoc.element.massive.query.prototype.queryOptions)
- description and source-code
```javascript
queryOptions = function () {
  if (_.isArray(this.order)) {
    var orderBody = this.orderBody;

    this.order = _.reduce(this.order, function (acc, val) {
      val.direction = val.direction || "asc";

      if (orderBody) {
        val.field = util.format("body->>'%s'", val.field);
      }

      if (val.type) {
        acc.push(util.format("(%s)::%s %s", val.field, val.type, val.direction));
      } else {
        acc.push(util.format("%s %s", val.field, val.direction));
      }

      return acc;
    }, []).join(",");
  }

  var sql = "";

  if (this.order) { sql = " order by " + this.order; }
  if (this.offset) { sql += " offset " + this.offset; }
  if (this.limit || this.single) { sql += " limit " + (this.limit || "1"); }

  return sql;
}
```
- example usage
```shell
...
this.stream = args.stream;
this.single = args.single || false;
};

Query.prototype.format = function (where) {
var from = this.only ? " FROM ONLY " : " FROM ";

return "SELECT " + this.selectList() + from + this.source + where + this.queryOptions();
};

Query.prototype.selectList = function () {
if (_.isArray(this.columns)) {
  return this.columns.join(',');
}
...
```

#### <a name="apidoc.element.massive.query.prototype.selectList"></a>[function <span class="apidocSignatureSpan">massive.query.prototype.</span>selectList ()](#apidoc.element.massive.query.prototype.selectList)
- description and source-code
```javascript
selectList = function () {
  if (_.isArray(this.columns)) {
    return this.columns.join(',');
  }

  return this.columns;
}
```
- example usage
```shell
...
this.stream = args.stream;
this.single = args.single || false;
};

Query.prototype.format = function (where) {
var from = this.only ? " FROM ONLY " : " FROM ";

return "SELECT " + this.selectList() + from + this.source + where + this.queryOptions();
};

Query.prototype.selectList = function () {
if (_.isArray(this.columns)) {
  return this.columns.join(',');
}
...
```



# <a name="apidoc.module.massive.queryable"></a>[module massive.queryable](#apidoc.module.massive.queryable)

#### <a name="apidoc.element.massive.queryable.queryable"></a>[function <span class="apidocSignatureSpan">massive.</span>queryable ()](#apidoc.element.massive.queryable.queryable)
- description and source-code
```javascript
queryable = function () {
  Entity.apply(this, arguments);

  // create delimited names now instead of at query time
  this.delimitedName = "\"" + this.name + "\"";
  this.delimitedSchema = "\"" + this.schema + "\"";

  // handle naming when schema is other than public:
  if(this.schema !== "public") {
    this.fullname = this.schema + "." + this.name;
    this.delimitedFullName = this.delimitedSchema + "." + this.delimitedName;
  } else {
    this.fullname = this.name;
    this.delimitedFullName = this.delimitedName;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.queryable.super_"></a>[function <span class="apidocSignatureSpan">massive.queryable.</span>super_ (args)](#apidoc.element.massive.queryable.super_)
- description and source-code
```javascript
super_ = function (args) {
  this.schema = args.schema || 'public';
  this.name = args.name;
  this.db = args.db;

  // create delimited names now instead of at query time
  this.delimitedName = "\"" + this.name + "\"";
  this.delimitedSchema = "\"" + this.schema + "\"";

  // handle naming when schema is other than public:
  if(this.schema !== "public") {
    this.fullname = this.schema + "." + this.name;
    this.delimitedFullName = this.delimitedSchema + "." + this.delimitedName;
  } else {
    this.fullname = this.name;
    this.delimitedFullName = this.delimitedName;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.massive.queryable.prototype"></a>[module massive.queryable.prototype](#apidoc.module.massive.queryable.prototype)

#### <a name="apidoc.element.massive.queryable.prototype.count"></a>[function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>count ()](#apidoc.element.massive.queryable.prototype.count)
- description and source-code
```javascript
count = function () {
  var args;
  var where;

  if (_.isObject(arguments[0])) {
    args = ArgTypes.findArgs(arguments, this);
    where = _.isEmpty(args.conditions) ? {where : " "} : Where.forTable(args.conditions);
  } else {
    args = ArgTypes.whereArgs(arguments, this);
    where = {where: " where " + args.where};
  }

  args.query.columns = "COUNT(1)";
  args.query.order = null;
  var sql = args.query.format(where.where);

  this.db.query(sql, where.params || args.params, {single : true}, function(err, res) {
    if (err) args.next(err, null);
    else args.next(null, res.count);
  });
}
```
- example usage
```shell
...
});
};
Queryable.prototype.findOneSync = DA(Queryable.prototype.findOne);

/**
 * Counts rows and calls back with any error and the total. There are two ways to use this method:
 *
 * 1. find() style: db.mytable.count({field: value}, callback);
 * 2. where() style: db.mytable.count("field=$1", [value], callback);
 */
Queryable.prototype.count = function() {
var args;
var where;

if (_.isObject(arguments[0])) {
...
```

#### <a name="apidoc.element.massive.queryable.prototype.countSync"></a>[function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>countSync ()](#apidoc.element.massive.queryable.prototype.countSync)
- description and source-code
```javascript
countSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.queryable.prototype.find"></a>[function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>find ()](#apidoc.element.massive.queryable.prototype.find)
- description and source-code
```javascript
find = function () {
  var args = ArgTypes.findArgs(arguments, this);

  if (typeof this.primaryKeyName === 'function' && Where.isPkSearch(args.conditions)) {
    var newArgs = {};
    newArgs[this.primaryKeyName()] = args.conditions;
    args.conditions = newArgs;
    args.query.single = true;
  }

  var where = _.isEmpty(args.conditions) ? {where: " "} : Where.forTable(args.conditions);
  var sql = args.query.format(where.where);

  if (args.query.stream) {
    this.db.stream(sql, where.params, args.query, args.next);
  } else {
    this.db.query(sql, where.params, args.query, args.next);
  }
}
```
- example usage
```shell
...

'''javascript
var massive = require("massive");

//you can use db for 'database name' running on localhost
//or send in everything using 'connectionString'
massive.connect({db : "myDb"}, function(err,db){
  db.myTable.find();
});
'''
## Usage

One of the key features of Massive is that it loads all of your tables, Postgres functions, and local query files up as functions
 (this is really cool, you want this. See below for more info). Massive is fast, and does this quickly. However, there is a one-
time execution penalty at intialization while all this happens. In most situations it makes sense to do this once, at application
 load. From there, maintain a reference to the Massive instance (Massive was conceived with this usage in mind). For example, if
 you are using Express as your application framework, you might do something like this:

####Express Example
...
```

#### <a name="apidoc.element.massive.queryable.prototype.findOne"></a>[function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>findOne ()](#apidoc.element.massive.queryable.prototype.findOne)
- description and source-code
```javascript
findOne = function () {
  var args = ArgTypes.findArgs(arguments, this);

  this.find(args.conditions, args.query, function(err,results) {
    if (err) {
      args.next(err,null);
    } else {
      var result;

      if (_.isArray(results)) {
        if (results.length > 0) { result = results[0]; }
      } else {
        result = results;
      }

      args.next(null,result);
    }
  });
}
```
- example usage
```shell
...
  columns : ["sku", "name"]
}
db.products.find({}, options, function(err,products){
  // an array of sku and name
});

//find a single user by id
db.users.findOne(1, function(err,user){
  //returns user with id (or whatever your PK is) of 1
});

//another way to do the above
db.users.find(1, function(err,user){
  //returns user with id (or whatever your PK is) of 1
});
...
```

#### <a name="apidoc.element.massive.queryable.prototype.findOneSync"></a>[function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>findOneSync ()](#apidoc.element.massive.queryable.prototype.findOneSync)
- description and source-code
```javascript
findOneSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
...
'''

## Synchronous Methods

Just about every method in Massive has a synchronous counterpart using [the deasync library](https://github.com/vkurchatkin/deasync
). These methods are here for convenience when you're not worried about I/O and just want to move some data around without a callback
 mess.

'''js
var myUser = db.users.findOneSync({id : 1});
'''

## We <3 Functions

Got a ~~tightly-wound~~ super-concientous DBA who ~~micro-manages~~ carefully limits developer access to the back end store? Feel
 bold, adventurous, and [unconstrained by popular dogma](http://rob.conery.io/2015/02/21/its-time-to-get-over-that-stored-procedure
-aversion-you-have/) about database functions/stored procedures? Unafraid to be called names by your less-enlightened friends?

Massive treats Postgres functions ("sprocs") as first-class citizens.
...
```

#### <a name="apidoc.element.massive.queryable.prototype.findSync"></a>[function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>findSync ()](#apidoc.element.massive.queryable.prototype.findSync)
- description and source-code
```javascript
findSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.queryable.prototype.search"></a>[function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>search (args, next)](#apidoc.element.massive.queryable.prototype.search)
- description and source-code
```javascript
search = function (args, next){
  //search expects a columns array and the term
  assert(args.columns && args.term, "Need columns as an array and a term string");

  if(!_.isArray(args.columns)){
    args.columns = [args.columns];
  }

  var tsv;
  var vectorFormat = 'to_tsvector("%s")';
  if(args.columns.length === 1){
    tsv = util.format("%s", args.columns[0]);
  }else{
    vectorFormat = 'to_tsvector(%s)';
    tsv= util.format("concat('%s')", args.columns.join(", ', '"));
  }
  var sql = "select * from " + this.delimitedFullName + " where " + util.format(vectorFormat, tsv);
  sql+= " @@ to_tsquery($1);";

  this.db.query(sql, [args.term],next);
}
```
- example usage
```shell
...
The goal with this API is expressiveness and terseness - allowing you to think as little as possible about accessing your data.

## Full Text Search Built In

If you need to query a table or a document store using Postgres' built-in Full Text Indexing, you certainly can. Just use 'search
' or 'searchDoc' and we'll build the index on the fly:

'''javascript
db.users.search({columns :["email"], term: "rob"}, function(err,users){
  //all users with the word 'rob' in their email
});
'''

This works the same for documents as well (more on documents in next section):

'''javascript
...
```

#### <a name="apidoc.element.massive.queryable.prototype.searchSync"></a>[function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>searchSync ()](#apidoc.element.massive.queryable.prototype.searchSync)
- description and source-code
```javascript
searchSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.queryable.prototype.where"></a>[function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>where ()](#apidoc.element.massive.queryable.prototype.where)
- description and source-code
```javascript
where = function (){
  var args = ArgTypes.whereArgs(arguments, this);

  var sql = args.query.format("where " + args.where);

  this.db.query(sql, args.params, args.next);
}
```
- example usage
```shell
...

//straight up SQL
db.run("select * from products where id=$1", [1], function(err,product){
  //product 1
});

//simplified SQL with a where
db.products.where("id=$1 OR id=$2", [10,21], function(err,products){
  //products 10 and 21
});

//an IN query
db.products.find({id : [10,21]}, function(err,products){
  //products 10 and 21
});
...
```

#### <a name="apidoc.element.massive.queryable.prototype.whereSync"></a>[function <span class="apidocSignatureSpan">massive.queryable.prototype.</span>whereSync ()](#apidoc.element.massive.queryable.prototype.whereSync)
- description and source-code
```javascript
whereSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.massive.runner"></a>[module massive.runner](#apidoc.module.massive.runner)

#### <a name="apidoc.element.massive.runner.runner"></a>[function <span class="apidocSignatureSpan">massive.</span>runner (connectionString, defaults)](#apidoc.element.massive.runner.runner)
- description and source-code
```javascript
runner = function (connectionString, defaults) {
  this.connectionString = connectionString;
  this.defaults = defaults;

  if (defaults) {
    _.each(defaults, function (v, k) {
      pg.defaults[k] = v;
    });
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.massive.runner.prototype"></a>[module massive.runner.prototype](#apidoc.module.massive.runner.prototype)

#### <a name="apidoc.element.massive.runner.prototype.end"></a>[function <span class="apidocSignatureSpan">massive.runner.prototype.</span>end ()](#apidoc.element.massive.runner.prototype.end)
- description and source-code
```javascript
end = function (){
  pg.end();
}
```
- example usage
```shell
...
  var self = this;
  var fileSql = fs.readFileSync(args.file, {encoding: 'utf-8'});
  self.query({sql:fileSql, params: args.params, next: next});
};

// close connections immediately
DB.prototype.end = function(){
  pg.end();
};

module.exports = DB;
...
```

#### <a name="apidoc.element.massive.runner.prototype.executeSqlFile"></a>[function <span class="apidocSignatureSpan">massive.runner.prototype.</span>executeSqlFile (args, next)](#apidoc.element.massive.runner.prototype.executeSqlFile)
- description and source-code
```javascript
executeSqlFile = function (args, next){
  var self = this;
  var fileSql = fs.readFileSync(args.file, {encoding: 'utf-8'});
  self.query({sql:fileSql, params: args.params, next: next});
}
```
- example usage
```shell
...

  // ONLY allow whitelisted items:
  if(this.whitelist) {
tableSql = __dirname + "/lib/scripts/whitelist.sql";
parameters = [this.whitelist];
  }

  this.executeSqlFile({file : tableSql, params: parameters}, function(err, tables) {
if (err) { return next(err, null); }

_.each(tables, function(table){
  var _table = new Table({
    schema : table.schema,
    name : table.name,
    pk : table.pk,
...
```

#### <a name="apidoc.element.massive.runner.prototype.query"></a>[function <span class="apidocSignatureSpan">massive.runner.prototype.</span>query ()](#apidoc.element.massive.runner.prototype.query)
- description and source-code
```javascript
query = function () {
  //we expect sql, options, params and a callback
  var args = ArgTypes.queryArgs(arguments);
  var e = new Error();  // initialize error object before we do any async stuff to get a useful stacktrace

  //check to see if the params are an array, which they need to be
  //for the pg module
  if(_.isObject(args.params)){
    //we only need the values from the object,
    //so swap it out
    args.params = _.values(args.params);
  }

  //weird param bug that will mess up multiple statements
  //with the pg_node driver
  if(args.params === [{}]) args.params = [];

  pg.connect(this.connectionString, function (err, db, done) {
    if (err) {
      done();

      return args.next(err,null);
    }

    db.query(args.sql, args.params, function (err, result) {
      //we have the results, release the connection
      done();

      if (err) {
        //DO NOT THROW if there's a query error
        //bubble it up
        //handle if it's that annoying parameter issue
        //wish I could find a way to deal with this
        if (err.toString().indexOf("there is no parameter") > -1) {
          e.message = "You need to wrap your parameter into an array";
        } else {
          e.message = err.message || err.toString();
          e.code = err.code;
          e.detail = err.detail;
        }

        args.next(_.defaults(e, err), null);
      } else {
        //only return one result if single is sent in
        if (args.options.single) {
          result.rows = result.rows.length >= 0 ? result.rows[0] : null;
        }

        args.next(null, result.rows);
      }
    });
  });
}
```
- example usage
```shell
...
    }
  }
  return result;
};

Massive.prototype.run = function(){
  var args = ArgTypes.queryArgs(arguments);
  this.query(args);
};
Massive.prototype.runSync = DA(Massive.prototype.run);

Massive.prototype.loadQueries = function() {
  walkSqlFiles(this, this.scriptsDir);
};
...
```

#### <a name="apidoc.element.massive.runner.prototype.stream"></a>[function <span class="apidocSignatureSpan">massive.runner.prototype.</span>stream ()](#apidoc.element.massive.runner.prototype.stream)
- description and source-code
```javascript
stream = function () {
  //we expect sql, options, params and a callback
  var args = ArgTypes.queryArgs(arguments);

  //check to see if the params are an array, which they need to be
  //for the pg module
  if(_.isObject(args.params)){
    //we only need the values from the object,
    //so swap it out
    args.params = _.values(args.params);
  }

  //weird param bug that will mess up multiple statements
  //with the pg_node driver
  if(args.params === [{}]) args.params = [];

  pg.connect(this.connectionString, function (err, db, done) {
    if (err) {
      done();

      return args.next(err,null);
    }

    var query = new QueryStream(args.sql, args.params);

    var stream = db.query(query);

    stream.on('end', done);

    args.next(null, stream);
  });
}
```
- example usage
```shell
...
// console.log("invoke opts: ", opts);
// console.log("invoke params: ", params);

var singleRow = this.singleRow && !opts.stream;
var singleValue = this.singleValue;

if (opts.stream) {
  this.db.stream(this.sql, params, null, function (err, stream) {
    if (err) return next(err);
    if (singleValue) {
      var singleValueTransform = SingleValueStream();
      return next(null, stream.pipe(singleValueTransform));
    } else {
      return next(null, stream);
    }
...
```



# <a name="apidoc.module.massive.table"></a>[module massive.table](#apidoc.module.massive.table)

#### <a name="apidoc.element.massive.table.table"></a>[function <span class="apidocSignatureSpan">massive.</span>table (args)](#apidoc.element.massive.table.table)
- description and source-code
```javascript
table = function (args) {
  Queryable.apply(this, arguments);

  this.pk = args.pk;

  _.extend(this,DocumentTable);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.table.super_"></a>[function <span class="apidocSignatureSpan">massive.table.</span>super_ ()](#apidoc.element.massive.table.super_)
- description and source-code
```javascript
super_ = function () {
  Entity.apply(this, arguments);

  // create delimited names now instead of at query time
  this.delimitedName = "\"" + this.name + "\"";
  this.delimitedSchema = "\"" + this.schema + "\"";

  // handle naming when schema is other than public:
  if(this.schema !== "public") {
    this.fullname = this.schema + "." + this.name;
    this.delimitedFullName = this.delimitedSchema + "." + this.delimitedName;
  } else {
    this.fullname = this.name;
    this.delimitedFullName = this.delimitedName;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.massive.table.prototype"></a>[module massive.table.prototype](#apidoc.module.massive.table.prototype)

#### <a name="apidoc.element.massive.table.prototype.containsPk"></a>[function <span class="apidocSignatureSpan">massive.table.prototype.</span>containsPk (args)](#apidoc.element.massive.table.prototype.containsPk)
- description and source-code
```javascript
containsPk = function (args){
  var keys = _.keys(args);
  return (keys.indexOf(this.primaryKeyName()) > -1) || (keys.indexOf(this.delimitedPrimaryKeyName()) > -1);
}
```
- example usage
```shell
...
  var keys = _.keys(args);
  return (keys.indexOf(this.primaryKeyName()) > -1) || (keys.indexOf(this.delimitedPrimaryKeyName()) > -1);
};

Table.prototype.save = function(args, next){
  assert(_.isObject(args), "Please pass in the criteria for saving as an object. This should include all fields needed to change
 or add. Include the primary key for an UPDATE.");

  if(this.containsPk(args)){
    this.update(args,next);
  }else{
    this.insert(args,next);
  }
};
Table.prototype.saveSync = DA(Table.prototype.save);
...
```

#### <a name="apidoc.element.massive.table.prototype.delimitedPrimaryKeyName"></a>[function <span class="apidocSignatureSpan">massive.table.prototype.</span>delimitedPrimaryKeyName ()](#apidoc.element.massive.table.prototype.delimitedPrimaryKeyName)
- description and source-code
```javascript
delimitedPrimaryKeyName = function () {
  return util.format('"%s"', this.pk);
}
```
- example usage
```shell
...

Table.prototype.delimitedPrimaryKeyName = function() {
return util.format('"%s"', this.pk);
};

Table.prototype.containsPk = function(args){
var keys = _.keys(args);
return (keys.indexOf(this.primaryKeyName()) > -1) || (keys.indexOf(this.delimitedPrimaryKeyName()) > -1);
};

Table.prototype.save = function(args, next){
assert(_.isObject(args), "Please pass in the criteria for saving as an object. This should include all fields needed to change or
 add. Include the primary key for an UPDATE.");

if(this.containsPk(args)){
  this.update(args,next);
...
```

#### <a name="apidoc.element.massive.table.prototype.destroy"></a>[function <span class="apidocSignatureSpan">massive.table.prototype.</span>destroy (args, next)](#apidoc.element.massive.table.prototype.destroy)
- description and source-code
```javascript
destroy = function (args, next){
  assert(_.isObject(args), "Please pass in the criteria for deleting. This should be in object format - {id : 1} for example");
  var sql = "DELETE FROM ONLY " + this.delimitedFullName;
  var where = {};

  if (Object.keys(args).length > 0) {
    where = Where.forTable(args);
    sql += where.where;
  }

  sql += " RETURNING *";
  this.db.query(sql, where.params, next);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.table.prototype.destroySync"></a>[function <span class="apidocSignatureSpan">massive.table.prototype.</span>destroySync ()](#apidoc.element.massive.table.prototype.destroySync)
- description and source-code
```javascript
destroySync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.table.prototype.insert"></a>[function <span class="apidocSignatureSpan">massive.table.prototype.</span>insert (data, next)](#apidoc.element.massive.table.prototype.insert)
- description and source-code
```javascript
insert = function (data, next) {
  var returnSingle = false;

  if (!data) {
    return next(new Error("insert should be called with data"));
  } else if (!_.isArray(data)) {
    returnSingle = true;
    data = [data];
  } else if (data.length === 0) {
    return next(null, []);  // just return empty arrays so bulk inserting variable-length lists is more friendly
  }

  var delimitedColumnNames = _.map(_.keys(data[0]), function(key){return util.format('"%s"', key);});
  var sql = util.format("INSERT INTO %s (%s) VALUES\n", this.delimitedFullName, delimitedColumnNames.join(", "));
  var parameters = [];
  var values = [];
  var fn = function() { return "$" + (++seed); };

  for(var i = 0, seed = 0; i < data.length; ++i) {
    var v = _.map(data[i], fn);
    values.push(util.format('(%s)', v.join(', ')));
    parameters.push(_.values(data[i]));
  }
  sql += values.join(",\n");
  sql += " RETURNING *";
  this.db.query(sql, _.flatten(parameters, true), {single : returnSingle}, next);
}
```
- example usage
```shell
...

Table.prototype.save = function(args, next){
assert(_.isObject(args), "Please pass in the criteria for saving as an object. This should include all fields needed to change or
 add. Include the primary key for an UPDATE.");

if(this.containsPk(args)){
  this.update(args,next);
}else{
  this.insert(args,next);
}
};
Table.prototype.saveSync = DA(Table.prototype.save);

Table.prototype.destroy = function(args, next){
assert(_.isObject(args), "Please pass in the criteria for deleting. This should be in object format - {id : 1} for example");
var sql = "DELETE FROM ONLY " + this.delimitedFullName;
...
```

#### <a name="apidoc.element.massive.table.prototype.insertSync"></a>[function <span class="apidocSignatureSpan">massive.table.prototype.</span>insertSync ()](#apidoc.element.massive.table.prototype.insertSync)
- description and source-code
```javascript
insertSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.table.prototype.primaryKeyName"></a>[function <span class="apidocSignatureSpan">massive.table.prototype.</span>primaryKeyName ()](#apidoc.element.massive.table.prototype.primaryKeyName)
- description and source-code
```javascript
primaryKeyName = function (){
  return this.pk;
}
```
- example usage
```shell
...
this.executeDocQuery(sql, params, args.options, args.next);
};
exports.searchDocSync = DA(this.searchDoc);

exports.saveDoc = function(args, next) {
assert(_.isObject(args), "Please pass in the document for saving as an object. Include the primary key for an UPDATE.");
var sql, params = [];
var pkName = this.primaryKeyName();
var pkVal = args[pkName];

// if there's a primary key, don't store it in the body as well
params.push(JSON.stringify(_.omit(args, pkName)));

if (pkVal) {
  sql = util.format("update %s set body = $1 where %s = $2 returning *;", this.fullname, pkName);
...
```

#### <a name="apidoc.element.massive.table.prototype.save"></a>[function <span class="apidocSignatureSpan">massive.table.prototype.</span>save (args, next)](#apidoc.element.massive.table.prototype.save)
- description and source-code
```javascript
save = function (args, next){
  assert(_.isObject(args), "Please pass in the criteria for saving as an object. This should include all fields needed to change
 or add. Include the primary key for an UPDATE.");

  if(this.containsPk(args)){
    this.update(args,next);
  }else{
    this.insert(args,next);
  }
}
```
- example usage
```shell
...

//simple query
db.users.find({active: true}, function(err,users){
  //all users who are active
});

//include the PK in the criteria for an update
db.users.save({id : 1, email : "test@example.com"}, function(err,updated){
  //the updated record for the new user
});

//no PK does an INSERT
db.users.save({email : "new@example.com"}, function(err,inserted){
  //the new record with the ID
});
...
```

#### <a name="apidoc.element.massive.table.prototype.saveSync"></a>[function <span class="apidocSignatureSpan">massive.table.prototype.</span>saveSync ()](#apidoc.element.massive.table.prototype.saveSync)
- description and source-code
```javascript
saveSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.table.prototype.search"></a>[function <span class="apidocSignatureSpan">massive.table.prototype.</span>search ()](#apidoc.element.massive.table.prototype.search)
- description and source-code
```javascript
search = function (){
  var args = ArgTypes.searchArgs(arguments, this);

  //search expects a columns array and the term
  assert(args.fields.columns && args.fields.term, "Need columns as an array and a term string");
  var params = [args.fields.term];
  if(!_.isArray(args.fields.columns)){
    args.fields.columns = [args.fields.columns];
  }
  var tsv;
  var vectorFormat = 'to_tsvector("%s")';
  if(args.fields.columns.length === 1){
    tsv = util.format("%s", args.fields.columns[0]);
    if(args.fields.columns[0].indexOf('>>') !== -1){
      vectorFormat = 'to_tsvector(%s)';
    }
  }else{
    vectorFormat = 'to_tsvector(%s)';
    tsv= util.format("concat(%s)", args.fields.columns.join(", ' ', "));
  }

  var whereString = "";
  if (args.fields.where) {
    var where = Where.forTable(args.fields.where, 'predicate', 1, " AND ");
    whereString = where.where;
    params = params.concat(where.params);
  }
  var sql = args.query.format(util.format(" WHERE " + vectorFormat + " @@ to_tsquery($1) %s", tsv, whereString));
  this.db.query(sql, params, args.options, args.next);
}
```
- example usage
```shell
...
The goal with this API is expressiveness and terseness - allowing you to think as little as possible about accessing your data.

## Full Text Search Built In

If you need to query a table or a document store using Postgres' built-in Full Text Indexing, you certainly can. Just use 'search
' or 'searchDoc' and we'll build the index on the fly:

'''javascript
db.users.search({columns :["email"], term: "rob"}, function(err,users){
  //all users with the word 'rob' in their email
});
'''

This works the same for documents as well (more on documents in next section):

'''javascript
...
```

#### <a name="apidoc.element.massive.table.prototype.searchSync"></a>[function <span class="apidocSignatureSpan">massive.table.prototype.</span>searchSync ()](#apidoc.element.massive.table.prototype.searchSync)
- description and source-code
```javascript
searchSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.table.prototype.update"></a>[function <span class="apidocSignatureSpan">massive.table.prototype.</span>update (conditions, fields, next)](#apidoc.element.massive.table.prototype.update)
- description and source-code
```javascript
update = function (conditions, fields, next) {
  var hasConditions = true;
  var options = {};

  if (_.isFunction(fields)) {
    var pkName = this.primaryKeyName();

    hasConditions = false;
    next = fields;
    fields = conditions;
    conditions = {};

    conditions[pkName] = fields[pkName];

    fields = _.omit(fields, function(value, key, object) {
      return _.isFunction(object[key]) || key === pkName;
    });

    options.single = true;
  }

  assert(_.isObject(fields), "Update requires a hash of fields=>values to update to");

  if (_.isEmpty(fields)) {
    // there's nothing to update, so just return the matching records
    if (options.single) {
      return this.findOne(conditions, next);
    } else {
      return this.find(conditions, next);
    }
  }

  var parameters = [];
  var f = [];
  var seed = 0;

  _.each(fields, function(value, key) {
    f.push(util.format('"%s" = $%s', key, (++seed)));
    parameters.push(value);
  });

  var sql = util.format("UPDATE ONLY %s SET %s", this.delimitedFullName, f.join(', '));

  if (!hasConditions || !_.isEmpty(conditions)) {
    var parsedWhere = Where.forTable(conditions, parameters.length);

    sql += parsedWhere.where;
  }

  sql += " RETURNING *";

  parameters = parameters.concat(
    _.chain(conditions)
    .values()
    .flatten()
    .without(null)  // nulls are inlined in the WHERE
    .value()
  );

  this.db.query(sql, parameters, options, next);
}
```
- example usage
```shell
...
  return (keys.indexOf(this.primaryKeyName()) > -1) || (keys.indexOf(this.delimitedPrimaryKeyName()) > -1);
};

Table.prototype.save = function(args, next){
  assert(_.isObject(args), "Please pass in the criteria for saving as an object. This should include all fields needed to change
 or add. Include the primary key for an UPDATE.");

  if(this.containsPk(args)){
    this.update(args,next);
  }else{
    this.insert(args,next);
  }
};
Table.prototype.saveSync = DA(Table.prototype.save);

Table.prototype.destroy = function(args, next){
...
```

#### <a name="apidoc.element.massive.table.prototype.updateSync"></a>[function <span class="apidocSignatureSpan">massive.table.prototype.</span>updateSync ()](#apidoc.element.massive.table.prototype.updateSync)
- description and source-code
```javascript
updateSync = function () {
			var done = false;
			var args = Array.prototype.slice.apply(arguments).concat(cb);
			var err;
			var res;

			fn.apply(this, args);
			module.exports.loopWhile(function(){return !done;});
			if (err)
				throw err;

			return res;

			function cb(e, r) {
				err = e;
				res = r;
				done = true;		
			}
		}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.massive.where"></a>[module massive.where](#apidoc.module.massive.where)

#### <a name="apidoc.element.massive.where.docPredicate"></a>[function <span class="apidocSignatureSpan">massive.where.</span>docPredicate (result, condition, value, conditions)](#apidoc.element.massive.where.docPredicate)
- description and source-code
```javascript
docPredicate = function (result, condition, value, conditions) {
  //if we have an array of objects, this is a deep traversal
  //we'll need to use a contains query to be sure we flex the index
  if(_.isArray(value) && _.isObject(value[0])) {
    //stringify the passed-in params
    result.params.push(JSON.stringify(conditions));
    result.predicates.push(util.format("body @> $%s", result.params.length + result.offset));
  }

  //if we have equality here, just use a JSON contains
  else if (condition.operator === '=' && !_.isArray(value)) {
    //parse the value into stringy JSON
    var param = {};
    param[condition.field]=value;
    result.params.push(JSON.stringify(param));
    result.predicates.push(util.format("body @> $%s", result.params.length + result.offset));
    return result;
  }

  //comparison stuff - same as method above but this time
  //we'll be coercing the document key values using pg's ::
  //not ideal, but it works nicely
  else if (_.isBoolean(value)) {
    result.predicates.push(
      util.format("(body ->> '%s')::boolean %s %s", condition.field, condition.operator, value)
    );
  } else if(_.isDate(value)) {
    result.params.push(value);
    result.predicates.push(
      util.format("(body ->> '%s')::timestamp %s $%d",
        condition.field,
        condition.operator,
        result.params.length + result.offset)
    );
  } else if(_.isNumber(value)) {
    result.predicates.push(
      util.format("(body ->> '%s')::decimal %s %d", condition.field, condition.operator, value)
    );
  }

  //anything non-array handling
  else if (!_.isArray(value)) {
    result.params.push(value);
    result.predicates.push(
      util.format("(body ->> '%s') %s $%s",
        condition.field,
        condition.operator,
        result.params.length + result.offset)
    );
  } else {
    var arrayConditions = [];

    _.each(value, function(v) {
      result.params.push(v);
      arrayConditions.push("$" + (result.params.length + result.offset));
    });

    condition.operator = condition.operator === '=' ? 'IN' : 'NOT IN';

    result.predicates.push(
      util.format("(body ->> '%s') %s (%s)",
        condition.field,
        condition.operator,
        arrayConditions.join(', '))
    );
  }

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.massive.where.forTable"></a>[function <span class="apidocSignatureSpan">massive.where.</span>forTable ()](#apidoc.element.massive.where.forTable)
- description and source-code
```javascript
forTable = function () {
  var args = ArgTypes.forArgs(arguments);

  if (_.isEmpty(args.conditions)) {
    return {
      where: args.prefix + 'TRUE',
      params: []
    };
  }

  var result = exports.generate({
    params: [],
    predicates: [],
    offset: args.placeholderOffset
  }, args.conditions, args.generator);

  return {
    where: args.prefix + result.predicates.join(' \nAND '),
    params: result.params
  };
}
```
- example usage
```shell
...

    if (keys.length === 1) {
var operator = keys[0].match("<=|>=|!=|<>|=|<|>");
var property = keys[0].replace(operator, "").trim();
if (property == this.primaryKeyName()) {
  // this is a query against the PK...we can use the
  // plain old table "where" builder:
  where = Where.forTable(conditions, 'predicate', offset, prefix);

  // only a true pk query if testing equality
  if ((operator === null || operator === "=") && !_.isObject(conditions[keys[0]])) {
    where.pkQuery = true;
  }
} else {
  where = Where.forTable(conditions, 'docPredicate', offset, prefix);
...
```

#### <a name="apidoc.element.massive.where.generate"></a>[function <span class="apidocSignatureSpan">massive.where.</span>generate (result, conditions, generator)](#apidoc.element.massive.where.generate)
- description and source-code
```javascript
generate = function (result, conditions, generator) {
  _.each(conditions, function(value, key) {
    var condition = exports.parseKey(key);

    if (condition.field === 'or') {
      if (!_.isArray(value)) { value = [value]; }

      var groupResult = _.reduce(value, function (acc, v) {
        // assemble predicates for each subgroup in this 'or' array
        var subResult = exports.generate({
          params: [],
          predicates: [],
          offset: result.params.length + acc.offset   // ensure the offset from predicates outside the subgroup is counted
        }, v, generator);

        // encapsulate and join the individual predicates with AND to create the complete subgroup predicate
        acc.predicates.push(util.format('(%s)', subResult.predicates.join(' AND ')));
        acc.params = acc.params.concat(subResult.params);
        acc.offset += subResult.params.length;

        return acc;
      }, {
        params: [],
        predicates: [],
        offset: result.offset
      });

      // join the compiled subgroup predicates with OR, encapsulate, and push the
      // complex predicate ("((x = $1 AND y = $2) OR (z = $3))") onto the result object
      result.params = result.params.concat(groupResult.params);
      result.predicates.push(util.format('(%s)', groupResult.predicates.join(' OR ')));
    } else {
      // no special behavior, just add this predicate and modify result in-place
      result = exports[generator](result, condition, value, conditions);
    }
  });

  return result;
}
```
- example usage
```shell
...
    var condition = exports.parseKey(key);

    if (condition.field === 'or') {
      if (!_.isArray(value)) { value = [value]; }

      var groupResult = _.reduce(value, function (acc, v) {
// assemble predicates for each subgroup in this 'or' array
var subResult = exports.generate({
  params: [],
  predicates: [],
  offset: result.params.length + acc.offset   // ensure the offset from predicates outside the subgroup is counted
}, v, generator);

// encapsulate and join the individual predicates with AND to create the complete subgroup predicate
acc.predicates.push(util.format('(%s)', subResult.predicates.join(' AND ')));
...
```

#### <a name="apidoc.element.massive.where.isPkSearch"></a>[function <span class="apidocSignatureSpan">massive.where.</span>isPkSearch (conditions)](#apidoc.element.massive.where.isPkSearch)
- description and source-code
```javascript
isPkSearch = function (conditions) {
  return _.isNumber(conditions) || (_.isString(conditions) && isUuid.test(conditions));
}
```
- example usage
```shell
...
if(_.isFunction(conditions) || conditions == "*") {
  // no criteria provided - treat like select *
  where.where = "";
  where.params = [];
  return where;
}

if (Where.isPkSearch(conditions)) {
  //assume it's a search on ID
  conditions = {id : conditions};
}

if (_.isObject(conditions)) {
  var keys = _.keys(conditions);
...
```

#### <a name="apidoc.element.massive.where.parseKey"></a>[function <span class="apidocSignatureSpan">massive.where.</span>parseKey (key)](#apidoc.element.massive.where.parseKey)
- description and source-code
```javascript
parseKey = function (key) {
  // remove single quotes from JSON keys, then split on double quotes to break
  // out "quoted field"s safely
  var parts = strip(key.replace(/\'/g, '').split('"')),
    operation = getOp(key),
    separators = ['::', '\\-\\>\\>','\\#\\>\\>'],
    re;

  if (operation.key) {
    // we found an operation, include the escaped key in the separators when we tokenize
    separators.push(operation.key.replace(/([^a-zA-Z0-9\s])/g, '\\$1'));
  }

  // capture separators in output array
  re = new RegExp(util.format("(%s)", separators.join('|')), 'i');

  if (parts.length === 0) {
    // the field wasn't quoted, so parts[0] is the whole thing
    parts = strip(parts[0].split(re));
  } else {
    // the field was quoted, so parts[0] is the full field name, but parts[1]
    // may contain JSON traversal and/or operations so split it up on those
    parts = parts.concat(strip(parts.pop().split(re)));
  }

  var field = parts.shift(),
    quotedField;

  if (parts[0] === '::') {
    // casting
    var type = parts.shift() && parts.shift();

    quotedField = util.format('"%s"::%s', field, type);
    field = util.format('%s::%s', field, type);
  } else {
    quotedField = util.format('"%s"', field);
  }

  if (parts[0] === '->>' || parts[0] === '#>>') {
    // json operation. pull the op and key out and append them to the field.
    var jsonOp = parts.shift();
    var jsonKey = parts.shift();

    // treat numeric json keys as array indices, otherwise quote it
    if (isNaN(jsonKey)) { jsonKey = util.format("'%s'", jsonKey); }

    quotedField = util.format('%s%s%s', quotedField, jsonOp, jsonKey);
  }

  return {
    field: field,
    quotedField: quotedField,
    operator: operation.operator || '=',
    mutator: operation.mutator
  };
}
```
- example usage
```shell
...
  }

  return result;
};

exports.generate = function (result, conditions, generator) {
  _.each(conditions, function(value, key) {
    var condition = exports.parseKey(key);

    if (condition.field === 'or') {
if (!_.isArray(value)) { value = [value]; }

var groupResult = _.reduce(value, function (acc, v) {
  // assemble predicates for each subgroup in this 'or' array
  var subResult = exports.generate({
...
```

#### <a name="apidoc.element.massive.where.predicate"></a>[function <span class="apidocSignatureSpan">massive.where.</span>predicate (result, condition, value)](#apidoc.element.massive.where.predicate)
- description and source-code
```javascript
predicate = function (result, condition, value) {
  if (value === null) {
    //interpolate nulls directly with is/is not
    condition.operator = condition.operator === '=' ? 'IS' : 'IS NOT';
  } else if (condition.mutator || !_.isArray(value)) {
    //parameterize any non-array or mutatey values
    if (condition.mutator) { value = condition.mutator(value); }
    result.params.push(value);
    value = util.format("$%s", result.params.length + result.offset);
  } else if (_.isArray(value)) {
    var arrayConditions = [];

    //loop the array
    _.each(value, function(v) {
      result.params.push(v);
      arrayConditions.push(util.format("$%s", result.params.length + result.offset));
    });

    condition.operator = condition.operator === '=' ? 'IN' : 'NOT IN';

    value = util.format('(%s)', arrayConditions.join(', '));
  }

  result.predicates.push(util.format('%s %s %s', condition.quotedField, condition.operator, value));

  return result;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
