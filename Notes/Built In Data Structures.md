# Objects
Unordered, key value paris of data.
```javascript
let instructor = {
    name: "Jose",
    favoriteLanguages: ["JavaScript", "Pytho"],
    isInstructor: true,
}
```
### When to use:
- When you don't need ordering.
- Fast access/insertion and removal

### Big O
#### Operations
- Insertion and removal - O(1)
- Access - O(1)
- Searching - O(n) - Check if a value is in any of the keys.

#### Methods
```javascript
instructor.keys(); // O(n) - Returns an array of keys.
// ["name", "favoriteLanguages", "isInstructor"]

instructor.values(); // O(n) - Returns an array of values.
// ["Jose", ["JavaScript", "Pytho"], true]

instructor.entries(); // O(n) -  Returns an array of key value pairs.
// [["name", "Jose"], ["favoriteLanguages", ["JavaScript", "Pytho"]], ["isInstructor", true]]

instructor.hasOwnProperty("name"); // O(1) - Returns true if the key exists.
// true
``` 

> When you don't need any ordering, objects are an excellent choice!

---
# Arrays
Ordered lists.
```javascript
let names = ["Jose", "Ricardo", "Pedro"];

let values = [true, {}, [], 2, "Jose"];
```
### When to use:
- When you need order in values.
- Fast access/insertion and removal (sort of...)

### Big O
#### Operations
- Insertion and removal - O(1) *(at the end)* or O(n) *(at the beginning because of reindexing)*
- Access - O(1)
- Searching - O(n) - Check for specific value in all the array.

#### Methods
```javascript
names.length; // O(1) - Returns the length of the array.
// 3

names.push("Juan"); // O(1) - Adds a new element to the end of the array.

names.pop(); // O(1) - Removes the last element of the array.
// "Juan"

names.shift(); // O(n) - Removes the first element of the array.
// "Jose"

names.unshift("Jose"); // O(n) - Adds a new element to the beginning of the array.

names.slice(1, 3); // O(n) - Returns a new array with the elements from the index 1 to 3(NOincluded)
// ["Ricardo", "Pedro"]

names.splice(1, 2); // O(n) - Removes the elements from the index 1 to 2(included)
// ["Ricardo", "Pedro"]

names.sort(); // O(n log n) - Sorts the array.
```

> When you need order in values, and you won't add/remove values that aren't at the end... arrays are an excellent choice!
---

