# SUMMARY-REPORT-OF-JAVASCRIPT-TUTORIAL

SECTION 1
JS is a scripting language used to interact with the web pages.
three main part in it are: ECMAScript, Document Object Model, Browser Object Model
works both client side and server side

SECTION 2
syntax of js:whitespace, statements, identifiers, comments, expressions, and keywords.
whitespace: JS ignores whitespace
statements: a line of code ending with ;
identifier: name given to variables,parameters, fns and classes
comments: notes that gives users an understanding of the code. JS ignores them an can be single or multi lined
expression: piece of code evaluating to a value
keywords: reserved words for specifc uses
data types in js are:
null ( type is object it is a bug)
undefined
boolean
number
string (are immuatable they cannot be modified once created)
symbol – available from ES2015
bigint – available from ES2020
and a complex data type object.
NOTE: IN JS null===undefined
Objects:collection of key-value pairs
keys are strings or are converted to strings
properties are accessed using dot operator and bracket
delete keyword deletes a property
in keyword checks existence
IN js, primitive values are stored in stack while functions, arrays and objects are stored in heap
array is an ordered list of values that stores values of different data types.

SECTION 3
Arithmetic Operators: 
Addition	+
Subtraction	-
Multiplication	*
Division	/
Remainder Operator: %
Assignment Operators:
+=,-=,*=,/= ETC
Unary Operators: +X,-X,++X,X++,--X,X--
Comparison Operators:
<	less than
>	greater than
<=	less than or equal to
>=	greater than or equal to
==	equal to
!=	not equal to
Logical Operators:
Logical NOT (!)
Logical AND (&&)
Logical OR (||) IN PRECEDENCE

SECTION 4
The if statement executes block if a condition is true
if you want to execute a statement if the condition is false, you can use an if...else statement.
To check multiple conditions and execute the corresponding block if a condition is true, you use the if...else...if
TERNARY OPERATOR is a shorthand form of representing if else
switch case: another way of writing if else if else
while: while statement creates a loop that executes a block as long as a condition evaluates to true.
do while:  do...while loop statement creates a loop that executes a block until a condition evaluates to false
for: The for loop statement creates a loop with three optional expressions.
break: break statement is used to terminate a loop prematurely.
continue: The continue statement terminates the execution of the statement in the current iteration of a loop such as a for, while, and do…while loop and immediately continues to the next iteration.
comma:A comma operator takes two expressions, evaluates them from left to right, and returns the value of the right expression.

SECTION 5
To declare a function, you use the function keyword.
To use a function, you need to call it
Parameter: that what is send to the func
Argument:that what is received by the func
function return type is undefined unless specified otherwise
arguments object: behaves like an array for the arguments
Function hoisting is a mechanism in which the JavaScript engine physically moves function declarations to the top of the code before executing them.
JavaScript Functions are First-Class Citizens because they can be stored, passed and returned
arrow fns: shorthand way to write funcs
func args are always passed by value so argument value does not change.
recursive fn: a fn that calls itself, always has a condition that stops the function from calling itself.

SECTION 6
JavaScript object methods: basically this part showed how to methods are added and used inside an object. Also learn the requirement of this keyword.
Constructor Function: name starts with capital letter and shoule be called using new keyword
you can use a constructor function to define a custom type and the new operator to create multiple objects from this type.
If a constructor function is called with the new keyword, the new.target returns a reference of the function. Otherwise, it returns undefined
Learnt prototyping chain, and object function I am quite confused about this topic.
JS uses prototypal inheritance, Inheritance allows an object to use the properties and methods of another object without duplicating the code.
if you have a car object with the start method, this inside the start method will refer to the car object itself
Use the globalThis object to reference the global object to make the code work across environments.
learnt about for in loop and how it works with objects and also with normal arrays
A property is enumerable if it has the enumerable attribute set to true. The obj.propertyIsEnumerable() determines whether or not a property is enumerable.
A property is a key-value pair.
The obj.hasOwnProperty() method determines whether or not a property is own.(INHERITED OR SELF MADE)
A factory function creates and returns a new object helps us from creating multiple duplicate objects with same properties and methods.
The Object.create() method creates a new object using an existing object as the prototype of the new object
Object destructing is a way to assign properties of an object to variables.
eg: let { firstName: fname, lastName: lname } = person;
optional chaining operator(?.): used as a shortcut to access nested properties in a series of objects
if any part of the chain is empty then it stops and gives undefined as a result.
 if the user is null or undefined, the optional chaining operator (?.) immediately returns undefined saves us from writing extra code
