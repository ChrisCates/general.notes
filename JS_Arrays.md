# Javascript Arrays
## How to traverse javascript arrays

### Traditionally you can use a regular for loop to access a javascript array

```
var array = [1, 2, 3, 4, 5]

//Access the first key in an array
console.log(array[0])
//Access all keys in an array
for (var i = 0; i < array.length; i++) {
	console.log(array[i])
}
```

### However you can use special functions like `.forEach()` and `.map()`

```
var array = [1, 2, 3, 4, 5]

//use a forEach loop on the array
array.forEach(function(value, i) {
	console.log(value, 'and its index', i)
})

//A map is similar except it assigns it to a new variable
array = array.map(function(value, i) {
	console.log(value, i)
	return value + 1
})

console.log(array)
//Array is now [2, 3, 4, 5, 6]
```

### You can also filter data with if statements

```
var array = [1, 2, 3, 4, 5]

var newArray = array.filter(function(value, i) {
	return value > 3
})
console.log(newArray)
//New array only has [4, 5]

var newArray2 = array.filter(function(value, i) {
	return i > 3
})
console.log(newArray2)
//Second new array only [1, 2] 
```