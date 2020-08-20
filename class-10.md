# ERROR HANDLING & DEBUGGNG 

### UNDERSTANDING ERRORS 
If a JavaScript statement generates an error, then it throws an exception . At that point, the interpreter stops and looks for exception-handling code.

```
function greetUser(){
// Interpreter 1ooks here 
}

function getName() {
//Imagine this had an error
//It was caused by greetUser() 
}
var greeting= greetUser(); 
 alert(greeting);
```
If you are anticipating that something in your code may cause an error, you can use a set of statements to handle the error (you meet them on p480).
This is important because if the error is not handled, the script will just stop processing and the user will not know why. So exception-handling code should inform users when there is a problem.

Whenever the interpreter comes across an error,
it will look for error-handling code. In the diagram below, the code has the same structure as the code you saw in the diagrams at the start of the chapter. The statement at step 1 uses the function in step 2, which in turn uses the function in step 3. Imagine that there has been an error at step 3.
When an exception is thrown, the interpreter
stops and checks the current execution context for exception-handling code. So if the error occurs in the getName () function ( 3), the interpreter starts to look for error handling code in that function.
If an error happens in a function and the function does not have an exception handler, the interpreter goes to the line of code that called the function.
In this case, the getName() function was called by greetUser(), so the interpreter looks for exception- handling code in the greetUser() function (2).
If none is found, it continues to the next level, checking to see if there is code to handle the error in that execution context. It can continue until it reaches the global context, where it would have to it terminate the script, and create an Error object.
So it is going through the stack looking for error- handling code until it gets to the global context. If there is still no error handler, the script stops running and the Error object is created.

### ERROR OBJECTS

#### SyntaxError 

SYNTAX IS NOT CORRECT : This is caused by incorrect use of the rules of the language. It is often the result of a simple typo.
MISMATCHING OR UNCLOSED QUOTES document.write("Howdyl );
SyntaxError: Unexpect ed EOF MISSING CLOSING BRACKET
document.getElementByid('page'I SyntaxErr or : Expected token ' ) '
MISSING COMMA IN ARRAY
Would be same for missing] at the end
var l ist = ['Item 1', 'Item 2'l 'rtem 3'];
SyntaxError : Expected token ' ] '
MALFORMED PROPERTY NAME
It has a space but is not surrounded by quote marks user = {f i rstl name: "Ben", lastName: "Lee"};
Synt axError: Expected an identifier but found 'name ' instead


#### ReferenceError 
VARIABLE DOES NOT EXIST : This is caused by a variable that is not declared or is out of scope.
VA RIABLE IS UNDECLARED var width = 12;
var area = width * llt!ftNU!;
ReferenceError: Can't find variable: height
NAMED FUNCTION IS UNDEFINED
document.write( randomFunction() ); ReferenceError: Can't find variable:
randomFunction

#### Error
GENERIC ERROR OBJECT
The generic Error object is the template (or prototype) from which all other error objects are created.


#### NaN
NOT AN ERROR
Note: If you perform a mathematica l operation using a value that is not a number, you end up with the value of NaN, not a type error.
NOT A NUMBER
var total =3 * 'Ivy';


###  HOW TO DEAL WITH ERRORS

* 1: DEBUG THE SCRIPT TO FIX ERRORS
If you come across an error while writing a script (or when someone reports a bug), you will need to debug the code, track down the source of the error, and fix it.
You will find that the developer tools available in every major modern browser will help you with
this task. In this chapter, you will learn about the developer tools in Chrome and Firefox. (The tools in Chrome are identical to those in Opera.)
IE and Safari also have their own tools (but there is not space to cover them all).

* 2: HANDLE ERRORS GRACEFULLY You can handle errors gracefully using try, catch,
throw, and f i na1ly statements.
Sometimes, an error may occur in the script for a reason beyond your control. For example, you might request data from a third party, and their server may not respond. In such cases, it is particularly important to write error-handling code.
In the latter part of the chapter, you will learn how to gracefully check whether something will work, and offer an alternative option if it fails.