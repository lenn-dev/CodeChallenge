# Use Recursion to Create a Range of Numbers
Continuing from the previous challenge, we provide you another opportunity to create a recursive function to solve a problem.

We have defined a function named `rangeOfNumbers` with two parameters. 
The function should return an array of integers which begins with a number represented by the `startNum` parameter 
and ends with a number represented by the `endNum` parameter. The starting number will always be less than or equal to the ending number. 
Your function must use recursion by calling itself and not use loops of any kind. 
It should also work for cases where both `startNum` and `endNum` are the same.

## Before
```javascript
function rangeOfNumbers(startNum, endNum) {
  return [];
};
```

## Answers
```javascript
function rangeOfNumbers(startNum, endNum) {
 
  if(startNum > endNum){
    return [];
  }else{
    const Array = rangeOfNumbers(startNum,endNum-1);
    Array.push(endNum);
    return Array;
  }
}

console.log(rangeOfNumbers(3,6));
```
