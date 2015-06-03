koa-ejs2x
=========

## Usage

### Example

```js
var koa = require('koa');
var render = require('koa-ejs2x');

var app = koa();
render(app, {
  root: path.join(__dirname, 'view'),
  layout: 'template',
  viewExt: 'html',
  cache: false,
  debug: true,
  locals: locals,
  filters: filters
});

app.use(function *() {
  yield this.render('user');
});

app.listen(3001);
```

### settings

* root: view root directory.
* layout: global layout file, default is `layout`, set `false` to disable layout.
* viewExt: view file extension, default is `html`.
* cache: cache compiled function flag.
* debug: debug flag.
* locals: global locals, can be function type, `this` in the function is koa's ctx.
* filters: ejs custom filters.
* open: open flog.
* close: close floag.

### more info
[https://github.com/koajs/ejs](https://github.com/koajs/ejs)

> koa-ejs2x just upgrade the EJS version to 2.x.x
> see ejs 2.x [https://github.com/koajs/ejs](https://github.com/koajs/ejs)
