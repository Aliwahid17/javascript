# Introduction

## Callback functions

Callback functions are functions passed as arguments. This programming pattern creates a sequence of function calls in both synchronous and asynchronous programming. Writing a callback function is no different from writing a function; however, the callback function must match the signature defined by the calling function.

```javascript
const sideLength = 5;

// Caller function takes a callback function
function applySideLength(callback) {
  return callback(sideLength);
}

// Callback must expect the possible argument from the calling function
function squareArea(side) {
  return side * side;
}

applySideLength(areaOfSquare); // => 25
```

You may also write callbacks as a function expression:

```javascript
applySideLength(function squarePerimeterLength(side) {
  return side * 4;
});
```
