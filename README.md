# Pluralsight HTML5

## Web Workers
## Web Sockets
## Microdata

## IIFE (Immediately-invoked Function Expression)

`
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

## LocalStorage & SessionStorage
`
