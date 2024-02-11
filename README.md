# JSCroot : A Pure ES6+ VanillaJS Static Web Transformator | Transform Static Web into Dynamic Website

Root your static website, and change it into a dynamic one. Get the benefit of a low-emission carbon code. Supported by many static web hosting.
Dare to [Benchmark This](https://krausest.github.io/js-framework-benchmark/current.html)?  

The JS Rule of Thumb:  
```txt
JavaScript is an asynchronous scripting language.  
Every line in JavaScript runs as a sub-process in a browser, not waiting.  
Use async await or promise if you want to run without a sub-process.
```

## How to Use

The first thing to do is create your html file and declare the type module js script.

```html
<!DOCTYPE html>
<html>
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
    import { setInner } from "https://cdn.jsdelivr.net/gh/jscroot/element@0.1.5/croot.js";
    setInner("demo","Dari croot.js");
    ```
8. or you might use the asterisk (*)
    ```js
    import * as croot from "https://cdn.jsdelivr.net/gh/jscroot/element@0.1.5/croot.js";
    croot.setInner("demo","Dari croot.js import fungsi dengan nama croot");
    ```
    
Choose the two paradigms in Javascript:
1. Micro Front End(MFE) : Just Look Into [examples](./examples/) section.
2. Conventional Single Page Application(SPA) : Use our [skeleton](https://github.com/jscroot/skeleton) and look at [demo](https://jscroot.github.io/skeleton/).

## List of components

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
