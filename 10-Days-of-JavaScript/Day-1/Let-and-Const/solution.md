# Day 1: Let and Const

## Objective
In this challenge, we practice declaring variables using the `let` and `const` keywords.

## Task
1. Declare a constant variable, `PI`, and assign it the value `Math.PI`. You will not pass this challenge unless the variable is declared as a constant and named `PI` (uppercase).
2. Read a number, `r`, denoting the radius of a circle from stdin.
3. Use `PI` and `r` to calculate the area and perimeter of a circle having radius `r`.
4. Print the area as the first line of output and print the perimeter as the second line of output.

## Input Format
A single integer, `r`, denoting the radius of a circle.

## Constraints
-  0 < `r` ≤ 100 
- `r` is a floating-point number scaled to at most 3 decimal places.

## Output Format
Print the following two lines:
1. On the first line, print the area of the circle having radius `r`.
2. On the second line, print the perimeter of the circle having radius `r`.

## Code
```javascript
'use strict';

process.stdin.resume();
process.stdin.setEncoding('utf-8');

let inputString = '';
let currentLine = 0;

process.stdin.on('data', inputStdin => {
    inputString += inputStdin;
});

process.stdin.on('end', _ => {
    inputString = inputString.trim().split('\n').map(string => {
        return string.trim();
    });
    
    main();    
});

function readLine() {
    return inputString[currentLine++];
}

function main() {
    // Write your code here. Read input using 'readLine()' and print output using 'console.log()'.
    const PI = Math.PI;
    let r = parseFloat(readLine());    
    console.log(PI * r * r);
    console.log(2 * PI * r);

    try {    
        // Attempt to redefine the value of constant variable PI
        PI = 0;
        // Attempt to print the value of PI
        console.log(PI);
    } catch (error) {
        console.error("You correctly declared 'PI' as a constant.");
    }
}
```

### Error (stderr)
```sh
You correctly declared 'PI' as a constant.
```

### Input (stdin)
```sh
2.6
```

### Your Output (stdout)
```sh
21.237166338267002
16.336281798666924
```

### Expected Output
```sh
21.237166338267002
16.336281798666924
```
