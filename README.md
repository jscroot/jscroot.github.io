# Root Static Website | Javascript Changer to transform Static Web into Dynamic Website  | A Pure VanillaJS ES6+ Base

Root your static website, and change it into a dynamic one. Get the benefit of a low-emission carbon code. Supported by many static web hosting.

[Benchmark](https://krausest.github.io/js-framework-benchmark/current.html)  
Rule of Thumb:  
```txt
Every line in JavaScript runs as a sub-process in a browser, not waiting.
Use async await or promise if you want to run without a sub-process.
```
This is a sample of a four-step run of the js command, where js can be run in serial and parallel mode:
```js
import {functionName, runFunction} from "https://cdn.jsdelvr.com/gh/jscroot/croot.js";
// Step 1: run and wait until finish execute
await functionName(arg);
// Step 2: Just run without waiting until finished, immediately go to the next step
runFunction(arg);
// Step 3: Run after HTML loaded
document.addEventListener('DOMContentLoaded', function() {
  // initial HTML document has been completely loaded and parsed, without waiting
  // for stylesheets, images, and subframes to finish loading
  console.log('DOM fully loaded and parsed');
});
// Step 4: Run after all loaded
window.addEventListener('load', (event) => {
    //This includes after-all assets like images, scripts, and CSS files.
    //Loaded
    console.log('The page has fully loaded');
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

## List of Static Web Hosting

Run your rooted dynammic website in this static web hosting providing list:
1. Github pages
2. Gitlab pages
3. AWS Amplify / Amazon S3
4. KeyCDN
5. Azure Static Web Apps
6. 21YunBox
7. Blogspot
8. Zeit
9. Forge
10. Bip.sh
11. DigitalOcean App Platform
12. Statically
13. Clodui
14. Cloud 66
15. Cloudflare Pages
16. Deploy Now
17. Firebase
18. Google Cloud Storage Bucket
19. Kinsta Static Site Hosting
20. Microsoft Azure
21. Netlify
22. Render
23. Static.app
24. Stormkit.io
25. Hostman
26. Surge.sh
27. tiiny.host
28. Back4App
29. Vercel
