### Basic Rules for Loops



**`for` loop:**
- Used when the number of iterations is known.
- Syntax:
  ```javascript
  for (initialization; condition; increment) {
      // Code to execute on each iteration
  }
  ```



**`while` loop:**
- Used when the number of iterations is not known and the loop should continue until a condition is met.
- Syntax:
  ```javascript
  while (condition) {
      // Code to execute as long as condition is true
  }
  ```




### Given Object
```javascript
const value = {
    name: "value1",
    next: {
        name: "value2",
        next: {
            name: "value3",
            next: null
        }
    }
};
```

### Using `while` Loop to Traverse the Object
```javascript
let currentNode = value;
while (currentNode !== null) {
    console.log(currentNode.name);
    currentNode = currentNode.next;
}
```

### Using `for` Loop to Traverse the Object
Since the `for` loop typically requires a known number of iterations and our object doesn't provide that directly, we can use a `for` loop in a similar manner to a `while` loop:

```javascript
for (let currentNode = value; currentNode !== null; currentNode = currentNode.next) {
    console.log(currentNode.name);
}
```

### Explanation
- **Using `while` loop:** We initialize `currentNode` to `value` and loop until `currentNode` is `null`. Inside the loop, we print the `name` property and then move to the next node by updating `currentNode` to `currentNode.next`.
- **Using `for` loop:** We use the same logic as the `while` loop but within the `for` loop's structure. The initialization (`let currentNode = value`), condition (`currentNode !== null`), and update (`currentNode = currentNode.next`) are all defined within the `for` loop syntax.


### ব্যাখ্যা
- `while` লুপ ব্যবহার করে: আমরা `currentNode`-কে `value` দিয়ে আরম্ভ করি এবং লুপটি চালাই যতক্ষণ `currentNode` `null` না হয়। লুপের ভিতরে, আমরা `name` প্রোপার্টিটি প্রিন্ট করি এবং তারপর `currentNode`-কে `currentNode.next` দিয়ে আপডেট করি।
- `for` লুপ ব্যবহার করে: আমরা `while` লুপের একই যুক্তি ব্যবহার করি কিন্তু `for` লুপের কাঠামোর মধ্যে। ইনিশিয়ালাইজেশন (`let currentNode = value`), কন্ডিশন (`currentNode !== null`), এবং আপডেট (`currentNode = currentNode.next`) সবই for লুপের সিনট্যাক্সের মধ্যে সংজ্ঞায়িত করা হয়েছে।

Both loops will traverse the nested object structure and print:
```
value1
value2
value3
```

**`for` loop_Array**

```javascript
const array = [1, 2, 3, 4, 5, 5];

for (let i = 0; i < array.length; i++) {
    console.log(array[i]);
}
```

**`while` loop_Array**

```javascript
const array = [1, 2, 3, 4, 5, 5];
let i = 0;

while (i < array.length) {
    console.log(array[i]);
    i++;
}
```


### javascript way 

- Basic Rules of Arrays in JavaScript

**Declaration: You can declare arrays using square brackets [] or the Array constructor.**

```javascript

let arr1 = [1, 2, 3];
let arr2 = new Array(1, 2, 3);

```
- Accessing Elements: Use zero-based indexing to access elements.

```javascript

let firstElement = arr1[0]; // 1
Length Property: Use the length property to get the number of elements.

```

```javascript

let length = arr1.length; // 3
Adding Elements: Use push to add elements to the end, and unshift to add to the beginning.

```

```javascript

    arr1.push(4); // [1, 2, 3, 4]
    arr1.unshift(0); // [0, 1, 2, 3, 4]
    Removing Elements: Use pop to remove the last element, and shift to remove the first.
```
```javascript
arr1.pop(); // [0, 1, 2, 3]
arr1.shift(); // [1, 2, 3]
```




Traversing Arrays
For Loop:

```javascript

let arr = [1, 2, 3, 4, 5];
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
```
**While Loop:**

```javascript
let i = 0;
while (i < arr.length) {
  console.log(arr[i]);
  i++;
}
```


**For...of Loop:**

```javascript

for (let value of arr) {
  console.log(value);
}
```

**ForEach Method:**

```javascript

arr.forEach(function(value) {
  console.log(value);
});
```


**Traversing Objects**

- For...in Loop: To iterate over the properties of an object.

```javascript
Copy code
let obj = { a: 1, b: 2, c: 3 };
for (let key in obj) {
  console.log(key + ": " + obj[key]);
}
```
- Object.keys(): To get an array of the object's own enumerable property names.

```javascript
Object.keys(obj).forEach(function(key) {
  console.log(key + ": " + obj[key]);
});
```




- Object.values(): To get an array of the object's own enumerable property values.

```javascript
Copy code
Object.values(obj).forEach(function(value) {
  console.log(value);
});
```



- Object.entries(): To get an array of the object's own enumerable property [key, value] pairs.

```javascript

Object.entries(obj).forEach(function([key, value]) {
  console.log(key + ": " + value);
});

```

**Array Traversal Example**

let numbers = [10, 20, 30, 40, 50];

```javascript
// For Loop
for (let i = 0; i < numbers.length; i++) {
  console.log(numbers[i]);
}

// While Loop
let i = 0;
while (i < numbers.length) {
  console.log(numbers[i]);
  i++;
}
```

```javascript
// For...of Loop
for (let number of numbers) {
  console.log(number);
}
```

***Object Traversal Example***




```javascript
let person = {
  name: "Alice",
  age: 25,
  city: "New York"
};

// For...in Loop
for (let key in person) {
  console.log(key + ": " + person[key]);
}

```
