# Just Croot It | A Pure Blood VanillaJS Lightweight ES6+ Kit

In the name of Javascript. Make Javascript Great Again. Don't worry if you're a beginner. It's just a Pure Blood Javascript with modern ES6+ Syntac.

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
* [mongo](https://jscroot.github.io/mongo/croot.js)

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

Use standard boilerplate within the folder: config, controller, template with the structure.

![image](https://user-images.githubusercontent.com/11188109/224894184-74bc9192-d635-47e1-bd02-f7dbe16a0d39.png)

croot.js file
```js
import { get } from "https://jscroot.github.io/api/croot.js";
import {setInner } from "https://jscroot.github.io/element/croot.js";
import {isiTablePresensi} from "./controller/table.js";
import {URLPresensi} from "./config/url.js";

get(URLPresensi,isiTablePresensi);

setInner("namadivisi","Dari croot.js");
```
config/url.js file
```js
export let URLPresensi = "https://gocroot.herokuapp.com/presensi";
```
controller/table.js file
```js
import { addChild } from "https://jscroot.github.io/element/croot.js";
import {getRandomColor,getRandomColorName} from "https://jscroot.github.io/image/croot.js";
import {presensiTag,presensiClass,presensiContent} from "../template/table.js";

export function isiTablePresensi(results){
    results.forEach(isiRow);
}

function isiRow(value){
    let content=presensiContent.replace("#NAMA#",value.Biodata.Nama).replace("#PHONENUMBER#",value.Phone_number).replace("#LOKASI#",value.Location).replace("#KET#",value.Checkin).replace("#MASUK#",value.Datetime).replace("#PULANG#",value.Datetime).replace("#DURASI#",value.Datetime).replace("#WARNA#",getRandomColor()).replace(/#WARNALOGO#/g,getRandomColorName());
    addChild("presensi",presensiTag,presensiClass,content);
}
```
template/table.js file
```js
export let presensiTag="tr";
export let presensiClass="h-18 border-b border-coolGray-100";
export let presensiContent=`
<th class="whitespace-nowrap px-4 bg-white text-left">
  <div class="flex items-center -m-2">
    <div class="w-auto p-2">
      <input class="w-4 h-4 bg-white rounded" type="checkbox">
    </div>
    <div class="w-auto p-2">
      <div class="flex items-center justify-center w-10 h-10 text-base font-medium text-#WARNALOGO#-600 bg-#WARNALOGO#-200 rounded-md">ADO</div>
    </div>
    <div class="w-auto p-2">
      <p class="text-xs font-semibold text-coolGray-800">#NAMA#</p>
      <p class="text-xs font-medium text-coolGray-500">#PHONENUMBER#</p>
    </div>
  </div>
</th>
<th class="whitespace-nowrap px-4 bg-white text-sm font-medium text-coolGray-800 text-left">#LOKASI#</th>
<th class="whitespace-nowrap px-4 bg-white text-sm font-medium text-coolGray-800 text-center">#KET#</th>
<th class="whitespace-nowrap px-4 bg-white text-sm font-medium text-green-500 text-left">#MASUK#</th>
<th class="whitespace-nowrap px-4 bg-white text-sm font-medium text-green-500 text-left">#PULANG#</th>
<th class="whitespace-nowrap px-4 bg-white text-sm font-medium text-coolGray-800 text-center">#DURASI#</th>
<th class="whitespace-nowrap pr-4 bg-white text-sm font-medium text-coolGray-800">
  <svg class="ml-auto" width="16" height="16" viewbox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
    <path d="M8 6.66669C7.73629 6.66669 7.47851 6.74489 7.25924 6.89139C7.03998 7.0379 6.86908 7.24614 6.76816 7.48978C6.66724 7.73341 6.64084 8.0015 6.69229 8.26014C6.74373 8.51878 6.87072 8.75636 7.05719 8.94283C7.24366 9.1293 7.48124 9.25629 7.73988 9.30773C7.99852 9.35918 8.26661 9.33278 8.51025 9.23186C8.75388 9.13094 8.96212 8.96005 9.10863 8.74078C9.25514 8.52152 9.33333 8.26373 9.33333 8.00002C9.33333 7.6464 9.19286 7.30726 8.94281 7.05721C8.69276 6.80716 8.35362 6.66669 8 6.66669ZM3.33333 6.66669C3.06963 6.66669 2.81184 6.74489 2.59257 6.89139C2.37331 7.0379 2.20241 7.24614 2.10149 7.48978C2.00058 7.73341 1.97417 8.0015 2.02562 8.26014C2.07707 8.51878 2.20405 8.75636 2.39052 8.94283C2.57699 9.1293 2.81457 9.25629 3.07321 9.30773C3.33185 9.35918 3.59994 9.33278 3.84358 9.23186C4.08721 9.13094 4.29545 8.96005 4.44196 8.74078C4.58847 8.52152 4.66667 8.26373 4.66667 8.00002C4.66667 7.6464 4.52619 7.30726 4.27614 7.05721C4.02609 6.80716 3.68696 6.66669 3.33333 6.66669ZM12.6667 6.66669C12.403 6.66669 12.1452 6.74489 11.9259 6.89139C11.7066 7.0379 11.5357 7.24614 11.4348 7.48978C11.3339 7.73341 11.3075 8.0015 11.359 8.26014C11.4104 8.51878 11.5374 8.75636 11.7239 8.94283C11.9103 9.1293 12.1479 9.25629 12.4065 9.30773C12.6652 9.35918 12.9333 9.33278 13.1769 9.23186C13.4205 9.13094 13.6288 8.96005 13.7753 8.74078C13.9218 8.52152 14 8.26373 14 8.00002C14 7.6464 13.8595 7.30726 13.6095 7.05721C13.3594 6.80716 13.0203 6.66669 12.6667 6.66669Z" fill="#WARNA#"></path>
  </svg>
</th>
`
```

## using form

``` html
<script type="module">
    import {PostSignUp} from "/sidang/js/pdsidang.js";
    window.PostSignUp = PostSignUp;
</script>

...

<form id="form" onsubmit="event.preventDefault();">
<button type="submit" id="button" onclick="PostSignUp()">submit</button>
 </form>
```


## How to Develop

* [What is export default in JavaScript ?](https://www.geeksforgeeks.org/what-is-export-default-in-javascript/)
* [What is "export default" in JavaScript?](https://stackoverflow.com/questions/21117160/what-is-export-default-in-javascript)
* [export](https://developer.mozilla.org/en-US/docs/web/javascript/reference/statements/export)
