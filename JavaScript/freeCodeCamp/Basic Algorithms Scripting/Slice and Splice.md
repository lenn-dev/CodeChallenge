# Slice and Splice
You are given two arrays and an index.

Copy each element of the first array into the second array, in order.

Begin inserting elements at index `n` of the second array.

Return the resulting array. The input arrays should remain the same after the function runs.

## Before 
```javascript
function frankenSplice(arr1, arr2, n) {
  return arr2;
}

frankenSplice([1, 2, 3], [4, 5, 6], 1);
```
## Answers
```javascript
function frankenSplice(arr1, arr2, n) {
    let newArr =arr2.slice(0,);
    newArr.splice(n,0, ...arr1); 
    return newArr;  
}
frankenSplice([1, 2, 3], [4, 5, 6], 1);
```

## Note 
Without `...` spread operator for the splice parameter, 
return value will be like this:  [ 4, [ 1, 2, 3 ], 5, 6 ]
