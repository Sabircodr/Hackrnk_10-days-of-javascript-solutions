# Day 2: Loops

## Objective
In this challenge, we practice looping over the characters of a string.

## Task
1. First, print each vowel in `s` on a new line. The English vowels are `a, e, i, o,` and `u`, and each vowel must be printed in the same order as it appeared in `s`.
2. Second, print each consonant (i.e., non-vowel) in `s` on a new line in the same order as it appeared in `s`.

## Function Description
Complete the `vowelsAndConsonants` function in the editor below.
`vowelsAndConsonants` has the following parameters:
- string `s`: the string to process

## Prints
Print each vowel of `s` in order on a new line, then print each consonant in order on a new line. Return nothing.

## Input Format
There is one line of input with the string `s`.

## Output Format
First, print each vowel in `s` on a new line (in the same order as they appeared in `s`). Second, print each consonant (i.e., non-vowel) in `s` on a new line (in the same order as they appeared in `s`).

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

/*
 * Complete the vowelsAndConsonants function.
 * Print your output using 'console.log()'.
 */
function vowelsAndConsonants(s) {
    const vowels = 'aeiou';
    let consonants = '';
    
    for (let i = 0; i < s.length; i++) {
        if (vowels.includes(s[i])) {
            console.log(s[i]);
        } else {
            consonants += s[i] + '\n';
        }
    }
    
    console.log(consonants.trim());
}

function main() {
    const s = readLine();
    
    vowelsAndConsonants(s);
}
```

## Input (stdin)
```sh
javascriptloops
```

## Your Output (stdout)
```sh
a
a
i
o
o
j
v
s
c
r
p
t
l
p
s
```

## Expected Output
```sh
a
a
i
o
o
j
v
s
c
r
p
t
l
p
s
```
