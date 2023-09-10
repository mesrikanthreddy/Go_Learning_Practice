# Go_Learning_Practice
# Variables
When writing Go programs, variables must be declared before they can be used. The example below shows how to declare single variables or a group of variables. In the interest of space, the output is displayed as an in-line comment.

# Types

Go offers a rich collection of types, including numerics, booleans, strings, error, and the ability to create custom types. Strings are a sequence of UTF-8 characters enclosed in double-quotes. Numerical types are the most versatile, with 8, 16, 32, and 64-bit variants for both signed (int) and unsigned (uint) integers.

A byte is an alias for uint8. A rune is an alias for int32. Floats (or floating-point numbers) are either float32 or float64. Complex numbers are also supported and can be represented as complex128 or complex64.

When a variable is declared it is assigned the natural “null” value of the corresponding type. For example, in var k int, k has the value 0. In var s string, s has the value "". The example below shows the difference between user-specified types and the default types assigned with a short variable declaration.
# Arrays
Storing a number of elements in a list can be achieved using arrays, slices, and maps (Go’s version of hash-maps). We’ll consider all three in the examples below. Arrays are defined by their fixed size and a common data type for all elements. Interestingly, the size of the array is part of the type, meaning arrays cannot grow or shrink, otherwise, they would have a different type. Array elements are accessed using square brackets. The example below shows how to declare an array containing strings and how to loop through its elements.
# Slices
Slices can be thought of as dynamic arrays. Slices always refer to an underlying array and can grow when new elements are added. The number of elements that are visible through a slice determines its length. If a slice has an underlying array that is larger, the slice may still have the capacity to grow. When it comes to slices, think of the length as the current number of elements, and think of the capacity as the maximum number of elements that can be stored. Let’s see an example in the file slices.go
# Maps
Most modern programming languages have a built-in implementation of a hash-map. For example, think of Python’s dictionary or JavaScript’s object. Fundamentally, a map is a data structure that stores key-value pairs with a constant look-up time. The efficiency of maps comes at the expense of randomizing the order of the keys and the associated values. In other words, we make no guarantees about the order of the elements in a map. The example below showcases this behavior.

# Control Flow
To wrap things up, we will consider the following scenario: Let’s suppose we’re given a slice containing floats, and we’re interested in computing their average value. We’ll proceed by creating a function called average that takes a slice as a parameter and returns a float called avg. The example below shows a possible implementation.

# Structs and pointers
Before we begin discussing structs and user-defined types, we have to cover pointers. The good news is that pointer arithmetic is not allowed in Go, which eliminates dangerous/unpredictable behavior. A pointer stores the memory address of a value. In Go, the type *T is a pointer to a T value. The default value for pointers is nil. Let’s go through an example.

