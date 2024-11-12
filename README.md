# JSCroot : A Pure Vanilla JavaScript ES6+ Modules Static Web Transformator | Transform Static Web into Dynamic Website

Root your static website and transform it into a dynamic one. Benefit from a low-emission carbon code. Many static web hosting providers support this.
Dare to [Benchmark This](https://krausest.github.io/js-framework-benchmark/current.html)?  

The JS Rule of Thumb:  
```txt
JavaScript is an asynchronous scripting language.  
Every line in JavaScript runs as an independent process in a browser, not waiting.  
Use async await or promise if you want to run without a sub-process.
```

JSCroot uses ES6+ Syntax module. [Download or Use JSCRoot Library from CDN](https://www.jsdelivr.com/package/gh/jscroot/lib)
```html
<script type="module" src="index.js"></script>
```

## Sweetalert

Meet sweet alert with JSCroot:
```js
import {addCSSInHead} from "https://cdn.jsdelivr.net/gh/jscroot/lib@0.1.6/element.js";
import Swal from 'https://cdn.jsdelivr.net/npm/sweetalert2@11/src/sweetalert2.js';

await addCSSInHead("https://cdn.jsdelivr.net/npm/sweetalert2@11/dist/sweetalert2.css");


Swal.fire({
      icon: "error",
      title: "Testing",
      text: "Hi, from JSCroot",
    });
```

## Quick Start with ChatGPT

Using JSCroot assisted by ChatGPT:
1. Download lib from [release page](https://github.com/jscroot/lib/releases)
2. Extract, choose js file and upload it into ChatGPT Prompt, for example : api.js
3. Input this text:
   ```txt
   I want to use JSCroot as ES modules to build my website, this is my library file from:
   https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.1/api.js
   ```
4. Other option: if you cant upload file, just paste the code inside api.js after cdn url with several new line
   ```txt
   I want to use JSCroot as ES modules to build my website, this is my library file from:
   https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.1/api.js

   ...content inside api.js file...
   ```

Need a basic concept? don't worry, follow this tutorial and exercise first:
1. [Pengenalan API dan Tools](https://universitas.bukupedia.co.id/ws/Chapter01/)
2. [HTTP Header and Body Capture](https://universitas.bukupedia.co.id/ws/Chapter02/)
3. [Dasar Cookie, Frontend dan Backend Package](https://universitas.bukupedia.co.id/ws/Chapter03/)

## How to Use

The first thing to do is create your html file and declare the **type module** js script.

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Module Example</title>
</head>
<body>
<p id="demo"></p>
<script type="module" src="index.js"></script>
</body>
</html>
```
This is your step:
1. create your first index.js file
2. go to **List of components** below
3. Open cdn jsdelivr link
4. Click on croot.js file in jsdelivr page
5. Copy the URL from the browser
6. Put in the import section statement
7. Don't forget to call the function name in the import section
    ```js
    import { setInner } from "https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.3/element.js";
    setInner("demo","Dari croot.js");
    ```
8. or you might use the asterisk (*)
    ```js
    import * as croot from "https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.3/element.js";
    croot.setInner("demo","Dari croot.js import fungsi dengan nama croot");
    ```

    
## Quick Start
index.html file:
```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css">
  </head>
<body>


<table class="table">
  <tbody id="lokasi">
    <tr>
      <th>Type</th>
      <th>Nama</th>
      <th>Kordinat</th>
    </tr>
  </tbody>
</table>

<script type="module" src="./main.js"></script>

</body>
</html>
```
main.js file:
```js
import { get } from "https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.3/api.js";
import {setInner,addChild } from "https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.3/element.js";

export let URLGeoJson = "https://jscroot.github.io/examples/api/get/fromfile/data.json";
export let tableTag="tr";
export let tableRowClass="content is-small";
export let tableTemplate=`
<td>#TYPE#</td>
<td>#NAME#</td>
<td>#KORDINAT#</td>
`
get(URLGeoJson,responseData);

export function responseData(results){
    console.log(results.features);
    results.features.forEach(isiRow);
}

export function isiRow(value){
    let content=tableTemplate.replace("#TYPE#",value.geometry.type)
        .replace("#NAME#",value.properties.name)
        .replace("#KORDINAT#",value.geometry.coordinates);
    console.log(content);
    addChild("lokasi",tableTag,tableRowClass,content);
}
```
We use Micro Front End(MFE) paradigm: Come into [examples](./examples/) section to begin your journey with JSCroot.

## List of library components

* https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.3/api.js
* https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.3/cookie.js
* https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.3/element.js
* https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.3/image.js
* https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.3/loading.js
* https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.3/mongo.js
* https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.3/url.js
* https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.3/useragent.js
* https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.3/websocket.js

## List of Template

* [File Explorer](https://jscroot.github.io/explorer/) | [Fork Github](https://github.com/jscroot/explorer)
* [PDF Web Viewer](https://jscroot.github.io/view/) | [Fork Github](https://github.com/jscroot/view)
* [Swagger](https://jscroot.github.io/swagger/) | [Fork Github](https://github.com/jscroot/swagger)
* [404 Not Found Template](https://jscroot.github.io/404/404.html) | [Fork Github](https://github.com/jscroot/404)

## Single Page Application(SPA)

Conventional Single Page Application(SPA) : Use our [skeleton](https://github.com/jscroot/skeleton) and look at [demo](https://jscroot.github.io/skeleton/).

## List of Static Web Hosting

Run your rooted dynamic website in this static web hosting providing list:
1. Github pages **(recommended)**.
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
