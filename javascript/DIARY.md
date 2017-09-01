# 01/09/2017

# Questions
. What is the difference between a primitive string a string object?

. function sayHi() { 
  if(true) { 
    var s = "hi"; 
  } 
  alert(s); // alert("hi") -- `s` is still within scope. }

  Why is that 's' is still available to anything outside the curly braces within the function? The variable is shifted to the top and is run first, but what if I don't want it to be available to the whole function?

. This also means that if you refer to a variable outside the scope of your function, you’ll use the value of that variable at the moment the code is run, not at the moment your function is created. This trips up beginners all the time:

 var thingsToDo = [];
 for(var i = 0; i < 2; i++) {
   thingsToDo.push(function() {alert('hello ' + i);}); 
 }
 for(var k in thingsToDo) {
   thingsToDo[k]();               // alerts "hello 2" twice.
 }

 What is even going on here?

 # Learnings

 . ECMAScript 6 will introduce a let keyword, which will allow you to declare a variable scoped to the curly-braces. This is known as Lexical Scoping.