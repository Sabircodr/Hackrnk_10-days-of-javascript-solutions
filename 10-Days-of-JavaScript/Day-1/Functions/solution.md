# Day 1: Functions

## Objective
Today, we're discussing JavaScript functions. Check out the attached tutorial for more details.

## Task
Implement a function named `factorial` that has one parameter: an integer `n`. It must return the value of `n!` (i.e., `n` factorial).

## Input Format
Locked stub code in the editor reads a single integer, `n`, from stdin and passes it to a function named `factorial`.

## Constraints
- 1 ≤ `n` ≤ 10

## Output Format
The function must return the value of `n!`.

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

function factorial(n) {
  var ans = 1;
  for (var i = 1; i <= n; i++) {
    ans = ans * i;
  }
  return ans;
}

function main() {
    const n = +(readLine());
    console.log(factorial(n));
}
```

### Input (stdin)
```sh
4
```

### Your Output (stdout)
```sh
24
```

### Expected Output
```sh
24
