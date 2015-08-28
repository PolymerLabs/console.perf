## console.perf

> Utilities for performance benchmarking your Polymer elements

### Usage

1. Include `console.perf.js` in your element or application.
2. Execute `console.perf()` before the work you would like to benchmark and `console.perfEnd()` once that work is complete.

Example:

```html
addEventListener('WebComponentsReady', function () {
  console.perf();
  var app = document.createElement('x-app');
  document.body.appendChild(app);
  app.renderData(data);
  console.perfEnd();
});
```

### Optional

`console.perf` also supports invoking the Chrome garbage collector if `window.gc()` is available. This requires running Chrome using a specific set of debug flags. To enable this feature, run Chrome using:

```
--js-flags '--expose_gc'
```
