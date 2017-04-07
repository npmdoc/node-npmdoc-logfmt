# api documentation for  [logfmt (v1.2.0)](https://github.com/csquared/node-logfmt)  [![npm package](https://img.shields.io/npm/v/npmdoc-logfmt.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-logfmt) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-logfmt.svg)](https://travis-ci.org/npmdoc/node-npmdoc-logfmt)
#### key=value logger and parser

[![NPM](https://nodei.co/npm/logfmt.png?downloads=true)](https://www.npmjs.com/package/logfmt)

[![apidoc](https://npmdoc.github.io/node-npmdoc-logfmt/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-logfmt_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-logfmt/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-logfmt/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-logfmt/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "csquared"
    },
    "bin": {
        "logfmt": "./bin/logfmt"
    },
    "bugs": {
        "url": "https://github.com/csquared/node-logfmt/issues"
    },
    "dependencies": {
        "lodash": "~2.4.1",
        "split": "0.2.x",
        "through": "2.3.x"
    },
    "description": "key=value logger and parser",
    "devDependencies": {
        "express": "3.3.x",
        "mocha": "*",
        "restify": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "1ccc067c1cfe65f3ecf5856c09d2654f69203572",
        "tarball": "https://registry.npmjs.org/logfmt/-/logfmt-1.2.0.tgz"
    },
    "homepage": "https://github.com/csquared/node-logfmt",
    "keywords": [
        "log",
        "parser",
        "logfmt"
    ],
    "license": "MIT",
    "main": "logfmt.js",
    "maintainers": [
        {
            "name": "csquared",
            "email": "christopher.continanza@gmail.com"
        }
    ],
    "name": "logfmt",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/csquared/node-logfmt.git"
    },
    "scripts": {
        "test": "mocha"
    },
    "version": "1.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module logfmt](#apidoc.module.logfmt)
1.  [function <span class="apidocSignatureSpan">logfmt.</span>bodyParser (options)](#apidoc.element.logfmt.bodyParser)
1.  [function <span class="apidocSignatureSpan">logfmt.</span>bodyParserStream (options)](#apidoc.element.logfmt.bodyParserStream)
1.  [function <span class="apidocSignatureSpan">logfmt.</span>error (err, id)](#apidoc.element.logfmt.error)
1.  [function <span class="apidocSignatureSpan">logfmt.</span>log (data, stream)](#apidoc.element.logfmt.log)
1.  [function <span class="apidocSignatureSpan">logfmt.</span>namespace (object)](#apidoc.element.logfmt.namespace)
1.  [function <span class="apidocSignatureSpan">logfmt.</span>parse (line)](#apidoc.element.logfmt.parse)
1.  [function <span class="apidocSignatureSpan">logfmt.</span>requestLogger (options, formatter)](#apidoc.element.logfmt.requestLogger)
1.  [function <span class="apidocSignatureSpan">logfmt.</span>streamParser (options)](#apidoc.element.logfmt.streamParser)
1.  [function <span class="apidocSignatureSpan">logfmt.</span>streamStringify (options)](#apidoc.element.logfmt.streamStringify)
1.  [function <span class="apidocSignatureSpan">logfmt.</span>stringify (data)](#apidoc.element.logfmt.stringify)
1.  [function <span class="apidocSignatureSpan">logfmt.</span>time (label)](#apidoc.element.logfmt.time)
1.  object <span class="apidocSignatureSpan">logfmt.</span>logfmt_parser
1.  object <span class="apidocSignatureSpan">logfmt.</span>logger
1.  object <span class="apidocSignatureSpan">logfmt.</span>request_logger
1.  object <span class="apidocSignatureSpan">logfmt.</span>streaming

#### [module logfmt.logfmt_parser](#apidoc.module.logfmt.logfmt_parser)
1.  boolean <span class="apidocSignatureSpan">logfmt.logfmt_parser.</span>debug
1.  [function <span class="apidocSignatureSpan">logfmt.logfmt_parser.</span>parse (line)](#apidoc.element.logfmt.logfmt_parser.parse)

#### [module logfmt.logger](#apidoc.module.logfmt.logger)
1.  [function <span class="apidocSignatureSpan">logfmt.logger.</span>error (err, id)](#apidoc.element.logfmt.logger.error)
1.  [function <span class="apidocSignatureSpan">logfmt.logger.</span>log (data, stream)](#apidoc.element.logfmt.logger.log)
1.  [function <span class="apidocSignatureSpan">logfmt.logger.</span>namespace (object)](#apidoc.element.logfmt.logger.namespace)
1.  [function <span class="apidocSignatureSpan">logfmt.logger.</span>time (label)](#apidoc.element.logfmt.logger.time)

#### [module logfmt.requestLogger](#apidoc.module.logfmt.requestLogger)
1.  [function <span class="apidocSignatureSpan">logfmt.</span>requestLogger (options, formatter)](#apidoc.element.logfmt.requestLogger.requestLogger)
1.  [function <span class="apidocSignatureSpan">logfmt.requestLogger.</span>commonFormatter (req, res)](#apidoc.element.logfmt.requestLogger.commonFormatter)

#### [module logfmt.request_logger](#apidoc.module.logfmt.request_logger)
1.  [function <span class="apidocSignatureSpan">logfmt.request_logger.</span>commonFormatter (req, res)](#apidoc.element.logfmt.request_logger.commonFormatter)
1.  [function <span class="apidocSignatureSpan">logfmt.request_logger.</span>init (logger, options, formatter)](#apidoc.element.logfmt.request_logger.init)

#### [module logfmt.streaming](#apidoc.module.logfmt.streaming)
1.  [function <span class="apidocSignatureSpan">logfmt.streaming.</span>streamParser (options)](#apidoc.element.logfmt.streaming.streamParser)
1.  [function <span class="apidocSignatureSpan">logfmt.streaming.</span>streamStringify (options)](#apidoc.element.logfmt.streaming.streamStringify)

#### [module logfmt.stringify](#apidoc.module.logfmt.stringify)
1.  [function <span class="apidocSignatureSpan">logfmt.</span>stringify (data)](#apidoc.element.logfmt.stringify.stringify)



# <a name="apidoc.module.logfmt"></a>[module logfmt](#apidoc.module.logfmt)

#### <a name="apidoc.element.logfmt.bodyParser"></a>[function <span class="apidocSignatureSpan">logfmt.</span>bodyParser (options)](#apidoc.element.logfmt.bodyParser)
- description and source-code
```javascript
bodyParser = function (options) {
  options || (options = {});
  var mime = options.contentType || "application/logplex-1";
  return bodyParser({ contentType: mime, parser: this.parse });
}
```
- example usage
```shell
...

## express/restify parsing middleware

'''javascript
  // streaming
  app.use(logfmt.bodyParserStream());
  // buffering
  app.use(logfmt.bodyParser());
'''

#### 'logfmt.bodyParserStream([opts])'

Valid Options:

- 'contentType': defaults to 'application/logplex-1'
...
```

#### <a name="apidoc.element.logfmt.bodyParserStream"></a>[function <span class="apidocSignatureSpan">logfmt.</span>bodyParserStream (options)](#apidoc.element.logfmt.bodyParserStream)
- description and source-code
```javascript
bodyParserStream = function (options) {
  options || (options = {});
  var mime = options.contentType || "application/logplex-1";
  return bodyParserStream({ contentType: mime });
}
```
- example usage
```shell
...
}).listen(3000);
'''

## express/restify parsing middleware

'''javascript
  // streaming
  app.use(logfmt.bodyParserStream());
  // buffering
  app.use(logfmt.bodyParser());
'''

#### 'logfmt.bodyParserStream([opts])'

Valid Options:
...
```

#### <a name="apidoc.element.logfmt.error"></a>[function <span class="apidocSignatureSpan">logfmt.</span>error (err, id)](#apidoc.element.logfmt.error)
- description and source-code
```javascript
error = function (err, id) {
  this.maxErrorLines = this.maxErrorLines || 10;
  if (id === undefined) {
    id = Math.random().toString().slice(2, 12);
  }
  var errorLogger = this.namespace({
    error: true,
    id:id,
    now: (new Date()).toISOString()
  })
  errorLogger.log({ message:err.message });
  if (err.stack) {
    var stack = err.stack.split('\n');
    for (var line in stack) {
      if (line >= this.maxErrorLines) break;
      errorLogger.log({ line:line, trace:stack[line] });
    }
  }
}
```
- example usage
```shell
...
var timer = logfmt.time('time').namespace({foo: 'bar'});
timer.log();
//=> time=1ms foo=bar
timer.log();
//=> time=2ms foo=bar
'''

### 'logfmt.error(error)'

Accepts a Javascript 'Error' object and converts it to logfmt format.

It will print up to 'logfmt.maxErrorLines' lines.

'''javascript
var logfmt = require('logfmt');
...
```

#### <a name="apidoc.element.logfmt.log"></a>[function <span class="apidocSignatureSpan">logfmt.</span>log (data, stream)](#apidoc.element.logfmt.log)
- description and source-code
```javascript
log = function (data, stream) {
  this.stream = this.stream || process.stdout;
  if(stream == undefined) stream = this.stream;

  var logData = _.extend({}, this.defaultData, data);

  if(this.timers){
    for(var key in this.timers){
      var now = (new Date()).getTime()
      logData[key] = (now - this.timers[key]).toString() + 'ms' ;
    }
  }

  stream.write(this.stringify(logData) + "\n");
}
```
- example usage
```shell
...
'''javascript
var logfmt2 = new logfmt;

// replace our stringify with JSON's
logfmt2.stringify = JSON.stringify

// now we log JSON!
logfmt2.log({foo: 'bar'})
// {"foo":"bar"}

// and the original logfmt is untouched
logfmt.log({foo: 'bar'})
// foo=bar
'''
...
```

#### <a name="apidoc.element.logfmt.namespace"></a>[function <span class="apidocSignatureSpan">logfmt.</span>namespace (object)](#apidoc.element.logfmt.namespace)
- description and source-code
```javascript
namespace = function (object) {
  var logfmt = require('../logfmt');
  var namespaced = new logfmt()
  var namespace  = _.extend({}, this.defaultData, object);
  namespaced.stream = this.stream;
  namespaced.defaultData = namespace
  namespaced.timers = this.timers;
  return namespaced;
}
```
- example usage
```shell
...
logfmt.log({hello: 'stdout'});
//=> hello=stdout

errorLogger.log({hello: 'stderr'});
//=> hello=stderr
'''

### 'logfmt.namespace(object)'

Returns a new 'logfmt' with object's data included in every 'log' call.

'''javascript
var logfmt = require('logfmt').namespace({app: 'logfmt'});

logfmt.log({ "foo": "bar", "a": 14, baz: 'hello kitty'})
...
```

#### <a name="apidoc.element.logfmt.parse"></a>[function <span class="apidocSignatureSpan">logfmt.</span>parse (line)](#apidoc.element.logfmt.parse)
- description and source-code
```javascript
parse = function (line) {
  var key = '';
  var value = '';
  var is_number = true;
  var in_key    = false;
  var in_value  = false;
  var in_quote  = false;
  var had_quote = false;
  var object    = {};
  var debug     = exports.debug;

  if(line[line.length - 1] == '\n'){
    line = line.slice(0,line.length - 1)
  }

  for(var i=0; i <= line.length; i++){

    if((line[i] == ' ' && !in_quote) || i == line.length){
      if(in_key && key.length > 0){
        object[key] = true;
      }else if(in_value){
        if(value == 'true') value = true;
        else if(value == 'false') value = false;
        else if(value === '' && !had_quote) value = null;
        object[key] = value;
        value = '';
      }

      if(i == line.length) break;
      else {
        in_key   = false;
        in_value = false;
        in_quote = false;
        had_quote = false;
      }
    }

    if(line[i] == '=' && !in_quote){
      if(debug) console.log('split')
      //split
      in_key = false;
      in_value = true;
    }
    else if(line[i] == '\\'){
      i ++ ;
      value += line[i];
      if(debug) console.log('escape: ' + line[i])
    }
    else if(line[i] == '"'){
      had_quote = true;
      in_quote = !in_quote;
      if(debug) console.log('in quote: ' + in_quote)
    }
    else if(line[i] != ' ' && !in_value && !in_key){
      if(debug) console.log('start key with: ' + line[i])
      in_key = true;
      key = line[i];
    }
    else if(in_key){
      if(debug) console.log('add to key: ' + line[i])
      key += line[i]
    }
    else if(in_value){
      if(debug) console.log('add to value: ' + line[i])
      value += line[i];
    }
  }

  return object;
}
```
- example usage
```shell
...

'''javascript
var logfmt = require('logfmt');

logfmt.stringify({foo: 'bar'});
// 'foo=bar'

logfmt.parse('foo=bar');
// {foo: 'bar'}
'''

It is also a constructor function, so you can use 'new logfmt' to create
a new 'logfmt' that you can configure differently.

'''javascript
...
```

#### <a name="apidoc.element.logfmt.requestLogger"></a>[function <span class="apidocSignatureSpan">logfmt.</span>requestLogger (options, formatter)](#apidoc.element.logfmt.requestLogger)
- description and source-code
```javascript
requestLogger = function (options, formatter) {
  return requestLogger.init(this, options, formatter);
}
```
- example usage
```shell
...
//=> at=error id=12345 line=0 trace="Error: test error"
//=> ...
'''

## express/restify logging middleware

'''javascript
app.use(logfmt.requestLogger());
//=> ip=127.0.0.1 time=2013-08-05T20:50:19.216Z method=POST path=/logs status=200 content_length=337 content_type=application/logplex
-1 elapsed=4ms
'''

#### 'logfmt.requestLogger([options], [formatter(req, res)])'

If no formatter is supplied it will default to 'logfmt.requestLogger.commonFormatter' which is based
on having similiar fields to the Apache Common Log format.
...
```

#### <a name="apidoc.element.logfmt.streamParser"></a>[function <span class="apidocSignatureSpan">logfmt.</span>streamParser (options)](#apidoc.element.logfmt.streamParser)
- description and source-code
```javascript
streamParser = function (options){
  var options = options || {};

  var streamParser = new PassThrough();
  var self = this;

  var logfmtStream = through(function(line){
    if(line !== '') this.queue(self.parse(line))
  })

  // When a source stream is piped to us, undo that pipe, and save
  // off the source stream piped into our internally managed streams.
  streamParser.on('pipe', function(source) {
    if(source.unpipe) source.unpipe(this);
    this.transformStream = source.pipe(split()).pipe(logfmtStream);
  });

  // When we're piped to another stream, instead pipe our internal
  // transform stream to that destination.
  streamParser.pipe = function(destination, options) {
    return this.transformStream.pipe(destination, options);
  };

  return streamParser;
}
```
- example usage
```shell
...
We cannot arbitrarily convert numbers because that will drop precision for numbers that require more than 32 bits to represent them
.


## Streaming

Put this in your pipe and smoke it.

### 'logfmt.streamParser()'

Creates a streaming parser that will automatically split and parse incoming lines and
emit javascript objects.

Stream in from STDIN

'''javascript
...
```

#### <a name="apidoc.element.logfmt.streamStringify"></a>[function <span class="apidocSignatureSpan">logfmt.</span>streamStringify (options)](#apidoc.element.logfmt.streamStringify)
- description and source-code
```javascript
streamStringify = function (options){
  var self = this;
  var options = options || {};
  if(options.hasOwnProperty('delimiter')){
    var delim = options.delimiter;
  }else{
    var delim = "\n";
  }

  return through(function(data){
    this.queue(self.stringify(data) + delim)
  }, function(){
    this.queue(null)
  })
}
```
- example usage
```shell
...

Or pipe from an HTTP request

'''javascript
req.pipe(logfmt.streamParser())
'''

### 'logfmt.streamStringify([options])'

Pipe objects into the stream and it will write logfmt.
You can customize the delimiter via the 'options' object, which
defaults to '\n' (newlines).

'''javascript
var parseJSON = function(line) {
...
```

#### <a name="apidoc.element.logfmt.stringify"></a>[function <span class="apidocSignatureSpan">logfmt.</span>stringify (data)](#apidoc.element.logfmt.stringify)
- description and source-code
```javascript
stringify = function (data){
  var line = '';

  for(var key in data) {
    var value = data[key];
    var is_null = false;
    if(value == null) {
      is_null = true;
      value = '';
    }
    else value = value.toString();

    var needs_quoting  = value.indexOf(' ') > -1 || value.indexOf('=') > -1;
    var needs_escaping = value.indexOf('"') > -1 || value.indexOf("\\") > -1;

    if(needs_escaping) value = value.replace(/["\\]/g, '\\$&');
    if(needs_quoting) value = '"' + value + '"';
    if(value === '' && !is_null) value = '""';

    line += key + '=' + value + ' ';
  }

  //trim traling space
  return line.substring(0,line.length-1);
}
```
- example usage
```shell
...
## node.js

The 'logfmt' module is a singleton that works directly from require.

'''javascript
var logfmt = require('logfmt');

logfmt.stringify({foo: 'bar'});
// 'foo=bar'

logfmt.parse('foo=bar');
// {foo: 'bar'}
'''

It is also a constructor function, so you can use 'new logfmt' to create
...
```

#### <a name="apidoc.element.logfmt.time"></a>[function <span class="apidocSignatureSpan">logfmt.</span>time (label)](#apidoc.element.logfmt.time)
- description and source-code
```javascript
time = function (label) {
  var logfmt = require('../logfmt');
  var startTime = (new Date()).getTime();
  var label  = label || 'elapsed';
  var timer  = new logfmt();
  timer.stream = this.stream;
  timer.defaultData = this.defaultData;
  timer.timers = _.extend({}, this.timers)
  timer.timers[label] = startTime;
  return timer;
}
```
- example usage
```shell
...
logfmt.log({})
//=> app=logfmt

logfmt.log({hello: 'world'})
//=> app=logfmt hello=world
'''

### 'logfmt.time([label])'

Log how long something takes.
Returns a new 'logfmt' with elapsed milliseconds included in every 'log' call.

- 'label': optional name for the milliseconds key. defaults to: 'elapsed=<milliseconds>ms'

'''javascript
...
```



# <a name="apidoc.module.logfmt.logfmt_parser"></a>[module logfmt.logfmt_parser](#apidoc.module.logfmt.logfmt_parser)

#### <a name="apidoc.element.logfmt.logfmt_parser.parse"></a>[function <span class="apidocSignatureSpan">logfmt.logfmt_parser.</span>parse (line)](#apidoc.element.logfmt.logfmt_parser.parse)
- description and source-code
```javascript
parse = function (line) {
  var key = '';
  var value = '';
  var is_number = true;
  var in_key    = false;
  var in_value  = false;
  var in_quote  = false;
  var had_quote = false;
  var object    = {};
  var debug     = exports.debug;

  if(line[line.length - 1] == '\n'){
    line = line.slice(0,line.length - 1)
  }

  for(var i=0; i <= line.length; i++){

    if((line[i] == ' ' && !in_quote) || i == line.length){
      if(in_key && key.length > 0){
        object[key] = true;
      }else if(in_value){
        if(value == 'true') value = true;
        else if(value == 'false') value = false;
        else if(value === '' && !had_quote) value = null;
        object[key] = value;
        value = '';
      }

      if(i == line.length) break;
      else {
        in_key   = false;
        in_value = false;
        in_quote = false;
        had_quote = false;
      }
    }

    if(line[i] == '=' && !in_quote){
      if(debug) console.log('split')
      //split
      in_key = false;
      in_value = true;
    }
    else if(line[i] == '\\'){
      i ++ ;
      value += line[i];
      if(debug) console.log('escape: ' + line[i])
    }
    else if(line[i] == '"'){
      had_quote = true;
      in_quote = !in_quote;
      if(debug) console.log('in quote: ' + in_quote)
    }
    else if(line[i] != ' ' && !in_value && !in_key){
      if(debug) console.log('start key with: ' + line[i])
      in_key = true;
      key = line[i];
    }
    else if(in_key){
      if(debug) console.log('add to key: ' + line[i])
      key += line[i]
    }
    else if(in_value){
      if(debug) console.log('add to value: ' + line[i])
      value += line[i];
    }
  }

  return object;
}
```
- example usage
```shell
...

'''javascript
var logfmt = require('logfmt');

logfmt.stringify({foo: 'bar'});
// 'foo=bar'

logfmt.parse('foo=bar');
// {foo: 'bar'}
'''

It is also a constructor function, so you can use 'new logfmt' to create
a new 'logfmt' that you can configure differently.

'''javascript
...
```



# <a name="apidoc.module.logfmt.logger"></a>[module logfmt.logger](#apidoc.module.logfmt.logger)

#### <a name="apidoc.element.logfmt.logger.error"></a>[function <span class="apidocSignatureSpan">logfmt.logger.</span>error (err, id)](#apidoc.element.logfmt.logger.error)
- description and source-code
```javascript
error = function (err, id) {
  this.maxErrorLines = this.maxErrorLines || 10;
  if (id === undefined) {
    id = Math.random().toString().slice(2, 12);
  }
  var errorLogger = this.namespace({
    error: true,
    id:id,
    now: (new Date()).toISOString()
  })
  errorLogger.log({ message:err.message });
  if (err.stack) {
    var stack = err.stack.split('\n');
    for (var line in stack) {
      if (line >= this.maxErrorLines) break;
      errorLogger.log({ line:line, trace:stack[line] });
    }
  }
}
```
- example usage
```shell
...
var timer = logfmt.time('time').namespace({foo: 'bar'});
timer.log();
//=> time=1ms foo=bar
timer.log();
//=> time=2ms foo=bar
'''

### 'logfmt.error(error)'

Accepts a Javascript 'Error' object and converts it to logfmt format.

It will print up to 'logfmt.maxErrorLines' lines.

'''javascript
var logfmt = require('logfmt');
...
```

#### <a name="apidoc.element.logfmt.logger.log"></a>[function <span class="apidocSignatureSpan">logfmt.logger.</span>log (data, stream)](#apidoc.element.logfmt.logger.log)
- description and source-code
```javascript
log = function (data, stream) {
  this.stream = this.stream || process.stdout;
  if(stream == undefined) stream = this.stream;

  var logData = _.extend({}, this.defaultData, data);

  if(this.timers){
    for(var key in this.timers){
      var now = (new Date()).getTime()
      logData[key] = (now - this.timers[key]).toString() + 'ms' ;
    }
  }

  stream.write(this.stringify(logData) + "\n");
}
```
- example usage
```shell
...
'''javascript
var logfmt2 = new logfmt;

// replace our stringify with JSON's
logfmt2.stringify = JSON.stringify

// now we log JSON!
logfmt2.log({foo: 'bar'})
// {"foo":"bar"}

// and the original logfmt is untouched
logfmt.log({foo: 'bar'})
// foo=bar
'''
...
```

#### <a name="apidoc.element.logfmt.logger.namespace"></a>[function <span class="apidocSignatureSpan">logfmt.logger.</span>namespace (object)](#apidoc.element.logfmt.logger.namespace)
- description and source-code
```javascript
namespace = function (object) {
  var logfmt = require('../logfmt');
  var namespaced = new logfmt()
  var namespace  = _.extend({}, this.defaultData, object);
  namespaced.stream = this.stream;
  namespaced.defaultData = namespace
  namespaced.timers = this.timers;
  return namespaced;
}
```
- example usage
```shell
...
logfmt.log({hello: 'stdout'});
//=> hello=stdout

errorLogger.log({hello: 'stderr'});
//=> hello=stderr
'''

### 'logfmt.namespace(object)'

Returns a new 'logfmt' with object's data included in every 'log' call.

'''javascript
var logfmt = require('logfmt').namespace({app: 'logfmt'});

logfmt.log({ "foo": "bar", "a": 14, baz: 'hello kitty'})
...
```

#### <a name="apidoc.element.logfmt.logger.time"></a>[function <span class="apidocSignatureSpan">logfmt.logger.</span>time (label)](#apidoc.element.logfmt.logger.time)
- description and source-code
```javascript
time = function (label) {
  var logfmt = require('../logfmt');
  var startTime = (new Date()).getTime();
  var label  = label || 'elapsed';
  var timer  = new logfmt();
  timer.stream = this.stream;
  timer.defaultData = this.defaultData;
  timer.timers = _.extend({}, this.timers)
  timer.timers[label] = startTime;
  return timer;
}
```
- example usage
```shell
...
logfmt.log({})
//=> app=logfmt

logfmt.log({hello: 'world'})
//=> app=logfmt hello=world
'''

### 'logfmt.time([label])'

Log how long something takes.
Returns a new 'logfmt' with elapsed milliseconds included in every 'log' call.

- 'label': optional name for the milliseconds key. defaults to: 'elapsed=<milliseconds>ms'

'''javascript
...
```



# <a name="apidoc.module.logfmt.requestLogger"></a>[module logfmt.requestLogger](#apidoc.module.logfmt.requestLogger)

#### <a name="apidoc.element.logfmt.requestLogger.requestLogger"></a>[function <span class="apidocSignatureSpan">logfmt.</span>requestLogger (options, formatter)](#apidoc.element.logfmt.requestLogger.requestLogger)
- description and source-code
```javascript
requestLogger = function (options, formatter) {
  return requestLogger.init(this, options, formatter);
}
```
- example usage
```shell
...
//=> at=error id=12345 line=0 trace="Error: test error"
//=> ...
'''

## express/restify logging middleware

'''javascript
app.use(logfmt.requestLogger());
//=> ip=127.0.0.1 time=2013-08-05T20:50:19.216Z method=POST path=/logs status=200 content_length=337 content_type=application/logplex
-1 elapsed=4ms
'''

#### 'logfmt.requestLogger([options], [formatter(req, res)])'

If no formatter is supplied it will default to 'logfmt.requestLogger.commonFormatter' which is based
on having similiar fields to the Apache Common Log format.
...
```

#### <a name="apidoc.element.logfmt.requestLogger.commonFormatter"></a>[function <span class="apidocSignatureSpan">logfmt.requestLogger.</span>commonFormatter (req, res)](#apidoc.element.logfmt.requestLogger.commonFormatter)
- description and source-code
```javascript
commonFormatter = function (req, res){
  if((typeof req.path) == 'function'){
    //in restify path is a function
    var path = req.path();
  }
  else{
    //in express it is an attribute
    var path = req.originalUrl || req.path || req.url;
  }

  var httpHeader = req.header && req.header('x-forwarded-for')
  var requestID  = req.header && req.header('x-request-id')

  var ip = req.ip || httpHeader
                  || req.connection.remoteAddress;

  var requestData =  {
    ip: ip,
    time: (new Date()).toISOString(),
    method: req.method,
    path: path,
    "status": res.statusCode,
  }

  if (requestID) {
    requestData.request_id = requestID;
  }

  if(res.get){
    requestData.content_length = res.get('content-length');
    requestData.content_type = res.get('content-type');
  }
  return requestData;
}
```
- example usage
```shell
...
//=> method=POST elapsed=4ms
'''

It's always possible to piggyback on top of the 'commonFormatter'

'''javascript
app.use(logfmt.requestLogger(function(req, res){
  var data = logfmt.requestLogger.commonFormatter(req, res)
  return {
    ip: data.ip,
    time: data.time,
    foo: 'bar'
  };
}));
//=> ip=127.0.0.1 time=2013-08-05T20:50:19.216Z foo=bar elapsed=4ms
...
```



# <a name="apidoc.module.logfmt.request_logger"></a>[module logfmt.request_logger](#apidoc.module.logfmt.request_logger)

#### <a name="apidoc.element.logfmt.request_logger.commonFormatter"></a>[function <span class="apidocSignatureSpan">logfmt.request_logger.</span>commonFormatter (req, res)](#apidoc.element.logfmt.request_logger.commonFormatter)
- description and source-code
```javascript
commonFormatter = function (req, res){
  if((typeof req.path) == 'function'){
    //in restify path is a function
    var path = req.path();
  }
  else{
    //in express it is an attribute
    var path = req.originalUrl || req.path || req.url;
  }

  var httpHeader = req.header && req.header('x-forwarded-for')
  var requestID  = req.header && req.header('x-request-id')

  var ip = req.ip || httpHeader
                  || req.connection.remoteAddress;

  var requestData =  {
    ip: ip,
    time: (new Date()).toISOString(),
    method: req.method,
    path: path,
    "status": res.statusCode,
  }

  if (requestID) {
    requestData.request_id = requestID;
  }

  if(res.get){
    requestData.content_length = res.get('content-length');
    requestData.content_type = res.get('content-type');
  }
  return requestData;
}
```
- example usage
```shell
...
//=> method=POST elapsed=4ms
'''

It's always possible to piggyback on top of the 'commonFormatter'

'''javascript
app.use(logfmt.requestLogger(function(req, res){
  var data = logfmt.requestLogger.commonFormatter(req, res)
  return {
    ip: data.ip,
    time: data.time,
    foo: 'bar'
  };
}));
//=> ip=127.0.0.1 time=2013-08-05T20:50:19.216Z foo=bar elapsed=4ms
...
```

#### <a name="apidoc.element.logfmt.request_logger.init"></a>[function <span class="apidocSignatureSpan">logfmt.request_logger.</span>init (logger, options, formatter)](#apidoc.element.logfmt.request_logger.init)
- description and source-code
```javascript
init = function (logger, options, formatter) {
  this.logger = logger;

  if(!formatter && !options){
    formatter = commonFormatter;
    options = {};
  }
  else if(!formatter){
    if(typeof options == 'function'){
      formatter = options;
      options = {};
    }else{
      formatter = commonFormatter;
    }
  }
  options = options || {};

  if(options.immediate){
    return immediateLogger(logger, options, formatter);
  }else{
    return timingLogger(logger, options, formatter);
  }
}
```
- example usage
```shell
...
logfmt.prototype.bodyParserStream = function(options) {
  options || (options = {});
  var mime = options.contentType || "application/logplex-1";
  return bodyParserStream({ contentType: mime });
};

logfmt.prototype.requestLogger = function(options, formatter) {
  return requestLogger.init(this, options, formatter);
};

logfmt.prototype.requestLogger.commonFormatter = requestLogger.commonFormatter;

_.extend(logfmt, logfmt.prototype);
...
```



# <a name="apidoc.module.logfmt.streaming"></a>[module logfmt.streaming](#apidoc.module.logfmt.streaming)

#### <a name="apidoc.element.logfmt.streaming.streamParser"></a>[function <span class="apidocSignatureSpan">logfmt.streaming.</span>streamParser (options)](#apidoc.element.logfmt.streaming.streamParser)
- description and source-code
```javascript
streamParser = function (options){
  var options = options || {};

  var streamParser = new PassThrough();
  var self = this;

  var logfmtStream = through(function(line){
    if(line !== '') this.queue(self.parse(line))
  })

  // When a source stream is piped to us, undo that pipe, and save
  // off the source stream piped into our internally managed streams.
  streamParser.on('pipe', function(source) {
    if(source.unpipe) source.unpipe(this);
    this.transformStream = source.pipe(split()).pipe(logfmtStream);
  });

  // When we're piped to another stream, instead pipe our internal
  // transform stream to that destination.
  streamParser.pipe = function(destination, options) {
    return this.transformStream.pipe(destination, options);
  };

  return streamParser;
}
```
- example usage
```shell
...
We cannot arbitrarily convert numbers because that will drop precision for numbers that require more than 32 bits to represent them
.


## Streaming

Put this in your pipe and smoke it.

### 'logfmt.streamParser()'

Creates a streaming parser that will automatically split and parse incoming lines and
emit javascript objects.

Stream in from STDIN

'''javascript
...
```

#### <a name="apidoc.element.logfmt.streaming.streamStringify"></a>[function <span class="apidocSignatureSpan">logfmt.streaming.</span>streamStringify (options)](#apidoc.element.logfmt.streaming.streamStringify)
- description and source-code
```javascript
streamStringify = function (options){
  var self = this;
  var options = options || {};
  if(options.hasOwnProperty('delimiter')){
    var delim = options.delimiter;
  }else{
    var delim = "\n";
  }

  return through(function(data){
    this.queue(self.stringify(data) + delim)
  }, function(){
    this.queue(null)
  })
}
```
- example usage
```shell
...

Or pipe from an HTTP request

'''javascript
req.pipe(logfmt.streamParser())
'''

### 'logfmt.streamStringify([options])'

Pipe objects into the stream and it will write logfmt.
You can customize the delimiter via the 'options' object, which
defaults to '\n' (newlines).

'''javascript
var parseJSON = function(line) {
...
```



# <a name="apidoc.module.logfmt.stringify"></a>[module logfmt.stringify](#apidoc.module.logfmt.stringify)

#### <a name="apidoc.element.logfmt.stringify.stringify"></a>[function <span class="apidocSignatureSpan">logfmt.</span>stringify (data)](#apidoc.element.logfmt.stringify.stringify)
- description and source-code
```javascript
stringify = function (data){
  var line = '';

  for(var key in data) {
    var value = data[key];
    var is_null = false;
    if(value == null) {
      is_null = true;
      value = '';
    }
    else value = value.toString();

    var needs_quoting  = value.indexOf(' ') > -1 || value.indexOf('=') > -1;
    var needs_escaping = value.indexOf('"') > -1 || value.indexOf("\\") > -1;

    if(needs_escaping) value = value.replace(/["\\]/g, '\\$&');
    if(needs_quoting) value = '"' + value + '"';
    if(value === '' && !is_null) value = '""';

    line += key + '=' + value + ' ';
  }

  //trim traling space
  return line.substring(0,line.length-1);
}
```
- example usage
```shell
...
## node.js

The 'logfmt' module is a singleton that works directly from require.

'''javascript
var logfmt = require('logfmt');

logfmt.stringify({foo: 'bar'});
// 'foo=bar'

logfmt.parse('foo=bar');
// {foo: 'bar'}
'''

It is also a constructor function, so you can use 'new logfmt' to create
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
