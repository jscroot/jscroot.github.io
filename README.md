# Just Croot

Make Javascript Great Again. Don't worry if you're beginner. It's just Javascript.

## List of component

* [element](https://jscroot.github.io/element/croot.js)
* [api](https://jscroot.github.io/api/croot.js)
* [useragent](https://jscroot.github.io/useragent/croot.js)
* [websocket](https://jscroot.github.io/websocket/croot.js)
* [cookie](https://jscroot.github.io/cookie/croot.js)

## How to use

[example](https://jscroot.github.io/croot.html)

croot.html :

```html
<!DOCTYPE html>
<html>
<body>
<p id="demo"></p>
<script type="module" src="croot.js"></script>
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
