# Python-Intro5

## Function
* Function is named sequence of statements that perform a specific task.
* Function breaks program into smaller and modular chunks (subtasks).
* Growing program becomes more manageable, tidy and organied.
* Function also allow to avoid code repetitions and make code reusable

## Function Definition Units
* `def` keyword marks the start of function definition
* function_name uniquely identify function
* parameters (arguments) through which we pass values to a function. They are optional
* : (colon) to markt the end of function header.
* `docstring` to describe what the function does.
* One or more valid python statements that make up the function body. Statements must have same indentation level
* An optional return statement to return a value from the function.

## Docstring
* Docstring is used to explain in brief, what a function does
* Docstring immediately forwards the function header
* Triple quotes are used for docstring

## Return Statement
* Return statement is used to exit a function and go back to the place from where it was called.
* By default, function is exited after last statement in its body
* Format: return [expression_list]

## Return Ojbect
* Return statement can contain expression which gets evaluated and the value is returned (to the place from where the call was)
* If there is no expression in the return statement, then the function will return the None object.

## Function work
2 units:
* function definition
* function call

## Variable scope
* Variable Scope is portion of program where variable is visible
* Parameters and variables created in function definition are not visible outside (local scope)
* Variables outside the function are visible from inside (global scope)

## Variable Lifetime
* Variable Lifetime is the period throughout which variable exists in memory.
* The lifetime of variable created inside function definition is as long as the function exists.

## Functions
* Built-in functions
* User-defined functions

## Function Arguments
* Function can have arbitrary number of arguments
* By default, calling a function we can place values for corresponding number of arguments in definition 

## Variable Number of Arguments
* Number of function arguments can be variable
* There are different methods how to define variable number of arguments

## Default Arguments
* We can set default argument value with assignment operator
* Default value will be captured if while calling no value has been passed
* Default arguments should follow non-default arguments.

## Arguments and access by Keywords
* We can pass value to argument either by position or by keyword
* When accessing by keyword the order is not important

## Mandatory Unpacking with *
`*` unpacks iterable objects like list

## Dictionary Unpacking with **
`**` unpacks dictionaries

## Arbitrary Number of Arguments
* Sometimes some function can handle different types of arguments
* To define arbitrary number of arguments we use *args and **kwargs.

## Anonymous/Lambda Functions
* Anonymous function in Python is a function that is defined without a name
* To define an anonymous function in Python we should use lambda keyword instead def.
* Anonymous functions are also referred as lambda functions.

## Lambda Syntax
* Format: lambda arguments: expression
* Lambda function:
  * can have any number of arguments
  * only one expression
* The expression is evaluated and the value is returned
* Lambda is special function writing that can be anywhere we can place function object.

## When to use Lambda?
* It's recommended to use lambda when we need nameless function for short period of time.
* As a rule lambda is passed as a parameter to function
* Often lambda is used in combination with filter(), map() and other functions.

## Function as an object
* In python function is an object that can be passed through the code, for instance, as another function argument
* Default type of function object is function class.
* Function is object that should __ call __() method.
* We can create our own class with __ call __(), then we will be able to call its object as function

## Nested Function
* A function defined inside another function is called a nested function
* Nested functions can access variables of the enclosing scope.

## Closure
* Python Closure are inner functions that are enclosed and returned within the outer function.
* Closure refer to variable present in the outer function scope. It can access these variables even after the outer function has
completed its execution.

## Closure Requirements
* We must have a nested function (function inside a function)
* The nested function must refer to a value defined in the enclosing function
* The enclosing function must return the nested function

## Closure Variable Access
We can refer to outer function variable for read access using its name, but for its modification we should nonlocaal keyword

## When to use Closure
* Closure can avoid the use of global values and provides some form of data hiding . It can also provide an object-oriented
solution to the problem.
* When there are few methods (one method in most cases) to be implemented in a class, closure can provide an alternate and
more elegant solution. But when the number of attributes and methods get larger, it's better to implement a class
* Closure are convenient to use when we need to wrap some function into some another adding extra features.

## Closure Data
All function objeccts have a __ closure __ attribute that returns a tuple of cell objects if it is a closure function. 
We can access their values using cell contents property

## Python Decorators
* Decorator is focused on extending of function features without modifying it.
* There can be lots of reason why to do it, for instance group of functions can have similar code and it doesn't worth
to repeat that code for each of them manually.

## Decorator Syntax
* We can use @decorator instead of creating new identifier for wrapped function or assigning to existing function name

## Map()
* Syntax: map(function_object, iterable1, iterable2, ...)
* map() expects a function object and any number of iterables like list, dictionary, etc. that corresponds to function object
parameters.
* map() executes the function_object for each element in the sequence and returns a list of the elements modified by the 
function object.

## filter()
* Syntax: filter(function_object, iterable)
* function_object returns a boolean value.
* function_object is called for each element of the iterable and filter returns only those elements for which the function_object
returns true.
* filter() can only have one iterable as input

## Reduce()
* Syntax: reduce(function, iterable, <initial_value>)
* reduce cumulatively performs an operation on all the iterable's elements and, therefore, can't be applied to infinite iterables.
* func must be a function takes two elements and returns a single value.
* functools.reduce() takes the first two elements A and B returned by the iterator and calculates func(A, B). It then requests
the third element C, calculates func(func(A, B), C), combines this result with the fourth element returned, and continues until
the iterable is exhausted.
* If the initial value is supplied, it's used as a starting point and func(initial_value, A) is the first calculation

## Type Annotations
* Type Annotations are used to indicate the datatypes of variables and input/output of functions and methods