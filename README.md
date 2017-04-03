# api documentation for  [readable-stream (v2.2.6)](https://github.com/nodejs/readable-stream#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-readable-stream.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-readable-stream) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-readable-stream.svg)](https://travis-ci.org/npmdoc/node-npmdoc-readable-stream)
#### Streams3, a user-land copy of the stream library from Node.js

[![NPM](https://nodei.co/npm/readable-stream.png?downloads=true)](https://www.npmjs.com/package/readable-stream)

[![apidoc](https://npmdoc.github.io/node-npmdoc-readable-stream/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-readable-stream_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-readable-stream/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-readable-stream/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-readable-stream/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "browser": {
        "util": false
    },
    "bugs": {
        "url": "https://github.com/nodejs/readable-stream/issues"
    },
    "dependencies": {
        "buffer-shims": "^1.0.0",
        "core-util-is": "~1.0.0",
        "inherits": "~2.0.1",
        "isarray": "~1.0.0",
        "process-nextick-args": "~1.0.6",
        "string_decoder": "~0.10.x",
        "util-deprecate": "~1.0.1"
    },
    "description": "Streams3, a user-land copy of the stream library from Node.js",
    "devDependencies": {
        "assert": "~1.4.0",
        "babel-polyfill": "^6.9.1",
        "buffer": "^4.9.0",
        "nyc": "^6.4.0",
        "tap": "~0.7.1",
        "tape": "~4.5.1",
        "zuul": "~3.10.0"
    },
    "directories": {},
    "dist": {
        "shasum": "8b43aed76e71483938d12a8d46c6cf1a00b1f816",
        "tarball": "https://registry.npmjs.org/readable-stream/-/readable-stream-2.2.6.tgz"
    },
    "gitHead": "f94eebc1c5b637e6575735e6923ec79ee3139284",
    "homepage": "https://github.com/nodejs/readable-stream#readme",
    "keywords": [
        "readable",
        "stream",
        "pipe"
    ],
    "license": "MIT",
    "main": "readable.js",
    "maintainers": [
        {
            "name": "cwmma",
            "email": "calvin.metcalf@gmail.com"
        },
        {
            "name": "isaacs",
            "email": "i@izs.me"
        },
        {
            "name": "matteo.collina",
            "email": "hello@matteocollina.com"
        },
        {
            "name": "rvagg",
            "email": "rod@vagg.org"
        },
        {
            "name": "tootallnate",
            "email": "nathan@tootallnate.net"
        }
    ],
    "name": "readable-stream",
    "nyc": {
        "include": [
            "lib/**.js"
        ]
    },
    "optionalDependencies": {},
    "react-native": {
        "stream": false
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/nodejs/readable-stream.git"
    },
    "scripts": {
        "browser": "npm run write-zuul && zuul --browser-retries 2 -- test/browser.js",
        "cover": "nyc npm test",
        "local": "zuul --local 3000 --no-coverage -- test/browser.js",
        "report": "nyc report --reporter=lcov",
        "test": "tap test/parallel/*.js test/ours/*.js",
        "write-zuul": "printf \"ui: tape\nbrowsers:\n  - name: $BROWSER_NAME\n    version: $BROWSER_VERSION\n\">.zuul.yml"
    },
    "version": "2.2.6"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module readable-stream](#apidoc.module.readable-stream)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>Duplex (options)](#apidoc.element.readable-stream.Duplex)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>PassThrough (options)](#apidoc.element.readable-stream.PassThrough)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>Readable (options)](#apidoc.element.readable-stream.Readable)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>ReadableState (options, stream)](#apidoc.element.readable-stream.ReadableState)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>Stream ()](#apidoc.element.readable-stream.Stream)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>Transform (options)](#apidoc.element.readable-stream.Transform)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>Writable (options)](#apidoc.element.readable-stream.Writable)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>Writable.WritableState (options, stream)](#apidoc.element.readable-stream.Writable.WritableState)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>_fromList (n, state)](#apidoc.element.readable-stream._fromList)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>super_ ()](#apidoc.element.readable-stream.super_)
1.  object <span class="apidocSignatureSpan">readable-stream.</span>Duplex.prototype
1.  object <span class="apidocSignatureSpan">readable-stream.</span>PassThrough.prototype
1.  object <span class="apidocSignatureSpan">readable-stream.</span>Transform.prototype
1.  object <span class="apidocSignatureSpan">readable-stream.</span>Writable.WritableState.prototype
1.  object <span class="apidocSignatureSpan">readable-stream.</span>Writable.prototype

#### [module readable-stream.Duplex](#apidoc.module.readable-stream.Duplex)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>Duplex (options)](#apidoc.element.readable-stream.Duplex.Duplex)
1.  [function <span class="apidocSignatureSpan">readable-stream.Duplex.</span>super_ (options)](#apidoc.element.readable-stream.Duplex.super_)

#### [module readable-stream.Duplex.prototype](#apidoc.module.readable-stream.Duplex.prototype)
1.  [function <span class="apidocSignatureSpan">readable-stream.Duplex.prototype.</span>_write (chunk, encoding, cb)](#apidoc.element.readable-stream.Duplex.prototype._write)
1.  [function <span class="apidocSignatureSpan">readable-stream.Duplex.prototype.</span>cork ()](#apidoc.element.readable-stream.Duplex.prototype.cork)
1.  [function <span class="apidocSignatureSpan">readable-stream.Duplex.prototype.</span>end (chunk, encoding, cb)](#apidoc.element.readable-stream.Duplex.prototype.end)
1.  [function <span class="apidocSignatureSpan">readable-stream.Duplex.prototype.</span>setDefaultEncoding (encoding)](#apidoc.element.readable-stream.Duplex.prototype.setDefaultEncoding)
1.  [function <span class="apidocSignatureSpan">readable-stream.Duplex.prototype.</span>uncork ()](#apidoc.element.readable-stream.Duplex.prototype.uncork)
1.  [function <span class="apidocSignatureSpan">readable-stream.Duplex.prototype.</span>write (chunk, encoding, cb)](#apidoc.element.readable-stream.Duplex.prototype.write)
1.  object <span class="apidocSignatureSpan">readable-stream.Duplex.prototype.</span>_writev

#### [module readable-stream.PassThrough](#apidoc.module.readable-stream.PassThrough)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>PassThrough (options)](#apidoc.element.readable-stream.PassThrough.PassThrough)
1.  [function <span class="apidocSignatureSpan">readable-stream.PassThrough.</span>super_ (options)](#apidoc.element.readable-stream.PassThrough.super_)

#### [module readable-stream.PassThrough.prototype](#apidoc.module.readable-stream.PassThrough.prototype)
1.  [function <span class="apidocSignatureSpan">readable-stream.PassThrough.prototype.</span>_transform (chunk, encoding, cb)](#apidoc.element.readable-stream.PassThrough.prototype._transform)

#### [module readable-stream.Transform](#apidoc.module.readable-stream.Transform)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>Transform (options)](#apidoc.element.readable-stream.Transform.Transform)
1.  [function <span class="apidocSignatureSpan">readable-stream.Transform.</span>super_ (options)](#apidoc.element.readable-stream.Transform.super_)

#### [module readable-stream.Transform.prototype](#apidoc.module.readable-stream.Transform.prototype)
1.  [function <span class="apidocSignatureSpan">readable-stream.Transform.prototype.</span>_read (n)](#apidoc.element.readable-stream.Transform.prototype._read)
1.  [function <span class="apidocSignatureSpan">readable-stream.Transform.prototype.</span>_transform (chunk, encoding, cb)](#apidoc.element.readable-stream.Transform.prototype._transform)
1.  [function <span class="apidocSignatureSpan">readable-stream.Transform.prototype.</span>_write (chunk, encoding, cb)](#apidoc.element.readable-stream.Transform.prototype._write)
1.  [function <span class="apidocSignatureSpan">readable-stream.Transform.prototype.</span>push (chunk, encoding)](#apidoc.element.readable-stream.Transform.prototype.push)

#### [module readable-stream.Writable](#apidoc.module.readable-stream.Writable)
1.  [function <span class="apidocSignatureSpan">readable-stream.</span>Writable (options)](#apidoc.element.readable-stream.Writable.Writable)
1.  [function <span class="apidocSignatureSpan">readable-stream.Writable.</span>WritableState (options, stream)](#apidoc.element.readable-stream.Writable.WritableState)
1.  [function <span class="apidocSignatureSpan">readable-stream.Writable.</span>super_ ()](#apidoc.element.readable-stream.Writable.super_)

#### [module readable-stream.Writable.WritableState](#apidoc.module.readable-stream.Writable.WritableState)
1.  [function <span class="apidocSignatureSpan">readable-stream.Writable.</span>WritableState (options, stream)](#apidoc.element.readable-stream.Writable.WritableState.WritableState)

#### [module readable-stream.Writable.WritableState.prototype](#apidoc.module.readable-stream.Writable.WritableState.prototype)
1.  [function <span class="apidocSignatureSpan">readable-stream.Writable.WritableState.prototype.</span>getBuffer ()](#apidoc.element.readable-stream.Writable.WritableState.prototype.getBuffer)

#### [module readable-stream.Writable.prototype](#apidoc.module.readable-stream.Writable.prototype)
1.  [function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>_write (chunk, encoding, cb)](#apidoc.element.readable-stream.Writable.prototype._write)
1.  [function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>cork ()](#apidoc.element.readable-stream.Writable.prototype.cork)
1.  [function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>end (chunk, encoding, cb)](#apidoc.element.readable-stream.Writable.prototype.end)
1.  [function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>pipe ()](#apidoc.element.readable-stream.Writable.prototype.pipe)
1.  [function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>setDefaultEncoding (encoding)](#apidoc.element.readable-stream.Writable.prototype.setDefaultEncoding)
1.  [function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>uncork ()](#apidoc.element.readable-stream.Writable.prototype.uncork)
1.  [function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>write (chunk, encoding, cb)](#apidoc.element.readable-stream.Writable.prototype.write)
1.  object <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>_writev



# <a name="apidoc.module.readable-stream"></a>[module readable-stream](#apidoc.module.readable-stream)

#### <a name="apidoc.element.readable-stream.Duplex"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>Duplex (options)](#apidoc.element.readable-stream.Duplex)
- description and source-code
```javascript
function Duplex(options) {
  if (!(this instanceof Duplex)) return new Duplex(options);

  Readable.call(this, options);
  Writable.call(this, options);

  if (options && options.readable === false) this.readable = false;

  if (options && options.writable === false) this.writable = false;

  this.allowHalfOpen = true;
  if (options && options.allowHalfOpen === false) this.allowHalfOpen = false;

  this.once('end', onend);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.PassThrough"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>PassThrough (options)](#apidoc.element.readable-stream.PassThrough)
- description and source-code
```javascript
function PassThrough(options) {
  if (!(this instanceof PassThrough)) return new PassThrough(options);

  Transform.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Readable"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>Readable (options)](#apidoc.element.readable-stream.Readable)
- description and source-code
```javascript
function Readable(options) {
  Duplex = Duplex || require('./_stream_duplex');

  if (!(this instanceof Readable)) return new Readable(options);

  this._readableState = new ReadableState(options, this);

  // legacy
  this.readable = true;

  if (options && typeof options.read === 'function') this._read = options.read;

  Stream.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.ReadableState"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>ReadableState (options, stream)](#apidoc.element.readable-stream.ReadableState)
- description and source-code
```javascript
function ReadableState(options, stream) {
  Duplex = Duplex || require('./_stream_duplex');

  options = options || {};

  // object stream flag. Used to make read(n) ignore n and to
  // make all the buffer merging and length checks go away
  this.objectMode = !!options.objectMode;

  if (stream instanceof Duplex) this.objectMode = this.objectMode || !!options.readableObjectMode;

  // the point at which it stops calling _read() to fill the buffer
  // Note: 0 is a valid value, means "don't call _read preemptively ever"
  var hwm = options.highWaterMark;
  var defaultHwm = this.objectMode ? 16 : 16 * 1024;
  this.highWaterMark = hwm || hwm === 0 ? hwm : defaultHwm;

  // cast to ints.
  this.highWaterMark = ~~this.highWaterMark;

  // A linked list is used to store data chunks instead of an array because the
  // linked list can remove elements from the beginning faster than
  // array.shift()
  this.buffer = new BufferList();
  this.length = 0;
  this.pipes = null;
  this.pipesCount = 0;
  this.flowing = null;
  this.ended = false;
  this.endEmitted = false;
  this.reading = false;

  // a flag to be able to tell if the onwrite cb is called immediately,
  // or on a later tick.  We set this to true at first, because any
  // actions that shouldn't happen until "later" should generally also
  // not happen before the first write call.
  this.sync = true;

  // whenever we return null, then we set a flag to say
  // that we're awaiting a 'readable' event emission.
  this.needReadable = false;
  this.emittedReadable = false;
  this.readableListening = false;
  this.resumeScheduled = false;

  // Crypto is kind of old and crusty.  Historically, its default string
  // encoding is 'binary' so we have to make this configurable.
  // Everything else in the universe uses 'utf8', though.
  this.defaultEncoding = options.defaultEncoding || 'utf8';

  // when piping, we only care about 'readable' events that happen
  // after read()ing all the bytes and not getting any pushback.
  this.ranOut = false;

  // the number of writers that are awaiting a drain event in .pipe()s
  this.awaitDrain = 0;

  // if true, a maybeReadMore has been scheduled
  this.readingMore = false;

  this.decoder = null;
  this.encoding = null;
  if (options.encoding) {
    if (!StringDecoder) StringDecoder = require('string_decoder/').StringDecoder;
    this.decoder = new StringDecoder(options.encoding);
    this.encoding = options.encoding;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Stream"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>Stream ()](#apidoc.element.readable-stream.Stream)
- description and source-code
```javascript
function Stream() {
  EE.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Transform"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>Transform (options)](#apidoc.element.readable-stream.Transform)
- description and source-code
```javascript
function Transform(options) {
  if (!(this instanceof Transform)) return new Transform(options);

  Duplex.call(this, options);

  this._transformState = new TransformState(this);

  var stream = this;

  // start out asking for a readable event once data is transformed.
  this._readableState.needReadable = true;

  // we have implemented the _read method, and done the other things
  // that Readable wants before the first _read call, so unset the
  // sync guard flag.
  this._readableState.sync = false;

  if (options) {
    if (typeof options.transform === 'function') this._transform = options.transform;

    if (typeof options.flush === 'function') this._flush = options.flush;
  }

  // When the writable side finishes, then flush out anything remaining.
  this.once('prefinish', function () {
    if (typeof this._flush === 'function') this._flush(function (er, data) {
      done(stream, er, data);
    });else done(stream);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Writable"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>Writable (options)](#apidoc.element.readable-stream.Writable)
- description and source-code
```javascript
function Writable(options) {
  Duplex = Duplex || require('./_stream_duplex');

  // Writable ctor is applied to Duplexes, too.
  // 'realHasInstance' is necessary because using plain 'instanceof'
  // would return false, as no '_writableState' property is attached.

  // Trying to use the custom 'instanceof' for Writable here will also break the
  // Node.js LazyTransform implementation, which has a non-trivial getter for
  // '_writableState' that would lead to infinite recursion.
  if (!realHasInstance.call(Writable, this) && !(this instanceof Duplex)) {
    return new Writable(options);
  }

  this._writableState = new WritableState(options, this);

  // legacy.
  this.writable = true;

  if (options) {
    if (typeof options.write === 'function') this._write = options.write;

    if (typeof options.writev === 'function') this._writev = options.writev;
  }

  Stream.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Writable.WritableState"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>Writable.WritableState (options, stream)](#apidoc.element.readable-stream.Writable.WritableState)
- description and source-code
```javascript
function WritableState(options, stream) {
  Duplex = Duplex || require('./_stream_duplex');

  options = options || {};

  // object stream flag to indicate whether or not this stream
  // contains buffers or objects.
  this.objectMode = !!options.objectMode;

  if (stream instanceof Duplex) this.objectMode = this.objectMode || !!options.writableObjectMode;

  // the point at which write() starts returning false
  // Note: 0 is a valid value, means that we always return false if
  // the entire buffer is not flushed immediately on write()
  var hwm = options.highWaterMark;
  var defaultHwm = this.objectMode ? 16 : 16 * 1024;
  this.highWaterMark = hwm || hwm === 0 ? hwm : defaultHwm;

  // cast to ints.
  this.highWaterMark = ~~this.highWaterMark;

  // drain event flag.
  this.needDrain = false;
  // at the start of calling end()
  this.ending = false;
  // when end() has been called, and returned
  this.ended = false;
  // when 'finish' is emitted
  this.finished = false;

  // should we decode strings into buffers before passing to _write?
  // this is here so that some node-core streams can optimize string
  // handling at a lower level.
  var noDecode = options.decodeStrings === false;
  this.decodeStrings = !noDecode;

  // Crypto is kind of old and crusty.  Historically, its default string
  // encoding is 'binary' so we have to make this configurable.
  // Everything else in the universe uses 'utf8', though.
  this.defaultEncoding = options.defaultEncoding || 'utf8';

  // not an actual buffer we keep track of, but a measurement
  // of how much we're waiting to get pushed to some underlying
  // socket or file.
  this.length = 0;

  // a flag to see when we're in the middle of a write.
  this.writing = false;

  // when true all writes will be buffered until .uncork() call
  this.corked = 0;

  // a flag to be able to tell if the onwrite cb is called immediately,
  // or on a later tick.  We set this to true at first, because any
  // actions that shouldn't happen until "later" should generally also
  // not happen before the first write call.
  this.sync = true;

  // a flag to know if we're processing previously buffered items, which
  // may call the _write() callback in the same tick, so that we don't
  // end up in an overlapped onwrite situation.
  this.bufferProcessing = false;

  // the callback that's passed to _write(chunk,cb)
  this.onwrite = function (er) {
    onwrite(stream, er);
  };

  // the callback that the user supplies to write(chunk,encoding,cb)
  this.writecb = null;

  // the amount that is being written when _write is called.
  this.writelen = 0;

  this.bufferedRequest = null;
  this.lastBufferedRequest = null;

  // number of pending user-supplied write callbacks
  // this must be 0 before 'finish' can be emitted
  this.pendingcb = 0;

  // emit prefinish if the only thing we're waiting for is _write cbs
  // This is relevant for synchronous Transform streams
  this.prefinished = false;

  // True if the error was already emitted and should not be thrown again
  this.errorEmitted = false;

  // count buffered requests
  this.bufferedRequestCount = 0;

  // allocate the first CorkedRequest, there is always
  // one allocated and free to use, and we maintain at most two
  this.corkedRequestsFree = new CorkedRequest(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream._fromList"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>_fromList (n, state)](#apidoc.element.readable-stream._fromList)
- description and source-code
```javascript
function fromList(n, state) {
  // nothing buffered
  if (state.length === 0) return null;

  var ret;
  if (state.objectMode) ret = state.buffer.shift();else if (!n || n >= state.length) {
    // read it all, truncate the list
    if (state.decoder) ret = state.buffer.join('');else if (state.buffer.length === 1) ret = state.buffer.head.data;else ret = state
.buffer.concat(state.length);
    state.buffer.clear();
  } else {
    // read part of list
    ret = fromListPartial(n, state.buffer, state.decoder);
  }

  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.super_"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>super_ ()](#apidoc.element.readable-stream.super_)
- description and source-code
```javascript
function Stream() {
  EE.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.readable-stream.Duplex"></a>[module readable-stream.Duplex](#apidoc.module.readable-stream.Duplex)

#### <a name="apidoc.element.readable-stream.Duplex.Duplex"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>Duplex (options)](#apidoc.element.readable-stream.Duplex.Duplex)
- description and source-code
```javascript
function Duplex(options) {
  if (!(this instanceof Duplex)) return new Duplex(options);

  Readable.call(this, options);
  Writable.call(this, options);

  if (options && options.readable === false) this.readable = false;

  if (options && options.writable === false) this.writable = false;

  this.allowHalfOpen = true;
  if (options && options.allowHalfOpen === false) this.allowHalfOpen = false;

  this.once('end', onend);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Duplex.super_"></a>[function <span class="apidocSignatureSpan">readable-stream.Duplex.</span>super_ (options)](#apidoc.element.readable-stream.Duplex.super_)
- description and source-code
```javascript
function Readable(options) {
  Duplex = Duplex || require('./_stream_duplex');

  if (!(this instanceof Readable)) return new Readable(options);

  this._readableState = new ReadableState(options, this);

  // legacy
  this.readable = true;

  if (options && typeof options.read === 'function') this._read = options.read;

  Stream.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.readable-stream.Duplex.prototype"></a>[module readable-stream.Duplex.prototype](#apidoc.module.readable-stream.Duplex.prototype)

#### <a name="apidoc.element.readable-stream.Duplex.prototype._write"></a>[function <span class="apidocSignatureSpan">readable-stream.Duplex.prototype.</span>_write (chunk, encoding, cb)](#apidoc.element.readable-stream.Duplex.prototype._write)
- description and source-code
```javascript
_write = function (chunk, encoding, cb) {
  cb(new Error('_write() is not implemented'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Duplex.prototype.cork"></a>[function <span class="apidocSignatureSpan">readable-stream.Duplex.prototype.</span>cork ()](#apidoc.element.readable-stream.Duplex.prototype.cork)
- description and source-code
```javascript
cork = function () {
  var state = this._writableState;

  state.corked++;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Duplex.prototype.end"></a>[function <span class="apidocSignatureSpan">readable-stream.Duplex.prototype.</span>end (chunk, encoding, cb)](#apidoc.element.readable-stream.Duplex.prototype.end)
- description and source-code
```javascript
end = function (chunk, encoding, cb) {
  var state = this._writableState;

  if (typeof chunk === 'function') {
    cb = chunk;
    chunk = null;
    encoding = null;
  } else if (typeof encoding === 'function') {
    cb = encoding;
    encoding = null;
  }

  if (chunk !== null && chunk !== undefined) this.write(chunk, encoding);

  // .end() fully uncorks
  if (state.corked) {
    state.corked = 1;
    this.uncork();
  }

  // ignore unnecessary end() calls.
  if (!state.ending && !state.finished) endWritable(this, state, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Duplex.prototype.setDefaultEncoding"></a>[function <span class="apidocSignatureSpan">readable-stream.Duplex.prototype.</span>setDefaultEncoding (encoding)](#apidoc.element.readable-stream.Duplex.prototype.setDefaultEncoding)
- description and source-code
```javascript
function setDefaultEncoding(encoding) {
  // node::ParseEncoding() requires lower case.
  if (typeof encoding === 'string') encoding = encoding.toLowerCase();
  if (!(['hex', 'utf8', 'utf-8', 'ascii', 'binary', 'base64', 'ucs2', 'ucs-2', 'utf16le', 'utf-16le', 'raw'].indexOf((encoding + '').
toLowerCase()) > -1)) throw new TypeError('Unknown encoding: ' + encoding);
  this._writableState.defaultEncoding = encoding;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Duplex.prototype.uncork"></a>[function <span class="apidocSignatureSpan">readable-stream.Duplex.prototype.</span>uncork ()](#apidoc.element.readable-stream.Duplex.prototype.uncork)
- description and source-code
```javascript
uncork = function () {
  var state = this._writableState;

  if (state.corked) {
    state.corked--;

    if (!state.writing && !state.corked && !state.finished && !state.bufferProcessing && state.bufferedRequest) clearBuffer(this
, state);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Duplex.prototype.write"></a>[function <span class="apidocSignatureSpan">readable-stream.Duplex.prototype.</span>write (chunk, encoding, cb)](#apidoc.element.readable-stream.Duplex.prototype.write)
- description and source-code
```javascript
write = function (chunk, encoding, cb) {
  var state = this._writableState;
  var ret = false;
  var isBuf = Buffer.isBuffer(chunk);

  if (typeof encoding === 'function') {
    cb = encoding;
    encoding = null;
  }

  if (isBuf) encoding = 'buffer';else if (!encoding) encoding = state.defaultEncoding;

  if (typeof cb !== 'function') cb = nop;

  if (state.ended) writeAfterEnd(this, cb);else if (isBuf || validChunk(this, state, chunk, cb)) {
    state.pendingcb++;
    ret = writeOrBuffer(this, state, isBuf, chunk, encoding, cb);
  }

  return ret;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.readable-stream.PassThrough"></a>[module readable-stream.PassThrough](#apidoc.module.readable-stream.PassThrough)

#### <a name="apidoc.element.readable-stream.PassThrough.PassThrough"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>PassThrough (options)](#apidoc.element.readable-stream.PassThrough.PassThrough)
- description and source-code
```javascript
function PassThrough(options) {
  if (!(this instanceof PassThrough)) return new PassThrough(options);

  Transform.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.PassThrough.super_"></a>[function <span class="apidocSignatureSpan">readable-stream.PassThrough.</span>super_ (options)](#apidoc.element.readable-stream.PassThrough.super_)
- description and source-code
```javascript
function Transform(options) {
  if (!(this instanceof Transform)) return new Transform(options);

  Duplex.call(this, options);

  this._transformState = new TransformState(this);

  var stream = this;

  // start out asking for a readable event once data is transformed.
  this._readableState.needReadable = true;

  // we have implemented the _read method, and done the other things
  // that Readable wants before the first _read call, so unset the
  // sync guard flag.
  this._readableState.sync = false;

  if (options) {
    if (typeof options.transform === 'function') this._transform = options.transform;

    if (typeof options.flush === 'function') this._flush = options.flush;
  }

  // When the writable side finishes, then flush out anything remaining.
  this.once('prefinish', function () {
    if (typeof this._flush === 'function') this._flush(function (er, data) {
      done(stream, er, data);
    });else done(stream);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.readable-stream.PassThrough.prototype"></a>[module readable-stream.PassThrough.prototype](#apidoc.module.readable-stream.PassThrough.prototype)

#### <a name="apidoc.element.readable-stream.PassThrough.prototype._transform"></a>[function <span class="apidocSignatureSpan">readable-stream.PassThrough.prototype.</span>_transform (chunk, encoding, cb)](#apidoc.element.readable-stream.PassThrough.prototype._transform)
- description and source-code
```javascript
_transform = function (chunk, encoding, cb) {
  cb(null, chunk);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.readable-stream.Transform"></a>[module readable-stream.Transform](#apidoc.module.readable-stream.Transform)

#### <a name="apidoc.element.readable-stream.Transform.Transform"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>Transform (options)](#apidoc.element.readable-stream.Transform.Transform)
- description and source-code
```javascript
function Transform(options) {
  if (!(this instanceof Transform)) return new Transform(options);

  Duplex.call(this, options);

  this._transformState = new TransformState(this);

  var stream = this;

  // start out asking for a readable event once data is transformed.
  this._readableState.needReadable = true;

  // we have implemented the _read method, and done the other things
  // that Readable wants before the first _read call, so unset the
  // sync guard flag.
  this._readableState.sync = false;

  if (options) {
    if (typeof options.transform === 'function') this._transform = options.transform;

    if (typeof options.flush === 'function') this._flush = options.flush;
  }

  // When the writable side finishes, then flush out anything remaining.
  this.once('prefinish', function () {
    if (typeof this._flush === 'function') this._flush(function (er, data) {
      done(stream, er, data);
    });else done(stream);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Transform.super_"></a>[function <span class="apidocSignatureSpan">readable-stream.Transform.</span>super_ (options)](#apidoc.element.readable-stream.Transform.super_)
- description and source-code
```javascript
function Duplex(options) {
  if (!(this instanceof Duplex)) return new Duplex(options);

  Readable.call(this, options);
  Writable.call(this, options);

  if (options && options.readable === false) this.readable = false;

  if (options && options.writable === false) this.writable = false;

  this.allowHalfOpen = true;
  if (options && options.allowHalfOpen === false) this.allowHalfOpen = false;

  this.once('end', onend);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.readable-stream.Transform.prototype"></a>[module readable-stream.Transform.prototype](#apidoc.module.readable-stream.Transform.prototype)

#### <a name="apidoc.element.readable-stream.Transform.prototype._read"></a>[function <span class="apidocSignatureSpan">readable-stream.Transform.prototype.</span>_read (n)](#apidoc.element.readable-stream.Transform.prototype._read)
- description and source-code
```javascript
_read = function (n) {
  var ts = this._transformState;

  if (ts.writechunk !== null && ts.writecb && !ts.transforming) {
    ts.transforming = true;
    this._transform(ts.writechunk, ts.writeencoding, ts.afterTransform);
  } else {
    // mark that we need a transform, so that any data that comes in
    // will get processed, now that we've asked for it.
    ts.needTransform = true;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Transform.prototype._transform"></a>[function <span class="apidocSignatureSpan">readable-stream.Transform.prototype.</span>_transform (chunk, encoding, cb)](#apidoc.element.readable-stream.Transform.prototype._transform)
- description and source-code
```javascript
_transform = function (chunk, encoding, cb) {
  throw new Error('_transform() is not implemented');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Transform.prototype._write"></a>[function <span class="apidocSignatureSpan">readable-stream.Transform.prototype.</span>_write (chunk, encoding, cb)](#apidoc.element.readable-stream.Transform.prototype._write)
- description and source-code
```javascript
_write = function (chunk, encoding, cb) {
  var ts = this._transformState;
  ts.writecb = cb;
  ts.writechunk = chunk;
  ts.writeencoding = encoding;
  if (!ts.transforming) {
    var rs = this._readableState;
    if (ts.needTransform || rs.needReadable || rs.length < rs.highWaterMark) this._read(rs.highWaterMark);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Transform.prototype.push"></a>[function <span class="apidocSignatureSpan">readable-stream.Transform.prototype.</span>push (chunk, encoding)](#apidoc.element.readable-stream.Transform.prototype.push)
- description and source-code
```javascript
push = function (chunk, encoding) {
  this._transformState.needTransform = false;
  return Duplex.prototype.push.call(this, chunk, encoding);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.readable-stream.Writable"></a>[module readable-stream.Writable](#apidoc.module.readable-stream.Writable)

#### <a name="apidoc.element.readable-stream.Writable.Writable"></a>[function <span class="apidocSignatureSpan">readable-stream.</span>Writable (options)](#apidoc.element.readable-stream.Writable.Writable)
- description and source-code
```javascript
function Writable(options) {
  Duplex = Duplex || require('./_stream_duplex');

  // Writable ctor is applied to Duplexes, too.
  // 'realHasInstance' is necessary because using plain 'instanceof'
  // would return false, as no '_writableState' property is attached.

  // Trying to use the custom 'instanceof' for Writable here will also break the
  // Node.js LazyTransform implementation, which has a non-trivial getter for
  // '_writableState' that would lead to infinite recursion.
  if (!realHasInstance.call(Writable, this) && !(this instanceof Duplex)) {
    return new Writable(options);
  }

  this._writableState = new WritableState(options, this);

  // legacy.
  this.writable = true;

  if (options) {
    if (typeof options.write === 'function') this._write = options.write;

    if (typeof options.writev === 'function') this._writev = options.writev;
  }

  Stream.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Writable.WritableState"></a>[function <span class="apidocSignatureSpan">readable-stream.Writable.</span>WritableState (options, stream)](#apidoc.element.readable-stream.Writable.WritableState)
- description and source-code
```javascript
function WritableState(options, stream) {
  Duplex = Duplex || require('./_stream_duplex');

  options = options || {};

  // object stream flag to indicate whether or not this stream
  // contains buffers or objects.
  this.objectMode = !!options.objectMode;

  if (stream instanceof Duplex) this.objectMode = this.objectMode || !!options.writableObjectMode;

  // the point at which write() starts returning false
  // Note: 0 is a valid value, means that we always return false if
  // the entire buffer is not flushed immediately on write()
  var hwm = options.highWaterMark;
  var defaultHwm = this.objectMode ? 16 : 16 * 1024;
  this.highWaterMark = hwm || hwm === 0 ? hwm : defaultHwm;

  // cast to ints.
  this.highWaterMark = ~~this.highWaterMark;

  // drain event flag.
  this.needDrain = false;
  // at the start of calling end()
  this.ending = false;
  // when end() has been called, and returned
  this.ended = false;
  // when 'finish' is emitted
  this.finished = false;

  // should we decode strings into buffers before passing to _write?
  // this is here so that some node-core streams can optimize string
  // handling at a lower level.
  var noDecode = options.decodeStrings === false;
  this.decodeStrings = !noDecode;

  // Crypto is kind of old and crusty.  Historically, its default string
  // encoding is 'binary' so we have to make this configurable.
  // Everything else in the universe uses 'utf8', though.
  this.defaultEncoding = options.defaultEncoding || 'utf8';

  // not an actual buffer we keep track of, but a measurement
  // of how much we're waiting to get pushed to some underlying
  // socket or file.
  this.length = 0;

  // a flag to see when we're in the middle of a write.
  this.writing = false;

  // when true all writes will be buffered until .uncork() call
  this.corked = 0;

  // a flag to be able to tell if the onwrite cb is called immediately,
  // or on a later tick.  We set this to true at first, because any
  // actions that shouldn't happen until "later" should generally also
  // not happen before the first write call.
  this.sync = true;

  // a flag to know if we're processing previously buffered items, which
  // may call the _write() callback in the same tick, so that we don't
  // end up in an overlapped onwrite situation.
  this.bufferProcessing = false;

  // the callback that's passed to _write(chunk,cb)
  this.onwrite = function (er) {
    onwrite(stream, er);
  };

  // the callback that the user supplies to write(chunk,encoding,cb)
  this.writecb = null;

  // the amount that is being written when _write is called.
  this.writelen = 0;

  this.bufferedRequest = null;
  this.lastBufferedRequest = null;

  // number of pending user-supplied write callbacks
  // this must be 0 before 'finish' can be emitted
  this.pendingcb = 0;

  // emit prefinish if the only thing we're waiting for is _write cbs
  // This is relevant for synchronous Transform streams
  this.prefinished = false;

  // True if the error was already emitted and should not be thrown again
  this.errorEmitted = false;

  // count buffered requests
  this.bufferedRequestCount = 0;

  // allocate the first CorkedRequest, there is always
  // one allocated and free to use, and we maintain at most two
  this.corkedRequestsFree = new CorkedRequest(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Writable.super_"></a>[function <span class="apidocSignatureSpan">readable-stream.Writable.</span>super_ ()](#apidoc.element.readable-stream.Writable.super_)
- description and source-code
```javascript
function Stream() {
  EE.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.readable-stream.Writable.WritableState"></a>[module readable-stream.Writable.WritableState](#apidoc.module.readable-stream.Writable.WritableState)

#### <a name="apidoc.element.readable-stream.Writable.WritableState.WritableState"></a>[function <span class="apidocSignatureSpan">readable-stream.Writable.</span>WritableState (options, stream)](#apidoc.element.readable-stream.Writable.WritableState.WritableState)
- description and source-code
```javascript
function WritableState(options, stream) {
  Duplex = Duplex || require('./_stream_duplex');

  options = options || {};

  // object stream flag to indicate whether or not this stream
  // contains buffers or objects.
  this.objectMode = !!options.objectMode;

  if (stream instanceof Duplex) this.objectMode = this.objectMode || !!options.writableObjectMode;

  // the point at which write() starts returning false
  // Note: 0 is a valid value, means that we always return false if
  // the entire buffer is not flushed immediately on write()
  var hwm = options.highWaterMark;
  var defaultHwm = this.objectMode ? 16 : 16 * 1024;
  this.highWaterMark = hwm || hwm === 0 ? hwm : defaultHwm;

  // cast to ints.
  this.highWaterMark = ~~this.highWaterMark;

  // drain event flag.
  this.needDrain = false;
  // at the start of calling end()
  this.ending = false;
  // when end() has been called, and returned
  this.ended = false;
  // when 'finish' is emitted
  this.finished = false;

  // should we decode strings into buffers before passing to _write?
  // this is here so that some node-core streams can optimize string
  // handling at a lower level.
  var noDecode = options.decodeStrings === false;
  this.decodeStrings = !noDecode;

  // Crypto is kind of old and crusty.  Historically, its default string
  // encoding is 'binary' so we have to make this configurable.
  // Everything else in the universe uses 'utf8', though.
  this.defaultEncoding = options.defaultEncoding || 'utf8';

  // not an actual buffer we keep track of, but a measurement
  // of how much we're waiting to get pushed to some underlying
  // socket or file.
  this.length = 0;

  // a flag to see when we're in the middle of a write.
  this.writing = false;

  // when true all writes will be buffered until .uncork() call
  this.corked = 0;

  // a flag to be able to tell if the onwrite cb is called immediately,
  // or on a later tick.  We set this to true at first, because any
  // actions that shouldn't happen until "later" should generally also
  // not happen before the first write call.
  this.sync = true;

  // a flag to know if we're processing previously buffered items, which
  // may call the _write() callback in the same tick, so that we don't
  // end up in an overlapped onwrite situation.
  this.bufferProcessing = false;

  // the callback that's passed to _write(chunk,cb)
  this.onwrite = function (er) {
    onwrite(stream, er);
  };

  // the callback that the user supplies to write(chunk,encoding,cb)
  this.writecb = null;

  // the amount that is being written when _write is called.
  this.writelen = 0;

  this.bufferedRequest = null;
  this.lastBufferedRequest = null;

  // number of pending user-supplied write callbacks
  // this must be 0 before 'finish' can be emitted
  this.pendingcb = 0;

  // emit prefinish if the only thing we're waiting for is _write cbs
  // This is relevant for synchronous Transform streams
  this.prefinished = false;

  // True if the error was already emitted and should not be thrown again
  this.errorEmitted = false;

  // count buffered requests
  this.bufferedRequestCount = 0;

  // allocate the first CorkedRequest, there is always
  // one allocated and free to use, and we maintain at most two
  this.corkedRequestsFree = new CorkedRequest(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.readable-stream.Writable.WritableState.prototype"></a>[module readable-stream.Writable.WritableState.prototype](#apidoc.module.readable-stream.Writable.WritableState.prototype)

#### <a name="apidoc.element.readable-stream.Writable.WritableState.prototype.getBuffer"></a>[function <span class="apidocSignatureSpan">readable-stream.Writable.WritableState.prototype.</span>getBuffer ()](#apidoc.element.readable-stream.Writable.WritableState.prototype.getBuffer)
- description and source-code
```javascript
function getBuffer() {
  var current = this.bufferedRequest;
  var out = [];
  while (current) {
    out.push(current);
    current = current.next;
  }
  return out;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.readable-stream.Writable.prototype"></a>[module readable-stream.Writable.prototype](#apidoc.module.readable-stream.Writable.prototype)

#### <a name="apidoc.element.readable-stream.Writable.prototype._write"></a>[function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>_write (chunk, encoding, cb)](#apidoc.element.readable-stream.Writable.prototype._write)
- description and source-code
```javascript
_write = function (chunk, encoding, cb) {
  cb(new Error('_write() is not implemented'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Writable.prototype.cork"></a>[function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>cork ()](#apidoc.element.readable-stream.Writable.prototype.cork)
- description and source-code
```javascript
cork = function () {
  var state = this._writableState;

  state.corked++;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Writable.prototype.end"></a>[function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>end (chunk, encoding, cb)](#apidoc.element.readable-stream.Writable.prototype.end)
- description and source-code
```javascript
end = function (chunk, encoding, cb) {
  var state = this._writableState;

  if (typeof chunk === 'function') {
    cb = chunk;
    chunk = null;
    encoding = null;
  } else if (typeof encoding === 'function') {
    cb = encoding;
    encoding = null;
  }

  if (chunk !== null && chunk !== undefined) this.write(chunk, encoding);

  // .end() fully uncorks
  if (state.corked) {
    state.corked = 1;
    this.uncork();
  }

  // ignore unnecessary end() calls.
  if (!state.ending && !state.finished) endWritable(this, state, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Writable.prototype.pipe"></a>[function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>pipe ()](#apidoc.element.readable-stream.Writable.prototype.pipe)
- description and source-code
```javascript
pipe = function () {
  this.emit('error', new Error('Cannot pipe, not readable'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Writable.prototype.setDefaultEncoding"></a>[function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>setDefaultEncoding (encoding)](#apidoc.element.readable-stream.Writable.prototype.setDefaultEncoding)
- description and source-code
```javascript
function setDefaultEncoding(encoding) {
  // node::ParseEncoding() requires lower case.
  if (typeof encoding === 'string') encoding = encoding.toLowerCase();
  if (!(['hex', 'utf8', 'utf-8', 'ascii', 'binary', 'base64', 'ucs2', 'ucs-2', 'utf16le', 'utf-16le', 'raw'].indexOf((encoding + '').
toLowerCase()) > -1)) throw new TypeError('Unknown encoding: ' + encoding);
  this._writableState.defaultEncoding = encoding;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Writable.prototype.uncork"></a>[function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>uncork ()](#apidoc.element.readable-stream.Writable.prototype.uncork)
- description and source-code
```javascript
uncork = function () {
  var state = this._writableState;

  if (state.corked) {
    state.corked--;

    if (!state.writing && !state.corked && !state.finished && !state.bufferProcessing && state.bufferedRequest) clearBuffer(this
, state);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.readable-stream.Writable.prototype.write"></a>[function <span class="apidocSignatureSpan">readable-stream.Writable.prototype.</span>write (chunk, encoding, cb)](#apidoc.element.readable-stream.Writable.prototype.write)
- description and source-code
```javascript
write = function (chunk, encoding, cb) {
  var state = this._writableState;
  var ret = false;
  var isBuf = Buffer.isBuffer(chunk);

  if (typeof encoding === 'function') {
    cb = encoding;
    encoding = null;
  }

  if (isBuf) encoding = 'buffer';else if (!encoding) encoding = state.defaultEncoding;

  if (typeof cb !== 'function') cb = nop;

  if (state.ended) writeAfterEnd(this, cb);else if (isBuf || validChunk(this, state, chunk, cb)) {
    state.pendingcb++;
    ret = writeOrBuffer(this, state, isBuf, chunk, encoding, cb);
  }

  return ret;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
