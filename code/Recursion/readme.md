//POWER SOLUTION
```js
function power(base, exponent){
    if(exponent === 0) return 1;
    return base * power(base,exponent-1);
}
```

//FACTORIAL SOLUTION
```js
function factorial(x){
   if (x < 0 ) return 0;
   if (x <= 1 ) return 1;
   return x * factorial(x-1);
}
```

//PRODUCT OF ARRAY SOLUTION
```js
function productOfArray(arr) {
    if(arr.length === 0) {
        return 1;
    }
    return arr[0] * productOfArray(arr.slice(1));
}
```
//RECURSIVE RANGE SOLUTION
```js
function recursiveRange(x){
   if (x === 0 ) return 0;
   return x + recursiveRange(x-1);
}
```

//FIBONACCI SOLUTION
```js
function fib(n){
    if (n <= 2) return 1;
    return fib(n-1) + fib(n-2);
}
```
