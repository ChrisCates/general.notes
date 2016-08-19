# JSON
## What is JSON and how do we use it?

### JSON stands for Javascript Object Notation and it is the lingua franca of web and HTTP.
### Every REST API uses it.

### JSON uses key, value stores in order to notate data.
#### Barebones example of a .json file

```
{
	"hello": "world"
}
```

### If you were to load this .json file as a variable (let's call it value).
### If you wanted to access the value "world" you would have to access it through the key "hello".

#### Example of accessing JSON files

```
var json = {
	"hello": "world"
}

console.log(json.hello)
//This will log "world"
```

### JSON can get a bit more complex. In this case scenario we can nest arrays and objects inside JSON objects

#### Example of a nested object

```
var json = {
	"nested_object": {
		"hello": "world"
	}
}
```

### In order to access the value "world"

```
console.log(json.nested_object.hello)
//This will log "world"
```

#### Example of a nested array

```
var array = {
	"nested_array": [1, 2, 3, 4, 5]
}
```

### In order to access this array
```
console.log(array.nested_array)
//This will log [1, 2, 3, 4, 5]
```