let user = getUser(2);
let profile = user ?. profile; THIS IS EQUIVALENT TO = let user = getUser(2);
let profile = (user !== null || user !== undefined)
            ? user.profile
            : undefined;
nullish coalescing operator(??) used in case a certain property is null or undefined and we need to put some value in it.


SECTION 7
class as always is the blueprint that used to create objects.
it stores related fns and propeties in it
classes in js are just special functions
There was no concept of class before ES6.
typeof classes = function
class methods are non-enumerable
Use the get and set keywords to define the JavaScript getters and setters for a class
class can be declared inside a variable as well and does not require the class name.
classes are first class citizens
Singleton is a design pattern that limits the instantiation of a class to a single instance. It ensures that only one instance of a class can be created throughout the system.
Computed properties allow you to create object properties dynamically using an expression in square brackets []
for inheritance we use the extends keyword and if the child class has a constructor then we need to call super to access methods in the parent class
new.target= allows you to detect whether a function or constructor was called using the new operator.
new.target is very useful to inspect at runtime whether a function is being executed as a function or as a constructor.
static methods are useful for defining helper or utility methods.
the objects cannot use static methods as one of its fucntions it is called directly with the class name.
static property same as static methods with the difference being that they are properties
private fields: to do this you need to put # before the field name
they are privately seen inside the class,Use the in operator to check if an object has a private field.
private methods: same private but methods
by default class members are public

SECTION 8
FUNCTION has two important properties: length and prototype
the bind() method creates a new function that you can execute later while the call() method executes the function immediately.
did not understand call() that much.
The apply() method is similar to the call() method excepts that it accepts the arguments of the function as an array instead of individual arguments.
The bind() method creates a new function that, when invoked, has the this sets to a provided value.
a closure is a function that references variables in the outer scope from its inner scope
immediately invoked function expression is a function defined as an expression and executed immediately after creation
To return multiple values from a function, you can pack the return values as elements of an array or as properties of an object.
arrow functions provide an alternative way to write a shorter syntax compared to the function expression.
JavaScript doesn’t allow a line break between the parameter definition and the arrow (=>) in an arrow function.
DO NOT USE ARROW FNS IN:Event handlers,Object methods,Prototype methods,Functions that use the arguments object
A rest parameter allows you to represent an indefinite number of arguments as an array(...)
function fn(a,b,...args) {
   //...
} SHOOULD BE AT THE END
An arrow function does not have the arguments object. Therefore, if you want to pass some arguments to the arrow function, you must use the rest parameters
a callback is a function that you pass into another function as an argument for executing later.

SECTION 9
a promise is an object that encapsulates the result of an asynchronous operation.
A promise object has a state that can be one of the following:
Pending
Fulfilled with a value
Rejected for a reason
Use then() method to schedule a callback to be executed when the promise is fulfilled, and catch() method to schedule a callback to be invoked when the promise is rejected.
Place the code that you want to execute in the finally() method whether the promise is fulfilled or rejected.
PROMISE chaining- mutiple diff promises being executed because many promises got fulfilled
Use then() method to schedule a callback to be executed when the promise is fulfilled, and catch() method to schedule a callback to be invoked when the promise is rejected.
Place the code that you want to execute in the finally() method whether the promise is fulfilled or rejected.
The Promise.race() static method accepts a list of promises as an iterable object and returns a new promise that fulfills or rejects as soon as there is one promise that fulfills or rejects, with the value or reason from that promise.(its like true in OR conditio as soon as one value is true it returns true or false)
The Promise.any() method accepts a list of Promise objects as an iterable object:
Promise.any(iterable);
Code language: JavaScript (javascript)
If one of the promises in the iterable object is fulfilled, the Promise.any() returns a single promise that resolves to a value which is the result of the fulfilled promise
Promise.allSettled() method that accepts a list of Promises and returns a new promise that resolves after all the input promises have settled, either resolved or rejected.
The finally() method of a Promise instance allows you to schedule a function to be executed when the promise is settled.
ERRORS IN PROMISE: Inside the promise, the catch() method will catch the error caused by the throw statement and reject().
If an error occurs and you don’t have the catch() method, the JavaScript engine issues a runtime error and stops the program
DID NOT UNDERSTAND ASYNC/AWAIT
DID NOT UNDERSTAND Promise.withResolvers()

