# dominode - node's evented API for HTML5
# dominode - node point browser
# dominode - node style streams for DOM nodes

** still alpha/work in progress **

node.js describes itself as a framework for dealing with "evented i/o" and traditionally runs on the server. clients, however, are just a i/o bound as servers (ajax requests, file uploads, indexeddb/websql, etc.) and can benefit from the nice APIs that node has developed to solve these problems in a server environment.

dominode uses a few key javascript libraries from node (Stream, Util, etc via [browserify](https://github.com/substack/node-browserify)) and adds some new syntax for dealing with the DOM. 

currently it is uses the [plates](https://github.com/flatiron/plates) templating library but something with CSS selectors would be nicer

    // pass in the selector location where the dominode will get rendered and the template it will use for each data event
    var list = dominode('.list', '<div id="number"></div>')
    
    // pipe some data to your dominode
    var readStream = new ExampleReadStream()
    readStream.pipe(list)

MIT LICENSE