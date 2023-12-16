# ꦗꦮ꦳ꦱ꧀ꦕꦥ꧀ꦠ꧀ | Just Change the Root | A Pure Blood VanillaJS ES6+ Kit

  
![ꦗꦮ꦳ꦱ꧀ꦕꦥ꧀ꦠ꧀](https://github.com/jscroot/jscroot.github.io/assets/11188109/3c0c88d0-9900-49c7-86d4-0c42bbc8f175)  
[Benchmark](https://krausest.github.io/js-framework-benchmark/current.html)  
Rule of Thumb:  
```txt
Every line in javascript run as sub process in browser, not waiting.
Use async await or promise if you want to run without sub process.
```
Skeleton of js
```js
import {functionNaem} from "https://cdn.jsdelvr.com/gh/jscroot/croot.js";
await functionName(arg);
document.addEventListener('DOMContentLoaded', function() {
  // initial HTML document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading
  console.log('DOM fully loaded and parsed');
});
window.addEventListener('load', (event) => {
    //This includes after all assets like images, scripts, and CSS files.
    console.log('The page has fully loaded');
    // Your code here
});
```
Just Look Into [examples](./examples/) section.

## List of component

* [element](https://jscroot.github.io/element/croot.js) | [cdn jsdelivr](https://cdn.jsdelivr.net/gh/jscroot/element/)
* [api](https://jscroot.github.io/api/croot.js) | [cdn jsdelivr](https://cdn.jsdelivr.net/gh/jscroot/api/)
* [cookie](https://jscroot.github.io/cookie/croot.js) | [cdn jsdelivr](https://cdn.jsdelivr.net/gh/jscroot/cookie/)
* [url](https://jscroot.github.io/url/croot.js) | [cdn jsdelivr](https://cdn.jsdelivr.net/gh/jscroot/url/)
* [mongo](https://jscroot.github.io/mongo/croot.js) | [cdn jsdelivr](https://cdn.jsdelivr.net/gh/jscroot/mongo/)
* [useragent](https://jscroot.github.io/useragent/croot.js) | [cdn jsdelivr](https://cdn.jsdelivr.net/gh/jscroot/useragent/)
* [websocket](https://jscroot.github.io/websocket/croot.js) | [cdn jsdelivr](https://cdn.jsdelivr.net/gh/jscroot/websocket/)
* [image](https://jscroot.github.io/image/croot.js) | [cdn jsdelivr](https://cdn.jsdelivr.net/gh/jscroot/image/)

## List of Template

* [Swagger](https://jscroot.github.io/swagger/) | [Fork Github](https://github.com/jscroot/swagger)

## How to Use

croot.html :

```html
<!DOCTYPE html>
<html>
<body>
<p id="demo"></p>
<script type="module" src="./croot.js"></script>
</body>
</html>
```

croot.js :

```js
import { setInner } from "https://jscroot.github.io/element/croot.js";
setInner("demo","Dari croot.js");
```
or
```js
import * as croot from "https://jscroot.github.io/element/croot.js";
croot.setInner("demo","Dari croot.js import fungsi dengan nama croot");
```

Just Look Into [examples](./examples/) section.
