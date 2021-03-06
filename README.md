node-jQuery
====

A stupid-simple wrapper over jQuery for Ender.JS (browser) and Node.JS (server). Currently 1.7.2.

Ender.JS
---

    ender add jQuery

    var $ = require('jQuery');

Node.JS
---

    npm install jQuery jsdom htmlparser xmlhttprequest

    var $ = require('jQuery');


Examples
---

    $("<h1>test passes</h1>").appendTo("body");
    console.log($("body").html());

In Node.JS you may also create separate window instances

    var jsdom = require('jsdom').jsdom
      , myWindow = jsdom().createWindow()
      , $ = require('jQuery')
      , jq = require('jQuery').create()
      , jQuery = require('jQuery').create(myWindow)
      ;

    $("<h1>test passes</h1>").appendTo("body");
    console.log($("body").html());

    jq("<h2>other test passes</h2>").appendTo("body");
    console.log(jq("body").html());

    jQuery("<h3>third test passes</h3>").appendTo("body");
    console.log(jQuery("body").html());

Output:

    <h1>test passes</h1>
    <h2>other test passes</h2>
    <h3>third test passes</h3>


TODO
====

* [`XMLHttpRequest`](https://github.com/driverdan/node-XMLHttpRequest) should be submitted to npm as `XMLHttpRequest` to match how Ender.JS requires the same in the browser.
* Update Node Unit to 0.7.4
* Add dependencies to package.json
* Make compatible with node 0.6.15
* Lock dependency versions in package.json




