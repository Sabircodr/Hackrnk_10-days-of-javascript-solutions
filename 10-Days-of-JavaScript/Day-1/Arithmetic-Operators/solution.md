# Day 1: Arithmetic Operators

## Objective
In this challenge, we practice using arithmetic operators. Check out the attached tutorial for resources.

## Task
Complete the following functions in the editor below:
1. `getArea(length, width)`: Calculate and return the area of a rectangle having sides `length` and `width`.
2. `getPerimeter(length, width)`: Calculate and return the perimeter of a rectangle having sides `length` and `width`.

The values returned by these functions are printed to stdout by locked stub code in the editor.

## Input Format
| Function    | Data Type | Parameter | Description                             |
|-------------|-----------|-----------|-----------------------------------------|
| `getArea`   | Number    | `length`  | A number denoting the length of a rectangle. |
|             | Number    | `width`   | A number denoting the width of a rectangle.  |
| `getPerimeter` | Number | `length`  | A number denoting the length of a rectangle. |
|             | Number    | `width`   | A number denoting the width of a rectangle.  |

## Constraints
- 1 ≤ `length`, `width` ≤ 1000
- `length` and `width` are scaled to at most three decimal places.

## Output Format
| Function     | Return Type | Description                                          |
|--------------|-------------|------------------------------------------------------|
| `getArea`    | Number      | The area of a rectangle having sides `length` and `width`. |
| `getPerimeter` | Number    | The perimeter of a rectangle having sides `length` and `width`. |

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

/**
*   Calculate the area of a rectangle.
*
*   length: The length of the rectangle.
*   width: The width of the rectangle.
*   
*   Return a number denoting the rectangle's area.
**/
function getArea(length, width) {
    let area;
    // Write your code here
    area = length * width;
    return area;
}

/**
*   Calculate the perimeter of a rectangle.
*   
*   length: The length of the rectangle.
*   width: The width of the rectangle.
*   
*   Return a number denoting the perimeter of a rectangle.
**/
function getPerimeter(length, width) {
    let perimeter;
    // Write your code here
    perimeter = 2 * (length + width);
    return perimeter;
}

function main() {
    const length = +(readLine());
    const width = +(readLine());
    
    console.log(getArea(length, width));
    console.log(getPerimeter(length, width));
}
```

### Input (stdin)
```sh
3
4.5
```

### Your Output (stdout)
```sh
13.5
15
```

### Expected Output
```sh
13.5
15
```
