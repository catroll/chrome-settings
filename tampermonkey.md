# Tampermonkey

```js
// ==UserScript==
// @name         一点资讯
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  try to take over the world!
// @author       You
// @match        http://www.yidianzixun.com/home?page=article&id=*
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    // jQuery
    // var ele = $('.content-hd');
    // var comment = ele.childNodes[2].data;
    // ele.append(comment);

    var class_name = 'content-hd';
    var ele = document.getElementsByClassName(class_name)[0];
    var comment = ele.childNodes[2].data;
    var newNode = document.createElement("span");
    newNode.innerHTML = comment;
    document.getElementById('source-name').appendChild(newNode);
})();
```
