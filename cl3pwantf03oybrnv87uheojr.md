## Objects in Javascript

![hello](https://media.giphy.com/media/E1w0yvMxBIv5M8WkL8/giphy.gif)

In this article, we will be discussing javascript objects.

We will see : 

- What are javascript objects 
- Different ways of creating them 
- Different ways of accessing them

### What are javascript objects?

Javascript objects are similar to real-world objects. Take an example of a car. A car is an object with different properties like color, model, etc.


Objects are used to store key-value store of data and multiple entities. Unlike primitive data types where value contains a single thing(string or number), objects can store multiple data types and even functions.   

### Ways to create objects 


- **Objects literal**

```
  const user = {    
  name: "Aaku",  
  age: 23        
}
```
In the user object, there are two properties : 

1. name which has  value "Aaku"
2. age which has  value 23 

- **new keyword**

```
let user = new Object()
user.name="Aaku"
user.age=23
```

### Accessing the properties of the object

- **dot notation**

```
let user = {
    name: "Aaku"
}

console.log(user.name)
```
 
- **brackets notation**

```
let user = {
    name: "Aaku"
}

console.log(user["name"])

```

### Bonus 💥
 **"in" operator**

In javascript, there will be no error if the property does not exist. It will simply return **undefined**.
Example: 
 ```
let user = {};

console.log( user.noSuchProperty === undefined ); // true means "no such property"
```

**for..in loop**
It is used to iterate over all the keys of the object.

```
for (let key in user) {
  // keys
  alert( key );  // name, age
  // values for the keys
  alert( user[key] ); // Aaku, 23
}

```


**Checking for emptiness**

function isEmpty(obj) which returns true if the object has no properties, false otherwise.

```
function isEmpty(obj) {
  for (let key in obj) {
    // if the loop has started, there is a property
    return false;
  }
  return true;
}
```

**References**
- [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)




That's all for this article. If you like this article do subscribe to the newsletter or follow me on [Twitter](https://twitter.com/Aakudhurandhar)

> PS: I am publishing a new blog after a very long time so I'll try to be more regular xD! Till then... bye bye 👋🏻.

![thanks](https://media.giphy.com/media/uWlpPGquhGZNFzY90z/giphy.gif)







