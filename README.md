# programming concept doc

1. Basic Rules for Loops

## Basic Rules for Loops



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

## Basic Rules for Loops finished