SECTION 10
FOR LOOP: its complexity grows when you nest a loop inside another loop. In addition, keeping track of multiple variables inside the loops is error-prone.
for...of is far more elegant than the for loop because it shows the true intent of the code – iterate over an array to access each element in the sequence.
A generator can pause midway and then continues from where it paused.
DENOTED using *funcname, Generators do not execute its body immediately when they are invoked.
yield keyword allows you to pause and resume a generator function
for...of that iterates over an iterable object such as:
Built-in Array, String, Map, Set, …
Array-like objects such as arguments or NodeList
User-defined objects that implement the iterator protocol.
DID NOT UNDERSTAND ASYNC ITERATORS

SECTION 11
ny variables or functions declared in the module won’t be added automatically to the global scope. WORKS IN STRICT MODE
ES6 modules allow you to organize JavaScript files into modules
Use the export statement to export variables, functions, and classes.
Use the import statement to import variables, functions, and classes from other modules.
There are two types of exports:
Named exports
Default exports
DID NOT UNDERSTAND TOP LEVEL AWAIT

SECTION 12
TO create a new symbol, you use the global Symbol() function
let s = Symbol('foo');
The Symbol() function creates a new unique value each time you call it
you use the Symbol.for() method to create a symbol that will be shared

SECTION 13
MAP:
When iterating a Map object, each iteration returns a 2-member array of [key, value]
DID NOT UNDERSTAN MAP MUCH AND HOW IT DIFFERS FROM AN OBJECT
SET:stores a collection of unique values of any type. To create a new empty Set, you use the following syntax:
let setObject = new Set();
FUNCTIONS IN set are: add,clear, delete(value),entries

SECTION 14
you use the try...catch statement - to handle the error and continue the execution.
try {
  // code may cause error
} catch(error){
  // code to handle error
}
First, place the code that may cause an error in the try block.
Second, implement the logic to handle the error in the catch block.
Sometimes, you want to execute a block whether exceptions occur or not THIS IS FINALLY
The finally block always executes whether exceptions occur or not
The throw statement allows you to throw an exception(USER DEFINED). Here’s the syntax of the throw statement:
throw expression;
the expression specifies the value of the exception
DID NOT UNDERSTAND catch binding

SECTION 15
The let keyword is similar to the var keyword, except that these variables are blocked-scope
var keyword, the scope of the variable is either global or local. If you declare a variable outside of a function, the scope of the variable is global. When you declare a variable inside a function, the scope of the variable is local.
The var keyword allows you to redeclare a variable without any issue:

var counter = 0;
var counter;
console.log(counter); // 0
Code language: JavaScript (javascript)
However, redeclaring a variable using the let keyword will result in an error:
let counter = 0;
let counter;
console.log(counter);
A variable declared by the let keyword has a so-called temporal dead zone (TDZ). The TDZ is the time from the start of the block until the variable declaration is processed
Variables declared using the let keyword are block-scoped, are not initialized to any value, and are not attached to the global object.
Redeclaring a variable using the let keyword will cause an error.
A temporal dead zone of a variable is declared using the let keyword starts from the block until the initialization is evaluated.
The global var variables are added to the global object as properties. 
The const keyword creates a read-only reference to a value(CANNOT BE CHANGED)
JUST LIKE LET- the const keyword declares blocked-scope variables. However, the block-scoped variables declared by the const keyword can’t be reassigned.
The const keyword ensures that the variable it creates is read-only. However, it doesn’t mean that the actual value to which the const variable reference is immutable. For example:
const person = { age: 20 };
person.age = 30; // OK
console.log(person.age); //30

