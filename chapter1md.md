# Week 1: Rebuilding Lodash

### Publishing on NPM

## The Tests

## The Functions

### filter(array, function/object/array)

Filter is one of the trickier ones, as a full implementation of Lodash's functionality requires the implementation of several subfunctions, including isMatch() and matches(), which is a "partially applied" version of isMatch(). 

Lodash's filter works almost exactly like the filter function that JavaScript has had since at least ES5, which is defined for Array.prototype. You'd call like this: 

ES5:

[1,2,3,5].filter(function (item) { return item < 5 })
=> [1,2,3]

ES6: 

[1,2,3,5].filter(item => item < 5)
=> [1,2,3]

ES6 has a nice shorthand for anonymous functions. The gotcha for someone used to languages with implicit return statements like the above (eg. Ruby, Coffeescript) is ONLY does implicit return when it's the only line in the anonymous function, as in the above.

As for the way Lodash's filter works, the difference is just that everything in Lodash is called off the Lodash object (as it's generally considered bad practice to just attach functions willy-nilly to Array.prototype), so the array becomes the first argument:

ES6:
_.filter([1,2,3,5], item => item < 5)

The second function just gets applied to every item in the array. The above is just saying "if the item is less than five, put it in a new array and return that array." One possible implementation of this, without error checking or anything, is to just run iterate across the array and run whatever that function is:

filter(list, iteratee) { 
  list.forEach(item => {
    Man, I'm going to bed.
  })
}



### matches()

### isMatch()


