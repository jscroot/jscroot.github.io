# JSCroot: A Pure Vanilla JavaScript ES6+ Modules Static Web Transformer | Transform Static Websites into Dynamic Experiences

Root your static website and effortlessly transform it into a dynamic website using JSCroot. Enjoy the benefits of a low-emission carbon code, making your website both efficient and eco-friendly. Many static web hosting providers seamlessly support JSCroot, offering a simple way to turn your static content into dynamic, interactive experiences.

With JSCroot, you can also take advantage of **anti-deface** protection, ensuring that your website remains secure against unauthorized changes. This makes your site less vulnerable to malicious alterations, adding an extra layer of security to your dynamic website.

JSCroot offers **very low-cost deployment**, which can even be done for **free** with many hosting providers, making it an ideal choice for anyone looking to deploy their website with minimal expenses. 

👉 This method is perfect for those who want a super lightweight application without any npm dependencies. 🚀

Ready to test its performance? Dare to [Benchmark This](https://krausest.github.io/js-framework-benchmark/current.html)?

### The JS Rule of Thumb:
```txt
JavaScript is an asynchronous scripting language.  
Every line in JavaScript runs as an independent process in a browser, not waiting.  
Use async await or promise if you want to run without a sub-process.
```

JSCroot leverages **ES6+ syntax** for modules:
```html
<script type="module" src="index.js"></script>
```

You can easily [Use JSCroot Library from CDN](https://www.jsdelivr.com/package/gh/jscroot/lib) to get started with minimal setup.  
[![](https://data.jsdelivr.com/v1/package/gh/jscroot/lib/badge?style=rounded)](https://www.jsdelivr.com/package/gh/jscroot/lib)  
[Read Documentation](./lib)

## WhatsAuth and GoCroot Integration

For example to get user data using WhatsAuth Token
```js
import {getCookie} from "https://cdn.jsdelivr.net/gh/jscroot/cookie@0.0.1/croot.js";
import {setInner} from "https://cdn.jsdelivr.net/gh/jscroot/element@0.1.5/croot.js";
import {getJSON} from "https://cdn.jsdelivr.net/gh/jscroot/api@0.0.7/croot.js";
import {redirect} from "https://cdn.jsdelivr.net/gh/jscroot/url@0.0.9/croot.js";

if (getCookie("login")===""){
    redirect("/");
}

getJSON("https://api.do.my.id/data/user","login",getCookie("login"),responseFunction)

function responseFunction(result){
    if (result.status === 404){
        setInner("content","Silahkan lakukan pendaftaran terlebih dahulu "+result.data.name);
        redirect("/signup");
    }else{
        setInner("content","Selamat datang "+result.data.name);
        redirect("/dashboard");
    }
    console.log(result);
}
```

## Sweetalert

Meet sweet alert with JSCroot:
```js
import {addCSS} from "https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.3/element.js";
import Swal from 'https://cdn.jsdelivr.net/npm/sweetalert2@11/src/sweetalert2.js';

await addCSS("https://cdn.jsdelivr.net/npm/sweetalert2@11/dist/sweetalert2.css");

//alert() replacement
Swal.fire('Hehe', 'Kalem bray can hudang keneh', 'info');//success,warning,info,question

//confirm() replacement
Swal.fire({
  title: 'Apakah Anda yakin?',
  text: 'Anda akan melanjutkan tindakan ini.',
  icon: 'warning',
  showCancelButton: true,  // Menampilkan tombol Cancel
  confirmButtonText: 'OK',
  cancelButtonText: 'Cancel'
}).then((result) => {
  if (result.isConfirmed) {
    Swal.fire('Melanjutkan...', 'Tindakan Anda telah dikonfirmasi.', 'success');
  } else {
    Swal.fire('Dibatalkan', 'Tindakan Anda dibatalkan.', 'info');
  }
});
```

## Quick Start with ChatGPT

Using JSCroot assisted by ChatGPT:
1. Download lib from [CDN](https://cdn.jsdelivr.net/gh/jscroot/lib/)
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
2. Open cdn jsdelivr link
4. Click on files tab in jsdelivr page
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

[Read Documentation](./lib)

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
