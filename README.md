# Pluralsight HTML5

## Web Workers
## Web Sockets
## Microdata

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

## IndexedDB
 - Key/Value Store (Object based)
 - Indizes with Object-Property-Paths to easy request Data
 - Integer Version and String Version to tell the Browser to use a new version (when Structure is changed)
 - Asynchronous API (Synchronous only for WebWorkers)
 - Supported by all current browsers (IE11 and Edge are missing some features)
 - Capacity: No limit, some browsers show notifications
 
