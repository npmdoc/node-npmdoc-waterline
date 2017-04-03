# api documentation for  [waterline (v0.11.11)](http://waterlinejs.org)  [![npm package](https://img.shields.io/npm/v/npmdoc-waterline.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-waterline) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-waterline.svg)](https://travis-ci.org/npmdoc/node-npmdoc-waterline)
#### An ORM for Node.js and the Sails framework.

[![NPM](https://nodei.co/npm/waterline.png?downloads=true)](https://www.npmjs.com/package/waterline)

[![apidoc](https://npmdoc.github.io/node-npmdoc-waterline/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-waterline_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-waterline/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-waterline/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-waterline/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "http://sailsjs.com/bugs"
    },
    "contributors": [
        {
            "name": "particlebanana"
        },
        {
            "name": "mikermcneil"
        },
        {
            "name": "zolmeister"
        },
        {
            "name": "seerepo"
        }
    ],
    "dependencies": {
        "anchor": "~0.11.0",
        "async": "1.5.2",
        "bluebird": "3.2.1",
        "deep-diff": "0.3.3",
        "lodash": "3.10.1",
        "prompt": "0.2.14",
        "switchback": "2.0.0",
        "waterline-criteria": "~0.11.2",
        "waterline-schema": "~0.2.1"
    },
    "description": "An ORM for Node.js and the Sails framework.",
    "devDependencies": {
        "codeclimate-test-reporter": "0.3.1",
        "eslint": "1.10.3",
        "espree": "3.0.1",
        "istanbul": "0.4.2",
        "mocha": "2.4.5",
        "sails-memory": "github:balderdashy/sails-memory",
        "should": "8.2.1",
        "waterline-adapter-tests": "~0.11.2"
    },
    "directories": {},
    "dist": {
        "shasum": "6d2ec14d8f6caea49434adad8832ae4a1beeb288",
        "tarball": "https://registry.npmjs.org/waterline/-/waterline-0.11.11.tgz"
    },
    "engines": {
        "node": ">=0.10.0"
    },
    "gitHead": "7bd345109c1503425c77a3988b48df303c4f2573",
    "homepage": "http://waterlinejs.org",
    "keywords": [
        "mvc",
        "orm",
        "mysql",
        "postgresql",
        "redis",
        "mongodb",
        "active-record",
        "waterline",
        "sails",
        "sails.js"
    ],
    "license": "MIT",
    "main": "./lib/waterline",
    "maintainers": [
        {
            "name": "balderdashy",
            "email": "mike@balderdash.co"
        },
        {
            "name": "mikermcneil",
            "email": "michael.r.mcneil@gmail.com"
        },
        {
            "name": "particlebanana",
            "email": "particlebanana@gmail.com"
        },
        {
            "name": "sgress454",
            "email": "sgress454@treeline.io"
        }
    ],
    "name": "waterline",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/balderdashy/waterline.git"
    },
    "scripts": {
        "browserify": "rm -rf .dist && mkdir .dist && browserify lib/waterline.js -s Waterline | uglifyjs > .dist/waterline.min.js",
        "prepublish": "npm prune",
        "test": "make test"
    },
    "version": "0.11.11"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module waterline](#apidoc.module.waterline)
1.  [function <span class="apidocSignatureSpan">waterline.</span>Collection (waterline, connections, cb)](#apidoc.element.waterline.Collection)
1.  [function <span class="apidocSignatureSpan">waterline.</span>Collection.super_ ()](#apidoc.element.waterline.Collection.super_)
1.  [function <span class="apidocSignatureSpan">waterline.</span>Model (context, mixins)](#apidoc.element.waterline.Model)
1.  object <span class="apidocSignatureSpan">waterline.</span>Collection.super_.prototype

#### [module waterline.Collection](#apidoc.module.waterline.Collection)
1.  [function <span class="apidocSignatureSpan">waterline.</span>Collection (waterline, connections, cb)](#apidoc.element.waterline.Collection.Collection)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.</span>extend (protoProps, staticProps)](#apidoc.element.waterline.Collection.extend)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.</span>super_ ()](#apidoc.element.waterline.Collection.super_)

#### [module waterline.Collection.super_](#apidoc.module.waterline.Collection.super_)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.</span>super_ ()](#apidoc.element.waterline.Collection.super_.super_)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.</span>extend (protoProps, staticProps)](#apidoc.element.waterline.Collection.super_.extend)

#### [module waterline.Collection.super_.prototype](#apidoc.module.waterline.Collection.super_.prototype)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>alter (attributes, cb)](#apidoc.element.waterline.Collection.super_.prototype.alter)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>buildDynamicFinders ()](#apidoc.element.waterline.Collection.super_.prototype.buildDynamicFinders)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>contains (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.contains)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>count (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.count)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>create (values, cb)](#apidoc.element.waterline.Collection.super_.prototype.create)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>createEach (valuesList, cb)](#apidoc.element.waterline.Collection.super_.prototype.createEach)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>describe (cb)](#apidoc.element.waterline.Collection.super_.prototype.describe)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>destroy (criteria, cb)](#apidoc.element.waterline.Collection.super_.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>drop (cb)](#apidoc.element.waterline.Collection.super_.prototype.drop)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>endsWith (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.endsWith)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>find (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.find)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>findAll (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.findAll)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>findLike (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.findLike)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>findOne (criteria, cb)](#apidoc.element.waterline.Collection.super_.prototype.findOne)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>findOneLike (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.findOneLike)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>findOrCreate (criteria, values, cb)](#apidoc.element.waterline.Collection.super_.prototype.findOrCreate)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>findOrCreateEach (criteria, valuesList, cb)](#apidoc.element.waterline.Collection.super_.prototype.findOrCreateEach)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>generateAssociationFinders (attrName)](#apidoc.element.waterline.Collection.super_.prototype.generateAssociationFinders)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>generateDynamicFinder (attrName, method, dontCapitalize)](#apidoc.element.waterline.Collection.super_.prototype.generateDynamicFinder)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>join (collection, fk, pk, cb)](#apidoc.element.waterline.Collection.super_.prototype.join)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>select ()](#apidoc.element.waterline.Collection.super_.prototype.select)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>startsWith (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.startsWith)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>stream (criteria, transformation)](#apidoc.element.waterline.Collection.super_.prototype.stream)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>sync (cb)](#apidoc.element.waterline.Collection.super_.prototype.sync)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>update (criteria, values, cb)](#apidoc.element.waterline.Collection.super_.prototype.update)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>validate (values, presentOnly, cb)](#apidoc.element.waterline.Collection.super_.prototype.validate)
1.  [function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>where ()](#apidoc.element.waterline.Collection.super_.prototype.where)



# <a name="apidoc.module.waterline"></a>[module waterline](#apidoc.module.waterline)

#### <a name="apidoc.element.waterline.Collection"></a>[function <span class="apidocSignatureSpan">waterline.</span>Collection (waterline, connections, cb)](#apidoc.element.waterline.Collection)
- description and source-code
```javascript
Collection = function (waterline, connections, cb) {

  var self = this;

  // Set the named connections
  this.connections = connections || {};

  // Cache reference to the parent
  this.waterline = waterline;

  // Default Attributes
  this.attributes = this.attributes || {};

  // Instantiate Base Collection
  Core.call(this);

  // Instantiate Query Language
  Query.call(this);

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_"></a>[function <span class="apidocSignatureSpan">waterline.</span>Collection.super_ ()](#apidoc.element.waterline.Collection.super_)
- description and source-code
```javascript
Collection.super_ = function () {

  // Create a reference to an internal Adapter Base
  this.adapter = new AdapterBase({
    connections: this.connections,
    query: this,
    collection: this.tableName || this.identity,
    identity: this.identity,
    dictionary: this.adapterDictionary
  });

  // Mixin Custom Adapter Functions.
  AdapterMixin.call(this);

  // Generate Dynamic Finders
  this.buildDynamicFinders();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Model"></a>[function <span class="apidocSignatureSpan">waterline.</span>Model (context, mixins)](#apidoc.element.waterline.Model)
- description and source-code
```javascript
Model = function (context, mixins) {

<span class="apidocCodeCommentSpan">  /**
   * Extend the model prototype with default instance methods
   */
</span>
  var prototypeFns = {

    toObject: function() {
      return new defaultMethods.toObject(context, this);
    },

    save: function(options, cb) {
      return new defaultMethods.save(context, this, options, cb);
    },

    destroy: function(cb) {
      return new defaultMethods.destroy(context, this, cb);
    },

    _defineAssociations: function() {
      new internalMethods.defineAssociations(context, this);
    },

    _normalizeAssociations: function() {
      new internalMethods.normalizeAssociations(context, this);
    },

    _cast: function(values) {
      _.keys(context._attributes).forEach(function(key) {
        var type = context._attributes[key].type;

        // Attempt to parse Array or JSON type
        if (type === 'array' || type === 'json') {
          if (!_.isString(values[key])) return;
          try {
            values[key] = JSON.parse(values[key]);
          } catch(e) {
            return;
          }
        }

        // Convert booleans back to true/false
        if (type === 'boolean') {
          var val = values[key];
          if (val === 0) values[key] = false;
          if (val === 1) values[key] = true;
        }

      });
    },

    /**
     * Model.validate()
     *
     * Takes the currently set attributes and validates the model
     * Shorthand for Model.validate({ attributes }, cb)
     *
     * @param {Function} callback - (err)
     * @return {Promise}
     */

    validate: function(cb) {
      // Collect current values
      var values = this.toObject();

      if (cb) {
        context.validate(values, function(err) {
          if (err) { return cb(err); }
          cb();
        });
        return;
      } else {
        return new Bluebird(function(resolve, reject) {
          context.validate(values, function(err) {
            if (err) { return reject(err); }
            resolve();
          });
        });
      }
    }

  };

  // If any of the attributes are protected, the default toJSON method should
  // remove them.
  var protectedAttributes = _.compact(_.map(context._attributes, function(attr, key) {return attr.protected ? key : undefined;}));

  prototypeFns.toJSON = function() {
    var obj = this.toObject();

    if (protectedAttributes.length) {
      _.each(protectedAttributes, function(key) {
        delete obj[key];
      });
    }

    // Remove toJSON from the result, to prevent infinite recursion with
    // msgpack or other recursive object transformation tools.
    //
    // Causes issues if set to null and will error in Sails if we delete it because blueprints call it.
    //
    // obj.toJSON = null;

    return obj;
  };

  var prototype = _.extend(prototypeFns, mixins);

  var model = Model.extend(prototype);

  // Return the extended model for use in Waterline
  return model;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.waterline.Collection"></a>[module waterline.Collection](#apidoc.module.waterline.Collection)

#### <a name="apidoc.element.waterline.Collection.Collection"></a>[function <span class="apidocSignatureSpan">waterline.</span>Collection (waterline, connections, cb)](#apidoc.element.waterline.Collection.Collection)
- description and source-code
```javascript
Collection = function (waterline, connections, cb) {

  var self = this;

  // Set the named connections
  this.connections = connections || {};

  // Cache reference to the parent
  this.waterline = waterline;

  // Default Attributes
  this.attributes = this.attributes || {};

  // Instantiate Base Collection
  Core.call(this);

  // Instantiate Query Language
  Query.call(this);

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.extend"></a>[function <span class="apidocSignatureSpan">waterline.Collection.</span>extend (protoProps, staticProps)](#apidoc.element.waterline.Collection.extend)
- description and source-code
```javascript
extend = function (protoProps, staticProps) {
  var parent = this;
  var child;

  if (protoProps && _.has(protoProps, 'constructor')) {
    child = protoProps.constructor;
  } else {
    child = function() { return parent.apply(this, arguments); };
  }

  _.extend(child, parent, staticProps);

  var Surrogate = function() { this.constructor = child; };
  Surrogate.prototype = parent.prototype;
  child.prototype = new Surrogate();

  if (protoProps) _.extend(child.prototype, protoProps);

  child.__super__ = parent.prototype;

  return child;
}
```
- example usage
```shell
...


#### Usage (standalone)
'''javascript
var Waterline = require('waterline');

// Define your collection (aka model)
var User = Waterline.Collection.extend({

  attributes: {

firstName: {
  type: 'string',
  required: true
},
...
```

#### <a name="apidoc.element.waterline.Collection.super_"></a>[function <span class="apidocSignatureSpan">waterline.Collection.</span>super_ ()](#apidoc.element.waterline.Collection.super_)
- description and source-code
```javascript
super_ = function () {

  // Create a reference to an internal Adapter Base
  this.adapter = new AdapterBase({
    connections: this.connections,
    query: this,
    collection: this.tableName || this.identity,
    identity: this.identity,
    dictionary: this.adapterDictionary
  });

  // Mixin Custom Adapter Functions.
  AdapterMixin.call(this);

  // Generate Dynamic Finders
  this.buildDynamicFinders();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.waterline.Collection.super_"></a>[module waterline.Collection.super_](#apidoc.module.waterline.Collection.super_)

#### <a name="apidoc.element.waterline.Collection.super_.super_"></a>[function <span class="apidocSignatureSpan">waterline.Collection.</span>super_ ()](#apidoc.element.waterline.Collection.super_.super_)
- description and source-code
```javascript
super_ = function () {

  // Create a reference to an internal Adapter Base
  this.adapter = new AdapterBase({
    connections: this.connections,
    query: this,
    collection: this.tableName || this.identity,
    identity: this.identity,
    dictionary: this.adapterDictionary
  });

  // Mixin Custom Adapter Functions.
  AdapterMixin.call(this);

  // Generate Dynamic Finders
  this.buildDynamicFinders();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.extend"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.</span>extend (protoProps, staticProps)](#apidoc.element.waterline.Collection.super_.extend)
- description and source-code
```javascript
extend = function (protoProps, staticProps) {
  var parent = this;
  var child;

  if (protoProps && _.has(protoProps, 'constructor')) {
    child = protoProps.constructor;
  } else {
    child = function() { return parent.apply(this, arguments); };
  }

  _.extend(child, parent, staticProps);

  var Surrogate = function() { this.constructor = child; };
  Surrogate.prototype = parent.prototype;
  child.prototype = new Surrogate();

  if (protoProps) _.extend(child.prototype, protoProps);

  child.__super__ = parent.prototype;

  return child;
}
```
- example usage
```shell
...


#### Usage (standalone)
'''javascript
var Waterline = require('waterline');

// Define your collection (aka model)
var User = Waterline.Collection.extend({

  attributes: {

firstName: {
  type: 'string',
  required: true
},
...
```



# <a name="apidoc.module.waterline.Collection.super_.prototype"></a>[module waterline.Collection.super_.prototype](#apidoc.module.waterline.Collection.super_.prototype)

#### <a name="apidoc.element.waterline.Collection.super_.prototype.alter"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>alter (attributes, cb)](#apidoc.element.waterline.Collection.super_.prototype.alter)
- description and source-code
```javascript
alter = function (attributes, cb) {
  this.adapter.alter(attributes, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.buildDynamicFinders"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>buildDynamicFinders ()](#apidoc.element.waterline.Collection.super_.prototype.buildDynamicFinders)
- description and source-code
```javascript
buildDynamicFinders = function () {
  var self = this;

  // For each defined attribute, create a dynamic finder function
  Object.keys(this._attributes).forEach(function(attrName) {

    // Check if attribute is an association, if so generate limited dynamic finders
    if (hasOwnProperty(self._schema.schema[attrName], 'foreignKey')) {
      if (self.associationFinders !== false) {
        self.generateAssociationFinders(attrName);
      }
      return;
    }

    var capitalizedMethods = ['findOneBy*', 'findOneBy*In', 'findOneBy*Like', 'findBy*', 'findBy*In',
      'findBy*Like', 'countBy*', 'countBy*In', 'countBy*Like'];

    var lowercasedMethods = ['*StartsWith', '*Contains', '*EndsWith'];


    if (self.dynamicFinders !== false) {
      capitalizedMethods.forEach(function(method) {
        self.generateDynamicFinder(attrName, method);
      });
      lowercasedMethods.forEach(function(method) {
        self.generateDynamicFinder(attrName, method, true);
      });
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.contains"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>contains (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.contains)
- description and source-code
```javascript
contains = function (criteria, options, cb) {
  var usage = utils.capitalize(this.identity) + '.startsWith([criteria],[options],callback)';

  criteria = normalize.likeCriteria(criteria, this._schema.schema, function applyContains(criteria) {
    return '%' + criteria + '%';
  });

  if (!criteria) return usageError('Criteria must be an object!', usage, cb);

  this.find(criteria, options, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.count"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>count (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.count)
- description and source-code
```javascript
count = function (criteria, options, cb) {
  var usage = utils.capitalize(this.identity) + '.count([criteria],[options],callback)';

  if (typeof criteria === 'function') {
    cb = criteria;
    criteria = null;
    options = null;
  }

  if (typeof options === 'function') {
    cb = options;
    options = null;
  }

  // Return Deferred or pass to adapter
  if (typeof cb !== 'function') {
    return new Deferred(this, this.count, criteria);
  }

  // Normalize criteria and fold in options
  criteria = normalize.criteria(criteria);

  // If there was something defined in the criteria that would return no results, don't even
  // run the query and just return 0
  if (criteria === false) {
    return cb(null, 0);
  }

  if (_.isObject(options) && _.isObject(criteria)) {
    criteria = _.extend({}, criteria, options);
  }

  if (_.isFunction(criteria) || _.isFunction(options)) {
    return usageError('Invalid options specified!', usage, cb);
  }

  // Transform Search Criteria
  criteria = this._transformer.serialize(criteria);

  // Remove any joins from the count criteria. They won't have any effect on the
  // number of results found.
  if (_.isArray(criteria.joins)) {
    delete criteria.joins;
  }

  if (criteria.where && _.isArray(criteria.where.joins)) {
    delete criteria.where.joins;
  }

  this.adapter.count(criteria, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.create"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>create (values, cb)](#apidoc.element.waterline.Collection.super_.prototype.create)
- description and source-code
```javascript
create = function (values, cb) {

  var self = this;

  // Handle Deferred where it passes criteria first
  if (arguments.length === 3) {
    var args = Array.prototype.slice.call(arguments);
    cb = args.pop();
    values = args.pop();
  }

  // Loop through values and pull out any buffers before cloning
  var bufferValues = {};

  _.each(_.keys(values), function(key) {
    if (Buffer.isBuffer(values[key])) {
      bufferValues[key] = values[key];
    }
  });

  values = _.cloneDeep(values) || {};

  // Replace clone keys with the buffer values
  _.each(_.keys(bufferValues), function(key) {
    values[key] = bufferValues[key];
  });

  // Remove all undefined values
  if (_.isArray(values)) {
    values = _.remove(values, undefined);
  }

  // Return Deferred or pass to adapter
  if (typeof cb !== 'function') {
    return new Deferred(this, this.create, {}, values);
  }


  // Handle Array of values
  if (Array.isArray(values)) {
    return this.createEach(values, cb);
  }

  // Process Values
  var valuesObject = processValues.call(this, values);

  // Create any of the belongsTo associations and set the foreign key values
  createBelongsTo.call(this, valuesObject, function(err) {
    if (err) return cb(err);

    beforeCallbacks.call(self, valuesObject, function(err) {
      if (err) return cb(err);
      createValues.call(self, valuesObject, cb);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.createEach"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>createEach (valuesList, cb)](#apidoc.element.waterline.Collection.super_.prototype.createEach)
- description and source-code
```javascript
createEach = function (valuesList, cb) {
  var self = this;

  // Handle Deferred where it passes criteria first
  if (arguments.length === 3) {
    var args = Array.prototype.slice.call(arguments);
    cb = args.pop();
    valuesList = args.pop();
  }

  // Return Deferred or pass to adapter
  if (typeof cb !== 'function') {
    return new Deferred(this, this.createEach, {}, valuesList);
  }

  // Validate Params
  var usage = utils.capitalize(this.identity) + '.createEach(valuesList, callback)';

  if (!valuesList) return usageError('No valuesList specified!', usage, cb);
  if (!Array.isArray(valuesList)) return usageError('Invalid valuesList specified (should be an array!)', usage, cb);
  if (typeof cb !== 'function') return usageError('Invalid callback specified!', usage, cb);

  var errStr = _validateValues(_.cloneDeep(valuesList));
  if (errStr) return usageError(errStr, usage, cb);

  // Handle undefined values
  var filteredValues = _.filter(valuesList, function(value) {
    return value !== undefined;
  });

  // Create will take care of cloning values so original isn't mutated
  async.map(filteredValues, self.create.bind(self), cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.describe"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>describe (cb)](#apidoc.element.waterline.Collection.super_.prototype.describe)
- description and source-code
```javascript
describe = function (cb) {
  this.adapter.describe(cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.destroy"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>destroy (criteria, cb)](#apidoc.element.waterline.Collection.super_.prototype.destroy)
- description and source-code
```javascript
destroy = function (criteria, cb) {
  var self = this;
  var pk;

  if (typeof criteria === 'function') {
    cb = criteria;
    criteria = {};
  }

  // Check if criteria is an integer or string and normalize criteria
  // to object, using the specified primary key field.
  criteria = normalize.expandPK(self, criteria);

  // Normalize criteria
  criteria = normalize.criteria(criteria);

  // Return Deferred or pass to adapter
  if (typeof cb !== 'function') {
    return new Deferred(this, this.destroy, criteria);
  }

  var usage = utils.capitalize(this.identity) + '.destroy([options], callback)';
  if (typeof cb !== 'function') return usageError('Invalid callback specified!', usage, cb);

  // If there was something defined in the criteria that would return no results, don't even
  // run the query and just return an empty result set.
  if (criteria === false) {
    return cb(null, []);
  }

  callbacks.beforeDestroy(self, criteria, function(err) {
    if (err) return cb(err);

    // Transform Search Criteria
    criteria = self._transformer.serialize(criteria);

    // Pass to adapter
    self.adapter.destroy(criteria, function(err, result) {
      if (err) return cb(err);

      // Look for any m:m associations and destroy the value in the join table
      var relations = getRelations({
        schema: self.waterline.schema,
        parentCollection: self.identity
      });

      if (relations.length === 0) return after();

      // Find the collection's primary key
      for (var key in self.attributes) {
        if (!self.attributes[key].hasOwnProperty('primaryKey')) continue;

        // Check if custom primaryKey value is falsy
        if (!self.attributes[key].primaryKey) continue;

        if (self.attributes[key].columnName) {
          pk = self.attributes[key].columnName;
        } else {
          pk = key;
        }

        break;
      }

      function destroyJoinTableRecords(item, next) {
        var collection = self.waterline.collections[item];
        var refKey = [];

        Object.keys(collection._attributes).forEach(function(key) {
          var attr = collection._attributes[key];
          if (attr.references !== self.identity) return;
          refKey.push(key);
        });

        // If no refKey return, this could leave orphaned join table values but it's better
        // than crashing.
        if (!refKey.length) return next();

        // Make sure we don't return any undefined pks
        var mappedValues = result.reduce(function(memo, vals) {
          if (vals[pk] !== undefined) {
            memo.push(vals[pk]);
          }
          return memo;
        }, []);

        var criteria = {};

        if (mappedValues.length > 0) {
          // Handle reflexive associations by building up an OR clause.
          if (refKey.length > 1) {
            var orCriteria = [];
            _.each(refKey, function(columnName) {
              var where = {};
              where[columnName] = mappedValues;
              orCriteria.push(where);
            });

            criteria = {
              or: orCriteria
            };
          } else {
            criteria[_.first(refKey)] = mappedValues;
          }

          collection.destroy(criteria).exec(next);
        } else {
          return next();
        }

      }

      async.each(relations, destroyJoinTableRecords, function(err) {
        if (err) return cb(err);
        after();
      });

      function after() {

        // If no result was returned, default to empty array
        if (!result) {
          result = [];
        }

        // If values is not an array, return an array
        if (!Array.isArray(result)) {
          result = [result];
        }

        // Unserialize each value
        var transformedValues = result.map(function(value) {
          return self._transformer.unserialize(value);
        });

        callbacks.afterDestroy(self, transformedValues, function(err) {
          if (err) return cb(err);
          cb(null, transformedValues);
        });
      }

    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.drop"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>drop (cb)](#apidoc.element.waterline.Collection.super_.prototype.drop)
- description and source-code
```javascript
drop = function (cb) {
  this.adapter.drop(cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.endsWith"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>endsWith (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.endsWith)
- description and source-code
```javascript
endsWith = function (criteria, options, cb) {
  var usage = utils.capitalize(this.identity) + '.startsWith([criteria],[options],callback)';

  criteria = normalize.likeCriteria(criteria, this._schema.schema, function applyEndsWith(criteria) {
    return '%' + criteria;
  });

  if (!criteria) return usageError('Criteria must be an object!', usage, cb);

  this.find(criteria, options, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.find"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>find (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.find)
- description and source-code
```javascript
find = function (criteria, options, cb) {
  var self = this;

  var usage = utils.capitalize(this.identity) + '.find([criteria],[options]).exec(callback|switchback)';

  if (typeof criteria === 'function') {
    cb = criteria;
    criteria = null;
    options = null;
  }

  if (typeof options === 'function') {
    cb = options;
    options = null;
  }

  // If the criteria is an array of objects, wrap it in an "or"
  if (Array.isArray(criteria) && _.all(criteria, function(crit) {return _.isObject(crit);})) {
    criteria = {or: criteria};
  }

  // Check if criteria is an integer or string and normalize criteria
  // to object, using the specified primary key field.
  criteria = normalize.expandPK(self, criteria);

  // Normalize criteria
  criteria = normalize.criteria(criteria);

  // Validate Arguments
  if (typeof criteria === 'function' || typeof options === 'function') {
    return usageError('Invalid options specified!', usage, cb);
  }

  // Return Deferred or pass to adapter
  if (typeof cb !== 'function') {
    return new Deferred(this, this.find, criteria, options);
  }

  // If there was something defined in the criteria that would return no results, don't even
  // run the query and just return an empty result set.
  if (criteria === false) {
    return cb(null, []);
  }

  // Fold in options
  if (options === Object(options) && criteria === Object(criteria)) {
    criteria = _.extend({}, criteria, options);
  }

  // Transform Search Criteria
  if (!self._transformer) {
    throw new Error('Waterline can not access transformer-- maybe the context of the method is being overridden?');
  }

  criteria = self._transformer.serialize(criteria);

  // serialize populated object
  if (criteria.joins) {
    criteria.joins.forEach(function(join) {
      if (join.criteria && join.criteria.where) {
        var joinCollection = self.waterline.collections[join.child];
        join.criteria.where = joinCollection._transformer.serialize(join.criteria.where);
      }
    });
  }

  // Build up an operations set
  var operations = new Operations(self, criteria, 'find');

  // Run the operations
  operations.run(function(err, values) {
    if (err) return cb(err);
    if (!values.cache) return cb();

    // If no joins are used grab current collection's item from the cache and pass to the returnResults
    // function.
    if (!criteria.joins) {
      values = values.cache[self.identity];
      return returnResults(values);
    }

    // If the values are already combined, return the results
    if (values.combined) {
      return returnResults(values.cache[self.identity]);
    }

    // Find the primaryKey of the current model so it can be passed down to the integrator.
    // Use 'id' as a good general default;
    var primaryKey = 'id';

    Object.keys(self._schema.schema).forEach(function(key) {
      if (self._schema.schema[key].hasOwnProperty('primaryKey') && self._schema.schema[key].primaryKey) {
        primaryKey = key;
      }
    });

    // Perform in-memory joins
    Integrator(values.cache, criteria.joins, primaryKey, function(err, results) {
      if (err) return cb(err);
      if (!results) return cb();

      // We need to run one last check on the results using the criteria. This allows a self
      // association where we end up with two records in the cache both having each other as
      // embedded objects and we only want one result. However we need to filter any join criteria
      // out of the top level where query so that searchs by primary key still work.
      var tmpCriteria = _.cloneDeep(criteria.where);
      if (!tmpCriteria) tmpCriteria = {};

      criteria.joins.forEach(function(join) {
        if (!hasOwnProperty(join, 'alias')) return;

        // Check for 'OR' criteria
        if (hasOwnProperty(tmpCriteria, 'or')) {
          tmpCriteria.or.forEach(function(search) {
            if (!hasOwnProperty(search, join.alias)) return;
            delete search[join.alias];
          });
        }

        if (!hasOwnProperty(tmpCriteria, join.alias)) return;
        delete tmpCriteria[join.alias]; ...
```
- example usage
```shell
...

'''javascript
var postgres = require('sails-postgresql');

new User({ tableName: 'foobar', adapters: { postgresql: postgres }}, function(err, Model) {

  // We now have an instantiated collection to execute queries against
  Model.find()
  .where({ age: 21 })
  .limit(10)
  .exec(function(err, users) {
    // Now we have an array of users
  });

});
...
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.findAll"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>findAll (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.findAll)
- description and source-code
```javascript
findAll = function (criteria, options, cb) {
  if (typeof criteria === 'function') {
    cb = criteria;
    criteria = null;
    options = null;
  }

  if (typeof options === 'function') {
    cb = options;
    options = null;
  }

  // Return Deferred or pass to adapter
  if (typeof cb !== 'function') {
    return new Deferred(this, this.findAll, criteria);
  }

  cb(new Error('In Waterline >= 0.9, findAll() has been deprecated in favor of find().' +
              '\nPlease visit the migration guide at http://sailsjs.org for help upgrading.'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.findLike"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>findLike (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.findLike)
- description and source-code
```javascript
findLike = function (criteria, options, cb) {
  var usage = utils.capitalize(this.identity) + '.findLike([criteria],[options],callback)';

  // Normalize criteria
  criteria = normalize.likeCriteria(criteria, this._schema.schema);
  if (!criteria) return usageError('Criteria must be an object!', usage, cb);

  this.find(criteria, options, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.findOne"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>findOne (criteria, cb)](#apidoc.element.waterline.Collection.super_.prototype.findOne)
- description and source-code
```javascript
findOne = function (criteria, cb) {
  var self = this;

  if (typeof criteria === 'function') {
    cb = criteria;
    criteria = null;
  }

  // If the criteria is an array of objects, wrap it in an "or"
  if (Array.isArray(criteria) && _.all(criteria, function(crit) {return _.isObject(crit);})) {
    criteria = {or: criteria};
  }

  // Check if criteria is an integer or string and normalize criteria
  // to object, using the specified primary key field.
  criteria = normalize.expandPK(self, criteria);

  // Normalize criteria
  criteria = normalize.criteria(criteria);

  // Return Deferred or pass to adapter
  if (typeof cb !== 'function') {
    return new Deferred(this, this.findOne, criteria);
  }

  // Transform Search Criteria
  criteria = self._transformer.serialize(criteria);

  // serialize populated object
  if (criteria.joins) {
    criteria.joins.forEach(function(join) {
      if (join.criteria && join.criteria.where) {
        var joinCollection = self.waterline.collections[join.child];
        join.criteria.where = joinCollection._transformer.serialize(join.criteria.where);
      }
    });
  }

  // If there was something defined in the criteria that would return no results, don't even
  // run the query and just return an empty result set.
  if (criteria === false || criteria.where === null) {
    // Build Default Error Message
    var err = '.findOne() requires a criteria. If you want the first record try .find().limit(1)';
    return cb(new Error(err));
  }

  // Build up an operations set
  var operations = new Operations(self, criteria, 'findOne');

  // Run the operations
  operations.run(function(err, values) {
    if (err) return cb(err);
    if (!values.cache) return cb();

    // If no joins are used grab the only item from the cache and pass to the returnResults
    // function.
    if (!criteria.joins) {
      values = values.cache[self.identity];
      return returnResults(values);
    }

    // If the values are already combined, return the results
    if (values.combined) {
      return returnResults(values.cache[self.identity]);
    }

    // Find the primaryKey of the current model so it can be passed down to the integrator.
    // Use 'id' as a good general default;
    var primaryKey = 'id';

    Object.keys(self._schema.schema).forEach(function(key) {
      if (self._schema.schema[key].hasOwnProperty('primaryKey') && self._schema.schema[key].primaryKey) {
        primaryKey = key;
      }
    });


    // Perform in-memory joins
    Integrator(values.cache, criteria.joins, primaryKey, function(err, results) {
      if (err) return cb(err);
      if (!results) return cb();

      // We need to run one last check on the results using the criteria. This allows a self
      // association where we end up with two records in the cache both having each other as
      // embedded objects and we only want one result. However we need to filter any join criteria
      // out of the top level where query so that searchs by primary key still work.
      var tmpCriteria = _.cloneDeep(criteria.where);
      if (!tmpCriteria) tmpCriteria = {};

      criteria.joins.forEach(function(join) {
        if (!hasOwnProperty(join, 'alias')) return;

        // Check for 'OR' criteria
        if (hasOwnProperty(tmpCriteria, 'or')) {
          tmpCriteria.or.forEach(function(search) {
            if (!hasOwnProperty(search, join.alias)) return;
            delete search[join.alias];
          });
        }

        if (!hasOwnProperty(tmpCriteria, join.alias)) return;
        delete tmpCriteria[join.alias];
      });

      // Pass results into Waterline-Criteria
      var _criteria = { where: tmpCriteria };
      results = waterlineCriteria('parent', { parent: results }, _criteria).results;

      results.forEach(function(res) {

        // Go Ahead and perform any sorts on the associated data
        criteria.joins.forEach(function(join) {
          if (!join.criteria) return;
          var c = normalize.criteria(join.criteria);
          if (!c.sort) return;

          var alias = join.alias;
          res[alias] = so ...
```
- example usage
```shell
...
## Query Methods

Queries can be run with either a callback interface or with a deferred object. For building complicated queries, the deferred object
 method is the best choice. For convenience, promises are supported by default.

**Callback Method**

'''javascript
User.findOne({ id: 1 }, function(err, user) {
  // Do stuff here
});
'''

**Deferred Object Method**

'''javascript
...
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.findOneLike"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>findOneLike (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.findOneLike)
- description and source-code
```javascript
findOneLike = function (criteria, options, cb) {
  var usage = utils.capitalize(this.identity) + '.findOneLike([criteria],[options],callback)';

  // Normalize criteria
  criteria = normalize.likeCriteria(criteria, this._schema.schema);
  if (!criteria) return usageError('Criteria must be an object!', usage, cb);

  this.findOne(criteria, options, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.findOrCreate"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>findOrCreate (criteria, values, cb)](#apidoc.element.waterline.Collection.super_.prototype.findOrCreate)
- description and source-code
```javascript
findOrCreate = function (criteria, values, cb) {
  var self = this;

  if (typeof values === 'function') {
    cb = values;
    values = null;
  }

  // If no criteria is specified, bail out with a vengeance.
  var usage = utils.capitalize(this.identity) + '.findOrCreate([criteria], values, callback)';
  if (typeof cb == 'function' && (!criteria || criteria.length === 0)) {
    return usageError('No criteria option specified!', usage, cb);
  }

  // Normalize criteria
  criteria = normalize.criteria(criteria);
  // If no values were specified, use criteria
  if (!values) values = criteria.where ? criteria.where : criteria;

  // Return Deferred or pass to adapter
  if (typeof cb !== 'function') {
    return new Deferred(this, this.findOrCreate, criteria, values);
  }

  // This is actually an implicit call to findOrCreateEach
  if (Array.isArray(criteria) && Array.isArray(values)) {
    return this.findOrCreateEach(criteria, values, cb);
  }

  if (typeof cb !== 'function') return usageError('Invalid callback specified!', usage, cb);

  // Try a find first.
  this.find(criteria).exec(function(err, results) {
    if (err) return cb(err);

    if (results && results.length !== 0) {

      // Unserialize values
      results = self._transformer.unserialize(results[0]);

      // Return an instance of Model
      var model = new self._model(results);
      return cb(null, model);
    }

    // Create a new record if nothing is found.
    self.create(values).exec(function(err, result) {
      if (err) return cb(err);
      return cb(null, result);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.findOrCreateEach"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>findOrCreateEach (criteria, valuesList, cb)](#apidoc.element.waterline.Collection.super_.prototype.findOrCreateEach)
- description and source-code
```javascript
findOrCreateEach = function (criteria, valuesList, cb) {
  var self = this;

  if (typeof valuesList === 'function') {
    cb = valuesList;
    valuesList = null;
  }

  // Normalize criteria
  criteria = normalize.criteria(criteria);

  // Return Deferred or pass to adapter
  if (typeof cb !== 'function') {
    return new Deferred(this, this.findOrCreateEach, criteria, valuesList);
  }

  // Validate Params
  var usage = utils.capitalize(this.identity) + '.findOrCreateEach(criteria, valuesList, callback)';

  if (typeof cb !== 'function') return usageError('Invalid callback specified!', usage, cb);
  if (!criteria) return usageError('No criteria specified!', usage, cb);
  if (!Array.isArray(criteria)) return usageError('No criteria specified!', usage, cb);
  if (!valuesList) return usageError('No valuesList specified!', usage, cb);
  if (!Array.isArray(valuesList)) return usageError('Invalid valuesList specified (should be an array!)', usage, cb);

  var errStr = _validateValues(valuesList);
  if (errStr) return usageError(errStr, usage, cb);

  // Validate each record in the array and if all are valid
  // pass the array to the adapter's findOrCreateEach method
  var validateItem = function(item, next) {
    _validate.call(self, item, next);
  };


  async.each(valuesList, validateItem, function(err) {
    if (err) return cb(err);

    // Transform Values
    var transformedValues = [];

    valuesList.forEach(function(value) {

      // Transform values
      value = self._transformer.serialize(value);

      // Clean attributes
      value = self._schema.cleanValues(value);
      transformedValues.push(value);
    });

    // Set values array to the transformed array
    valuesList = transformedValues;

    // Transform Search Criteria
    var transformedCriteria = [];

    criteria.forEach(function(value) {
      value = self._transformer.serialize(value);
      transformedCriteria.push(value);
    });

    // Set criteria array to the transformed array
    criteria = transformedCriteria;

    // Pass criteria and attributes to adapter definition
    self.adapter.findOrCreateEach(criteria, valuesList, function(err, values) {
      if (err) return cb(err);

      // Unserialize Values
      var unserializedValues = [];

      values.forEach(function(value) {
        value = self._transformer.unserialize(value);
        unserializedValues.push(value);
      });

      // Set values array to the transformed array
      values = unserializedValues;

      // Run AfterCreate Callbacks
      async.each(values, function(item, next) {
        callbacks.afterCreate(self, item, next);
      }, function(err) {
        if (err) return cb(err);

        var models = [];

        // Make each result an instance of model
        values.forEach(function(value) {
          models.push(new self._model(value));
        });

        cb(null, models);
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.generateAssociationFinders"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>generateAssociationFinders (attrName)](#apidoc.element.waterline.Collection.super_.prototype.generateAssociationFinders)
- description and source-code
```javascript
generateAssociationFinders = function (attrName) {
  var self = this;
  var name, model;

  // Find the user defined key for this attrName, look in self defined columnName
  // properties and if that's not set see if the generated columnName matches the attrName
  for (var key in this._attributes) {

    // Cache the value
    var cache = this._attributes[key];

    if (!hasOwnProperty(cache, 'model')) continue;

    if (cache.model.toLowerCase() + '_id' === attrName) {
      name = key;
      model = cache.model;
    }
  }

  if (!name || !model) return;

  // Build a findOneBy<attrName> dynamic finder that forces a join on the association
  this['findOneBy' + utils.capitalize(name)] = function dynamicAssociationMethod(value, cb) {

    // Check proper usage
    var usage = utils.capitalize(self.identity) + '.' + 'findBy' + utils.capitalize(name) +
      '(someValue, callback)';

    if (typeof value === 'undefined') return usageError('No value specified!', usage, cb);
    if (typeof value === 'function') return usageError('No value specified!', usage, cb);

    var criteria = associationQueryCriteria(self, value, attrName);
    return this.findOne(criteria, cb);
  };

  // Build a findBy<attrName> dynamic finder that forces a join on the association
  this['findBy' + utils.capitalize(name)] = function dynamicAssociationMethod(value, cb) {

    // Check proper usage
    var usage = utils.capitalize(self.identity) + '.' + 'findBy' + utils.capitalize(name) +
      '(someValue, callback)';

    if (typeof value === 'undefined') return usageError('No value specified!', usage, cb);
    if (typeof value === 'function') return usageError('No value specified!', usage, cb);

    var criteria = associationQueryCriteria(self, value, attrName);
    return this.find(criteria, cb);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.generateDynamicFinder"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>generateDynamicFinder (attrName, method, dontCapitalize)](#apidoc.element.waterline.Collection.super_.prototype.generateDynamicFinder)
- description and source-code
```javascript
generateDynamicFinder = function (attrName, method, dontCapitalize) {
  var self = this;
  var criteria;

  // Capitalize Attribute Name for camelCase
  var preparedAttrName = dontCapitalize ? attrName : utils.capitalize(attrName);

  // Figure out actual dynamic method name by injecting attribute name
  var actualMethodName = method.replace(/\*/g, preparedAttrName);

  // Assign this finder to the collection
  this[actualMethodName] = function dynamicMethod(value, options, cb) {

    if (typeof options === 'function') {
      cb = options;
      options = null;
    }

    options = options || {};

    var usage = utils.capitalize(self.identity) + '.' + actualMethodName + '(someValue,[options],callback)';

    if (typeof value === 'undefined') return usageError('No value specified!', usage, cb);
    if (options.where) return usageError('Cannot specify 'where' option in a dynamic ' + method + '*() query!', usage, cb);

    // Build criteria query and submit it
    options.where = {};
    options.where[attrName] = value;

    switch (method) {


      ///////////////////////////////////////
      // Finders
      ///////////////////////////////////////


      case 'findOneBy*':
      case 'findOneBy*In':
        return self.findOne(options, cb);

      case 'findOneBy*Like':
        criteria = _.extend(options, {
          where: {
            like: options.where
          }
        });

        return self.findOne(criteria, cb);


      ///////////////////////////////////////
      // Aggregate Finders
      ///////////////////////////////////////


      case 'findBy*':
      case 'findBy*In':
        return self.find(options, cb);

      case 'findBy*Like':
        criteria = _.extend(options, {
          where: {
            like: options.where
          }
        });

        return self.find(criteria, cb);


      ///////////////////////////////////////
      // Count Finders
      ///////////////////////////////////////


      case 'countBy*':
      case 'countBy*In':
        return self.count(options, cb);

      case 'countBy*Like':
        criteria = _.extend(options, {
          where: {
            like: options.where
          }
        });

        return self.count(criteria, cb);


      ///////////////////////////////////////
      // Searchers
      ///////////////////////////////////////

      case '*StartsWith':
        return self.startsWith(options, cb);

      case '*Contains':
        return self.contains(options, cb);

      case '*EndsWith':
        return self.endsWith(options, cb);
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.join"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>join (collection, fk, pk, cb)](#apidoc.element.waterline.Collection.super_.prototype.join)
- description and source-code
```javascript
join = function (collection, fk, pk, cb) {
  this._adapter.join(collection, fk, pk, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.select"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>select ()](#apidoc.element.waterline.Collection.super_.prototype.select)
- description and source-code
```javascript
select = function () {
  this.find.apply(this, Array.prototype.slice.call(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.startsWith"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>startsWith (criteria, options, cb)](#apidoc.element.waterline.Collection.super_.prototype.startsWith)
- description and source-code
```javascript
startsWith = function (criteria, options, cb) {
  var usage = utils.capitalize(this.identity) + '.startsWith([criteria],[options],callback)';

  criteria = normalize.likeCriteria(criteria, this._schema.schema, function applyStartsWith(criteria) {
    return criteria + '%';
  });

  if (!criteria) return usageError('Criteria must be an object!', usage, cb);

  this.find(criteria, options, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.stream"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>stream (criteria, transformation)](#apidoc.element.waterline.Collection.super_.prototype.stream)
- description and source-code
```javascript
stream = function (criteria, transformation) {
  var self = this;

  var usage = utils.capitalize(this.identity) + '.stream([criteria],[options])';

  // Normalize criteria and fold in options
  criteria = normalize.criteria(criteria);

  // Transform Search Criteria
  criteria = self._transformer.serialize(criteria);

  // Configure stream to adapter, kick off fetch, and return stream object
  // so that user code can use it as it fires data events
  var stream = new ModelStream(transformation);

  // very important to wait until next tick before triggering adapter
  // otherwise write() and end() won't fire properly
  process.nextTick(function() {

    // Write once immediately to force prefix in case no models are returned
    stream.write();

    // Trigger Adapter Method
    self.adapter.stream(criteria, stream);
  });

  return stream;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.sync"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>sync (cb)](#apidoc.element.waterline.Collection.super_.prototype.sync)
- description and source-code
```javascript
sync = function (cb) {
  var self = this;

  // If any adapters used in this collection have syncable turned off set migrate to safe.
  //
  // I don't think a collection would ever need two adapters where one needs migrations and
  // the other doesn't but it may be a possibility. The way the auto-migrations work now doesn't
  // allow for this either way so this should be good. We will probably need to revist this soonish
  // however and take a pass at getting something working for better migration systems.
  // - particlebanana

  _.keys(this.connections).forEach(function(connectionName) {
    var adapter = self.connections[connectionName]._adapter;

    // If not syncable, don't sync
    if (hop(adapter, 'syncable') && !adapter.syncable) {
      self.migrate = 'safe';
    }
  });

  // Assign synchronization behavior depending on migrate option in collection
  if (this.migrate && ['drop', 'alter', 'create', 'safe'].indexOf(this.migrate) > -1) {

    // Determine which sync strategy to use
    var strategyMethodName = 'migrate' + utils.capitalize(this.migrate);

    // Run automigration strategy
    this.adapter[strategyMethodName](function(err) {
      if (err) return cb(err);
      cb();
    });
  }

  // Throw Error
  else cb(new Error('Invalid 'migrate' strategy defined for collection. Must be one of the following: drop, alter, create, safe'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.update"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>update (criteria, values, cb)](#apidoc.element.waterline.Collection.super_.prototype.update)
- description and source-code
```javascript
update = function (criteria, values, cb) {

  var self = this;

  if (typeof criteria === 'function') {
    cb = criteria;
    criteria = null;
  }

  // Return Deferred or pass to adapter
  if (typeof cb !== 'function') {
    return new Deferred(this, this.update, criteria, values);
  }

  // If there was something defined in the criteria that would return no results, don't even
  // run the query and just return an empty result set.
  if (criteria === false) {
    return cb(null, []);
  }

  // Ensure proper function signature
  var usage = utils.capitalize(this.identity) + '.update(criteria, values, callback)';
  if (!values) return usageError('No updated values specified!', usage, cb);

  // Format Criteria and Values
  var valuesObject = prepareArguments.call(this, criteria, values);

  // Create any of the belongsTo associations and set the foreign key values
  createBelongsTo.call(this, valuesObject, function(err) {
    if (err) return cb(err);

    beforeCallbacks.call(self, valuesObject.values, function(err) {
      if (err) return cb(err);
      updateRecords.call(self, valuesObject, cb);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.validate"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>validate (values, presentOnly, cb)](#apidoc.element.waterline.Collection.super_.prototype.validate)
- description and source-code
```javascript
validate = function (values, presentOnly, cb) {
  var self = this;

  // Handle optional second arg
  if (typeof presentOnly === 'function') {
    cb = presentOnly;
    presentOnly = false;
  }

  async.series([

    // Run Before Validate Lifecycle Callbacks
    function(cb) {
      var runner = function(item, callback) {
        item.call(self, values, function(err) {
          if (err) return callback(err);
          callback();
        });
      };

      async.eachSeries(self._callbacks.beforeValidate, runner, function(err) {
        if (err) return cb(err);
        cb();
      });
    },

    // Run Validation
    function(cb) {
      self._validator.validate(values, presentOnly, function _afterValidating(err, invalidAttributes) {
        // If fatal error occurred, handle it accordingly.
        if (err) {
          return cb(err);
        }

        // Otherwise, check out the invalid attributes that were sent back.
        //
        // Create validation error here
        // (pass in the invalid attributes as well as the collection's globalId)
        if (invalidAttributes) {
          return cb(new WLValidationError({
            invalidAttributes: invalidAttributes,
            model: self.globalId || self.adapter.identity
          }));
        }

        cb();
      });
    },

    // Run After Validate Lifecycle Callbacks
    function(cb) {
      var runner = function(item, callback) {
        item(values, function(err) {
          if (err) return callback(err);
          callback();
        });
      };

      async.eachSeries(self._callbacks.afterValidate, runner, function(err) {
        if (err) return cb(err);
        cb();
      });
    }

  ], function(err) {
    if (err) return cb(err);
    cb();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.waterline.Collection.super_.prototype.where"></a>[function <span class="apidocSignatureSpan">waterline.Collection.super_.prototype.</span>where ()](#apidoc.element.waterline.Collection.super_.prototype.where)
- description and source-code
```javascript
where = function () {
  this.find.apply(this, Array.prototype.slice.call(arguments));
}
```
- example usage
```shell
...
'''javascript
var postgres = require('sails-postgresql');

new User({ tableName: 'foobar', adapters: { postgresql: postgres }}, function(err, Model) {

  // We now have an instantiated collection to execute queries against
  Model.find()
  .where({ age: 21 })
  .limit(10)
  .exec(function(err, users) {
    // Now we have an array of users
  });

});
'''
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
