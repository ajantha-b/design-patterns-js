# Module Design Pattern


Module design pattern provides loose coupling to support well-structured and maintainable code in our projects.
For those who are familiar with encapsulation to protect state and behaviour from being access from classes this is a good solution.
Moduler pattern priovides public and private access levels.

In javascript we need to use IIFE(Immediatly-invoked function expresion) to implement module pattern.This IIFE privides privete scope
to our module.

``` js

const Factory = (function() {
  let privateFName;
  let PrivateLname;
  
  const setFirName = function(fname) {
    privateFName = fname;
  }
  
  const setLastName = function(lname) {
    PrivateLname = lname;
  }
  
  const getFullName = function() {
    return privateFName + " " + PrivateLname;
  }
  
  // return all public methods and variables
  return {
    setFirName,
    setLastName,
    getFullName
  }
})();
```
