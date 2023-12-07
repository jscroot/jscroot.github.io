# Just Change the Root | A Pure Blood VanillaJS ES6+ Kit

In the name of Javascript. Make Javascript Great Again. Don't worry if you're a beginner. It's just a Pure Blood Javascript with modern ES6+ Syntac.

[Benchmark](https://krausest.github.io/js-framework-benchmark/current.html)

![Pure Blood](./img/pureblood.gif "Pure Blood")

Just Look Into [examples](./examples/) section.

## List of component

* [element](https://jscroot.github.io/element/croot.js) | [cdn jsdelivr](https://cdn.jsdelivr.net/gh/jscroot/element/)
* [api](https://jscroot.github.io/api/croot.js) | [cdn jsdelivr](https://cdn.jsdelivr.net/gh/jscroot/api/)
* [useragent](https://jscroot.github.io/useragent/croot.js)
* [websocket](https://jscroot.github.io/websocket/croot.js)
* [cookie](https://jscroot.github.io/cookie/croot.js) | [cdn jsdelivr](https://cdn.jsdelivr.net/gh/jscroot/cookie/)
* [image](https://jscroot.github.io/image/croot.js)
* [url](https://jscroot.github.io/url/croot.js) | [cdn url](https://cdn.jsdelivr.net/gh/jscroot/url/)
* [mongo](https://jscroot.github.io/mongo/croot.js)

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
