# 01/09/2017

# Questions

* What is the difference between a primitive string a string object?

*
``` 
 function sayHi() { 
  if(true) { 
    var s = "hi"; 
  } 
  alert(s); // alert("hi") -- `s` is still within scope. }

```

  Why is that 's' is still available to anything outside the curly braces within the function? The variable is shifted to the top and is run first, but what if I don't want it to be available to the whole function?

 # Learnings

 * ECMAScript 6 will introduce a let keyword, which will allow you to declare a variable scoped to the curly-braces. This is known as Lexical Scoping.