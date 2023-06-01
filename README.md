# ES2015restSpread
In this exercise ES5 code is refactored into ES2015 code. 

The function shown below, filterOutOdds, has been refactored into
ES2015 code using rest operator and an arrow function.

**ES5 code:**
function filterOutOdds() {
  var nums = Array.prototype.slice.call(arguments);
  return nums.filter(function(num) {
    return num % 2 === 0
  });
}

The function, filterOutOdds, shown above has been refactored as shown
below into ES2015 code.

**ES2015 code:**
const filterOutOdds = (...nums) => nums.filter(num => num % 2 === 0);

The function shown below, findMin, accepts a variable number of arguments and returns the smallest argument
by using a rest and a spread operator in the function.

**Function, findMin:**
const findMin = (...args) => Math.min(...args);

Below is a function, mergeObjects, that accepts two objects and returns a new object which contains 
all the keys and values of the first object and second object. 

**Function, mergeObjects:**
const mergeObjects = (obj1, obj2) => ({...obj1, ...obj2});


Below is a function, doubleAndReturnArgs, which accepts an array and a variable number of arguments. 
The function should return a new array with the original array values and all of additional arguments doubled. 

**Function, doubleAndReturnArgs:**
const doubleAndReturnArgs = (arr, ...args) => [...arr, ...args.map(arg => arg * 2)];

In the section below, functions have been written using rest and spread.  
As well the functions have been factored using arrow functions.  

**Function removeRandom:**
const removeRandom = items => {
  const index = Math.floor(Math.random() * items.length);
  return [...items.slice(0, index), ...items.slice(index + 1)];
}

**Function extend:**
const extend = (array1, array2) => [...array1, ...array2];

**Function addKeyVal:**
const addKeyVal = (obj, key, val) => ({...obj, [key]: val});

**Function removeKey:**
const removeKey = (obj, key) => {
  const newObj = {...obj};
  delete newObj[key];
  return newObj;
}

**Function combine:**
const combine = (obj1, obj2) => ({...obj1, ...obj2});

**Function update:**
const update = (obj, key, val) => ({...obj, [key]: val});



