# FLIP

FLIP -  Functional Language for Intuitive Programming

Example:

```flip
// Define a function to check if a number is odd
define isOdd(n) = n % 2 != 0;

// Define a function to square a number
define square(n) = n * n;

// Define a function to sum a list
define sumList(l) = reduce(l, 0, (acc, x) => acc + x);

// Define the main function to process the list
define processList(numbers) {
    let oddNumbers = filter(numbers, isOdd);          // Filter the odd numbers
    let squaredNumbers = map(oddNumbers, square);     // Square the odd numbers
    return sumList(squaredNumbers);                   // Sum the squared numbers
}

// Sample input and execution
let inputNumbers = [1, 2, 3, 4, 5];
let result = processList(inputNumbers);
print(result);  // Output: 1^2 + 3^2 + 5^2 = 1 + 9 + 25 = 35

```
