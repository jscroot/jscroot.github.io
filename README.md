# Just Croot It | A Pure Blood VanillaJS Lightweight Micro Framework

In the name of Javascript. Make Javascript Great Again. Don't worry if you're beginner. It's just a Pure Blood Javascript.

[Benchmark](https://krausest.github.io/js-framework-benchmark/current.html)

![Pure Blood](./img/pureblood.gif "Pure Blood")


## List of component

* [element](https://jscroot.github.io/element/croot.js)
* [api](https://jscroot.github.io/api/croot.js)
* [useragent](https://jscroot.github.io/useragent/croot.js)
* [websocket](https://jscroot.github.io/websocket/croot.js)
* [cookie](https://jscroot.github.io/cookie/croot.js)
* [image](https://jscroot.github.io/image/croot.js)
* [url](https://jscroot.github.io/url/croot.js)

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

## Cheat Sheet

### Post with custom token to API

```js
import { setInner } from "https://jscroot.github.io/element/croot.js";
import { postWithToken } from "https://jscroot.github.io/api/croot.js";

function headingContent(result){
    setInner(result.message); // json object 
}

let datainjson = {
    "namadepan": namadepan,
    "namabelakang": namabelakang,
    "email": email,
    "password": password
    }

postWithToken("https://foo.bar","Token","dsf9ygf87h98u479y98dj0fs89nfd7",datainjson,headingContent);

```

### Fill table from API JSON Data

```js
import { get } from "https://jscroot.github.io/api/croot.js";
import { setInner, addInner } from "https://jscroot.github.io/element/croot.js";
import { getRandomColor } from "https://jscroot.github.io/image/croot.js"
import { stringdiv, icons } from "./html.js";

       

function userTable(jsonParse){
    var stringtable = '';
    jsonParse.data.forEach((element, index) => {
      let svgicon = icons.replace("#WARNA#", getRandomColor());
        if (index % 2 === 0){
            stringtable += stringdiv.replace("#NAMA#", element['first_name']).replace("#EMAIL#", element['email']).replace("#BG#", "bg-gray-50").replace("#SVG#", svgicon);
        } else{
            stringtable += stringdiv.replace("#NAMA#", element['first_name']).replace("#EMAIL#", element['email']).replace("#BG#", "").replace("#SVG#", svgicon);
        }
    });

    addInner("demo",stringtable);

}

get("https://reqres.in/api/users",userTable);
```

## How to Develop

* [What is export default in JavaScript ?](https://www.geeksforgeeks.org/what-is-export-default-in-javascript/)
* [What is "export default" in JavaScript?](https://stackoverflow.com/questions/21117160/what-is-export-default-in-javascript)
* [export](https://developer.mozilla.org/en-US/docs/web/javascript/reference/statements/export)
