# Pluralsight HTML5 Path

## Web Workers

Web workers are background threads in the web browser that can be used to perform calculation intensive tasks.
You can only send strings between the foreground "ui" thread and those workers. To send objects you can JSONify them first.

## Web Sockets

Web Sockets are a continuously open connection between the server and the webbrowser. The communication is performed bidirectional and requires a second protocol for the socket transmissions. A big advantage is the small overhead because when polling a server for updates you need to pass a big HTTP header along. Web Sockets do not have that, thus they are much more performant at scale.

## Microdata

Microdata is a set of attributes that can be attached to html tags. This way you annotate your html with information about what the tags contain. There is a big amount of standardized descriptions already available from google that you can use to make your site more readable to screen scrapers, especially the google one. 

## IIFE (Immediately-invoked Function Expression)

```javascript
let someData = (function() {
  
  let m = {
  
    // PUBLIC
    doSomething = function() { }
    
    // PRIVATE
    doSomethingElse = function() { }
  }
  
  return {
    name: 'Some useful value',
    doSomething: m.doSomething;
  };
})();

// These don't return a value - no brackets needed because of +. -, ! or ~.
!function() { doSomthing() }();
+function() { doSomthing() }();
-function() { doSomthing() }();
~function() { doSomthing() }();
```

## LocalStorage & SessionStorage

Those two storage methods can store up to 5 MB of string data in a key value store within the browser. 
The biggest advantage to cookies is that this information stays local to the client and is not send with every mouse click to the server.
This way you can store bigger amounts of data that stay within the browser.

Whilest LocalStorage and SessionStorage are constrained in size there are methods like LZString to make a bit more out of it. 

## IndexedDB

IndexedDB is a Key-Value store, similar to the localStorage and sessionStorage. It does not have a constrained size and is available on many browsers and mobile devices. 

 - Key/Value Store (Object based)
 - Indizes with Object-Property-Paths to easy request Data
 - Integer Version and String Version to tell the Browser to use a new version (when Structure is changed)
 - Asynchronous API (Synchronous only for WebWorkers)
 - Supported by all current browsers (IE11 and Edge are missing some features)
 - Capacity: No limit, some browsers show notifications
 
