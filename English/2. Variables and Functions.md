# Variables and Functions

In LUA, variables are used to store and manipulate data, and functions are used to organize and reuse code.

## Variables
In LUA, variables are declared using the `local` keyword or without it.
```lua
-- Declaring a variable
local x = 5

-- Declaring a variable without the `local` keyword
y = 10
```
It's recommended to use the local keyword when declaring a variable, as it limits the scope of the variable to the current function or file, and prevents accidental global variable assignments.

LUA supports several data types, including numbers, strings, booleans, and tables.
```lua
-- Declaring a number variable
local age = 25

-- Declaring a string variable
local name = "John"

-- Declaring a boolean variable
local isValid = true

-- Declaring a table variable
local myTable = {1, 2, 3}
```
## Functions
In LUA, functions are declared using the function keyword and can be called using the function name followed by parentheses.
```lua
-- Declaring a function
function sayHello()
    print("Hello!")
end

-- Calling a function
sayHello()
```
Functions can also take parameters and return values.
```lua
-- Declaring a function with parameters
function add(x, y)
    return x + y
end

-- Calling a function with arguments
result = add(5, 10)
```
Functions can be stored in variables and passed as arguments to other functions.
```lua
-- Storing a function in a variable
local myFunction = function()
    print("Hello!")
end

-- Passing a function as an argument
otherFunction(myFunction)
```
This is just a small introduction to variables and functions in LUA, there is much more to learn and explore, such as closures, recursion, and more.