# Callback function

Callback function is a function that allows a function to take another function as a parameter.

You can think about it as a chain of functions.

```javascript
function executeCallback(some) { 
    console.log("callback:"+some); 
}
function main_function(num, myCallback) { 
    console.log(num); 
    myCallback(num+1); 
}
```

Question: What happened when we call main\_function(5, executeCallback)?