SECTION 16
PROXY OBJECT: A JavaScript Proxy is an object that wraps another object (target) and intercepts the fundamental operations of the target object.(NOT EXACTLY SURE WHAT THIS MEANS)
To create a new proxy object, you use the following syntax:

let proxy = new Proxy(target, handler);
Code language: JavaScript (javascript)
In this syntax:
target – is an object to wrap.
handler – is an object that contains methods to control the behaviors of the target. The methods inside the handler object are called traps.
DID NOT UNDERSTAND VARIOUS TRAPS UNDER THIS
Reflection is the ability of a program to manipulate variables, properties, and methods of objects at runtime.
I DID NOT UNDERSTAND THE REST OF THE CONTENT IN THIS SECTION

SECTION 17
Create the global object i.e., window in the web browser or global in Node.js.
Create the this object and bind it to the global object.
Set up a memory heap for storing variables and function references.
Store the function declarations in the memory heap and variables within the global execution context with the initial values as undefined.
DID NOT UNDERSTAND CALL STACK
DID NOT UNDERSTAND EVENT LOOP
Variable hoisting means the JavaScript engine moves the variable declarations to the top of the script.
The JavaScript engine doesn’t hoist the function expressions and arrow functions
VARIABLES HAVE THREE SCOPES: GLOBAL( It can be accessible everywhere in the script.),LOCAL(The variables that you declare inside a function are local to the function.) AND BLOCK(INSIDE CURLY BRACES FORM A BLOCK)

SECTION 18
PRIMITIVE WRAPPER TYPES MAKE IT EASIER TO USE PRIMITIVE VALUES(BOOLEAN,NUMBER,STRING)
let language = 'JavaScript';
let str = language.substring(4);
Code language: JavaScript (javascript)
is technically equivalent to the following code:
let language = 'JavaScript';
// behind the scenes of the language.substring(4);
let tmp = new String(language);
str = temp.substring(4);
temp = null;
BOOLEAN
Data Type	Values converted to true	Value Converted to false
string	Any non-empty string	“” (empty string)
number	Any Non-zero number	0, NaN
object	Any object	null
undefined	(not relevant)	undefined
NUMBER
To create a Number object, you use the Number constructor and pass in a number value as follows:
var numberObject = new Number(100);
BigInt that allows you to represent big whole numbers, which cannot represent by the number type (larger than 253 - 1).
STRING TYPE
Can be created by using the String constructor as follows:
let str = new String('JavaScript String Type');
LEARNT ABOUT STRING MANIPULATION USING DIFFERENT FUNCTIONS

SECTION 19
three logical assignment operators including:
Logical OR assignment operator (||=)
Logical AND assignment operator (&&=)
Nullish coalescing assignment operator (??=)
Logical Assignment Operators	Logical Operators
x ||= y	x || (x = y)
x &&= y	x && (x = y)
x ??= y	x ?? (x = y);
The logical OR assignment (x ||= y) operator only assigns y to x if x is falsy.
The logical AND assignment (x &&= y) operator only assigns y to x if x is truthy.
The nullish coalescing assignment (x ??= y) operator only assigns y to x if x is nullish.
The nullish coalescing operator (??) is a logical operator that accepts two values and returns the second value if the first one is null or undefined.
The exponentiation operator ** raises a number to the power of an exponent.
The exponentiation operator ** accepts values of the type number or bigint.

TO be honest,there were some parts in certain sectiobs that I did not understand at all, some that I understood while readin but on rechecking forgot about it.Learning did happen, but there are parts which I need to revisit and parts were I need your help to understand.
