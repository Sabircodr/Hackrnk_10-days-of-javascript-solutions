# Day 2: Conditional Statements: Switch

## Objective
In this challenge, we learn about switch statements.

## Task
Complete the `getLetter(s)` function. It has one parameter: a string, `s`, consisting of lowercase English alphabetic letters (i.e., a through z). It must return A, B, C, or D depending on the following criteria:
- If the first character in string `s` is in the set {a, e, i, o, u}, then return A.
- If the first character in string `s` is in the set {b, c, d, f, g}, then return B.
- If the first character in string `s` is in the set {h, j, k, l, m}, then return C.
- If the first character in string `s` is in the set {n, p, q, r, s, t, v, w, x, y, z}, then return D.

## Function Description
Complete the `getLetter` function in the editor below.
`getLetter` has the following parameters:
- string `s`: a string

## Returns
- string: a single letter determined as described above

## Input Format
Stub code in the editor reads a single string denoting `s` from stdin.

## Code

### Approach 1
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

function getLetter(s) {
    let letter;
    // Write your code here
    switch (s.charAt(0)) {
        case 'a':
        case 'e':
        case 'i':
        case 'o':
        case 'u':
            letter = 'A';
            break;

        case 'b':
        case 'c':
        case 'd':
        case 'f':
        case 'g':
            letter = 'B';
            break;

        case 'h':
        case 'j':
        case 'k':
        case 'l':
        case 'm':
            letter = 'C';
            break;

        default:
            letter = 'D';
    }
    return letter;
}

function main() {
    const s = readLine();
    
    console.log(getLetter(s));
}
```

### Approach 2
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

function getLetter(s) {
    let letter;
    // Write your code here
        switch (s.charAt(0))
        {
            case ( 'a' || 'e' || 'o' || 'i' || u):
                letter = 'A';
                break;

            case ('b' || 'c' || 'd' || 'f' || 'g'):
                letter = 'B';
                break;

            case ('h' || 'j' || 'k' || 'l' || 'm'):
                letter = 'C';
                break;

            case ('z' || 'n' || 'p' || 'q' || 'r' || 's' || 't' || 'v' || 'w' || 'x' || 'y' ):
                letter = 'D';

        }
    return letter;
}


function main() {
    const s = readLine();
    
    console.log(getLetter(s));
}
```

## Input (stdin)
```sh
adfgt
```

## Your Output (stdout)
```sh
A
```

## Expected Output
```sh
A
```
