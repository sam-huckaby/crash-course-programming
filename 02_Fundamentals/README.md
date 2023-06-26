# Programming Fundamentals
Perhaps you're wondering how you've made it this far and are only just now being shown "the fundamentals". Fear not, you have not wasted time learning about HTML and CSS. We started with things like Git, HTML, and CSS for a number of reasons:
1. They're fun to write!
2. You get to see what you build right away (instant gratification)
3. It gets you used to typing the kinds of characters you need in programing
4. Without a lot of programming experience, these pieces of tech are the most relevant to jobs you could apply for right away

You are now hopefully unsatisfied with the limits of HTML/CSS and want something that "does something", which is where we now begin.

## Foundational Concepts

### Variables

At its core, a variable in computer programming is a storage location that's paired with an identifiable name (an identifier), which holds some specific or nonspecific quantity of information, also known as a value.

Think of a variable as a labelled box where you can store different values.

Variables in programming enable programmers to write code that's both flexible and generalizable. Instead of using specific, hard-coded values for every operation, variables allow our code to be adaptable to varying conditions or inputs.

Each variable has a specific type, which determines what kind of values it can store. These types can range from integers, floating-point numbers, strings, booleans, to more complex data structures like lists, arrays, or objects. Depending on the programming language, the type of a variable can be either explicitly declared or inferred from the initial value it's assigned.

Now, let's take a look at how variables are declared and utilized in a few popular programming languages:

1. Python: Python is a dynamically-typed language. This means that you do not have to declare the type of a variable when you create it. The Python interpreter will infer the type based on the assigned value.

```python
x = 10  # An integer
y = "Hello, World!"  # A string
```

2. JavaScript: Like Python, JavaScript is also dynamically-typed. Variables can be declared using `var`, `let`, or `const`, depending on the scope and mutability you need.

```javascript
let x = 10;  // An integer
const y = "Hello, World!";  // A string
```

3. Golang (Go): Unlike Python and JavaScript, Go is a statically-typed language. This means you need to declare the type of a variable when you create it.

```go
var x int = 10  // An integer
var y string = "Hello, World!"  // A string
// Or with type inference
x := 10
y := "Hello, World!"
```

4. C++: C++ is also a statically-typed language. You must declare the type of each variable explicitly.

```c++
int x = 10;  // An integer
std::string y = "Hello, World!";  // A string
```

Regardless of the language, the basic principles surrounding variables—the storage and manipulation of values—remain consistent. However, the exact syntax and rules of use can vary, as seen in the examples above.

Different languages handle variables and data types differently, including aspects like memory management, type casting and conversion, mutable vs immutable variables, and more. When starting to learn a new language, it's important to understand how it manages variables.

Lastly, keep in mind that variables have a scope—they can either be available throughout the entire program (global variables), or only within a specific function or block of code (local variables). The rules for managing this also depend on the programming language.

Understanding variables is a fundamental part of learning how to program, so it's great that you're diving into this topic! They're one of the first concepts you should familiarize yourself with as you aspire to become a proficient programmer.

### Functions

A function in computer programming is a named sequence of statements that performs a specific task, potentially operating on provided inputs (also known as arguments or parameters) and producing an output (the return value). Functions are one of the primary building blocks in programming, allowing us to write reusable code that can be called multiple times within a program.

To put functions in the context of Magic: The Gathering, you might say that a function is a Saga that lets you design the steps. The same logic is applied each time, though you could use conditional statements to direct the flow of processing to different parts of the function, like perhaps your function gives +1/+1 to your creatures, but only the ones with a type of Goblin.

Functions serve several purposes:

1. Code reuse: If you find yourself needing to perform the same set of instructions multiple times in different parts of your program, that's a good indicator that a function could be useful. 

2. Abstraction: Functions allow you to hide the complex details of what they're doing. Once a function is written, you can use it without worrying about how it accomplishes its task. 

3. Modularity: Functions allow you to break down complex problems into smaller, more manageable parts. 

A function can take zero, one, or multiple parameters, and it can return a value. Not all functions return a value, however. In some languages, such functions might be called procedures or subroutines.

Now, let's look at how to declare and use functions in several programming languages, starting with a simple function that takes no input and performs a simple operation, and then moving on to a function that accepts multiple inputs.

1. Python:
```python
# A simple function with no input
def greet():
    print("Hello, World!")

# Call the function
greet()

# A function with two inputs
def add_numbers(x, y):
    return x + y

# Call the function
result = add_numbers(5, 3)
print(result)  # Outputs: 8
```

2. JavaScript:
```javascript
// A simple function with no input
function greet() {
    console.log("Hello, World!");
}

// Call the function
greet();

// A function with two inputs
function addNumbers(x, y) {
    return x + y;
}

// Call the function
let result = addNumbers(5, 3);
console.log(result);  // Outputs: 8
```

3. Go (Golang):
```go
// A simple function with no input
func greet() {
    fmt.Println("Hello, World!")
}

// Call the function
greet()

// A function with two inputs
func addNumbers(x int, y int) int {
    return x + y
}

// Call the function
result := addNumbers(5, 3)
fmt.Println(result)  // Outputs: 8
```

4. C++:
```c++
#include <iostream>

// A simple function with no input
void greet() {
    std::cout << "Hello, World!" << std::endl;
}

// A function with two inputs
int addNumbers(int x, int y) {
    return x + y;
}

int main() {
    // Call the functions
    greet();
    int result = addNumbers(5, 3);
    std::cout << result << std::endl;  // Outputs: 8

    return 0;
}
```

In all these examples, the `greet` function performs the same operation every time it's called—it prints "Hello, World!" to the console. The `addNumbers` function, on the other hand, accepts two inputs and adds them together, returning the result. The exact output will depend on the specific numbers you pass in when you call the function.

Functions can be much more complex than these examples, accepting many parameters, performing complex calculations or manipulations, and returning complex data types. But these basic examples should give you a starting point to understand the concept of functions in programming.

